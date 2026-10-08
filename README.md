# WR Topografia e Projetos (demo)

Landing page de demonstração, HTML único (`index.html`), sem dependências além das fontes do Google Fonts. Não publicada.

## Estrutura
- `index.html`: o site (hero com guia "Do que você precisa?", serviços em 4 frentes com filtro, onde atuamos, aerofotogrametria, quem somos, como trabalhamos, formulário que abre o WhatsApp, dúvidas, contato com mapa)
- `Copy.txt`: texto da página
- `design-system-wr.md` / `.html`: design system
- `assets/`: logo com fundo transparente (`logo-completa.png`), bússola (`marca-bussola*.png`), favicon e imagem de compartilhamento
- `Logo/`, `Fotos/`, `Info maps.txt`, `Texto e serviços (enviado pelo cliente).txt`: materiais de origem

## Como visualizar
Na pasta da agência: `node "_ferramentas/preview-local.mjs" "4. Meus Clientes/2. Demos e propostas/WR Topografia e Projetos Ltda"` e abrir o endereço mostrado.

## Antes de publicar
- O `index.html` tem `<meta name="robots" content="noindex, nofollow">` para a demo não aparecer no Google. Remover ao publicar o site definitivo.
- Os itens `[A CONFIRMAR]` aparecem no site com borda tracejada; a lista completa está na ficha em `4. Meus Clientes/_Fichas/WR Topografia.pdf`.
- Sem fotos reais o hero usa curvas de nível geradas por script. Quando chegarem, colocar em `Fotos/`, rodar `node "_ferramentas/otimizar-fotos.mjs"` e usar no hero e na seção do Wellington.
- O número (31) 99140-1391 veio do Google Maps; confirmar que é WhatsApp (`WA_NUMBER` no script do fim do arquivo).
- `Logo WR com Bússola Metálica e Tagline.png` (versão 3D) tem ruído colorido nas bordas e não foi usada; pedir o arquivo original ao cliente se ele preferir essa versão.
