# Primeiros passos Git e GitHub

📘 **Descrição do projeto**  
Este repositório faz parte do curso **Git e GitHub** da Udemy, cujo objetivo é ensinar, de forma prática e progressiva, os principais conceitos e boas práticas de **Git** e **GitHub**, desde o básico até fluxos mais avançados de versionamento e colaboração.

---

## 📌 Objetivo dessa documentação

- Primeiros passos com o Git para controle de versão
- Utilizar o GitHub como plataforma de colaboração
- Trabalhar com repositórios locais e remotos
- Aplicar boas práticas de versionamento em projetos reais

---

> ## 🔧 Instalando o Git no seu computador

Para instalar o git em sua maquina, acesse o site e faça o download:

```bash
https://git-scm.com/install/
```

> *Primeiros comandos*

Inicialmente você precisa cadastrar

- user 
- e-mail
- branch default normalmente main

```bash
git config --global user.name "Seu Usuario"   
git config --global user.email seuemail@email.com
git config --global init.default branch main
```
> *Iniciando o git em um diretório*

Crie um diretorio para o seu novo projeto, você pode clonar esse repositorio nesse novo diretório.
Para iniciar o git nesse repositório novo, navegue até a pasta pelo terminal e rode esse comando

```bash
git init
```
Uma pasta oculta será criada ./git, nessa pasta fica todo o controle de versionamento

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
---

> ## 🔧 Comando para clonar esse repositório

bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
