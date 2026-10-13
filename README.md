# O Segredo das Indianas — Página de vendas

Página de vendas estática (HTML + CSS + JS) para o e-book **O Segredo das Indianas** (99 MT).

## Estrutura do projecto

```
index.html
vercel.json
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

## Como publicar na Vercel

### 1. Criar o repositório no GitHub

1. Abre [github.com](https://github.com) e faz login.
2. Clica em **New repository**.
3. Nome sugerido: `segredo-das-indianas`.
4. Marca **Public**.
5. Clica **Create repository**.

O Ghost IA aplica os ficheiros neste repositório.

### 2. Carregar as 3 imagens no repositório

1. No repositório GitHub, clica em **Add file** → **Create new file**.
2. Nome: `assets/placeholder.txt` (isto cria a pasta `assets/`).
3. Conteúdo: uma linha qualquer.
4. **Commit changes**.
5. Entra na pasta `assets`.
6. **Add file** → **Upload files**.
7. Envia:
   - `antes-depois-1.jpg`
   - `antes-depois-2.jpg`
   - `antes-depois-3.jpg`
8. **Commit changes**.
9. Apaga o `placeholder.txt` (opcional).

### 3. Importar o projecto na Vercel

1. Abre [vercel.com/dashboard](https://vercel.com/dashboard).
2. Clica **Add New** → **Project**.
3. Escolhe **Import Git Repository**.
4. Autoriza o GitHub se pedir.
4. Seleciona o repositório `segredo-das-indianas`.
5. Nas configurações do projecto:
   - **Framework Preset:** deixa em **Other** (é HTML/CSS/JS puro, não é React/Vite).
   - **Build Command:** vazio.
   - **Output Directory:** vazio.
   - **Install Command:** vazio.
6. Clica **Deploy**.
7. Espera 30 segundos.

A Vercel dá-te automaticamente um URL tipo:

```
https://segredo-das-indianas.vercel.app
```

### 4. Ligar o domínio próprio

1. Na Vercel, entra no projecto.
2. **Settings** → **Domains**.
3. Escreve o teu domínio (ex: `osegredodasindianas.com`) e clica **Add**.
4. A Vercel mostra-te **2 registos DNS** (A e CNAME) que tens de adicionar no teu fornecedor de domínio (Namecheap, GoDaddy, Cloudflare, etc.).
5. Vai ao painel do teu fornecedor de domínio e adiciona esses registos.
6. Espera 5-30 minutos até a Vercel mostrar o domínio como **Valid Configuration**.

Se não tiveres domínio, o URL `.vercel.app` funciona perfeitamente para começar.

### 5. Redeploy automático

Cada vez que o Ghost IA aplica um patch no GitHub, a Vercel detecta a alteração e faz deploy automático em 30-60 segundos. Não precisas de fazer nada.

## Como testar o questionário

1. Abre o site (URL Vercel ou domínio próprio).
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

1. Coloca `assets/capa-ebook.jpg` no repositório.
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
