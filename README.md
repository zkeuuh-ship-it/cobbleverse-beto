# COBBLEVERSE - Beto

Lista de mods do servidor `ultra-01.roxy.net.br:25646`, lida pelo launcher a cada partida.

**O launcher busca este arquivo:** [`pack.json`](pack.json)

Quando você troca mods no servidor e atualiza este arquivo, todos os jogadores recebem a
mudança sozinhos na próxima vez que abrirem o launcher — ninguém precisa baixar um `.exe` novo.
Se o GitHub estiver fora do ar, o launcher usa a lista que veio dentro dele.

## O que tem dentro do pack.json

| Campo | Para que serve |
|---|---|
| `packVersion` | Mude quando alterar a lista (aparece no launcher) |
| `minecraft` / `fabricLoader` / `javaMajor` | Versões que o launcher instala |
| `server` | Endereço para onde o botão JOGAR conecta |
| `overrides` | Zip do modpack de onde saem configs, shaders e resource packs |
| `mods` | Os 166 mods: nome do arquivo, tamanho, SHA-1 e endereço de download |

Cada mod é conferido pelo **SHA-1** antes de abrir o jogo. Se um arquivo vier corrompido ou
faltando, o launcher baixa de novo sozinho.

> Não edite o `pack.json` na mão sem cuidado: um `sha1` errado faz o launcher rejeitar o arquivo
> e baixar em loop. O jeito certo é gerar a lista de novo a partir da pasta `mods/` do servidor.
