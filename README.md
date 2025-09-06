# Banco API Tests

## Objetivo
Este projeto contém uma suíte de **testes automatizados** para a API REST disponível em [Banco API](https://github.com/juliodelimas/banco-api). 
O objetivo é validar o funcionamento correto dos endpoints, assegurando qualidade, confiabilidade e integridade das funcionalidades oferecidas.
Garantir que as operações da API REST sejam validadas por meio de testes automatizados, abrangendo cenários de sucesso e falha, além de fornecer relatórios de execução.

## Stack Utilizada
- **Linguagem**: JavaScript (Node.js)
- **Framework de testes:** [Mocha](https://mochajs.org/)
- **Biblioteca de requisições:** [Supertest] (http://github.com/ladis/supertest)
- **Biblioteca de Asserções:** [Chai](https://www.chaijs.com/)
- **Relatórios de Testes:** [Mochawesome](http://guihub.com/adamgruber/mochawesome)
- **Gerenciamento de Variaveis de ambiente:** [dotenv](https://github.com/mtdotla/dotenv)

## Estrutura de Diretórios

```
banco-api-tests/
├── test/                   # Testes organizados por funcionalidades
│   ├── login.test.js
│   └── transferencias.test.js
├── mochawesome-report/     # Diretório onde são salvos os relatórios HTML
├── .env.example            # Arquivo para configuração da variavel BASE_URL
├── .gitignore
├── package.json            # Dependências e scripts
└── README.md               # Documentação do projeto
```

## Formato do arquivo `.env`

O projeto requer um arquivo `.env` na raiz do repositório para definir variáveis de ambiente.

Exemplo de configuração:
```
BASE_URL=http://localhost:3000
```

Substitua `http://localhost:3000` pela URL onde a API `banco-api` está rodando.

## Execução dos Testes

Instale as dependências do projeto:
```bash
npm install
```

Execute todos os testes:
```bash
npm test
```

Execute os testes com relatório Mochawesome:
```bash
npm run test:report
```

## Relatórios
Após a execução com `npm run test:report`, o relatório em HTML será gerado no diretório `mochawesome-report/`.

Sugestão: para executar os test e abrir o relatório HTML automaticamente, adicione um script no `package.json`:
```json
"scripts": {
	"test: report": "npm test && open mochawesome-report/mochawesome.html"
}
```

Para visualizar:
1. Acesse o diretório `mochawesome-report/`
2. Abra o arquivo `mochawesome.html` em um navegador.


## Documentação das Dependências
- [Mocha](https://mochajs.org/)
- [Chai](https://www.chaijs.com/)
- [Supertest](https://www.npmjs.com/package/supertest)
- [Mochawesome](https://www.npmjs.com/package/mochawesome)
- [dotenv](https://github.com/mtdotla/dotenv)

