# Instruktioner

- Starta WSL
- cd eller cd ~ för att komma till hemkatalogen
- cd code
- cd webb-komponenter
- code . för att starta vscode

För att skapa mappen webb-komponenter:
```bash
cd 
mkdir code
cd code
mkdir webb-komponenter
cd webb-komponenter
```

Annars skapa ett repo på github.
Kör Git clone på det.

```bash
git clone <url>
```

# Test mappen

Introduktion till NPM och package.json

```bash
mkdir newfolder
npm init -y
npm i sass
```

I package.json kan vi nu skapa scriptet som launchar sass
```json
"scripts": {
  "watch:sass": "sass --watch css" <- SAMMA MAPP
  "watch:sass": "sass --watch scss:css" <- SCSS byggs till CSS
 }
 ```
 Skapa en mapp för din css, alternativ för scss -> css. 
 
 Nu kan vi launcha detta genom debug menyn i vscode.
 Använd run, debug, skapa en config, lägg till en config för NPM run.
 Ändra scriptet som ska startas will watch:sass
 
 
 # SASS @use
 
 Vi bör använda @use istället för @import då import ska fasas ut.
 Vi kan då inte längre fortsätta med vår bad practice, globala variabler 😢
 
 Istället för att deklarera variabler i ```styles.scss``` så flyttar vi det till en ```_theme.scss``` fil.
 Vi kan då använda @use för att importera filen till ett theme namespace där vi behöver den.
 ```sass
 @use "theme" as theme;
 
 color: theme.$fg-color;
 ```
 
