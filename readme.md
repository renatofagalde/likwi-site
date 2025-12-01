✅ PASSO 1 — Instalar Node.js corretamente (via NVM)

Esse é o jeito que você costuma usar, e funciona em qualquer Linux, inclusive Arch.

Execute:

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash


Depois carregue o NVM:

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"


Agora instale o Node LTS:

nvm install --lts
nvm use --lts


Teste:

node -v
npm -v


Se aparecer versão, está OK.

✅ PASSO 2 — Instalar o Firebase CLI

Depois do Node funcionar:

npm install -g firebase-tools


Teste:

firebase --version


E faça login:

firebase login

⚠️ IMPORTANTE — Verificar se o PATH está quebrado

Me envie a saída destes comandos para garantir que o PATH está correto (principalmente usando zsh):

echo $PATH | tr ':' '\n'
which node
which npm
ls -la ~/.nvm


Assim eu ajusto o ~/.zshrc certinho.

Se quiser, já te deixo pronto o comando para atualizar seu site:

firebase deploy --only hosting


Manda os outputs e deixo tudo funcionando.