# 🚀 Comandos-dev
## Arsenal de Comandos para consulta

## git básico
git init                    # Cria um repositório Git na pasta atual - Usar quando o projeto está local e você quer começar a versionar
git add .                   # Salva as mudanças feitas, coloca o arquivo na área de preparo (adiciona tudo)
git add exemplo.html        # Salva mudanças específicas 
git commit -m "msg"         # Cria uma versão do projeto (importante incluir mensagens claras e objetivas no commit"
git push -u origin (branch) # Envia seu código para o GitHub
git remote add origin (URL) # Conecta seu projeto local ao GitHub (usar depois de ter um repositório criado no GitHub)

## Status e Histórico 

git status                             # Mostra tudo que está acontecendo (arquivos modificados e não rastreados)
git log --oneline                      # histórico resumido
git log                                #ver os commits
git checkout <id-do-commit>            #acessar uma versão sem apagar nada
git checkout -b nome-da-nova-branch    #trabalhar na versão escolhida

## Reset

git reset --soft <commit>      #Voltar commit mantendo alterações
git reset --mixed <commit>     #Voltar commit mantendo arquivos, mas não commits
git reset --hard <commit>      #Voltar commit apagando tudo


## Recuperar e Ver histórico 

git log                           # Histórico completo
git log --oneline --graph --all   # Mostra commits resumidos, estrutura das branches e histórico visual
git tag v1.0                      # Marca um commit como versão (usar em entregas importantes)
git reflog                        # Vai mostrar tudo que foi feito
git reset --hard (n° commit)      # Move seu projeto inteiro para o commit e apaga tudo que veio depois.
git diff                          # Mostra o que mudou no código


## Adicionar e Alterar arquivos 

git add .                 # adiciona tudo
git add nome-arquivo      # adiciona específico
git commit -m "mensagem"  # Slava as atualizações na branch

## Enviar ou Puxar do Github 

git push                # envia mudanças
git pull                # puxa mudanças
git fetch               # atualiza sem aplicar
git clone https:/****   # Baixa um repositório do GitHub pra sua máquina (Usar quando o projeto já existe no GitHub)

# Branches 

git branch                   # listar branches existentes e também verificar em qual você está 
git branch (nome)            # criar branch
git switch tal-branch        # trocar de branch
git checkout main            # Troca de Branch (só trocar main pela branch que quer trocar)
git checkout -b nova-branch  # Cria uma nova branch e entra nela
git switch -c nova-branch    # Cria uma nova branch e entra nela
git pull origin *branch*     # Atualiza seu projeto com o que está no GitHub (Sempre utilizar antes de trabalhar no projeto)
git merge main               # Junta sua branch a outra (Mantém histórico real)
git rebase main              # Junta sua branch a outra (reescreve histórico)
git push -u origin (branch)  # Envia seu código para o GitHub
git restore arquivo.txt      # Desfaz alterações que não foram commitadas


## Descartar alterações 

git restore nome-arquivo  # Descarta alterações de um arquivo específico que ainda não foram commitadas.
git reset --hard          # Volta o projeto inteiro para o último commit e apaga todas as alterações não salvas
git checkout -- .         # Descarta alterações não comitadas 

## Salvar temporário 

git stash         # Guarda alterações sem precisar commitar
git stash pop     # Recuperar o commit
git stash list    # Ver Lista

## Conectar GitHub

git remote add origin URL
git push -u origin main


# DOCKER

## Rodar postgresql

docker run                        # Cria e inicia um container
docker run --name postgres-db     # inicia um container que já existe
-e POSTGRES_PASSWORD=123456       # Define uma variável de ambiente dentro do container   
-p 5432:5432                      # Mapeia portas
-d postgres                       # Roda o container em segundo plano

## subir banco
docker start postgres-db         # Roda um container
docker ps                        # Lista todos os containers que estão rodando no momento.

## Iniciar ou parar

docker start postgres-db
docker stop postgres-db

## Entrar no container 

docker exec -it postgres-db bash

## Entrar no banco 

psql -U postgres

## Ver bancos 

\l

## Conectar banco 

\c nome-container

## Ver tabelas 

\dt

# BANCO DE DADOS

## Inserir usuário 

INSERT INTO usuarios (nome_usuario, senha_hash, eh_admin)
VALUES ('admin', 'HASH_AQUI', true);

## Buscar usuario

SELECT * FROM usuarios;

## Deletar

DELETE FROM usuarios WHERE id = 1;

## Atualizar 

UPDATE usuarios SET nome_usuario = 'novo' WHERE id = 1;

# DOTNET

## Rodar o projeto 

dotnet run

## Restaura pendencias 

dotnet restore

## Instalar pacote 

dotnet add package Npgsql

## Buildar projeto 

dotnet build


