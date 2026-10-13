# O Segredo das Indianas — Página de vendas

Página de vendas estática (HTML + CSS + JS) para o e-book **O Segredo das Indianas** (99 MT).

## Estrutura do projecto

```
index.html
assets/
  antes-depois-1.jpg
  antes-depois-2.jpg
  antes-depois-3.jpg
README.md
```

## O que a página faz

1. Apresenta a oferta: nome, descrição, preço (99 MT), botão "QUERO TER ACESSO AO SEGREDO".
2. Mostra 3 imagens antes/depois (ficheiros locais em `assets/`).
3. Apresenta o conteúdo do e-book (3 cartões).
4. Secção de depoimentos (placeholders para substituir).
5. Questionário de 4 perguntas, uma de cada vez, com barra de progresso e avanço automático.
6. Animação de análise (2-3 segundos).
7. Resultado final com botão para o WhatsApp (+258 83 536 7771), com as respostas incluídas na mensagem.

## Como publicar no GitHub Pages

### 1. Criar o repositório

1. Abre [github.com](https://github.com) e faz login.
2. Clica em **New repository**.
3. Nome sugerido: `segredo-das-indianas`.
4. Marca **Public**.
5. Clica **Create repository**.

### 2. Carregar o index.html

1. No repositório vazio, clica em **Add file** → **Upload files** (ou **Create new file**).
2. Se for Create new file, escreve `index.html` no nome e cola o conteúdo.
3. Clica **Commit changes**.

### 3. Criar a pasta assets

1. Clica em **Add file** → **Create new file**.
2. No nome escreve `assets/placeholder.txt` (para forçar a criação da pasta).
3. Conteúdo: uma linha qualquer.
4. **Commit changes**.

### 4. Carregar as 3 imagens

1. Clica na pasta `assets`.
2. **Add file** → **Upload files**.
3. Envia:
   - `antes-depois-1.jpg`
   - `antes-depois-2.jpg`
   - `antes-depois-3.jpg`
4. **Commit changes**.
5. Podes apagar o `placeholder.txt` depois.

Se as imagens não estiverem disponíveis, a página mostra automaticamente um placeholder discreto a indicar o nome do ficheiro em falta. Nada quebra.

### 5. Activar o GitHub Pages

1. No repositório, clica em **Settings**.
2. Menu lateral → **Pages**.
3. **Source:** `Deploy from a branch`.
4. **Branch:** `main` e pasta `/ (root)`.
5. Clica **Save**.
6. Espera 1-2 minutos.

### 6. Obter o link público

Aparece no topo da página de Pages:

```
https://SEU-USUARIO.github.io/segredo-das-indianas/
```

Abre esse link no telemóvel para testar.

## Como testar o questionário

1. Abre a página.
2. Clica no botão dourado.
3. Responde às 4 perguntas.
4. A animação de análise aparece.
5. O resultado aparece com o botão verde do WhatsApp.
6. Ao clicar, abre o WhatsApp com a mensagem já preenchida (incluindo as respostas).

## Como substituir os depoimentos

No `index.html`, procura:

```
[Adicionar depoimento real de cliente]
[Nome ou iniciais]
```

Substitui os 3 blocos pelos depoimentos verdadeiros. Se não tiveres depoimentos reais, podes apagar a secção inteira (`<section class="bloco depoimentos">...</section>`).

**Nunca inventes depoimentos.**

## Como substituir a capa

Actualmente a capa é feita em HTML/CSS (o bloco `.capa-ebook`). Se quiseres usar uma imagem real:

1. Coloca `assets/capa-ebook.jpg`.
2. No `index.html`, substitui o bloco `<div class="capa-ebook">...</div>` por:

```html
<div class="capa-ebook" style="padding:0;overflow:hidden;">
  <img src="assets/capa-ebook.jpg" alt="Capa do e-book" style="width:100%;height:100%;object-fit:cover;border-radius:16px;" />
</div>
```

## Avisos importantes

- Este material é informativo e não substitui aconselhamento médico ou nutricional profissional.
- Cada percurso é individual. As imagens não garantem que outras pessoas obtenham os mesmos resultados.
- Não há garantia de perda de peso específica.
- O WhatsApp é usado apenas para o cliente falar com o vendedor e receber instruções de pagamento. Não há pagamento automático.
