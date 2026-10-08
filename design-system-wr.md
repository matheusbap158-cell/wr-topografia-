# Design system: WR Topografia e Projetos

Base: a logo enviada pelo cliente (bússola em cobre e bronze, "WR" em azul-ciano degradê, linha cobre). Tudo parte dela: o azul-ciano é a cor de identidade, o cobre é a cor de ação, o preto é o fundo da marca.

## Tom visual (3 linhas)
1. Escuro, técnico e limpo, como a tela de um equipamento de campo: fundo quase preto, linhas finas e curvas de nível.
2. Azul-ciano para informação e destaque, cobre para o que o visitante deve clicar.
3. Rigor de planta topográfica (coordenadas, grade, escala) com acabamento premium, sem enfeite.

## 1. Cores

| Papel | Token | Hex | Uso |
|---|---|---|---|
| Fundo principal | --bg-950 | #04070B | Hero, rodapé, seções escuras |
| Fundo alternado | --bg-900 | #08111A | Seções escuras alternadas |
| Superfície | --bg-800 | #0D1B28 | Cards sobre fundo escuro |
| Ciano (identidade) | --cyan-400 | #43C3F0 | Destaques, ícones, links em fundo escuro |
| Ciano médio | --cyan-500 | #2AA6D6 | Hover de links, linhas |
| Ciano profundo | --cyan-700 | #176C93 | Texto de destaque em fundo claro (contraste 5,2:1) |
| Cobre (ação) | --copper-500 | #E27A3A | Botão primário |
| Cobre claro | --copper-400 | #F08A4B | Hover do botão primário, a bússola |
| Cobre escuro | --copper-600 | #C4642A | Estado ativo |
| Bronze claro | --bronze-300 | #E9D3A8 | Detalhes finos, números |
| Papel | --paper-50 | #F2F6F8 | Seções claras |
| Papel 2 | --paper-100 | #E4ECF0 | Seção clara alternada |
| Tinta | --ink | #0A1A24 | Texto em fundo claro |
| Texto secundário | --muted | #475F6D | Texto de apoio em fundo claro |
| Texto em fundo escuro | --text-on-dark | #EAF2F6 | Corpo em fundo escuro |
| Apoio em fundo escuro | --muted-on-dark | #9FB4C0 | Texto de apoio em fundo escuro |
| WhatsApp | --wa-500 | #25D366 | **Exclusivo** do botão e do flutuante de WhatsApp |
| Alerta | --alert-500 | #E5624A | Erro de formulário |

Regras: o verde do WhatsApp nunca é decorativo. Texto de corpo com contraste mínimo de 4,5:1. O botão primário usa texto escuro (#04070B) sobre o cobre (contraste acima de 7:1).

## 2. Tipografia

| Uso | Fonte | Peso |
|---|---|---|
| Títulos | Sora | 600 e 700 |
| Corpo | Inter | 400, 500 e 600 |
| Dados, coordenadas, rótulos | JetBrains Mono | 500 |

Link de fontes: `https://fonts.googleapis.com/css2?family=Sora:wght@600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@500&display=swap`

Hierarquia (desktop / mobile):
- H1: 56 px / 34 px, peso 700, entrelinha 1,06, espaçamento -0,03em
- H2: 42 px / 29 px, peso 700, entrelinha 1,1, espaçamento -0,025em
- H3: 20 px / 18 px, peso 600, entrelinha 1,25
- Corpo: 17 px / 16 px, peso 400, entrelinha 1,7
- Rótulo (mono): 12,5 px, caixa alta, espaçamento 0,14em
- Botão: 15 px, peso 700

## 3. Componentes

**Botão primário:** fundo cobre, texto #04070B, 54 px de altura, raio 10 px. Hover: cobre claro e sobe 2 px. Foco: contorno ciano de 3 px.
**Botão secundário (ghost):** contorno branco a 40% (ciano profundo em fundo claro), fundo transparente.
**Botão WhatsApp:** verde #25D366, texto escuro #04070B (contraste AA; o branco não passa), só nos CTAs de contato direto. Um por dobra, no máximo dois.
**Card de serviço:** fundo --bg-800, borda de 1 px a 10% de branco, raio 14 px. Hover: borda ciano e leve elevação. Contém ícone de linha fina (ciano), título, texto, rótulo "Indicado para" e link "Pedir orçamento deste serviço".
**Filtro (chip):** pílula com borda fina; ativo = fundo ciano e texto escuro.
**Campo de formulário:** fundo --bg-800, borda a 14% de branco, raio 10 px, 52 px de altura. Foco: borda ciano e anel de 3 px. Erro: borda --alert-500 e mensagem abaixo.
**Placeholder de pendência:** borda tracejada, texto "[A CONFIRMAR]", sempre visível.

## 4. Estética
- Raios: 10 px (controles), 14 px (cards), 999 px (chips).
- Sombras: quase nenhuma. Profundidade vem de borda fina e fundo mais claro. Só o botão primário tem um brilho cobre suave.
- Espaçamento (base 8): 8, 16, 24, 32, 48, 64, 96 px. Seções com 96 px no desktop e 60 px no mobile.
- Linhas: 1 px, 10% de branco. Grade de coordenadas e curvas de nível como textura de fundo, com opacidade entre 6% e 14%.
- Movimento: bússola que oscila devagar, linhas de nível que se desenham e revelação suave ao rolar. Tudo desligado com `prefers-reduced-motion`.

## 5. Conversão para WhatsApp
- CTA no topo (cabeçalho), no hero, depois do catálogo, no "Quem somos" e no fim.
- Cada card de serviço leva ao formulário já com o serviço escolhido, e a mensagem do WhatsApp chega dizendo qual serviço a pessoa quer.
- O guia "Do que você precisa?" no hero reduz a dúvida de quem não conhece o nome técnico.
- O número do Wellington e o botão flutuante estão sempre à mão no celular.
- Autoridade: coordenadas reais da sede, os quatro produtos de aerolevantamento explicados, e o fundador com nome e rosto.

## Tokens prontos (CSS)

```css
:root{
  --bg-950:#04070B; --bg-900:#08111A; --bg-800:#0D1B28;
  --cyan-400:#43C3F0; --cyan-500:#2AA6D6; --cyan-700:#176C93;
  --copper-400:#F08A4B; --copper-500:#E27A3A; --copper-600:#C4642A;
  --bronze-300:#E9D3A8;
  --paper-50:#F2F6F8; --paper-100:#E4ECF0;
  --ink:#0A1A24; --muted:#475F6D;
  --text-on-dark:#EAF2F6; --muted-on-dark:#9FB4C0;
  --wa-500:#25D366; --alert-500:#E5624A;
  --line:rgba(255,255,255,.1);
  --font-display:'Sora',system-ui,sans-serif;
  --font-body:'Inter',-apple-system,'Segoe UI',sans-serif;
  --font-mono:'JetBrains Mono',ui-monospace,monospace;
  --r-ctl:10px; --r-card:14px; --r-pill:999px;
}
```
