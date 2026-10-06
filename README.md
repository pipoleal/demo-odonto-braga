# Demo — Odonto Braga

Site demo da **Odonto Braga** (Boiçucanga, São Sebastião – SP). HTML, CSS e JS puro, sem build.

## Como editar

- **Dados** (WhatsApp, endereço, horário, nota, equipe, tratamentos, feriados, responsável técnico): objeto `CONFIG` no início do `<script>`.
- **Fotos da equipe**: coloque o arquivo em `img/` e preencha `foto` em `CONFIG.equipe` (ex: `"img/dra-erica.webp"`). Sem foto, o card mostra as iniciais e "Foto em breve".
- **Cores**: `:root` do CSS (`--eucalipto`, `--salvia`, `--sol`, `--tinta`).
- **Fontes**: Bricolage Grotesque (títulos) + Atkinson Hyperlegible Next (texto, feita para máxima legibilidade), do Google Fonts, hospedadas em `fonts/`.
- **Fora do CONFIG** (fixos no `<head>`): tags Open Graph e JSON-LD `Dentist`. Se o domínio mudar, atualize as URLs nos dois.

## Agendamento

- Bloqueia datas passadas, sábados, domingos e **feriados** (nacionais fixos, Carnaval, Sexta-feira Santa e Corpus Christi calculados pela Páscoa, e 20/01 — Dia de São Sebastião). Sugere o próximo dia útil com um clique.
- Depois das 16h, o primeiro dia disponível passa a ser o próximo dia útil.
- "Aberto agora / Fechado agora" usa o horário de Brasília.
- Urgência tem duas mensagens prontas: em português e em inglês (turistas).

## Regras do CRO/CFO — checklist

- [x] Sem fotos de antes e depois; nenhuma foto mostra resultado de tratamento (só ambiente, conversa e família).
- [x] Sem preços, promoções ou condições de pagamento.
- [x] Sem promessa de resultado (textos falam do atendimento, não do resultado).
- [x] Rodapé com responsável técnico: **placeholder** `Responsável técnico: Dr(a). ____ — CRO-SP ____` (preencher em `CONFIG.responsavel`).
- [x] CRO de cada profissional: **placeholder** `CRO-SP 00000` (preencher em `CONFIG.equipe`).
- [ ] **Validar com a clínica**: especialidades do Dr. Enrique e da Dra. Tatiana (coloquei "Cirurgião(ã)-dentista"), e se a Dra. Erica tem título de especialista em Ortodontia registrado no CRO — só pode anunciar "especialista" quem tem o título.
- [ ] **Depoimentos**: são **de exemplo**, inspirados no que os pacientes elogiam (atendimento, paciência com quem tem medo, urgência para turistas, família toda). Antes de publicar de verdade, confirmar com o responsável técnico se o uso de depoimentos está de acordo com as normas vigentes do CFO; a alternativa segura é manter só a nota e o link para as avaliações do Google.

## O que é de exemplo

- Depoimentos (nomes fictícios), especialidades do Dr. Enrique e da Dra. Tatiana, CROs, responsável técnico.
- Divisão manhã (9h–12h) / tarde (13h–17h) — confirmar se há intervalo de almoço.
- "Atendemos turistas e estrangeiros" vem do briefing; a mensagem em inglês é um extra.
- Fotos: banco de imagens (não são da clínica nem da equipe).

## Fotos — créditos

Todas do [Unsplash](https://unsplash.com/license) (licença Unsplash: uso livre, comercial inclusive; créditos registrados por boa prática).
WebP em duas larguras (`*.webp` 1600px e `*-sm.webp` 800px). `og.jpg` (1200×630) é um recorte de `hero.webp`.

| Arquivo | Autor | Link |
|---|---|---|
| `hero.webp` | [Harold Hisona](https://unsplash.com/pt-br/@harold_angus) | [Unsplash](https://unsplash.com/pt-br/fotografias/dentista-conversando-com-o-paciente-em-um-consultorio-odontologico-moderno-Bg81yWKZlMg) |
| `conversa.webp` | [D Dental Office](https://unsplash.com/pt-br/@ddentalof1) | [Unsplash](https://unsplash.com/pt-br/fotografias/um-homem-sorrindo-para-outro-homem-t5o3tjnaFMk) |
| `sala-espera.webp` | [Lisa Anna](https://unsplash.com/pt-br/@lisaanna195) | [Unsplash](https://unsplash.com/pt-br/fotografias/uma-cozinha-com-balcao-cadeiras-e-bar-oLtNPzG0_uU) |
| `familia.webp` | [Philip White](https://unsplash.com/pt-br/@philipwhite) | [Unsplash](https://unsplash.com/pt-br/fotografias/um-homem-e-uma-mulher-estao-segurando-um-bebe-Vg3l_fjmqXc) |
| `praia.webp` | [Chathura Anuradha Subasinghe](https://unsplash.com/pt-br/@chathuraanuradha) | [Unsplash](https://unsplash.com/pt-br/fotografias/uma-praia-com-barcos-e-arvores--Y5Tf8Lz8JQ) |

## Publicar (repositório privado)

```bash
gh repo create demo-odonto-braga --private --source=. --remote=origin --push
vercel project add demo-odonto-braga
vercel deploy --prod --yes --project demo-odonto-braga
```
