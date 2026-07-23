# 🏗 Arquitetura do Sistema

Projeto: Calc-Grower Pro

Versão: v0.1 Alpha

---

# Objetivo

O Calc-Grower Pro é uma plataforma para formulação nutricional e gerenciamento de cultivos em fibra de coco.

O sistema foi projetado para ser modular, permitindo futuras expansões como aplicativo desktop, aplicativo mobile e versão web.

---

# Filosofia

O projeto é baseado em cinco pilares.

- Precisão química
- Base científica
- Arquitetura modular
- Evolução contínua
- Transparência dos cálculos

Nenhum cálculo importante ficará oculto.

Toda decisão de engenharia será documentada.

---

# Arquitetura Geral

                Usuário
                   │
                   ▼
           Configuração Inicial
                   │
                   ▼
          Banco de Fertilizantes
                   │
                   ▼
        Motor Matemático (Core)
                   │
        ┌──────────┼──────────┐
        ▼          ▼          ▼
     Receitas   Resultados  Diagnóstico
        │          │          │
        └──────────┼──────────┘
                   ▼
           Dashboard Principal

---

# Estrutura do Projeto

Calc-Grower-Pro/

docs/
Documentação técnica

excel/
Planilhas principais

banco/
Base de dados

formulas/
Biblioteca de receitas

imagens/
Diagramas e capturas

testes/
Validação experimental

---

# Componentes

## Dashboard

Responsável pela interação com o usuário.

Funções

- Seleção da fase
- Tipo de água
- Volume do reservatório
- EC alvo
- pH alvo

Não realiza cálculos.

---

## Banco de Fertilizantes

Biblioteca contendo todas as matérias-primas.

Cada fertilizante possui:

- composição química
- fabricante
- preço
- grupo do concentrado
- solubilidade
- observações

---

## Motor Matemático (Core)

É o coração do sistema.

Responsável por:

- converter g/L em ppm
- calcular macronutrientes
- calcular micronutrientes
- estimar EC
- calcular custo
- validar relações nutricionais

Todo cálculo do sistema deverá passar pelo Core.

---

## Receitas

Armazena as formulações.

Cada receita possui:

- nome
- versão
- data
- objetivo
- composição
- observações

---

## Diagnóstico

Compara os dados do cultivo.

Entradas

- EC entrada
- EC saída
- pH entrada
- pH saída

Saídas

- ajuste nutricional
- excesso de sais
- deficiência provável
- recomendações

---

## Histórico

Armazena todas as versões das receitas.

Nenhuma receita será perdida.

---

# Fluxo de Dados

Usuário

↓

Receita

↓

Motor Matemático

↓

Resultados

↓

Diagnóstico

↓

Histórico

---

# Evolução Planejada

v0.1

Banco de fertilizantes

Motor matemático

Receitas

Resultados

---

v0.2

Dashboard

Banco de genéticas

Controle de água

---

v0.3

Gráficos

Dashboard avançado

Custos

---

v0.4

Diário de cultivo

Analytics

Banco de resultados

---

v1.0

Primeira versão estável

Aplicação completa

---

# Princípios de Desenvolvimento

1. Nenhuma fórmula será criada sem justificativa técnica.

2. Toda alteração será registrada no CHANGELOG.

3. Todo módulo deverá ser independente.

4. O sistema deverá ser escalável.

5. O projeto prioriza clareza em vez de complexidade.

6. Toda recomendação deverá poder ser revisada e melhorada.

---

# Visão de Longo Prazo

Transformar o Calc-Grower Pro em uma plataforma completa de gerenciamento nutricional para cultivos em substratos inertes.

O sistema deverá ser capaz de:

- formular nutrientes;
- acompanhar cultivos;
- analisar resultados;
- gerar diagnósticos;
- reduzir custos;
- aumentar repetibilidade entre ciclos.

