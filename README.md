# 🏙️ ZelaSP — Zeladoria Cidadã Inteligente
> Projeto integrado desenvolvido para a **Global Solution 2026.2** da **FIAP**  
> Curso: **Engenharia de Software (1º Ano)** · Tema: **CitizenTech**

[![ODS 11 - Cidades e Comunidades Sustentáveis](https://img.shields.io/badge/ODS%2011-Cidades%20Sustent%C3%A1veis-F99D26?style=for-the-badge&logo=target)](https://brasil.un.org/pt-br/sdgs/11)
[![ODS 9 - Indústria, Inovação e Infraestrutura](https://img.shields.io/badge/ODS%209-Inova%C3%A7%C3%A3o%20e%20Infraestrutura-F36D25?style=for-the-badge&logo=target)](https://brasil.un.org/pt-br/sdgs/9)
[![FIAP](https://img.shields.io/badge/FIAP-Global%20Solution-ED145B?style=for-the-badge)](https://www.fiap.com.br/)

---

## 📋 A Ficha da CitizenTech (Base Oficial)

* **Nome da CitizenTech:** ZelaSP
* **Cidade e Bairro:** São Paulo — SP (foco em bairros com fiação aérea densa e histórico de quedas de energia e temporais, como Pinheiros, Bela Vista, Mooca e periferias).
* **Cidadão Beneficiado:** Moradores, pedestres, comerciantes e pessoas com deficiência ou mobilidade reduzida que enfrentam riscos urbanos diários (cabos rompidos nas calçadas, entulhos obstruindo passagens, buracos em vias e carros abandonados).
* **Problema em uma Frase:** O canal oficial atual (SP 156) é burocrático, demorado e opaco, desestimulando o cidadão a relatar incidentes urbanos graves e impedindo a vizinhança de acompanhar e apoiar chamados do mesmo quarteirão.
* **Como Funciona:** O cidadão registra uma ocorrência em menos de 15 segundos enviando foto e localização automática; a plataforma exibe relatos abertos no mesmo raio (permitindo apoiar chamados existentes em vez de duplicá-los); e disponibiliza uma linha do tempo transparente com fotos antes/depois da execução do serviço.
* **O que Cada Parte Faz:**
  * **Lógica (Computational Thinking with Python):** Sistema de triagem, cálculo de risco/urgência (cabo elétrico vs. entulho) e persistência em arquivos JSON.
  * **Interface & Interação (Front-end Design & Web Development):** WebApp mobile-first em React + Tailwind CSS com consumo de API (CRUD completo), 8 componentes e Custom Hooks.
  * **Sensor (Edge Computing & Computer Systems):** Dispositivo embarcado com ESP32 simulado no Wokwi para monitorar vibração e integridade mecânica de cabos em postes, emitindo alerta sonoro/visual local.
  * **Matemática (Differentiated Problem Solving):** Modelagem diferencial da taxa de chegada de incidentes pós-tempestade versus capacidade de resposta da equipe de zeladoria.
  * **Experiência (Software & Total Experience Design):** Slide deck com requisitos funcionais, não funcionais, regras de negócio justificadas, casos de uso e heurísticas de usabilidade.
  * **Pitch (Storytelling & Inspiração Empreendedora):** Videopitch de 3 minutos em 9 etapas e e-mail executivo fundamentando o arquétipo de marca (O Cuidador / O Cidadão).
* **Indicador de Impacto:** Redução do tempo médio de reporte de 8 minutos (no SP 156) para menos de 30 segundos, com taxa de 0% de duplicidade de chamados no mesmo quarteirão.
* **ODS Conectados:** ODS 11 (Cidades e Comunidades Sustentáveis) e ODS 9 (Indústria, Inovação e Infraestrutura).

---

## 🛠️ Arquitetura Integrada do Ecossistema

```text
       [ Cidadão / Munícipe ]
                 │
                 ▼
   ┌───────────────────────────┐
   │    ZelaSP WebApp (React)   │ ◄── Interface Mobile-First & Acessível
   │      Tailwind CSS + CRUD  │
   └─────────────┬─────────────┘
                 │
                 ▼
   ┌───────────────────────────┐
   │   Motor de Triagem Python │ ◄── Lógica de Decisão, Validação,
   │       Persistência JSON   │     Cálculo de Risco & Severidade
   └─────────────▲─────────────┘
                 │
                 │ Telemetria de Alertas Físicos
                 │
   ┌─────────────┴─────────────┐
   │    Estação ESP32 (Wokwi)  │ ◄── Sensor de Borda em Poste Urbano
   │  Alerta Sonoro/LED Local  │     (Queda de Cabos / Abalroamento)
   └───────────────────────────┘
```

---

## 👥 Integrantes da Equipe

* **Gustavo** — RM: [Inserir RM]
* **João Pedro** — RM: [Inserir RM]
* **Lucas** — RM: [Inserir RM]
* **[Nome do 4º Integrante]** — RM: [Inserir RM]

---
*Global Solution 2026.2 · Engenharia de Software · FIAP Campus Lins / Paulista*
