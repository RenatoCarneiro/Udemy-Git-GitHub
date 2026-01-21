# Primeiros passos Git e GitHub

## 🧩 Diferença entre Git e GitHub

**Git** e **GitHub** não são a mesma coisa, apesar dos nomes parecidos.

- **Git** é um sistema de controle de versão que roda no seu computador.  
  Ele serve para registrar mudanças, criar branches e manter o histórico do projeto.

- **GitHub** é uma plataforma online que hospeda repositórios Git.  
  Ele permite compartilhar código, colaborar com outras pessoas e gerenciar projetos. Existem outras plataformas que proporcionam isso também, como o GitLab!

👉 **Resumo:**  
**Git** versiona seu código localmente.  
**GitHub** armazena esse código na nuvem e facilita a colaboração e compartilhamento.

---

## 📌 Requisitos

- Conta no GitHub
- Conhecimento minimo na navegação no terminal de comandos

---

## 🔧 Instalando o Git no seu computador

Para instalar o git em sua maquina, acesse o site e faça o download:

```bash
https://git-scm.com/install/
```

> *Primeiros comandos*

Inicialmente você precisa cadastrar

- user 
- e-mail
- branch default normalmente main

Abra o terminal de comandos em seu computador

```bash
git config --global user.name "Seu Usuario"   
git config --global user.email seuemail@email.com
git config --global init.default branch main
```
> *Iniciando o git em um diretório*

Crie um diretorio em seu computador.
Para iniciar o git nesse repositório novo, navegue até a pasta pelo terminal e rode esse comando

```bash
git init
```
Uma pasta oculta será criada ./git, nessa pasta fica todo o controle de versionamento

Nesse modelo, estamos usando apenas a nossa maquina para guardar as versões, é necessario trackear todos os arquivos fazendo um primeiro commit geral de todos os arquivos que estão na pasta

Note, o git funciona em três partes, *WORK* > *STAGE* > *COMMIT*

Inicialmente você está trabalhando na "camada" WORK, para mover todos os arquivos para a stage
```bash
git add .
```
O comando git add . ou git add all move todos os arquivos para a stage, você pode ir digitando o comando git status para verificar o estado atual

Para iniciar o git, precisamos fazer um primeiro commit geral, pra ele criar os snapshots dos arquivos
```bash
git commit -m "Primeiro commit geral da pasta"
```

O parametro -m seguido da mensagem entre aspas fornece uma descrição para o commit que está sendo realizado

A partir de agora, todos os arquivos estão trackeados

---

> ## 🔧 Criando e trabalhando com diferentes *Branches*

Branches permitem que você trabalhe em novas funcionalidades, correções ou experimentos **sem afetar diretamente a branch principal (`main`)**.  
Cada branch representa uma linha independente de desenvolvimento.

Utilizar branches separadas é uma boa prática porque:

- Evita quebrar o código que já está em produção  
- Permite trabalhar em paralelo com outras pessoas  
- Facilita revisão de código via Pull Request  
- Organiza melhor o histórico de commits  

---

## 🌱 Criar uma nova branch

Cria uma nova branch a partir da branch atual.
```bash
git branch nome-da-branch
```
## ⚡️ Criar e já entrar na nova branch

Cria a branch e já muda para ela em um único comando.
```bash
git checkout -b nome-da-branch
```

## 📋 Listar todas as branches

Mostra as branches locais e indica em qual você está atualmente.
```bash
git branch
```
## 🔀 Fazer merge de uma branch na main

Após finalizar o desenvolvimento em uma branch, você deve unir (merge) suas alterações à branch principal.

Passo 1 — Voltar para a branch (`main`)
```bash
git checkout main
```
Passo 2 — Atualizar a branch (`main`) com o repositório remoto
```bash
git pull origin main
```
Passo 3 — Fazer o merge da branch de trabalho na (`main`)
```bash
git merge nome-da-branch
```

## 🗑 Apagar uma branch após o merge

Depois que a branch já foi integrada, é uma boa prática removê-la.

Apagar branch local
```bash
git branch -d nome-da-branch
```

Apagar branch remoto (caso você tenha criado alguma no GitHub)
```bash
git push origin --delete nome-da-branch
```

---

> ## 🔧 Associando e sincronizando com o GitHub
Crie um repositorio no GitHub

Agora vamos associar o repositorio local ao GitHub com o seguinte comando
```bash
git remote add origin https://github.com/RenatoCarneiro/seu-repositorio.git
```
O comando `git remote add origin` é utilizado para **associar (conectar)** o repositório local a um repositório remoto no GitHub.

Agora vamos fazer nosso primeiro push
```bash
git push -u origin main
```
Provavelmente o seu repositório no git deve ter sido populado com todos os arquivos da sua pasta local

---

> ## 🔧 Comandos de verificação
Verifica status geral (quais arquivos foram modificados)
```bash
git status
```

Verifica diferença (o que foi mudado em um arquivo)
```bash
git diff
```

Verifica log completo
```bash
git log
```

Verifica todo o log sumarizando por linha (facil vizualização
```bash
git log --oneline
```

Verifica log em um nivel maior detalhe
```bash
git log -p
```
