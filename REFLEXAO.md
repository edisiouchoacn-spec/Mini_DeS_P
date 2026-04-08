# Reflexão — Portfólio Git

# O que achei difícil;

A parte mais complicada foi entender a lógica de onde cada comando deve ser executado. No começo não ficava claro por que precisava clonar o repositório, entrar na pasta e só então começar a trabalhar. A relação entre o repositório local e o remoto (GitHub) demorou para fazer sentido, especialmente o fato de que um commit existe primeiro só na minha máquina e só vai para o site depois do "git push".

Criar o conflito de merge foi trabalhoso. Entender que precisava editar o mesmo trecho do mesmo arquivo em duas branches diferentes, e que o Git não consegue decidir sozinho qual versão manter, exigiu tentativa e erro. O momento em que o arquivo abriu cheio de marcadores '<<<<<<<' e '>>>>>>>' foi confuso, não sabia exatamente o que apagar e o que manter.

Os commits semânticos também exigiram atenção constante. É fácil esquecer o padrão e digitar uma mensagem genérica como "atualização". Precisei pausar antes de cada commit para pensar no tipo correto e numa descrição útil.

# O que ficou evidente para mim;

Ficou claro que o Git é essencialmente um sistema de snapshots — cada commit é uma fotografia do projeto naquele momento, e o histórico é a sequência dessas fotos. Essa analogia ajudou muito a entender por que os commits precisam ser descritivos: uma foto sem legenda não diz nada.

Também ficou claro o propósito das branches. Trabalhar em uma branch separada significa que posso experimentar sem medo de estragar a main. O merge só acontece quando eu decido que o trabalho está pronto. Isso faz sentido especialmente em equipes, onde várias pessoas trabalham em paralelo.

O fluxo 'add → commit → push' ficou automático. Entendo agora que 'add' seleciona o que vai na foto, 'commit' tira a foto e 'push' envia para o álbum online.

# O que ainda é confuso meio confuso

Ainda não entendo completamente o estado do HEAD durante operações de merge. Quando estava resolvendo o conflito, o terminal mostrava informações sobre o HEAD que não ficaram totalmente claras — sabia o que fazer na prática mas não entendia exatamente o que estava acontecendo por baixo.

Também fiquei com dúvida sobre quando usar 'git merge' versus 'git rebase'. Ouvi falar em rebase mas não usei neste exercício — preciso entender a diferença e quando cada um é mais adequado.

Por fim, o comportamento do Git com arquivos não rastreados (untracked) ainda gera dúvidas ocasionais. Às vezes arquivos aparecem como untracked sem eu entender por quê, e fico inseguro sobre se devo adicioná-los ou ignorá-los.