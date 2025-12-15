# Clima Hoje

Projeto desenvolvido para estudo do FullStack Club Code Start.

## Visão Geral

- Aplicação estática feita com `HTML` e `CSS` que apresenta um painel de clima.
- Não há JavaScript nem integração com APIs de meteorologia: os dados exibidos são exemplos fixos.
- Estrutura simples e ideal para iniciantes entenderem HTML semântico, layout com Flexbox e organização de estilos.

## Tecnologias

- `HTML5` para marcação.
- `CSS3` para estilos e layout.
- Fonte `Poppins` via Google Fonts.

## Pré-requisitos

- Qualquer navegador moderno (Chrome, Edge, Firefox, Safari).

## Como Executar

- Abra o arquivo `index.html` diretamente no navegador (duplo clique ou botão direito → Abrir com).

## Estrutura de Pastas

```
ClimaHoje/
├─ images/                 # Ícones e imagens usadas na interface
│  ├─ logo.png
│  ├─ search-icon.svg
│  ├─ sun.svg
│  ├─ sun-cloud.svg
│  ├─ sun-clouds.svg
│  ├─ sun-clouds-icon.svg
│  ├─ clouds.svg
│  ├─ moon-clouds.svg
│  ├─ Vector.svg
│  ├─ Vector (1).svg
│  ├─ icon.svg
│  └─ icon (1).svg
├─ index.html              # Estrutura do conteúdo
├─ styles.css              # Estilos globais
└─ .gitattributes         # Normalização de EOL no Git
```

## HTML (Guia para iniciantes)

- Cabeçalho e estilos: `index.html:4` inclui `styles.css`.
- Container principal: `index.html:7` agrupa a interface central.
- Header com logo e busca:
  - Logo: `index.html:9` (`<img class="logo" ... />`).
  - Área de busca: `index.html:10` contém ícone (`index.html:11`) e campo de texto (`index.html:12`).
- Seção superior do clima atual: `index.html:20`
  - Cidade: `index.html:22`
  - Chance de chuva: `index.html:23`
  - Temperatura principal: `index.html:24`
  - Ícone de clima: `index.html:26`
- Seção do período do dia (cards horários): `index.html:32`
  - Cada bloco horário usa `.mid-item` (ex.: `index.html:33` para 6:00 AM).
- Métricas rápidas (sensação, chuva, vento, UV): `index.html:64`
  - Sensação térmica: `index.html:66–70`
  - Chance de chuva: `index.html:72–77`
  - Vento (km/h): `index.html:79–86`
  - Índice UV: `index.html:88–94`
- Previsão semanal (barra lateral): `index.html:98`
  - Cada dia usa `.left-item` com ícone e máximas/mínimas (ex.: `index.html:99` para Segunda).

## CSS (Guia para iniciantes)

- Import da fonte Poppins: `styles.css:1`.
- Reset básico e box model: `styles.css:3–8`.
- Layout do `body` com Flexbox: `styles.css:10–16`.
- Container principal `.main-div-container`: `styles.css:18–22`.
- Estilos do `header`: `styles.css:24–28` e `styles.css:30–37` (duas regras para o mesmo seletor).
- Estilos do `input`: `styles.css:39–42`.
- Conteúdo principal `.main-container`: `styles.css:44–51`.
- Atenção ao seletor do logo: `styles.css:53–56` usa `.logo img`, mas no HTML o `img` possui a classe `logo` diretamente. Trocar para `.logo` se quiser aplicar largura/altura ao próprio elemento.
- Área de busca `.search-container`: `styles.css:58–66`.
- Ícone de busca `.search-icon`: `styles.css:68–72`.
- Campo de busca `.search-input`: `styles.css:74–78`.
- Seção superior `#section-top`: `styles.css:80–86`.
- Textos principais:
  - `.temperature`: `styles.css:88–90`
  - `.city`: `styles.css:92–94`
  - `.chance-of-rain`: `styles.css:96–99`
- Faixa de horários `#section-mid` com gradiente e sombra: `styles.css:101–109`.
- Cartões horários `.mid-item` e textos `.mid-hours-text`: `styles.css:111–122`.
- Tamanhos específicos dos ícones: `styles.css:124–152`.
- Container das métricas `.section-buttom`: `styles.css:154–158`.
- Card de métrica `.buttom-item`: `styles.css:160–170`.
- Linha de temperatura/ícone `.temperature-bottom`: `styles.css:172–176`.
- Valores e unidades:
  - `.buttom-item-condicion`: `styles.css:178–180`
  - `.buttom-item-span`: `styles.css:182–184`
- Barra lateral `#left-content`: `styles.css:186–195`.
- Itens da lateral `.left-item`: `styles.css:197–202`.
- Texto e destaque de graus `.left-item-graus`: `styles.css:204–208`.
- Texto auxiliar `.left-item-text`, `.left-item-texts`, `.left-items`: `styles.css:210–218`.

## Imagens e Ícones

- Todos os arquivos estão em `images/`. Substitua por seus próprios ícones se desejar.
- Exemplos usados no HTML: `sun.svg`, `sun-cloud.svg`, `clouds.svg`, `moon-clouds.svg`, etc.

## Personalização

- Mudar cidade/temperaturas: edite os textos em `index.html` (`.city`, `.temperature`, cards e lateral).
- Alterar cores: substitua valores em `styles.css` (ex.: gradiente em `styles.css:105` e `box-shadow` em `styles.css:108`).
- Ajustar fontes: troque o import em `styles.css:1` ou modifique `font-family` em `styles.css:6`.
- Corrigir seletor do logo: altere `.logo img` para `.logo` em `styles.css` se quiser estilizar o `img` diretamente.

## Observações

- Este projeto é apenas para fins educativos. Em produção, você pode incluir JavaScript para buscar dados reais de uma API (ex.: OpenWeatherMap) e validar entradas do campo de busca.
- Há um pequeno desacordo de seletor no logo (ver nota em CSS acima), comum em projetos iniciais — ótimo ponto para prática.

## Créditos

- Projeto desenvolvido para estudo do FullStack Club Code Start.
