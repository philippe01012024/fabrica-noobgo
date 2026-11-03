# Fábrica noobgo

Painel do canal **noobgo**: radar de outliers dos concorrentes de CS2, descoberta de canais parecidos, fila de pautas e agenda de shorts.

Tudo roda no seu navegador, com a API oficial e gratuita do YouTube. Não há servidor nem mensalidade.

## Como funciona

- **Radar de outliers:** lê os últimos 50 vídeos de cada canal e calcula quantas vezes cada um superou a mediana do próprio canal, separando vídeos longos de Shorts.
- **Ordenar:** clique em Multiplicador, Views ou Data. Clicar de novo inverte (mais novo ↔ mais antigo).
- **Descobrir canais:** busca por tema no YouTube, ou lista os canais que seus concorrentes indicam na página deles.
- **Aprovação:** aprove pautas e copie um prompt pronto para o Claude escrever títulos e descrição.

## Custo

Zero. A API do YouTube dá 10.000 unidades por dia por projeto. Uma atualização completa com 11 canais usa cerca de 33 unidades, e as buscas de canais têm uma cota separada de 100 por dia.

## Configurar a chave (uma vez, 5 minutos)

1. Abra o [Google Cloud Console](https://console.cloud.google.com/projectcreate) e crie um projeto (ex.: `fabrica-noobgo`).
2. Ative a [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com).
3. Em [Credenciais](https://console.cloud.google.com/apis/credentials), clique em **Criar credenciais → Chave de API**.
4. Edite a chave:
   - **Restrições de aplicativo → Sites:** adicione `https://SEU-USUARIO.github.io/*`
   - **Restrições de API:** escolha só **YouTube Data API v3**
5. Abra o painel, vá em **Configuração**, cole a chave e clique em **Salvar e testar**.

A chave fica guardada só no navegador onde você colou. Ela **não** vai para este repositório. Nunca cole a chave em nenhum arquivo daqui.

## Publicar no GitHub Pages

1. No repositório, abra **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)` e salve.
3. Em um ou dois minutos o painel fica em `https://SEU-USUARIO.github.io/fabrica-noobgo/`.

## Arquivos

- `index.html`: o painel inteiro (HTML, CSS e JavaScript num só arquivo).
