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
git clone <url-do-repositorio>
cd magazord-qa-part5-mobile

### 2. Inicializar o projeto Node.js
npm init -y
### 3. Instalar dependências principais
npm install webdriverio
npm install appium --save-dev
### 4. Instalar o Appium globalmente, se necessário
npm install -g appium
### 5. Instalar o driver Android compatível com Appium 2
appium driver install uiautomator2@4
### 6. Validar instalação do Appium
appium -v
appium driver list --installed
Configuração do ambiente Android/iOS

Os detalhes completos de configuração do ambiente estão documentados em:

questao5.1-mobile/SETUP.md
Pré-requisitos importantes para Android

### Antes da execução, é necessário garantir que:

o Android Studio esteja instalado
o Android SDK esteja configurado
a variável de ambiente ANDROID_HOME esteja definida
o ADB esteja disponível no terminal
exista um emulador Android online ou um device físico conectado
Validar se o device/emulador está disponível
adb devices

O resultado esperado deve exibir um device ou emulador com status device.

### Como executar o teste
1. Subir o Appium manualmente
appium
2. Em outro terminal, executar o teste mobile básico
node questao5.1-mobile/testes/mobile-basic.spec.js

```bash
