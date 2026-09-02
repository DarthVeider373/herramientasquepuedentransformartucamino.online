# Clone — Página de vídeo (VSL)

Página original: `https://contenidosquepuedentransformatucamino.site/reveIaciondeIcontenidodeIaconciencia/`

## Estrutura

```
pagina-conciencia-clone/
├── index.html      → estrutura da página (título, vídeo, rodapé)
├── css/
│   └── style.css   → todos os estilos, organizados por seção
└── README.md
```

## O que foi replicado

- Título principal (H1) com trecho destacado em amarelo, fonte Poppins.
- Seção de vídeo (VSL) usando o mesmo player embutido (Vturb/Converteai) do
  site original — o script já está referenciado no `index.html`.
- Rodapé com links de "Políticas de Privacidad" / "Términos de Uso" e aviso
  legal, fundo azul-marinho, fonte Roboto.

## Observação sobre a imagem de fundo

A imagem de fundo original (`.../1f78c735-...-style-container-backgro.jpeg`,
hospedada no CDN `media.atomicatmedia.net`) estava retornando um erro do
servidor de origem (o CDN devolvia HTML no lugar do JPEG). Por isso, no clone
ela foi substituída por um gradiente em CSS (`.hero` em `style.css`) com tons
próximos aos da paleta original. Se você tiver a imagem correta, basta:

1. Salvá-la em `assets/images/bg-hero.jpg`
2. Trocar, em `css/style.css`, a propriedade `background` da classe `.hero`
   por `background: url("../assets/images/bg-hero.jpg") center/cover no-repeat;`

## Como usar

Basta abrir `index.html` em qualquer navegador. Não há dependência de build,
é HTML/CSS puro (com um único `<script>` externo para carregar o player de
vídeo, igual ao site original).
