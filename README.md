# Part 5 Mobile - Teste Magazord

Este repositório contém a implementação da **Parte 5 - Testes Mobile** do desafio técnico para a vaga da Magazord.

O foco desta etapa é demonstrar:

- entendimento de estratégia de automação mobile
- clareza na escolha de ferramenta
- capacidade de estruturar ambiente de execução
- validação de navegação básica em fluxo mobile
- abordagem para simulação de geolocalização

---

## Objetivo do projeto

Este projeto foi criado para atender aos cenários propostos na **Parte 5** do teste técnico, cobrindo:

### Questão 5.1 - Automação Mobile
Estruturação de uma abordagem de automação mobile com foco em:

- definição da ferramenta
- configuração do ambiente
- execução de um teste básico de navegação
- estratégia de mock de geolocalização
- visão de execução para Android e iOS

---

## Stack utilizada

- **Node.js** 18+
- **Appium**
- **JavaScript**

---

## Por que essa stack foi escolhida

A escolha do **Appium + JavaScript** foi feita por ser uma abordagem amplamente conhecida no mercado para automação mobile, com suporte a **Android** e **iOS** e boa aderência a cenários de testes funcionais em aplicações nativas, híbridas e web mobile.

Além disso, essa escolha permite demonstrar uma estratégia mais próxima de um ambiente corporativo real, onde a mesma base conceitual pode ser adaptada para múltiplas plataformas e diferentes pipelines de execução.

---

## Instalação do projeto
### 1. Clonar o repositório
- git clone <url-do-repositorio>
- cd magazord-qa-part5-mobile
### 2. Inicializar o projeto Node.js
- npm init -y
### 3. Instalar dependências principais
- npm install webdriverio
- npm install appium --save-dev
### 4. Instalar o Appium globalmente, se necessário
- npm install -g appium
### 5. Validar instalação do Appium
- appium -v
### 6. Configurar ambiente Android/iOS
- Os detalhes de configuração do ambiente estão documentados em:
- questao5.1-mobile/SETUP.md

### Executar o teste mobile básico
- node questao5.1-mobile/testes/mobile-basic.spec.js
### Executar após subir o Appium manualmente
- appium
- node questao5.1-mobile/testes/mobile-basic.spec.js
```bash
