A: echo 01 > arquivo.txt
foi criado o arquivo.txt

B: git add arquivo.txt
o arquivo foi adicionado ao modo de staging

C: git commit -m "git add example - arquivo.txt"
[main (root-commit) 98b1782] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt

 D: echo 02 > arquivo.txt

 E: git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

F: git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

G: git diff --staged
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02


H: echo 03 > arquivo.txt

I: git diff
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03


J: 
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ git restore --staged arquivo.txt
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")




K:
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ git commit -m "Passo K do exercicio 01"
[main e8100bc] Passo K do exercicio 01
 1 file changed, 1 insertion(+), 1 deletion(-)
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ git log
commit e8100bc0ea4f41347ae4fd3554a2592287803652 (HEAD -> main)
Author: Andruei Silva <andruei.silva@aluno.faculdadeimpacta.com.br>
Date:   Thu Aug 8 23:30:00 2024 +0000

    Passo K do exercicio 01

commit 98b17823ee4fc9aec85d37420a93b3e558507dc0
Author: Andruei Silva <andruei.silva@aluno.faculdadeimpacta.com.br>
Date:   Thu Aug 8 23:16:59 2024 +0000

    git add example - arquivo.txt


L:
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ echo *.txt > .gitignore
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ ls -la
total 20
drwxrwxrwx+ 3 codespace codespace 4096 Aug  8 23:31 .
drwxrwxrwx+ 3 codespace root      4096 Aug  8 21:30 ..
drwxrwxrwx+ 8 codespace codespace 4096 Aug  8 23:30 .git
-rw-rw-rw-  1 codespace codespace   12 Aug  8 23:31 .gitignore
-rw-rw-rw-  1 codespace codespace    3 Aug  8 23:22 arquivo.txt


M: 
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ touch novo.txt
@AndrueiSilva ➜ /workspaces/codespaces-blank/aula (main) $ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        novo.txt

nothing added to commit but untracked files present (use "git add" to track)
