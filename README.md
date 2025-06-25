# Teste-Projeto
# Projeto de Automação de Testes – Sauce Demo E2E

## 1. Objetivo

[cite_start]Este projeto contém a automação de testes E2E (End-to-End) para o site de e-commerce [Sauce Demo](https://www.saucedemo.com/v1/), desenvolvida como solução para a Prova Prática de Automação Web.

[cite_start]O objetivo foi automatizar os principais fluxos de usuário do site, aplicando boas práticas de desenvolvimento de testes e documentação. [cite_start]A ferramenta de automação utilizada foi o Cypress.

## 2. Tecnologias Utilizadas

* **Framework de Automação:** Cypress
* **Linguagem:** JavaScript
* **Gerenciador de Pacotes:** NPM
* **Ambiente de Execução:** Node.js

## 3. Funcionalidades Cobertas

[cite_start]A automação cobre os seguintes casos de uso, conforme solicitado:

* ✅ **Login e Logout:**
    * Login com usuário e senha corretos.
    * Validação de erro para usuário incorreto/bloqueado.
    * Logout após login bem-sucedido.
* ✅ **Produtos:**
    * Validação da exibição da lista de produtos.
    * Visualização de detalhes de um produto específico.
    * Ordenação de produtos por nome e preço.
* ✅ **Carrinho:**
    * Adicionar produtos ao carrinho.
    * Remover produtos do carrinho.
* ✅ **Checkout:**
    * Preenchimento de dados obrigatórios (nome, sobrenome, CEP).
    * Validação do resumo da compra.
    * Finalização da compra e validação da mensagem de sucesso.

## 4. Estrutura do Projeto

O projeto está organizado da seguinte forma para separar responsabilidades e facilitar a manutenção:
/ATIVIDADE_TESTE
|
|-- /casos_de_teste_bdd/   <-- Casos de teste escritos em BDD 
|   |-- 01_login_logout.feature
|   |-- 02_produtos.feature
|   |-- 03_carrinho.feature
|   |-- 04_checkout.feature
|
|-- /cypress/                <-- Pasta principal do Cypress
|   |-- /e2e/                <-- Scripts de testes automatizados 
|   |   |-- 01_login.cy.js
|   |   |-- 02_produtos.cy.js
|   |   |-- 03_carrinho.cy.js
|   |   |-- 04_checkout.cy.js
|   |-- /support/            <-- Comandos customizados (ex: login)
|       |-- commands.js
|
|-- cypress.config.js      <-- Arquivo de configuração do Cypress
|-- package.json           <-- Dependências do projeto
|-- README.md              <-- Esta documentação


## 5. Pré-requisitos

Antes de executar, garanta que você tenha o **Node.js** instalado em sua máquina (versão LTS é recomendada).

## 6. Instalação

1.  Clone este repositório para sua máquina local.
2.  Abra um terminal na pasta raiz do projeto (`ATIVIDADE_TESTE`).
3.  Execute o seguinte comando para instalar todas as dependências necessárias:
    ```bash
    npm install
    ```

## 7. Como Executar os Testes

Você pode executar os testes de duas maneiras:

#### Modo Interativo (Recomendado para desenvolvimento)

Este modo abre a interface gráfica do Cypress, permitindo que você veja os testes sendo executados em tempo real e depure com facilidade.

```bash
npx cypress open
Modo Headless (Recomendado para integração contínua)
Este modo executa todos os testes em segundo plano, sem abrir uma interface gráfica. É ideal para verificar a saúde do projeto de forma rápida. Os resultados, screenshots de erros e vídeos são salvos na pasta /cypress.

Bash

npx cypress run

Com este `README.md`, seu projeto está muito bem documentado e pronto para ser avaliado.
