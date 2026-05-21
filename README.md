# Serviço de Pagamento

Projeto criado como trabalho de conclusao da disciplina de Programação para Automaçâo de Testes.
O projeto implementa uma classe que possua dois métodos: um para realizar pagamento e outro para consultar o último pagamento. 
Foi feito usando JavaScript rodando no Node.js


# Requisitos

- Node.js instalado
- npm instalado

---


# Estrutura do Projeto

```txt
servico-pagamento/
├── src/
│   └── ServicoDePagamento.js
├── test/
│   └── ServicoDePagamento.test.js
├── package.json
└── README.md
```


# Funcionalidades

A classe possui dois métodos:

## realizarPagamento

Responsável por registrar um pagamento.

## consultarUltimoPagamento

Responsável por consultar o ultimo pagamento realizado.
Caso não exista pagamento, retorna `null`.

### Regra de categoria

- Valor maior que `100` → categoria `"cara"`
- Valor menor ou igual a `100` → categoria `"padrão"`

---

# Exemplo de uso

```javascript
const ServicoDePagamento = require('./src/ServicoDePagamento');

const servicoDePagamento = new ServicoDePagamento();

servicoDePagamento.pagar(
  '0987-7656-3475',
  'Samar',
  156.87
);

console.log(
  servicoDePagamento.consultarUltimoPagamento()
);
```

## Saída

```javascript
{
  codigoBarras: '0987-7656-3475',
  empresa: 'Samar',
  valor: 156.87,
  categoria: 'cara'
}
```


## Instalação

```bash
npm install
```

## Rodar testes

```bash
npm test
```

---

## Gerar relatório

```bash
npm run test:report
```

---

# Tecnologias utilizadas

- Node.js
- Mocha
- Assert

---

# Autor

Desenvolvido para desafio técnico por Pannuvia Soares Monteiro