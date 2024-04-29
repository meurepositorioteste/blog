+++
title = 'Git Exposed Attack'
date = 2024-04-26T16:29:22-03:00
draft = false
+++

# Git exposed Attack

* Exposição da pasta `.git` em um servidor web
* Obtém acesso a todo código fonte da aplicação
* Pasta `objects` fica todas as alterações feita
* Extensão `dotGit` ajuda achar .git exposto
* O `wfuzz` mapea a url do site procurando a pasta .git exposta
```bash
wfuzz -c -z file, [wordlist] [filtro de tamanho] [url]/FUZZ
```

* A ferramenta git-dumper extrai dados do arquivo .git
```bash
git_dumper.py [url] [pasta de output]
```

Baixa o arquivo .git
para ver se existe arquivos novos
```bash
git status
```
para ver os commits
```bash
git log  
```
mostra o conteudo do commit
```bash
git show [hash]
```
