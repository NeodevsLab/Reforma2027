# Reforma 2027

Instruções para qualquer sessão do Claude Code neste repositório. Leia antes de começar.

## O que é

Ecossistema pro bono que orienta empresários, sobretudo pequenos e microempresários, sobre a reforma
tributária do consumo (CBS, IBS e Imposto Seletivo). Reúne estudantes de contabilidade, contadores
autônomos e escritórios. Limitado ao Espírito Santo. Será apresentado ao Conselho Regional de
Contabilidade (CRC).

O código anterior foi perdido. Este repositório é a reescrita do zero.

## Fonte de verdade

- Briefing completo (leia primeiro): https://claude.ai/artifact/DZy6hqaUdabtT5Nz3u5ZGE
  É um documento do Claude Docs; leia pelo conector Claude Docs, não pelo navegador.
- Protótipo navegável publicado: https://claude.ai/artifact/3erM1dy7ruTEFC2rqd1t1v
- Design system (primeira proposta, ainda não aprovada): https://claude.ai/artifact/R6dXHhiBhjXjDAvrZvxHRu

## Estado atual

- Branch de trabalho: `claude/prototipo-reforma2027`. Contém `index.html`, um protótipo estático de
  página única, sem banco de dados, com dados de exemplo.
- O protótipo tem: abertura em cinco cenas com botão "Pular intro"; tela de entrada com login;
  cadastro por perfil; aplicativo interno para seis perfis (Empresário, Escritório validador,
  Estudante, Instituição de ensino, Supervisor CRC, Administrador).
- O visual ainda NÃO está aprovado. O responsável quer o design da primeira versão (a perdida) e vai
  enviar referências. Não mude a aparência sem a referência dele em mãos.

## Regras de trabalho

- O responsável costuma operar pelo celular. Respostas curtas, em português, dizendo sempre o que foi
  recebido, o que foi feito e o próximo passo. Avise na hora quando faltar algum acesso.
- Commit e push ao fim de cada tarefa, sem exceção. Perder o código de novo é o maior risco do projeto.
- Trabalhe em uma branch; só altere a `main` com autorização explícita.
- Antes de publicar no artefato do protótipo, leia a versão que está no ar: outra sessão pode ter
  publicado. Junte as mudanças em vez de sobrescrever.
- Não use a palavra "rascunho" para o que os bots produzem: é "atualização inicial".
- Tom sempre positivo e informativo, nunca punitivo.

## Regras inegociáveis do produto

- Nenhuma informação é publicada sem o aval de um escritório validador.
- Ninguém altera pontos à mão, nem o Administrador.
- Rodízio de indicações automático, por regra de sistema.
- Log de auditoria imutável.
- Imparcialidade: sem marca, sem serviço pago, sem opinião política. Só fontes oficiais.
- Mudança de regra só com 30 dias de aviso.

## Conteúdo tributário

Nada é afirmado de memória. Toda informação sobre a reforma leva fonte oficial e data de vigência.
Os textos do protótipo são exemplos e precisam ser conferidos na EC 132/2023 e na LC 214/2025 antes
de qualquer apresentação.

## Tecnologia

Proposta no briefing, ainda em aberto: Next.js, Supabase e Vercel. Por enquanto o protótipo é HTML,
CSS e JavaScript puros, sem etapa de build.
