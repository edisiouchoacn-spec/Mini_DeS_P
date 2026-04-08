# Registro de Conflito de Merge

# O que causou o conflito

O conflito ocorreu no arquivo 'projeto/hello-world/index.js'. Duas branches criadas a partir do mesmo commit editaram o mesmo trecho do arquivo — a constante 'GREETINGS' e o comentário inicial. A branch 'fix/versao-a' alterou para português e a branch 'fix/versao-b' para inglês.

# Como decidi qual versão manter

Após o merge da "fix/versao-a" na main, ao tentar mergear a "fix/versao-b", o Git não conseguiu resolver automaticamente. Optei por manter a versão que considerei mais adequada, removendo os marcadores de conflito ('<<<<<<<', '=======', '>>>>>>>') manualmente no VS Code.

# Como resolvi

```bash
git checkout fix/versao-b
git merge main
# editei o arquivo manualmente no VS Code
git add projeto/hello-world/index.js
git commit -m "fix(hello-world): resolve conflito entre versão A e versão B"
git push
```