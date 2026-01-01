# Cheat-sheet: comandos básicos (PowerShell & Git)

Este arquivo reúne os comandos básicos que você pode usar no Windows (PowerShell) e no Git.

## PowerShell (Windows)

- Listar / Navegar: `ls` / `Get-ChildItem`, `cd <pasta>`, `pwd`
- Criar pasta: `mkdir <pasta>`
- Remover arquivo/pasta: `rm -Recurse <arquivo|pasta>`
- Copiar / Mover: `cp <origem> <destino>` / `mv <origem> <destino>`
- Ver arquivo: `Get-Content <arquivo>` (ou `cat`)
- Abrir no VS Code: `code .`
- Limpar terminal: `cls`

Exemplo:
```
cd "C:\Users\SeuUsuario\projeto"
ls
code .
```

## Git — fluxo básico

- Clonar: `git clone <url>`
- Ver status: `git status`
- Adicionar: `git add .` ou `git add -A`
- Commitar: `git commit -m "mensagem"`
- Enviar (push): `git push origin <branch>`
- Puxar (pull): `git pull`
- Criar/ir para branch: `git checkout -b <nome>` / `git checkout <nome>`
- Ver histórico: `git log --oneline --graph --decorate`
- Ver diferenças: `git diff`
- Stash: `git stash` / `git stash pop`
- Remotos: `git remote -v`

Exemplo de workflow:
```
git status
git add -A
git commit -m "feat: descrição"
git push origin main
```

## Comandos de correção/undo (use com cuidado)

- `git restore <arquivo>` — desfaz alterações não staged
- `git restore --staged <arquivo>` — remove do staged
- `git reset --soft HEAD~1` — desfaz último commit mantendo mudanças
- `git reset --hard HEAD~1` — desfaz último commit e descarta mudanças (perigoso)
- `git revert <commit>` — cria commit que inverte outro commit

## Dicas rápidas

- Sempre rode `git status` antes de commitar.
- Use mensagens de commit concisas e padronizadas (`feat:`, `fix:`, `docs:`).
- Trabalhe em branches para features/bugs.

Feito para te ajudar a lembrar os comandos mais usados. — Boa codificação!
