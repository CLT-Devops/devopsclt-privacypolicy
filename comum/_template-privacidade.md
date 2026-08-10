# Template — Política de Privacidade de aplicativo ChinaLink

> Molde para criar a política de um app novo. **Não é publicado** (o `_` no nome marca isso).
>
> Como usar: copie a estrutura para `app-<slug>-<ano>/privacidade.html`, reaproveite os blocos
> marcados **[FIXO]** como estão, e reescreva os marcados **[POR APP]** com o que aquele app faz de
> verdade.
>
> A regra por trás da marcação: as lojas comparam a declaração com o comportamento observado do app.
> Bloco **[FIXO]** é o que não varia entre apps da mesma empresa; bloco **[POR APP]** é exatamente o
> que a loja verifica. Copiar um **[POR APP]** de outro app é como a declaração fica falsa.
>
> Antes de escrever, levante o que o app realmente coleta — no ChinaLink Fair isso virou um documento
> próprio no repositório do app (`docs/privacidade-inventario-de-dados.md`), e é ele que alimenta a
> política, o Data safety do Play, o App Privacy da Apple e o `PrivacyInfo.xcprivacy` do iOS. Quatro
> formulários, um levantamento.

---

## Cabeçalho

- Título: `Política de Privacidade — <Nome do App>`
- `Última atualização: <data>`
- Nota de topo ligando aos [Termos de Uso comuns](termos-de-uso-apps.html) e à política institucional.

## 1. Quem somos — **[FIXO]**

China Link do Brasil Consultoria Internacional Ltda, CNPJ 23.239.704/0001-17, Rua Alexandre
Herculano, 197, Conjunto 501, Gonzaga, Santos - SP, CEP 11050-031. Controladora para fins da LGPD.

## 2. O que o aplicativo faz — **[POR APP]**

Dois ou três parágrafos em linguagem de usuário. Diga também **quem pode usar** (aberto ao público?
só cliente com convite?) — a loja usa isso para entender por que há login.

## 3. Quais dados tratamos — **[POR APP]**

Subdivida por **sujeito de dado**, não por tela. Quem são os titulares?

- **3.1 Dados de quem usa o aplicativo** — identificação, credencial, dados de contexto.
- **3.2 Dados de terceiros**, se houver. Se o app permite registrar informação de alguém que não é
  usuário, isto **tem de estar escrito**. É o ponto que mais frequentemente falta e o de maior risco.
- **3.3 Dados técnicos** — identificadores de instalação, diagnóstico, dados de uso.
- **3.4 O que não coletamos** — vale listar. Sustenta os "não" dos formulários e é o que permite
  afirmar ausência de rastreamento publicitário.

## 4. Permissões do dispositivo — **[POR APP]**

Tabela: permissão · para quê · o que acontece se recusar.

Liste **só o que o app declara de fato** no `AndroidManifest.xml` e no `Info.plist`. Permissão
declarada e não listada é subdeclaração; listada e não declarada é pior — promete um recurso que o app
não consegue executar.

## 5. Finalidades e base legal — **[POR APP]**

Tabela: finalidade · base legal da LGPD (art. 7º). Execução de contrato para o que é o serviço em si;
legítimo interesse para o que é acessório e esperado; obrigação legal para retenção fiscal e afins.

Se houver tratamento de dado de terceiro, justifique-o em parágrafo próprio: contexto, natureza
profissional do dado, finalidade e limite de uso.

## 6. Como os dados são guardados — **[POR APP]**

Onde o dado vive (device, servidor, storage), se funciona offline, e que medidas de segurança existem.
Descreva medidas que existem — não copie uma lista genérica de controles.

## 7. Com quem compartilhamos — **[POR APP]**

Comece por "não vendemos dados pessoais e não os cedemos para fins publicitários", se verdadeiro.
Depois liste os destinos reais: outros usuários com papel definido, sistemas internos, prestadores de
serviço por categoria, autoridades quando exigido por lei.

## 8. Transferência internacional — **[POR APP]**

Só se houver. Diga quais países e por quê. Para app usado na China com empresa no Brasil, isso é
obrigatório e envolve também a legislação chinesa.

## 9. Retenção — **[POR APP]**

Por quanto tempo, e o critério. Se algum dado tem ciclo próprio (por exemplo, imagem original
descartada após processamento), diga.

## 10. Direitos do titular — **[FIXO]**

Os direitos do art. 18 da LGPD: confirmação e acesso, correção, anonimização/bloqueio/eliminação,
portabilidade, informação sobre compartilhamento, oposição a legítimo interesse, revogação de
consentimento.

## 11. Contato e DPO — **[FIXO]**

Encarregado de Proteção de Dados: Leonardo Odinez Santos Borin —
privacidade@chinalinktrading.com

Use **este** canal, não um e-mail de equipe técnica: a LGPD espera o encarregado identificado, e
divergir do endereço publicado na política institucional cria contradição entre dois documentos da
mesma empresa.

## 12. Menores de idade — **[FIXO]**

Os apps da ChinaLink são de uso profissional, destinados a maiores de 18 anos. Manter coerente com o
item 1 dos Termos de Uso comuns.

## 13. Alterações — **[FIXO]**

Como as mudanças são comunicadas, e que a data no topo é a referência.

---

## Antes de publicar

- [ ] Nenhum placeholder `[...]` sobrou no arquivo — texto legal público com marcação de modelo à
      vista é a falha mais fácil de evitar e a mais visível
- [ ] O nome do app aparece no título e no corpo
- [ ] Permissões conferidas contra `AndroidManifest.xml` e `Info.plist`
- [ ] Data de atualização é a de hoje
- [ ] Entrada acrescentada em `index.html`
- [ ] URL aberta em aba anônima: carrega direto, sem login, sem redirect
- [ ] Data safety (Play) e App Privacy (Apple) preenchidos com o **mesmo** conteúdo
