# Gerar Chave Git
$ ssh-keygen -t ed25519 -C sergio2119wyz@gmail.com
Generating public/private ed25519 key pair.
Enter file in which to save the key (/c/Users/js058/.ssh/id_ed25519):
******************************************************************************
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ cd /c/users/js058/.ssh/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/users/js058/.ssh
$ ls
id_ed25519  id_ed25519.pub
**************************************************************************
# Verificar a chave publica gerada e copiar para a conta GitHub
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/users/js058/.ssh
$ cat id_ed25519.pub
***********************************************************************************
# Iniciar a Chave no Windows e add a chave privada 
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/users/js058/.ssh
$ eval $(ssh-agent -s)
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/users/js058/.ssh
$ ssh-add id_ed25519
Enter passphrase for id_ed25519:
Identity added: id_ed25519 (sergio2119wyz@gmail.com)
************************************************************************************
# Clonar um repositorio GitHub
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/users/js058/.ssh
$ git clone git@github.com:airbnb/javascript.git
*********************************************************************************
# Criando um Projeto
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace
$ mkdir livro-receitas
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace
$ cd livro-receitas/
********************************************************************************
# Inicializar o GIT
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas
$ git init
Initialized empty Git repository in C:/Workspace/livro-receitas/.git/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ ls -a
./  ../  .git/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ cd .git
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas/.git (GIT_DIR!)
$ ls
HEAD  config  description  hooks/  info/  objects/  refs/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas/.git (GIT_DIR!)
$ cd ..
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
*************************************************************************************
# Configuracao Inicial
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git config --global user.email "sergio2119wyz@gmail"
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git config --global user.name jsergio
****************************************************************************************
# Criando Arquivo Markdown
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git add *
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git commit -m "commit inicial"
[master (root-commit) 640f350] commit inicial
 1 file changed, 192 insertions(+)
 create mode 100644 lista.md
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean
$ mkdir receitas
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ ls
lista.md  receitas/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ mv lista.md ./receitas/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ ls
receitas/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    lista.md
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        receitas/
no changes added to commit (use "git add" and/or "git commit -a")
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git add lista.md receitas/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    lista.md -> receitas/lista.md
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git commit  -m "Cria pasta receitas,move arquivo para receitas"
[master 4fbbfd1] Cria pasta receitas,move arquivo para receitas
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename lista.md => receitas/lista.md (100%)

jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ echo > README.md

jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ ls
README.md  receitas/

jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git add *

jsergio@LAPTOP-CBSQ8HH4 MINGW64 /c/Workspace/livro-receitas (master)
$ git commit -m "Adiciona index"
[master e6813da] Adiciona index
 1 file changed, 150 insertions(+)
 create mode 100644 README.md
********************************************************************************************
Configurações do Git Cliente
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=true
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=sergio2119wyz@gmail
user.name=jsergio
*********************************************************************************
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ git config --global --unset user.name

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=true
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=sergio2119wyz@gmail
******************************************************************
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ git config --global  user.name "jssergio"

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=true
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=sergio2119wyz@gmail
user.name=jssergio

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ git config --global  user.email "sergio2119wyz@gmail.com"

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=true
pull.rebase=false
credential.helper=manager-core
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=sergio2119wyz@gmail.com
user.name=jssergio
****************************************************************************
Add Remote GitHub
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace
$ ls
GitHub/  livro-receitas/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace
$ cd livro-receitas/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ ls
README.md  receitas/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git remote add origin git@github.com:jssergio/livro-receitas.git
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git remote -v
origin  git@github.com:jssergio/livro-receitas.git (fetch)
origin  git@github.com:jssergio/livro-receitas.git (push)
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git status
On branch master
nothing to commit, working tree clean
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git push origin master
Enter passphrase for key '/c/Users/js058/.ssh/id_ed25519':
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (8/8), 3.16 KiB | 1.58 MiB/s, done.
Total 8 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:jssergio/livro-receitas.git
 * [new branch]      master -> master
******************************************************************************************
Envio do Arquivo README.md alterado
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git add *

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md


jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git commit -m "Altera o README,md"
[master 8057725] Altera o README,md
 1 file changed, 1 insertion(+)

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git push origin master
Enter passphrase for key '/c/Users/js058/.ssh/id_ed25519':
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 349 bytes | 349.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:jssergio/livro-receitas.git
   e6813da..8057725  master -> master
****************************************************************************************
Envio do Arquivo README.md alterado por outra Pessoa
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git add *

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md


jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git commit -m "Altera o README,md"
[master 65607b7] Altera o README,md
 1 file changed, 2 insertions(+), 1 deletion(-)

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git push origin master
Enter passphrase for key '/c/Users/js058/.ssh/id_ed25519':
To github.com:jssergio/livro-receitas.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'github.com:jssergio/livro-receitas.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git pull origin master
Enter passphrase for key '/c/Users/js058/.ssh/id_ed25519':
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 695 bytes | 23.00 KiB/s, done.
From github.com:jssergio/livro-receitas
 * branch            master     -> FETCH_HEAD
   8057725..fd31e87  master     -> origin/master
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master|MERGING)
$ git status
On branch master
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master|MERGING)
$ git add *

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master|MERGING)
$ git commit -m "Altera o README.md"
[master b0dfd34] Altera o README.md

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/livro-receitas (master)
$ git push origin master
Enter passphrase for key '/c/Users/js058/.ssh/id_ed25519':
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 649 bytes | 649.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To github.com:jssergio/livro-receitas.git
   fd31e87..b0dfd34  mast
***************************************************
Iniciando um novo Projeto(Pasta)- git@github.com:jssergio/GitHub.git
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/GitHub
$ git init
Initialized empty Git repository in C:/Users/js058/Desktop/Workspace/GitHub/.git/
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/GitHub (master)
$ git remote add origin git@github.com:jssergio/GitHub.git

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/GitHub (master)
$ git remote -v
origin  git@github.com:jssergio/GitHub.git (fetch)
origin  git@github.com:jssergio/GitHub.git (push)
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/GitHub (master)
$ git status
On branch master
No commits yet
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        GitHub.md
nothing added to commit but untracked files present (use "git add" to track)
jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/GitHub (master)
$ git add *

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/GitHub (master)
$ git commit -m "Enviar o GitHub.md"
[master (root-commit) 2bad6f7] Enviar o GitHub.md
 1 file changed, 410 insertions(+)
 create mode 100644 GitHub.md

jsergio@LAPTOP-CBSQ8HH4 MINGW64 ~/Desktop/Workspace/GitHub (master)
$ git push origin master
Enter passphrase for key '/c/Users/js058/.ssh/id_ed25519':
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 2.91 KiB | 2.91 MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:jssergio/GitHub.git
 * [new branch]      master -> master




