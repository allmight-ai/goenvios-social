# goenvios-social

Hospedagem pública das imagens dos posts do **GO!Envios**.

Existe por um motivo só: a API do Instagram **não aceita arquivo local** — ela
recebe uma URL e baixa a imagem. Repositório privado não serve, porque o
servidor do Instagram não tem token e recebe 404.

**A URL só precisa estar viva durante a publicação.** O Instagram guarda a
própria cópia ao criar o post, então depois de publicado dá pra apagar a pasta
sem afetar nada que já esteja no ar.

Nada de código nem de dado aqui — só imagem que vai virar post público de
qualquer forma.

```
posts/<ano-mes>-<nome>/slide-NN.jpg
```

Geradas por `growth/cards`, no repositório principal (privado):

```
npm run generate -- out/origem --deck=origem --theme=light --accent=cobalt
node scripts/to-upload.mjs out/origem
```
