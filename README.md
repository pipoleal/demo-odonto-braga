# Demo — Odonto Braga (versão 2)

Site demo **bilíngue (PT | EN)** da **Odonto Braga** (Boiçucanga, São Sebastião – SP). HTML, CSS e JS puro, sem build.

## Direção visual

- **Cor da marca** `#0E3C5C` (marinho) como base, sobre branco-porcelana frio; acento quente **damasco** `#E8A98A` (cobre `#9A4E2E` para texto sobre fundo claro, contraste AA). Sem dourado nem creme — distante da Gomes Odontologia.
- **Tipografia**: Bodoni Moda (títulos, alto contraste, clima boutique) + Hanken Grotesk (texto). Hospedadas em `fonts/`.
- **Composição editorial**: seções numeradas (N° 01…12), fotos grandes com revelação em cortina, faixa corrida de tratamentos, lista de tratamentos com prévia de foto ao passar o mouse (desktop), linha da jornada que se desenha com a rolagem.

## Como editar

- **Dados** (WhatsApp, endereço, horário, nota, equipe, tratamentos, feriados): objeto `CONFIG` no início do `<script>`.
- **Retratos da equipe**: coloque as fotos em `img/` e preencha `foto` em `CONFIG.equipe` (ex: `"img/dra-erica.webp"`, formato 4:5). Sem foto, o card mostra o primeiro nome em tipografia + "Retrato oficial em breve" — **não** usamos foto de banco no lugar de profissionais reais.
- **Textos em inglês**: objeto `EN` (interface) e `T.en` (mensagens, erros, datas). O português fica no próprio HTML.
- **Imagem de prévia** (`img/og.jpg`): gerada com a marca (painel marinho + foto). Tags OG e JSON-LD `Dentist` ficam fixos no `<head>`.

## Funcionalidades

- PT | EN instantâneo (sem recarregar), inclusive mensagens do WhatsApp, datas, mapa e status de horário. `?lang=en` abre em inglês; lembra a escolha.
- Agendamento: tratamento (chips), 5 próximos dias úteis em botões + "outra data", período, nome, primeira consulta, prévia. Bloqueia passado, fins de semana e feriados (fixos + Carnaval, Sexta-feira Santa e Corpus Christi pela Páscoa, e 20/01). Botões "Agendar…" nas seções já escolhem o tratamento.
- "Aberto agora / Fechado" pelo horário de Brasília, com o dia de hoje destacado na tabela.
- Urgência com mensagem pronta no idioma escolhido + ligação para o fixo.

## Regras do CFO/CRO — checklist

- [x] Sem antes e depois; nenhuma foto mostra resultado de tratamento.
- [x] Sem preços, promoções ou condições de pagamento.
- [x] Sem promessa de resultado (prazos "estimados", indicação "após avaliação clínica").
- [x] Responsável técnico com CRO no rodapé e CRO de cada profissional.
- [ ] **Confirmar**: responsável técnica = Dra. Erica Braga (assumido por ser a fundadora).
- [ ] **Confirmar**: "áreas de atuação" foram escritas sem a palavra "especialista". Se tiverem título de especialista registrado no CRO, dá para dizer "Especialista em Ortodontia".
- [ ] **Confirmar**: se a clínica é provedora Invisalign certificada (o nome da marca aparece no site; há a nota de marca registrada da Align Technology).
- [ ] **Depoimentos**: são **de exemplo**, inspirados no que os pacientes elogiam. Confirmar com o responsável técnico se o uso está de acordo com as normas vigentes do CFO; alternativa segura: manter só a nota 5,0 e o link para o Google.

## O que é de exemplo

- Depoimentos (nomes fictícios), textos de bio da equipe, divisão manhã 9h–12h / tarde 13h–17h.
- Fotos de banco (não são da clínica nem da equipe).

## Fotos — créditos

Todas do [Unsplash](https://unsplash.com/license) (licença Unsplash: uso livre, comercial inclusive; créditos por boa prática). `hero-v` é o recorte vertical do hero para celular. `og.jpg` foi montada a partir de `hero.webp`.

| Arquivo | Autor | Link |
|---|---|---|
| `hero.webp` | [Phước Sang](https://unsplash.com/pt-br/@phuocsangvn) | [Unsplash](https://unsplash.com/pt-br/fotografias/jovem-sorrindo-enquanto-apoia-o-queixo-na-mao-jBqMJdzTcgA) |
| `sala.webp` | [Amy Vosters](https://unsplash.com/pt-br/@amyvosters) | [Unsplash](https://unsplash.com/pt-br/fotografias/sala-de-espera-moderna-com-cadeiras-e-letreiro-inspirador-pxOQ-P97sA8) |
| `consulta.webp` | [Harold Hisona](https://unsplash.com/pt-br/@harold_angus) | [Unsplash](https://unsplash.com/pt-br/fotografias/dentista-conversando-com-o-paciente-em-um-consultorio-odontologico-moderno-Bg81yWKZlMg) |
| `crianca.webp` | [Ortopediatri Çocuk Ortopedi Akademisi](https://unsplash.com/pt-br/@ortopediatri) | [Unsplash](https://unsplash.com/pt-br/fotografias/um-homem-sentado-em-um-banco-ao-lado-de-um-menino-ogfwXs_la2g) |
| `crianca-sorriso.webp` | [Amanda Sofia Pellenz](https://unsplash.com/pt-br/@amanda_sofia_) | [Unsplash](https://unsplash.com/pt-br/fotografias/menino-em-azul-branco-e-vermelho-xadrez-botao-ate-camisa-sorrindo-YuidWzM37C0) |
| `protese.webp` | [Peter Kasprzyk](https://unsplash.com/pt-br/@petekasprzyk) | [Unsplash](https://unsplash.com/pt-br/fotografias/pessoa-usando-anel-prateado-enquanto-segura-a-protese-U1gvhqVQ2kQ) |
| `litoral.webp` | [Wallace Fonseca](https://unsplash.com/pt-br/@waally) | [Unsplash](https://unsplash.com/pt-br/fotografias/uma-praia-com-uma-colina-e-arvores-kPTerEU1Vsw) |
| `consultorio.webp` | [Kari Bjorn Photography](https://unsplash.com/pt-br/@karibjorn) | [Unsplash](https://unsplash.com/pt-br/fotografias/uma-sala-odontologica-com-mesa-e-cadeiras-Fdku_oMrDvk) |
| `alinhador-maos.webp` | [Katarzyna Zygnerska](https://unsplash.com/pt-br/@katasha) | [Unsplash](https://unsplash.com/pt-br/fotografias/uma-pessoa-de-luvas-azuis-segurando-uma-escova-de-dentes-Mv7xZmOgrQk) |

## Publicar (repositório privado)

```bash
gh repo create demo-odonto-braga --private --source=. --remote=origin --push
vercel deploy --prod --yes --project demo-odonto-braga
```
