# devopsclt-privacypolicy

Documentos legais dos aplicativos móveis da **China Link do Brasil Consultoria Internacional Ltda**,
publicados por GitHub Pages em <https://clt-devops.github.io/devopsclt-privacypolicy/>.

As lojas exigem uma URL pública de política de privacidade para cada app. Este repositório é essa
URL: estático, versionado, sem CMS no caminho, e o `git log` responde "o que foi publicado, quando".

---

## Estrutura

```text
index.html                        # índice público — aponta para tudo
comum/
  termos-de-uso-apps.html         # UMA url, todos os apps apontam para ela
  _template-privacidade.md        # molde para criar a política de um app novo
app-<slug>-<ano>/
  privacidade.html                # a url que vai na ficha da loja
```

## A regra que organiza isto

**Termos de uso são comuns. Política de privacidade é por app.**

Não é preferência de organização — é requisito de loja. O Google Play exige política *relevante ao
app*; a Apple, na diretriz 5.1.1, exige que ela *identifique os dados que aquele app coleta*. Uma
política genérica, que não nomeia o app nem lista suas permissões, é motivo de rejeição — e deixa o
formulário de Data safety / App Privacy indefensável, porque a loja compara a declaração com o
comportamento observado do app.

O exemplo concreto: o app de guia de viagem não coleta nada; o ChinaLink Fair coleta câmera,
microfone e dado de contato de terceiro. Uma política servindo aos dois seria falsa para um.

O que **é** reaproveitável é o molde: controlador, direitos do titular, DPO, segurança, foro. É por
isso que existe `comum/_template-privacidade.md` — o trabalho repetido vira preenchimento, não
redação.

## Cada política é auto-contida

A política de um app não linka para o comum buscando o conteúdo dela: ela contém tudo o que precisa
ser lido. Revisor de loja que não clica em link, ou link que quebra numa reorganização de pastas, vê
política incompleta. HTML estático é barato; duplicar seis parágrafos invariantes custa menos que uma
rejeição.

## Publicar a política de um app novo

1. `cp -r` a pasta de um app existente para `app-<slug>-<ano>/`, ou preencha
   `comum/_template-privacidade.md`.
2. Substitua as seções específicas: o que o app faz, que dados trata, permissões, finalidades e base
   legal, compartilhamento, transferência internacional, retenção.
3. Atualize a data no topo.
4. Acrescente a entrada em `index.html`.
5. Merge na `main` — o Pages publica em segundos.
6. Cole a URL na ficha do Google Play e do App Store Connect.

**Antes de informar a URL à loja**, abra-a numa aba anônima: tem de carregar o documento direto, sem
login e sem redirecionar para outra página.

## Regra de manutenção

A política descreve o comportamento do app. Quando o app passa a coletar algo novo — uma permissão,
um campo, um destino de dado —, a política muda **no mesmo ciclo**, e os formulários das duas lojas
são revisados junto. Declaração desatualizada é o risco real: a loja compara o que você declarou com
o que o app faz.

Para o ChinaLink Fair, a fonte factual dessa manutenção mora no repositório do app:
`docs/privacidade-inventario-de-dados.md` (o que se coleta, de quem, para onde vai) e
`docs/privacidade-politica.md` (o texto em markdown, versionado ao lado do código).

## Contato

Encarregado de Proteção de Dados (DPO): Leonardo Odinez Santos Borin —
<privacidade@chinalinktrading.com>
