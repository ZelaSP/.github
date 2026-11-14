# 🏙️ ZelaSP — Zeladoria Cidadã Inteligente

> Projeto integrado desenvolvido para a **Global Solution 2026.2** da **FIAP**  
> Curso: **Engenharia de Software (1º Ano)** · Tema: **CitizenTech** · **Protótipo Web:** [https://zelasp-web.vercel.app/](https://zelasp-web.vercel.app/)

[![ODS 11 - Cidades e Comunidades Sustentáveis](https://img.shields.io/badge/ODS%2011-Cidades%20Sustent%C3%A1veis-F99D26?style=for-the-badge&logo=target)](https://brasil.un.org/pt-br/sdgs/11)
[![ODS 9 - Indústria, Inovação e Infraestrutura](https://img.shields.io/badge/ODS%209-Inova%C3%A7%C3%A3o%20e%20Infraestrutura-F36D25?style=for-the-badge&logo=target)](https://brasil.un.org/pt-br/sdgs/9)
[![FIAP](https://img.shields.io/badge/FIAP-Global%20Solution-ED145B?style=for-the-badge)](https://www.fiap.com.br/)

---

## 📋 A Ficha da CitizenTech (Visão Unificada)

* **Nome da CitizenTech:** ZelaSP
* **Cidade e Bairros:** São Paulo — SP, com foco territorial prioritário em **Jabaquara, Vila Mariana, Saúde, Bela Vista, Mooca e Vila Mascote**.
* **Cidadão Beneficiado:** Moradores, pedestres, idosos, pessoas com deficiência (PcD) ou mobilidade reduzida e comerciantes que enfrentam riscos urbanos diários (fios soltos, bueiros sem tampa, buracos, entulho e carros abandonados), além das equipes das Subprefeituras.
* **Problema:** O canal tradicional de zeladoria envolve etapas longas no registro, gera relatos repetidos no mesmo ponto em dias de temporal e oferece pouca clareza sobre a fila de prioridade.
* **Como Funciona na Versão Atual:** O cidadão registra ocorrências via endereço (ViaCEP ou digitação, com captura opcional de GPS do navegador), conta com seleção demonstrativa de foto (sem envio, armazenamento ou análise da imagem) e pode apoiar manualmente chamados existentes no painel para incentivar a redução de relatos repetidos.
* **O que Cada Parte Faz:**
  * **Interface & Interação (Front-end Design & Web Development):** WebApp em React + Vite + Tailwind CSS conectado à MockAPI (CRUD completo) e ViaCEP, com cache local apenas para consulta offline, Custom Hooks e protótipo 3D WebGL na tela inicial.
  * **Lógica (Computational Thinking with Python):** Aplicação CLI em Python com triagem pela regra única de prioridade e persistência em JSON.
  * **Matemática (Differentiated Problem Solving):** Estudo acadêmico simulado em 24h com taxa operacional não negativa `max(0, q(t))`, derivadas e integrais de volume excedente.
  * **Experiência (Software & Total Experience Design):** Documentação de escopo, requisitos (RF/RNF/RN), Diagrama de Casos de Uso UML, wireframes de média fidelidade, heurísticas de Nielsen, Total Experience e roadmap.
  * **Sensor (Edge Computing & Computer Systems):** Protótipo embarcado com ESP32 simulado no Wokwi para monitorar vibração/inclinação e alertar localmente ocorrências em postes urbanos.
  * **Pitch (Storytelling & Inspiração Empreendedora):** Videopitch em 9 etapas e e-mail executivo estruturados no arquétipo de marca (O Cuidador / O Cidadão).
* **ODS Conectados:** ODS 11 (Cidades e Comunidades Sustentáveis) e ODS 9 (Indústria, Inovação e Infraestrutura).

### 🎯 Formulações Oficiais do Projeto

* **Tempo de relato:** Meta de registro em até 15 segundos, a validar com testes de usabilidade.
* **Duplicidade atual:** Apoio manual a ocorrências existentes para incentivar a redução de relatos repetidos.
* **Meta de duplicidade:** Meta futura de reduzir em 45% a parcela de chamados duplicados.
* **Resultado matemático:** Redução simulada de 38,5% do excedente sobre a base já deduplicada, após reforço de capacidade, nas hipóteses do exercício.
* **Foto e localização:** Funcionalidade futura: foto como evidência e apoio à localização da ocorrência; seleção demonstrativa na versão atual.
* **Arquitetura:** Web com MockAPI e ViaCEP; CLI Python com JSON; estudo matemático independente; integração entre módulos e IoT prevista na evolução.

> **Detalhe sobre imagens e localização:** A proposta de evolução do ZelaSP inclui o uso de fotografias como evidência e apoio à localização da ocorrência, aproveitando metadados GPS disponíveis no arquivo e a confirmação do cidadão. No protótipo acadêmico atual, a seleção de foto é demonstrativa: o conteúdo da imagem não é enviado, armazenado ou analisado. Recursos como upload real de imagens, localização por foto, histórico fotográfico antes/depois, autenticação real, gravação/sincronização offline e integração completa entre módulos permanecem no roadmap.

---

## ⚖️ Regra Única de Prioridade (Níveis 1 a 5)

Política interna de triagem acadêmica adotada uniformemente nos repositórios (`zelasp-python`, `zelasp-web` e `zelasp-tx-design`):

1. **Risco elétrico marcado:** atribui **nível 5** em qualquer categoria.
2. **Sem risco elétrico marcado (prioridade-base):**
   * Tampa de Bueiro Furtada/Quebrada: **5**
   * Buraco em Via ou Calçada: **4**
   * Fios e Cabos Rompidos/Soltos: **3**
   * Poda de Árvore com Risco Elétrico: **3**
   * Descarte Irregular de Entulho: **2**
   * Carro Abandonado: **1**
3. **Apoio comunitário:** a partir de **10 apoios**, soma **+1 único nível** à prioridade-base (teto 5), recalculado sempre a partir da base. Ocorrências `RESOLVIDO` não recebem novos apoios.

---

## 🛠️ Arquitetura Atual e Evolução Prevista

```text
MÓDULOS ATUAIS INDEPENDENTES
  ├── ZelaSP WebApp (React + Tailwind) ──► MockAPI (CRUD) + ViaCEP + cache de consulta
  ├── CLI de Triagem Python            ──► Persistência local em ocorrencias_zelasp.json
  ├── Estudo Matemático (DPS)          ──► Simulação acadêmica 24h (taxa não negativa)
  ├── Estação ESP32 (Wokwi - Edge)     ──► Alerta sonoro/LED local (simulação de borda)
  └── Documentação TX Design           ──► Escopo, UML de Casos de Uso, heurísticas e roadmap

EVOLUÇÃO FUTURA (ROADMAP)
  └── Plataforma unificada com envio/armazenamento real de fotos, localização por imagem,
      deduplicação geográfica, histórico antes/depois, autenticação real, fila offline e
      ingestão de telemetria IoT e gatilho preditivo GPCT em produção.
```

---

## 📦 Repositórios da Organização

| Repositório | Disciplina / Papel | Descrição |
|---|---|---|
| [`zelasp-web`](https://github.com/ZelaSP/zelasp-web) | Front-end Design & Web Development | Aplicação React + Vite + Tailwind com MockAPI, ViaCEP opcional, cache local de consulta e seleção demonstrativa de foto. *(Repositório público para avaliação acadêmica, conforme liberação dos professores).* |
| [`zelasp-python`](https://github.com/ZelaSP/zelasp-python) | Computational Thinking with Python | CLI acadêmica em Python com persistência JSON seguindo a regra única de prioridade. |
| [`zelasp-math`](https://github.com/ZelaSP/zelasp-math) | Differentiated Problem Solving | Simulação acadêmica 24h com taxa não negativa `max(0, q(t))`, derivadas e integrais de volume excedente. |
| [`zelasp-tx-design`](https://github.com/ZelaSP/zelasp-tx-design) | Software & Total Experience Design | Escopo, RF/RNF/RN, UML de Casos de Uso, wireframes de média fidelidade, heurísticas, TX e roadmap. |

---

## 👥 Integrantes da Equipe (1ESPW)

| Nome | RM |
|---|---|
| João Pedro Maschion da Cruz Sá | RM570509 |
| Gustavo Rezende Louro | RM570708 |
| João Pedro Lagonegro Bosco e Silva | RM569444 |
| Lucas Henrique Alves da Silva | RM572216 |

---
*Global Solution 2026.2 · Engenharia de Software · FIAP Campus Paulista*
