# Reforma 2027 — instruções para o Claude Code

Este arquivo é lido automaticamente em toda sessão. **Não peça ao usuário para repetir o briefing nem o pipeline: está tudo aqui.**

## Antes de qualquer trabalho
1. Leia `docs/BRIEFING.md` (briefing completo: perfis, módulos, cadastro, regras).
2. Leia `docs/DECISOES.md` (decisões tomadas depois do briefing, mais recentes no topo).
3. O protótipo atual está em `index.html` (HTML único, dados de exemplo, sem banco de dados).

## Resumo em 30 segundos
- Ecossistema **pro bono** que orienta empresários sobre a reforma tributária do consumo (CBS, IBS, Imposto Seletivo), com informação validada por contadores. Imparcial: só fontes oficiais, nenhuma marca recomendada.
- Será apresentado ao **Conselho Regional de Contabilidade (CRC)**: a interface precisa impressionar, com uma introdução bonita e chamativa, mesmo sem backend.
- Frase-chave: "Nada vai ao ar sem o aval de um contador."

## O pipeline (ciclo de atualização) — o coração do app
Nenhuma informação é publicada sem passar pelas 4 etapas, nesta ordem:
1. **Bots** (cerca de 52–56, cada um responsável por uma aba: oportunidade, risco, Lucro Real, Lucro Presumido, Simples Nacional, MEI etc.) sondam fontes oficiais e geram uma **atualização inicial** com fonte. Nunca usar a palavra "rascunho".
2. **Estudantes** revisam e ganham **horas complementares**.
3. **IA open source** (separada do Grok, treinada com o material do NotebookLM) confere a revisão.
4. **Escritório validador** dá o aval final, anexa a fonte oficial e ganha **pontos**. Só então publica.

Regras: registro único por atualização (data, fonte, quem atuou em cada etapa, resultado); log por etapa; prazo do escritório 5 dias úteis (48 h vale mais pontos); transparência pública de quem atuou; leads são **resgatados** pelo escritório (cada resgate desconta 1 ponto de verificação). Detalhes em `docs/BRIEFING.md`, seção 2.

## Perfis
Administrador (Luis), Supervisor CRC, Escritório validador (inclui contador autônomo), Empresário, Estudante, Instituição de ensino. Bot e IA são atores do sistema; Comitê de revisão é papel, não perfil.

## Como trabalhar com o usuário
- O usuário usa principalmente o celular. Respostas curtas, em português, dizendo: o que foi feito, o link para ver, e o próximo passo.
- Sempre fazer commit **e push** ao terminar; o container é apagado.
- Toda decisão nova que o usuário der no chat: registrar em `docs/DECISOES.md` (com data) no mesmo commit. É isso que impede que as anotações se percam.
