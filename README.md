# Comandos-dev
Arsenal de Comandos para consultas

# git básico
git add .
git commit -m "msg"
git push

//Status e Histórico 

git status                             # ver alterações
git log --oneline                      # histórico resumido
git log                                #ver os commits
git checkout <id-do-commit>            #acessar uma versão sem apagar nada
git checkout -b nome-da-nova-branch    #trabalhar na versão escolhida

//Reset

git reset --soft <commit>      #Voltar mantendo alterações
git reset --mixed <commit>     #Voltar mantendo arquivos, mas não commits
git reset --hard <commit>      #Voltar apagando tudo


//Recuperar 

git reflog                #vai mostrar tudo que foi feito
git reset --hard xyz789   #recupera


//Adicionar e Alterar arquivos 

git add .               # adiciona tudo
git add nome-arquivo    # adiciona específico

git commit -m "mensagem"

//Enviar ou Puxar do Github 

git push                # envia mudanças
git pull                # puxa mudanças
git fetch               # atualiza sem aplicar

//Branches 

git branch              # listar branches
git branch nome         # criar branch

git switch nome         # trocar de branch
git checkout nome       # alternativa

//Mandar branch para main depois de resolvido os conflitos

git checkout main
git pull
git merge sua-branch
git push

git branch backup    #criar checkpoint

//Merge - juntar branches 

git merge nome-branch

//Descartar alterações 

git restore nome-arquivo
git reset --hard

//Salvar temporário 

git stash
git stash pop

//Conectar GitHub

git remote add origin URL
git push -u origin main


*************DOCKER****************

//Rodar postgresql

docker run --name postgres-db \
-e POSTGRES_PASSWORD=123456 \
-p 5432:5432 \
-d postgres

# subir banco
docker start postgres-db

//Ver container 

docker ps

// Iniciar ou parar

docker start postgres-db
docker stop postgres-db

//Entrar no container 

docker exec -it postgres-db bash

//Entrar no banco 

psql -U postgres

//Ver bancos 

\l

//Conectar banco 

\c axiomcode

//Ver tabelas 

\dt

****************BANCO DE DADOS*****************

//Inserir usuário 

INSERT INTO usuarios (nome_usuario, senha_hash, eh_admin)
VALUES ('admin', 'HASH_AQUI', true);

//Buscar usuario

SELECT * FROM usuarios;

//Deletar

DELETE FROM usuarios WHERE id = 1;

//Atualizar 

UPDATE usuarios SET nome_usuario = 'novo' WHERE id = 1;

*************DOTNET*******************

//Rodar o projeto 

dotnet run

//Restaura pendencias 

dotnet restore

//Instalar pacote 

dotnet add package Npgsql

//Buildar projeto 

dotnet build



git switch -c nome      # cria e troca

//
