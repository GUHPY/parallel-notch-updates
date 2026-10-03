# Parallel Notch releases

Este canal público distribui somente metadados e instaladores do Parallel Notch.
O código-fonte permanece no repositório privado do projeto.

Feed estável: https://raw.githubusercontent.com/GUHPY/parallel-notch-updates/main/updates/stable.json

O feed inicial não anuncia nenhuma release. `latest: null` significa que ainda
não há um instalador publicado neste canal. Nunca anuncie uma versão antes de
publicar o instalador correspondente.

Para cada release, gere o instalador e execute `installer/New-ReleaseFeed.ps1`
no repositório privado. Confira versão, página, tamanho e SHA-256 no JSON gerado.
Publique o instalador no repositório público com a tag `notch-v<versão>`, e só
depois atualize `updates/stable.json` neste canal.

O cliente aceita apenas schema 1, canal stable, versão numérica e páginas HTTPS
de releases deste repositório. Ele abre a página de download; instalação
automática e assinatura de pacotes pertencem à integração de distribuição da
Fase 19. Nenhum token ou credencial é distribuído junto do aplicativo.
