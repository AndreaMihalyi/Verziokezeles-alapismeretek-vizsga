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

Új fájl létrehozása a már meglévő fájlok mellé:

.gitignore

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

V. Kiindulási verzió létrehozása:

1. Fájlok hozzáadása a Staging area-hoz:

    Ezek a fájlok lesznek követve verziókövetéssel

    Három mód:

    - Fájlok hozzáadása a Staging area-hoz egyesével:

        $ git add fájlnév.fájlkiterjesztés megadása

    - Fájlok hozzáadása a Staging area-hoz kiterjesztés alapján:

        $ git add *.fájlkiterjesztés megadása

    - Valamennyi fájl hozzáadása a Staging area-hoz:

        $ git add .

    (Tévesen Staging area-hoz hozzáadott fájlok eltávolítása:

$ git rm --cached fájlnév.fájlkiterjesztés megadása)

2. Kiindulási verzió létrehozása -> Verzió mentése a helyi gyűjteménybe:
$ git commit -m "README.md és .gitignore fájlok hozzáadva"

    [console 7c4303b] README.md és .gitignore fájlok hozzáadva

     2 files changed, 70 insertions(+)

    create mode 100644 .gitignore

    create mode 100644 README.md

VI. App.js fájl módosítása: Ha az oldal betöltődött, akkor a consolba írjuk ki „Az oldal sikeresen betöltődött.”

App.js fájl módosítása -> Megjelenik az M-Modified jelzés

1. Státusz lekérése: 

    Tájékoztat az utoljára létrehozott/módosított fájlokról/mappákról

    $ git status

    On branch console

    Changes not staged for commit:

    (use "git add <file>..." to update what will be committed)

    (use "git restore <file>..." to discard changes in working directory)

    modified:   README.md

    modified:   app.js

    no changes added to commit (use "git add" and/or "git commit -a")

2. Fájlok hozzáadása a Staging area-hoz:
    
    Ezek a fájlok lesznek követve verziókövetéssel

    Három mód:
    - Fájlok hozzáadása a Staging area-hoz egyesével:

        $ git add fájlnév.fájlkiterjesztés megadása

    - Fájlok hozzáadá sa a Staging area-hoz egyesével:

        $ git add *.fájlkiterjesztés megadása

    - Valamennyi fájl hozzáadása a Staging area-hoz:

        $ git add.

(Tévesen Staging area-hoz hozzáadott fájlok eltávolítása:

$ git rm --cached fájlnév.fájlkiterjesztés megadása)

$ git add .

3. Státusz lekérése:
    
    Tájékoztat az utoljára létrehozott/módosított fájlokról/mappákról
    
    $ git status

    On branch console

    Changes to be committed:

    (use "git restore --staged <file>..." to unstage)

    modified:   README.md

    modified:   app.js

    Changes not staged for commit:

    (use "git add <filef>..." to update what will be committed)

    (use "git restore <file>..." to discard changes in working directory)

    modified:   README.md

4. App.js fájl módosítása: Ha az oldal betöltődött, akkor a consolba írjuk ki „Az oldal sikeresen betöltődött.”
-> Verzió mentése a helyi gyűjteménybe.

    $ git commit -m "Módosítás az app.js fájlban létrehozva."

    [console 3dd1dc9] Módosítás az app.js fájlban létrehozva.

    2 files changed, 20 insertions(+), 10 deletions(-)

VI. CSS fájlban a weboldal háttérszínének módosítása:

CSS fájl módosítása -> Megjelenik az M-Modified jelzés

1. $ clear - Törlés, hogy a terminál üres legyen

2. Státusz lekérése:

    Tájékoztat az utoljára létrehozott/módosított fájlokról/mappákról

    $ git status

    On branch console
    Changes not staged for commit:

    (use "git add <file>..." to update what will be committed)

    (use "git restore <file>..." to discard changes in working directory)

    modified:   README.md

    modified:   style.css

    no changes added to commit (use "git add" and/or "git commit -a")

2. Fájlok hozzáadása a Staging area-hoz:
Ezek a fájlok lesznek követve verziókövetéssel

    Három mód:
    - Fájlok hozzáadása a Staging area-hoz egyesével:
           
        $ git add fájlnév.fájlkiterjesztés megadása

    - Fájlok hozzáadá sa a Staging area-hoz egyesével:

        $ git add *.fájlkiterjesztés megadása

    - Valamennyi fájl hozzáadása a Staging area-hoz:

        $ git add.

(Tévesen Staging area-hoz hozzáadott fájlok eltávolítása:

$ git rm --cached fájlnév.fájlkiterjesztés megadása)

$ git add .

3. Státusz lekérése:

    Tájékoztat az utoljára létrehozott/módosított
fájlokról/mappákról

    $ git status

    On branch console

    Changes to be committed:

    (use "git restore --staged <file>..." to unstage)

    modified:   README.md

    modified:   style.css

4. CSS fájl módosítása: CSS fájlban a weboldal háttérszínének módosítása -> Verzió mentése a helyi gyűjteménybe.

    $ git commit -m "Módosítás a CSS fájlban létrehozva."

    [console 7c19a14] Módosítás a CSS fájlban létrehozva.

    2 files changed, 44 insertions(+), 2 deletions(-)

VII. A "console" ág végleges verizójának feltöltése a helyi gyűjteményből a távoli gyűjteménybe (saját Github fiókba)

1. Távoli gyűjtemény megadása:

    $ git remote add origin https://github.com/AndreaMihalyi/Verziokezeles-alapismeretek-vizsga.git

2. Feltöltés távoli gyűjteménybe:

    $ git push u- origin console