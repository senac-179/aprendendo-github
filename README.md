👩‍🏫 Projeto: aprendendo-github

Vamos treinar trabalho em equipe usando branch + Pull Request (PR).

✅ Regras rápidas

NUNCA faça push na main. Sempre use sua própria branch.

Edite somente o README.md e adicione 1 linha no final.

A professora aprova os PRs. Depois do merge, todos atualizam a main.

0) Preparar o Git (uma vez só)

No VS Code → Terminal:

git config --global user.name "seu-usuario-no-github"
git config --global user.email "seu-email-da-conta-github"
git config --global credential.helper manager   # abre login no navegador no primeiro push


Conferir:

git config user.name
git config user.email


Se pedir “senha” no push, o Git abre o login do GitHub. Se pedir token, gere em
GitHub → Settings → Developer settings → Personal access tokens (classic) → Generate (escopo repo).

1) Clonar o repositório
git clone https://github.com/<SUA-ORG>/aprendendo-github.git
cd aprendendo-github
code .


Troque <SUA-ORG> pelo nome da organização (ex.: senac-179).

2) Atualizar e criar sua branch

Use seu primeiro nome (sem acentos/espaços).

git checkout main
git pull origin main
git checkout -b meu-nome
git branch      # deve aparecer: * meu-nome

3) Editar o README.md

Abra o arquivo README.md e adicione UMA linha no final, assim:

- SeuNome — sua frase aqui


Salve o arquivo.

4) Commit e Push da sua branch
git add README.md
git commit -m "Adiciona SeuNome no README"
git push -u origin meu-nome


Se tudo estiver certo, o terminal mostra um link “Create a pull request”.

5) Abrir o Pull Request (PR)

No GitHub do repositório:

Clique no botão Compare & pull request (verde)
ou vá em Pull requests → New pull request e escolha:

base: main

compare: meu-nome

Título do PR: Adiciona SeuNome no README → Create pull request.

Aguarde a professora aprovar ✅.

6) Depois do merge (todo mundo)

Quando a professora aceitar seu PR:

git checkout main
git pull origin main

7) Se o GitHub mostrar “This branch is N commits behind main”

Atualize sua branch com as mudanças da main:

git checkout main
git pull origin main
git checkout meu-nome
git merge main            # resolva conflitos se aparecerem
git push                  # envia a branch atualizada

8) Como resolver conflito no GitHub (bem rápido)

Se ao abrir o PR aparecer “Resolving conflicts”:

Clique em Resolve conflicts.

No arquivo, apague os marcadores:

<<<<<<< minha-branch
=======
>>>>>>> main


Deixe as duas linhas (uma por colega) ou ajuste o texto.

Clique Mark as resolved → Commit merge → volte e finalize o PR.

Exemplo final sem marcadores:

- Yuri — estou aprendendo GitHub!
- Adriana — estou aprendendo GitHub!!

9) Check rápido (quando algo não aparece)

Conferir repositório remoto

git remote -v


Deve ser: https://github.com/<SUA-ORG>/aprendendo-github.git

Ver se a branch subiu

git branch -r


Deve aparecer origin/meu-nome.
Se não aparecer → faça git push -u origin meu-nome.

“nothing to commit” → você não salvou o arquivo. Edite o README.md, salve e refaça add + commit.

Acesso negado → você não aceitou o convite da organização ou está logado na conta errada. Entre no GitHub com a conta correta e repita o push.

10) Padrão do projeto

Uma linha por pessoa, sempre no fim do README.md.

Mensagem de commit: Adiciona SeuNome no README.

Branch: seuprimeironome.

Bom trabalho! 🚀
