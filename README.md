## 1.1 Initialization
```bash
sudo apt-get install git hugo nano
hugo new site shared-consulting && cd shared-consulting
git init
git submodule add https://github.com/hotpotcookie/nord-hugo-book.git themes/nord-hugo-book
hugo server --minify --theme nord-hugo-book
## https://favicon.io/favicon-generator/
```
## 1.2 Config Setup
```bash
nano config.toml
```
```toml
baseURL = 'https://shared-consulting.netlify.app/'
languageCode = 'en-us'
title = 'Shared Consulting'
theme = 'nord-hugo-book'

[params]
  BookTheme = 'light'
  BookSearch = true
  BookRepo = 'https://github.com/monsieurDuke/shared-consulting' 
  BookDateFormat = '02-02-2002'
  favicon = '/favicon.png'

[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true

  [markup.highlight]
    anchorLineNos = false
    codeFences = true
    guessSyntax = false
    hl_Lines = ''
    hl_inline = false
    lineAnchors = ''
    lineNoStart = 1
    lineNos = false
    lineNumbersInTable = true
    noClasses = true
    noHl = false
    tabWidth = 4
```

## push to github
```bash
git config --global user.name "monsieurDuke"
git config --global user.email "icatmuhammad2@gmail.com"
git remote add origin https://github.com/monsieurDuke/shared-consulting.git
git branch -M main
git push -u origin main
```
