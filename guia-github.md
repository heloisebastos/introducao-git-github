# Primeiros Passos com Git e GitHub

Este guia apresenta uma introdução a práticas recomendadas para começar a usar **Git** e **GitHub**.

---

## 1. Conceitos

### Git
- Git é um **sistema de controle de versão distribuído**.  
- Cada desenvolvedor mantém uma cópia completa do repositório localmente.  
- Permite rastrear alterações, criar ramificações (branches) etc.  

### GitHub
- Plataforma de hospedagem de repositórios Git remotos.  
- Adiciona funcionalidades colaborativas como *pull requests*, *issues* e revisão de código.  
- Facilita o trabalho em equipe em projetos distribuídos.  


---

## 2. Configuração

### GitHub
1. Acesse [https://github.com](https://github.com)  
2. Crie sua conta (nome de usuário, e-mail e senha)  
3. Configure seu perfil  
4. (Recomendado) Ative autenticação de dois fatores para mais segurança  

### Git
1. Instale o Git:  
   - **Windows ou MAC**: baixe no [site oficial](https://git-scm.com/downloads)  
   - **Linux**: use o gerenciador de pacotes (`apt`, `yum`, etc.)  
   - **Vídeo no Youtube** : [Como instalar o GIT no Windows](https://youtu.be/pSJz4DzvbFI)
   - **Vídeo no Youtube** : [Como instalar o GIT no MAC](https://youtu.be/B8Rsvb9TW_E)


2. Configure seu usuário:  
   ```
   git config --global user.name "Seu Nome"
   git config --global user.email "seu-email@exemplo.com"
   ```


---

## 3. Criar um repositório local e enviar ao remoto:

No diretório do projeto
```
cd caminho/do/projeto
```

Iniciar repositório Git
```
git init
```

Adicionar arquivos ao stage
```
git add .
```
Fazer primeiro commit
```
git commit -m "Primeiro commit: estrutura inicial"
```

### Criar repositório remoto no GitHub e copiar a URL

Conectar repositório local ao remoto
```
git remote add origin <URL_DO_REPOSITORIO>
```

Enviar para branch principal
```
git push -u origin main
```

---

## 4. Comandos básicos do GIT


| Comando               | Descrição                                   |
| --------------------- | ------------------------------------------- |
| `git status`          | Mostra o estado atual dos arquivos e branch |
| `git add <arquivo>`   | Adiciona arquivo ao *stage*                 |
| `git add .`           | Adiciona todas as mudanças ao *stage*       |
| `git commit -m "msg"` | Registra alterações no histórico            |
| `git push`            | Envia commits locais ao remoto              |
| `git pull`            | Baixa e mescla alterações do remoto         |
| `git log`             | Lista o histórico de commits                |
| `git diff`            | Mostra diferenças entre versões             |
| `git branch`          | Lista branches locais                       |
| `git branch <nome>`   | Cria nova branch                            |
| `git checkout <nome>` | Troca para outra branch                     |
| `git merge <branch>`  | Mescla branch especificada na atual         |


---
## 5. Branches e fluxo de trabalho recomendado

Branches principais:

main → código estável (produção)

dev → branch de integração (desenvolvimento)

feature/* → branches de funcionalidades específicas (nova funcionalidade ou correção de bug)

---

## 6. Recomendação

Antes de começar a desenvolver:

```
git checkout dev
git pull origin dev
```


Criar sua branch de feature a partir da dev:

```
git checkout -b feature/nome-da-feature
```

Durante o desenvolvimento diário:

- Faça commits frequentes com mensagens claras

- Teste localmente suas alterações

No final do desenvolvimento diário:

```
git push origin feature/nome-da-feature
```

Quando a feature estiver pronta:

- Abra um Pull Request (PR) no GitHub para mesclar sua feature na dev

- Após revisão e testes, mesclar dev na main 

---

## Referências

- [Pro Git Book Inglês](https://git-scm.com/book/en/v2)
- [Pro Git Book Português](https://git-scm.com/book/pt-br/v2)
- [Documentação Github](https://docs.github.com/pt)
- [Gitflow Workflow](https://www.atlassian.com/br/git/tutorials/comparing-workflows/gitflow-workflow)