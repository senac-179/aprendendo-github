# 📌 Projeto: aprendendo-github

Vamos treinar **trabalho em equipe** usando **branch + Pull Request (PR)**.

---

## ✅ Regras rápidas

- 🚫 **NUNCA** faça `push` na `main`.  
- 🌱 Sempre crie **sua própria branch** (use seu primeiro nome).  
- ✍️ Edite apenas o **README.md** e adicione **1 linha no final**.  
- 👩‍🏫 A professora aprova os PRs.  
- 🔄 Depois do merge, todos atualizam a `main`.  

---

## 🔧 0) Configuração inicial do Git (apenas uma vez)

No **VS Code → Terminal**:

```bash
git config --global user.name "seu-usuario-no-github"
git config --global user.email "seu-email-da-conta-github"
git config --global credential.helper manager   # login no navegador no 1º push


Conferir:

git config user.name
git config user.email


Se pedir token, crie em:
GitHub → Settings → Developer settings → Personal access tokens (classic) → Generate (escopo repo).

📥 1) Clonar o repositório
git clone https://github.com/<SUA-ORG>/aprendendo-github.git
cd aprendendo-github
code .


Troque <SUA-ORG> pelo nome da organização (ex.: senac-179).

🌱 2) Criar sua branch
git checkout main
git pull origin main
git checkout -b meu-nome
git branch      # deve aparecer: * meu-nome

📝 3) Editar o README.md

No final do arquivo, adicione uma linha no formato:

- SeuNome — sua frase aqui


Exemplo:

- Yuri — estou aprendendo GitHub!

📤 4) Commit e Push da sua branch
git add README.md
git commit -m "Adiciona SeuNome no README"
git push -u origin meu-nome


Se der certo, aparece o link Create a pull request.

🔀 5) Abrir o Pull Request (PR)

No GitHub:

Clique em Compare & pull request (verde)
ou vá em Pull requests → New pull request e escolha:

base: main

compare: meu-nome

Título do PR:

Adiciona SeuNome no README


Aguarde aprovação da professora ✅.

🔄 6) Atualizar a main (depois do merge)
git checkout main
git pull origin main

⚠️ 7) Se aparecer "This branch is N commits behind main"
git checkout main
git pull origin main
git checkout meu-nome
git merge main      # resolva conflitos se aparecerem
git push

🧩 8) Resolver conflitos no GitHub

Se aparecer Resolve conflicts ao abrir PR:

Clique em Resolve conflicts

Apague os marcadores:

<<<<<<< minha-branch
- Linha do colega
=======
- Minha linha
>>>>>>> main


Deixe as duas linhas (uma por pessoa).

Clique em Mark as resolved → Commit merge

Finalize o PR.

🔎 9) Check rápido

Conferir repositório remoto:

git remote -v


Deve ser:

https://github.com/<SUA-ORG>/aprendendo-github.git


Ver se a branch subiu:

git branch -r


Se não aparecer, faça:

git push -u origin meu-nome


Erros comuns:

"nothing to commit" → não salvou o arquivo.

"Acesso negado" → não aceitou convite da org ou está logado na conta errada.

📏 10) Padrão do projeto

Uma linha por pessoa (no fim do README).

Mensagem de commit:

Adiciona SeuNome no README


Nome da branch:

seuprimeironome
