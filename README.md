# A Forja

**Um app de construção de hábitos com constância real, reflexão diária e dados que pertencem a você.**

O A Forja é um aplicativo Android nativo de acompanhamento de ofensivas ("streaks") voltado a desenvolvimento pessoal — não a engajamento por vaidade. Cada ofensiva exige uma reflexão diária obrigatória sobre dificuldades e aprendizados, e todo o histórico do usuário é assinado com sua própria chave via o protocolo [Nostr](https://nostr.com), garantindo que os dados de progresso pertençam a quem os produziu, não ao aplicativo.

## Por que existe

A maioria dos apps de hábito trata constância como um jogo de números: um risco verde por dia, uma contagem que sobe. O A Forja parte de outro princípio — que construir um hábito de verdade exige parar, escrever e refletir sobre o que aquele dia custou e ensinou. Sem esse registro, não há check-in.

O segundo princípio é sobre propriedade: se o app parar de existir amanhã, o histórico do usuário não pode ir junto. Por isso a persistência principal é via Nostr — um protocolo aberto, sem servidor central — em vez de um banco de dados proprietário.

## Principais características

- **Ofensivas personalizáveis**, com prazos de 7, 14 ou 30 dias e marcos de condecoração até 3 anos
- **Reflexão diária obrigatória** (limite de 280 caracteres), com "modo artigo" desbloqueado a cada marco para relatos mais longos
- **Zero tolerância e sem retroatividade** — a disciplina é real, não uma planilha preenchida depois
- **Persistência via Nostr**, privada por padrão (NIP-78), com publicação pública opcional e compartilhável
- **Sistema de badges** (NIP-58) para slots de ofensiva, progressão de nível e condecorações
- **Mídia via protocolo Blossom**, com espelho automático de resiliência
- **Login sem custódia de chave**, via signer remoto (NIP-46 — Amber ou nsec.app)
- **Local-first**: nenhum check-in depende de estar online no momento em que é feito
- **Onboarding educativo sobre Nostr**, pensado para quem nunca ouviu falar do protocolo
- **Widgets de tela inicial** nativos, com lembrete e progresso agregado
- **Exportação completa dos dados** a qualquer momento, em `.zip`

## Stack técnica

| Camada | Tecnologia |
|---|---|
| Linguagem | Kotlin |
| UI | Jetpack Compose |
| Arquitetura | MVVM |
| Persistência local | Room |
| Sincronização em segundo plano | WorkManager |
| Protocolo de dados | Nostr ([Quartz](https://github.com/vitorpamplona/amethyst)) |
| Mídia | [Blossom](https://github.com/hzrd149/blossom) |
| Widgets | Jetpack Glance |
| CI/CD | GitHub Actions + Dependabot |

## Status do projeto

Em desenvolvimento ativo, solo, com apoio de IA. Todas as decisões de produto e arquitetura estão documentadas e versionadas junto ao planejamento do projeto — consulte o histórico de decisões para o estado atual de cada etapa.

Plataforma Android primeiro; uma versão iOS é planejada para depois da publicação na Google Play.

## Licença

A definir.

---

*A Forja: onde a constância é moldada, um dia de cada vez.*
