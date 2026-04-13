### 5.1.a) Qual ferramenta você escolheria e por quê? (Appium, Detox, Maestro, etc.)

A ferramenta escolhida seria o **Appium**.

Essa escolha faz sentido porque o Appium é uma das soluções mais conhecidas do mercado para automação mobile e oferece suporte a **Android** e **iOS**, permitindo reutilizar a mesma base conceitual de automação em diferentes plataformas.

Além disso, o Appium é aderente a cenários corporativos em que a estratégia de testes precisa contemplar aplicações nativas, híbridas ou web mobile, com possibilidade de integração em pipelines e execução em dispositivos reais ou emuladores.

Ponto importante é a flexibilidade. O Appium permite validar interações de navegação, campos, permissões e comportamentos do aplicativo em um nível mais próximo da experiência real do usuário, o que o torna adequado para testes funcionais mobile.

---

### 5.1.b) Como você mockaria geolocalização em testes automatizados?

A abordagem depende da plataforma e do ambiente utilizado, mas a estratégia geral é substituir a localização real do dispositivo por coordenadas controladas durante a execução do teste.

Em Android e iOS, isso pode ser feito por meio do emulador, simulador ou recursos do próprio ambiente de automação, configurando latitude e longitude específicas antes ou durante o fluxo. Dessa forma, o teste pode validar comportamentos que dependem de localização sem depender da posição real do dispositivo.

Essa abordagem é importante porque torna o cenário reproduzível e previsível, permitindo validar regras de negócio como:
- exibição de conteúdo por região
- comportamento de mapas
- permissões relacionadas à localização
- respostas condicionadas à posição do usuário

Em contextos mais completos, também é recomendável combinar essa simulação com validações de permissão, bloqueio de acesso e fallback quando a localização não estiver disponível.

---

### 5.1.c) Estratégia para executar mesmos testes em iOS e Android?

A estratégia mais adequada é manter a lógica de teste o mais reutilizável possível, separando a regra do fluxo da configuração específica de cada plataforma.

Na prática, isso significa:
- reutilizar os mesmos cenários de teste sempre que o comportamento funcional for equivalente
- isolar capabilities, configurações de device e particularidades de plataforma em arquivos ou camadas separadas
- tratar diferenças específicas de seletor, permissão ou comportamento apenas quando necessário
- manter a mesma intenção funcional do teste em ambas as plataformas

Quando houver diferenças reais entre Android e iOS, o ideal é encapsular essas variações de forma controlada, sem duplicar o fluxo inteiro desnecessariamente. Assim, a suíte continua coerente, legível e sustentável ao longo do tempo.