# Simulador de Empréstimo Consignado

Um simulador de empréstimo consignado desenvolvido com **HTML, CSS e JavaScript puro**, que permite calcular o valor das parcelas, os juros e o total a pagar com base nos dados informados pelo usuário.

O projeto foi desenvolvido para praticar programação web, manipulação do DOM, eventos JavaScript e cálculos financeiros.

## Funcionalidades

- Informar o valor desejado do empréstimo.
- Definir a taxa de juros mensal.
- Escolher a quantidade de parcelas.
- Calcular o valor da prestação mensal pelo sistema Price.
- Calcular o total de juros do empréstimo.
- Calcular o valor total a pagar.
- Exibir os resultados em reais (R$).
- Validar os valores informados pelo usuário.
- Permitir simulações com juros iguais a zero.

## Tecnologias utilizadas

- **HTML5:** estrutura da página e formulário.
- **CSS3:** estilização e layout responsivo.
- **JavaScript:** validação dos dados, cálculos financeiros e atualização dos resultados.
- **Intl.NumberFormat:** formatação dos valores monetários no padrão brasileiro.

## Como executar

O projeto não exige instalação de bibliotecas ou configuração de servidor.

1. Faça o download ou clone este repositório.
2. Localize o arquivo `desafio.html`.
3. Abra o arquivo em um navegador, como Google Chrome ou Firefox.
4. Informe os dados do empréstimo.
5. Clique em **Simular empréstimo** para visualizar os resultados.

## Como utilizar

O simulador solicita três informações:

| Campo | Descrição |
|---|---|
| Valor do empréstimo | Quantia desejada pelo usuário. |
| Juros mensais | Taxa de juros aplicada mensalmente, em porcentagem. |
| Quantidade de parcelas | Número de prestações, de 1 a 120. |

Após o preenchimento, o sistema apresenta:

- **Valor solicitado:** quantia inicial do empréstimo.
- **Parcela mensal:** valor estimado de cada prestação.
- **Total de juros:** custo dos juros ao longo do financiamento.
- **Total a pagar:** soma das prestações calculadas.

## Cálculo financeiro

O simulador utiliza o sistema Price, que calcula prestações fixas com base no valor financiado, na taxa de juros mensal e no prazo.

Quando a taxa de juros é maior que zero, a fórmula utilizada é:

```text
Parcela = Valor × [i × (1 + i)^n] / [(1 + i)^n - 1]
```

Onde:

- `Valor` representa o valor solicitado.
- `i` representa a taxa mensal em formato decimal.
- `n` representa a quantidade de parcelas.

Quando a taxa de juros é zero, o valor do empréstimo é dividido igualmente pelo número de parcelas.

O programa arredonda a prestação para duas casas decimais antes de calcular o total pago e os juros.

## Exemplo de simulação

Considere os seguintes dados:

- Valor do empréstimo: R$ 5.000,00
- Taxa de juros mensal: 1,8%
- Prazo: 24 parcelas

O resultado será aproximadamente:

| Resultado | Valor |
|---|---:|
| Parcela mensal | R$ 258,97 |
| Total de juros | R$ 1.215,28 |
| Total a pagar | R$ 6.215,28 |

Os valores são ilustrativos e podem apresentar pequenas diferenças de arredondamento.

## Conceitos de programação praticados

Este projeto permite estudar:

- Estruturação de páginas com HTML.
- Estilização de formulários com CSS.
- Seleção de elementos com `document.getElementById()`.
- Manipulação de eventos com `addEventListener()`.
- Captura e conversão de dados com `Number()`.
- Estruturas condicionais com `if/else`.
- Validação de entradas com `Number.isFinite()` e `Number.isInteger()`.
- Cálculos matemáticos com `Math.pow()`.
- Manipulação do conteúdo da página com `textContent`.
- Formatação monetária com `toLocaleString()`.
- Prevenção do envio tradicional do formulário com `event.preventDefault()`.

## Estrutura do projeto

```text
simulador-consignado/
└── desafio.html
```

O arquivo reúne o HTML, o CSS e o JavaScript necessários para executar o simulador.

## Limitações

Este é um simulador educativo. Ele não se conecta a bancos ou instituições financeiras, não realiza consultas de crédito e não garante a aprovação de empréstimos.

Os cálculos não incluem necessariamente IOF, seguros, tarifas ou outros custos que podem compor o Custo Efetivo Total (CET) de um contrato real.

O total apresentado é calculado a partir da prestação arredondada multiplicada pela quantidade de parcelas, podendo haver diferenças de centavos em relação a contratos reais.

## Melhorias futuras

Algumas funcionalidades que podem ser adicionadas em versões futuras:

- Cadastro de dados do cliente e do empregador.
- Validação de CPF e CNPJ.
- Simulação de margem consignável.
- Comparação de condições entre bancos fictícios.
- Criação de APIs com Node.js e Express.
- Testes automatizados dos cálculos.
- Armazenamento de simulações em banco de dados.

## Licença

Este projeto é destinado a fins educacionais. Caso seja publicado sob a licença MIT, adicione um arquivo `LICENSE` ao repositório com os termos correspondentes.

---

Desenvolvido como projeto de prática em programação web com HTML, CSS e JavaScript.