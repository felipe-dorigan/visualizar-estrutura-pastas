# Visualizador de Estrutura de Pastas

Este projeto é uma página simples que permite visualizar a estrutura de pastas e arquivos de um projeto.

## Como usar

1. Abra o arquivo `index.html` no Google Chrome ou Microsoft Edge.
2. Clique em **Selecionar Diretório**.
3. Escolha a pasta que deseja visualizar.
4. A estrutura será exibida na tela e também em formato de texto.

## Funcionalidades

- Mostra as pastas e os arquivos em formato de árvore.
- Exibe a quantidade total de pastas e arquivos encontrados.
- Mostra quantos arquivos existem dentro de cada pasta.
- Permite expandir ou recolher uma pasta ao clicar em seu nome.
- Possui botões para expandir ou recolher todas as pastas.
- Permite buscar uma pasta ou arquivo pelo nome.
- Permite copiar toda a estrutura como texto.
- Pode ocultar as extensões dos arquivos.
- Ignora pastas e arquivos informados no campo **Ignorar pastas/arquivos**.

## Como funciona

Todo o projeto está no arquivo `index.html`, dividido em três partes:

- **HTML:** cria os botões, campos, painéis e textos da página.
- **CSS:** define as cores, espaçamentos e a organização visual.
- **JavaScript:** seleciona e lê a pasta, cria a árvore e controla as funcionalidades.

Ao selecionar um diretório, o JavaScript usa a API `showDirectoryPicker()` do navegador. A função `lerDiretorio()` percorre todas as subpastas e monta um objeto com os nomes e tipos dos itens encontrados.

Depois da leitura:

- `gerarVisual()` cria a árvore interativa exibida no painel esquerdo.
- `gerarTexto()` cria a versão em texto exibida no painel direito.
- `aplicarBusca()` destaca os nomes que correspondem a busca.
- `copiarEstrutura()` envia o texto gerado para a área de transferência.

## Observação

A seleção de diretórios depende de uma API que funciona principalmente no Google Chrome e no Microsoft Edge. Outros navegadores podem não oferecer suporte.
