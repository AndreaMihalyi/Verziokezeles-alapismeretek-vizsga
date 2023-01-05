Verziókezelés alapismeretek vizsga:
A vizsga során alkalmazott git parancsok dokumentálása lépésenként:
I. Adott projekt klónozása saját gépre:
A. Mihályi Andrea Verziókezelés alapismeretek vizsga mappa létrehozása az asztalon
Mappába belépve jobb klikk->Git Bash Here: Terminál megnyitása
B. Git parancsok a megnyitott terminálban:
1. Git verziókezelő inicializálása a mappában:
$ git init
2. Távoli gyűjteményből letöltés helyi gyűjteménybe:
$ git pull https://github.com/szabopeter92/git-vizsga0104.git
remote: Enumerating objects: 15, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 15 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (15/15), 14.06 MiB | 7.86 MiB/s, done.
From https://github.com/szabopeter92/git-vizsga0104
 * branch            HEAD       -> FETCH_HEAD
II. README.md elnevezésű fájl létrehozása
Belépés a Visual Studio Code-ba
Mihályi Andrea Verziókezelés alapismeretek mappa megnyitása Visual Studio Code-ban
Új fájl létrehozása a már meglévő fájlok mellé: README.md
Git parancsok dokumentálása
III. .gitignore fájl létrehozása a .txt, .doc, .docx, .pdf kiterjesztésű fájlok figyelmen kívül hagyására
Nem támogatott fájlok listázása:
.gitignore fájl: Azon fájlok, mappák megadása akár név, akár kiterjesztés szerint, amelyek nem lesznek kezelve verziókövetéssel, nem kerülnek a Staging area-ba és nem lesznek feltöltve sem a helyi, sem a távoli gyűjteménybe.
-Egyes fájlok megadása: fájlnév.kiterjesztés
-Fájlok megadása kiterjesztés szerint: *.kiterjesztés
-Mappák megadása: mappanév/
Új fájl létrehozása a már meglévő fájlok mellé: .gitignore
#.txt fájlok ignorálása:
*.txt
#.doc fájlok ignorálása:
*.doc
#.docx fájlok ignorálása:
*.docx
#.pdf fájlok ignorálása:
*.pdf
IV. "console" elnevezésű ág létrehozása
1. "console" elnevezésű ág létrehozása:
$ git branch console
2. Váltás a "main" ágról a "console" ágra:
$ git checkout console

1. Státusz lekérése: Tájékoztat az utoljára létrehozott/módosított fájlokról/mappákról
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
Csak a README.md fájl van jelölve létrahozott, de nem követett fájlként, a többi fájl nincs hozzáadva
2. Fájlok hozzáadása a Staging area-hoz: Ezeknek a fájlok lesznek követve verziókövetéssel
Három mód: - Fájlok hozzáadása a Staging area-hoz egyesével:
           $ git add fájlnév.fájlkiterjesztés megadása
           - Fájlok hozzáadá sa a Staging area-hoz egyesével:
            $ git add *.fájlkiterjesztés megadása
           - Valamennyi fájl hozzáadása a Staging area-hoz:
             $ git add.
(Tévesen Staging area-hoz hozzáadott fájlok eltávolítása:
$ git rm --cached fájlnév.fájlkiterjesztés megadása)
$ git add .