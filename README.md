
# 26_1-TCC2
**Título do TCC:** Impacto de Índices de Instabilidade Atmosférica no Desempenho de Modelos de Aprendizado de Máquina para Nowcasting de Precipitação

**Alunos:** Ênnya Gomes

**Semestre de Defesa:** 2026-1

[PDF do TCC](TCC2_2026_EnnyaCampos.pdf)


# TL;DR

<!-- Resumo super conciso para quem não quer ler o README e começar a executar o código -->
Para rodar:
```$ pm2 start ecosystem.config.js```


# Descrição Geral
Este trabalho investiga o impacto da incorporação de índices de instabilidade atmosférica no desempenho de modelos de aprendizado de máquina aplicados à previsão de precipitação em curtíssimo prazo, conhecida como nowcasting.

O estudo considera o município do Rio de Janeiro e integra diferentes fontes de dados meteorológicos, incluindo radiossondas, produtos atmosféricos do satélite GOES-16 e observações pluviométricas da rede WebSirene.

# Funcionalidades
<!-- Descreva as principais funcionalidades do seu código. Exemplo: -->
* Funcionalidade principal 1
   * detalhe a
   * detalhe b
   * detalhe c
* Funcionalidade principal 2
   * detalhe d
   * detalhe e


# Arquitetura
<!-- Descreva nessa seção a arquitetura do seu código. Sugestão use mermaid para inclusão de diagramas que ajudem a entender seu código (https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams) -->

```mermaid
graph TD;
    A[Fontes de Dados] --> B[Pré-processamento];

    A1[WebSirene] --> A;
    A2[Radiossondas IGRA/UOW] --> A;
    A3[GOES-16] --> A;

    B --> C[Integração dos Dados];
    C --> D[Construção dos Alvos];

    D --> E1[Classificação Binária];
    D --> E2[Classificação Multiclasse];
    D --> E3[Regressão];

    E1 --> F[Treinamento dos Modelos];
    E2 --> F;
    E3 --> F;

    F --> G1[Random Forest];
    F --> G2[CatBoost];

    G1 --> H[Avaliação dos Resultados];
    G2 --> H;
```

# Dependências

<!-- Apresente a lista de dependências do seu código. Quando necessário, incluia links. Exemplo: -->
* Mosquitto MQTT Broker
* Node JS
* 
* [PM2](https://pm2.keymetrics.io)
* [NW.js](https://nwjs.io)
* [FFmpeg](https://ffmpeg.org)


# Execução

<!-- Descreva como instalar/executar seu código. Exemplo: -->
Componentes executados com PM2.
```$ pm2 start ecosystem.config.js```
 
