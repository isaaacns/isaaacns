<!-- Isaac Matias-->
# Olá, eu sou Isaac Matias!

## Sobre mim
Estudante Analise e Desenvolvimento de Sistema 3º semestre
## Projetos Destacados
- Gerador-de-Mensagens-Personalizadas
- Projeto Startup

![Estatísticas do GitHub](https://github-readme-stats.vercel.app/api?username=seu_nome&show_icons=true&theme=radical)

# .github/workflows/ci.yml
name: CI

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'

      - name: Install Dependencies
        run: npm install

      - name: Run Tests
        run: npm test
