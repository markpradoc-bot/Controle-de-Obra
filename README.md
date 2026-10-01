# Controle de Obra

Acompanhamento de obra: avanço físico, cronograma Gantt semanal editável,
orçamento, contratos, pagamentos, recebimentos por medição, solicitações de
material, cotações, equipes, pendências, diário com fotos e relatórios.

Roda inteiro no navegador. Não precisa de servidor nem instalação.

---

## O que vai no repositório

```
index.html    a página
app.js        o sistema
dados.json    a base oficial da obra
.nojekyll     impede o GitHub de processar os arquivos
README.md     este arquivo
```

Os cinco arquivos ficam na raiz, lado a lado. Não mude os nomes: o
`index.html` procura o `app.js` e o `dados.json` pelo nome.

---

## Publicando

1. Crie um repositório novo no GitHub.
2. Suba os arquivos na raiz (**Add file › Upload files**, pode arrastar).
3. **Settings › Pages**.
4. Em **Source**, escolha **Deploy from a branch**; em **Branch**, `main` e a
   pasta `/ (root)`. Salve.
5. Em um ou dois minutos o endereço aparece no topo dessa mesma tela, no
   formato `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

Esse é o link que você manda para a equipe.

---

## Colocando os dados da sua obra

O `dados.json` que veio aqui está vazio. Para publicar a obra que você já tem
lançada:

1. Abra o sistema que você usa hoje.
2. **Configurações › Exportar backup (.json)**.
3. Renomeie o arquivo baixado para `dados.json`.
4. Suba no repositório, substituindo o que está lá.

Quem abrir o link passa a ver a obra já carregada.

---

## Atualizando a obra depois

O ciclo da semana:

1. Você lança avanço, pagamentos, medições e pendências no seu navegador.
2. **Configurações › Exportar backup (.json)**.
3. Renomeia para `dados.json` e substitui no GitHub.

Na próxima vez que alguém abrir o link, aparece uma faixa na parte de baixo
da tela avisando que há uma versão mais recente, com duas opções:

- **Carregar a versão publicada** — troca o que está no navegador da pessoa
  pela base oficial que você acabou de subir.
- **Manter os meus dados** — ignora e continua com o que ela tem.

---

## Como os dados funcionam — leia antes de distribuir o link

O GitHub Pages hospeda arquivos, não roda banco de dados. Por isso:

- **Cada pessoa tem a própria cópia.** O que ela digitar fica no navegador
  dela, no computador dela.
- **As alterações não se juntam sozinhas.** Se duas pessoas editarem ao mesmo
  tempo, cada uma vê só a própria versão.
- **O `dados.json` é a fonte oficial.** Vale o que está publicado nele.

O arranjo que funciona: uma pessoa lança os dados e publica; as outras abrem
para consultar e, quando quiserem, carregam a base nova.

Para várias pessoas lançando na mesma base ao mesmo tempo, o GitHub Pages não
resolve — isso exige servidor.

---

## Fotos do diário

As fotos ficam guardadas **só no navegador onde foram anexadas**. Elas não
entram no `dados.json` e não vão junto na publicação: quem abrir o link verá
os textos do diário, mas não as imagens.

É uma limitação de tamanho — um `dados.json` com dezenas de fotos ficaria
pesado demais para carregar a cada visita. Se precisar circular as fotos,
guarde-as também numa pasta compartilhada à parte.

---

## Cuidados

- Não troque o repositório de nome nem de endereço depois de começar. O
  navegador guarda os dados por endereço; mudando o endereço, a pessoa perde
  o que tinha lançado localmente.
- Faça o backup em **Configurações › Exportar backup (.json)** de tempos em
  tempos. Limpar os dados de navegação do navegador apaga o que não foi
  publicado.
- Repositório público é público: qualquer pessoa com o link vê orçamento,
  contratos, pagamentos e recebimentos que estiverem no `dados.json`.
  Repositório privado restringe o acesso, mas o GitHub Pages exige plano pago
  para publicar a partir de um repositório privado.
