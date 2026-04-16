Olá Teo, boa noite!
(aqui vai minha contribuição)

# git-test-2026

## Fluxo de Git

Este repositório utiliza as branches:

- `main`: versão estável em produção
- `develop`: integração das funcionalidades em desenvolvimento
- `feat/readme`: branch de funcionalidade para criação/ajuste do README

### 1) Atualizar main e criar a develop pela 1a vez

```bash
git pull origin main

git checkout -b develop
```

### 2) Criar branch de funcionalidade a partir de `develop`

```bash
git checkout -b feat/readme
```

### 3) Desenvolver e versionar alterações

```bash
git add .
git commit -m "docs: atualiza readme com fluxo de git"
git push -u origin feat/readme
```

### 4) Abrir Pull Request para `develop`

Abra um PR com:

- **base**: `develop`
- **compare**: `feat/readme`

Após revisão e aprovação, faça o merge em `develop`.

### 5) Promover `develop` para `main`

Quando as alterações de `develop` estiverem prontas para release:

- abrir PR de `develop` para `main`
- revisar e aprovar
- realizar merge em `main`

### 6) Sincronizar as branches locais (seu computador)

```bash
git checkout main
git pull origin main

git checkout develop
git pull origin develop
```
