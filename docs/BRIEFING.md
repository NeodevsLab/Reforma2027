# Reforma 2027 — Briefing completo do aplicativo
- Versão 1, para revisão do Luis. O que veio dos documentos de regras e das conversas está escrito como decisão. O que é sugestão minha está marcado com [ideia nova]. Todos os números continuam sendo propostas até a apresentação ao CRC.
## 1. O que é o aplicativo 
- Ecossistema integrado que reúne estudantes de contabilidade, contadores autônomos e contadores de escritórios de contabilidade, abrangendo toda a fase da vida profissional do contador: do aluno que ganha horas complementares ao escritório que valida e recebe indicações. É assim quel,
-    ouvir o aplicativo (decisão do Luis, 19/11/2026).
- Ecossistema pro bono que orienta empresários sobre a reforma tributária do consumo no Brasil (CBS, IBS e Imposto Seletivo), com informação sempre atualizada e validada por contadores.
- Não tem clientes pagantes nem meta de receita. As metas são de impacto:p1p0⁰0 empresas atendidas, contadores usando, adoção pelo CRC e por faculdades.
- Imparcial: nenhuma marca, software, escritório ou serviço pago é recomendado. Só fontes oficiais. O app orienta, mas não substitui o contador.
- Quem programa é o Claude Code, no repositório NeoDevsLab/Reforma2027. O  y código anterior foi perdido; esta é a reescrita do zero.
## 2. O ciclo de atualização (o coração do app)
Nenhuma informação vai ao ar sem passar pelas quatro etapas, nesta ordem:
Etapa 1 nas palavras do Luis (19/11/2026, para o Claude Code): os bots sondam as atualizações iniciais em fontes oficiais, de acordo com o prompt direcionado a cada um. Cada bot é responsável por uma aba do app: oportunidade, risco, Lucro Real, Lucro Presumido, Simples Nacional, MEI, e assim por diante. São 52 bots, o que dá e sobra. Não usar a palavra "rascunho": o que o bot produz é uma atualização inicial, que segue para as etapas seguintes.
- Bots (cerca de 56 instâncias no Grok, prompts fechados) buscam informação nova e criam um rascunho de atualização, com a fonte.
- Estudantes revisam o rascunho e ganham horas complementares.
- IA open source (modelo aberto, separado do Grok, treinado com o material do NotebookLM) confere a revisão.
- Escritório validador dá o aval final, anexa a fonte oficial e ganha pontos. Só então a informação é publicada.
Regras do ciclo:
- Cada atualização tem um registro único com data, fonte, quem atuou em cada etapa e o resultado.
- Prazo do escritório: 5 dias úteis. Em 48 horas vale mais pontos.
- Qualquer etapa pode devolver a atualização para a anterior com justificativa registrada. [ideia nova]
- Se o escritório não responder no prazo, a atualização vai para o próximo da fila e o anterior perde pontos. [ideia nova, para fechar um vazio dos documentos]
- Informação publicada que depois se mostra errada é corrigida publicamente, com o histórico visível. [ideia nova]
- Log por etapa (Luis, 19/11/2026): cada estudante, IA e escritório que atua numa atualização gera um registro próprio: quem, quando, o quê. Quando a informação sai errada, dá para saber em qual etapa e quem errou.
- Transparência para todos (Luis, 19/11/2026): em cada informação publicada aparece quem atuou em cada etapa, por exemplo "revisado por Camila Vieira, da instituição X". Se a informação estiver errada, uma janela abre ao clicar, com o motivo do erro: contradição com a fonte oficial, informação desatualizada, interpretação incorreta, fonte não oficial, erro de digitação (lista a fechar com o Luis). Tom informativo, nunca punitivo.
- Leads por resgate (Luis, 19/11/2026): o escritório não recebe leads automaticamente. Ele solicita o resgate dos leads a que tem direito, e cada lead resgatado desconta um ponto do seu total de verificações, como quem resgata uma recompensa. O rodízio continua definindo qual lead cabe a quem; o escritório só decide quando resgatar.
- Estudante que errou (Luis, 19/11/2026): o estudante que revisou uma informação depois confirmada como errada pode perder o ponto de horas complementares daquela revisão, mesmo já verificado. A perda fica registrada e aparece para a instituição.
- O que toda informação inserida carrega (Luis, 19/11/2026): data e hora de inserção; fonte oficial com link; data de vigência da regra; versão anterior, quando houver (informação nova não tem anterior e o campo fica vazio); quem atuou em cada etapa, com data e hora. Motivo: a regra pode ter mudado durante certo tempo.
## 3. Perfis: poderes, deveres e responsabilidades
Cada conta tem um único perfil. Permissões valem no banco de dados, não só na tela.
### Administrador (Luis)
- Pode: gerenciar usuários, configurações, cadastros e regras; ver todas as etapas, pontuações, penalidades, contestações e o log completo; suspender ou excluir escritório, só pelas regras publicadas e com registro.
- Deve: manter o app no ar, cuidar dos backups, da segurança e da LGPD; publicar mudança de regra com 30 dias de aviso; responder às solicitações de dados dos usuários.
- Não pode: aprovar atualização no lugar de um escritório, alterar pontos, níveis ou resultado de contestação, nem escolher quem recebe indicação.
- Responsabilidade: pela operação e pela imparcialidade. Toda ação dele entra no log, visível ao Supervisor CRC. Conta com verificação em duas etapas.
- Acrescentado pelo Luis em 19/11/2026: pode excluir informação em qualquer etapa da cadeia, na hora, para tirar do ar o que estiver errado (exclui, não edita nem aprova; a exclusão fica no log). Pode banir usuários temporária ou permanentemente. Seus acessos de leitura são permanentes. Admin e Supervisor entram pela mesma tela, com uma caixa de seleção "Admin" ou "Supervisor".
### Supervisor CRC
- Pode: consultar, somente leitura, os registros de pontuação, penalidades, contestações, histórico de validações, log de auditoria e relatório trimestral; participar do comitê de revisão como convidado.
- Deve: acompanhar os processos e reportar ao CRC.
- Não pode: escrever nada no app nem decidir sobre níveis.
- Responsabilidade: nenhuma sobre o conteúdo; o CRC não se compromete com o app nem com escritório algum. Desligamento com 30 dias de aviso.
- Cadastro (decisão do Luis em 19/11/2026): além de nome, e-mail, cargo no conselho e telefone, informa o número do registro dele no CRC, conferido antes da ativação.
- Acrescentado pelo Luis em 19/11/2026: o Supervisor é o membro do CRC responsável por supervisionar os escritórios e a contabilidade em geral. Tem acesso à fiscalização da distribuição das recompensas (pontos, níveis e indicações). Se identificar algo estranho, marca uma bandeira amarela no item. Inicialmente, cada bandeira vai para o Administrador revisar. A bandeira é a única escrita que o Supervisor faz; ela fica no log.
- Tem acesso às informações dos escritórios. Às informações dos alunos, em princípio não; ponto em aberto, a pensar mais e a validar na reunião do conselho (Luis, 19/11/2026).
### Escritório validador (inclui o contador autônomo)
- Pode: ver atualizações em andamento, aprovar para publicação, apontar erros, ver pontuação e nível próprios e de todos (os outros só leitura), abrir contestação, receber indicações de empresários.
- Deve: validar dentro do prazo, anexar a fonte oficial quando exigida, manter o registro no CRC ativo, aceitar que a pontuação é pública.
- Não pode: validar sem ler, usar fonte falsa, combinar pontos com outro escritório (fraude comprovada = exclusão definitiva), nem ver dados de empresário antes de ele aceitar a indicação.
- Responsabilidade: é o maior responsável pela informação publicada. Erro grave aprovado = -10 pontos; 2 erros graves em 90 dias = suspensão de 30 dias; 3 em 6 meses = volta a Participante.
- Contador autônomo: mesmo perfil, mesma fila e mesmas regras; no cadastro informa o registro profissional no CRC e o CNPJ é opcional.
### Empresário
- Pode: consultar tudo o que está publicado, apontar erro, receber indicação de escritório pelo rodízio e escolher outro se quiser, ver o relatório trimestral.
- Deve: manter CNPJ e porte atualizados para a indicação ser útil.
- Não pode: ver atualizações em andamento nem dados de outros empresários.
- Responsabilidade: pelas decisões que tomar; o app orienta, o contador decide com ele.
### Estudante
- Pode: revisar atualizações (etapa 2), apontar erro, ver o próprio histórico e pontos, escolher a instituição, informar satisfação com ela (voluntário) e decidir se aceita ofertas de outras instituições (desmarcado por padrão).
- Deve: revisar com cuidado e dentro do prazo; informar matrícula e instituição corretas.
- Não pode: aprovar nada para publicação nem ver pontuação de escritórios.
- Responsabilidade: pela qualidade da revisão; o vínculo com a instituição só vale depois que ela confirma.
### Instituição de ensino
- Pode: ver só os próprios alunos confirmados, com pontos e atividades; dar baixa nas horas já computadas na matrícula; desfazer a baixa com justificativa; ver a satisfação agrupada (mínimo de 10 respostas).
- Deve: confirmar o vínculo de cada aluno pelo e-mail oficial; registrar as horas na matrícula.
- Não pode: ver alunos de outra instituição, alterar pontos, validações ou níveis, nem ver a nota individual de satisfação.
- Responsabilidade: pela emissão correta das horas complementares aos seus alunos.
- Acrescentado pelo Luis em 19/11/2026: cada instituição recebe um número de identificação próprio dentro do nosso cadastro, para nunca haver dualidade nem mistura entre instituições. Ela tem acesso ao log dos alunos dela (o que cada um fez e quanto tempo contribuiu), nunca ao log geral. As horas complementares são contadas por número de manutenções e revisões feitas pelo aluno, sem medir tempo (decisão do Luis: tempo não dá para medir). Quantas horas cada revisão vale será definido com a instituição. A forma de computar será confirmada com a Multivix, que é o case inicial (primeira instituição parceira).
### Bot e IA open source
- Não fazem login como pessoas: usam chaves próprias, limitadas à etapa deles (bot cria rascunho; IA confere).
- Devem: sempre anexar a fonte e a data; nunca publicar.
- Responsabilidade: do Administrador, que controla as chaves e os prompts.
### Comitê de revisão (papel, não perfil)
- Mínimo de 3 pessoas, idealmente indicadas pelo CRC. Decide contestações em até 15 dias e classifica erros como leves ou graves. Nenhum perfil sozinho decide. O app registra a decisão.
- [ideia nova] criar a função de registrar a decisão do comitê, com assinatura de pelo menos 3 membros, porque hoje nenhum perfil pode fazer isso.
## 4. Funções do aplicativo, por módulo
### Conteúdo da reforma
- Informações publicadas, organizadas por tema, regime (Simples puro ou híbrido, Lucro Presumido, Lucro Real), porte e atividade.
- Cada informação mostra fonte oficial, data de vigência e quem validou. [ideia nova: selo de validação visível]
- Alíquotas, prazos e normas ficam em tabela com fonte e vigência, nunca fixos no código.
- Calendário de prazos da reforma, com avisos para o empresário. [ideia nova]
- Correção pública de erro: aviso a quem viu a versão errada. [ideia nova]
- Busca simples e glossário de termos. [ideia nova]
### Validação (as quatro etapas)
- Fila de atualizações com estado de cada uma.
- Distribuição automática das atualizações entre os escritórios, com rodízio e prazo. [ideia nova, vazio dos documentos]
- Caixa de tarefas por perfil: cada um entra e vê só o que espera por ele. [ideia nova]
- Avisos de prazo (e-mail e no app) com calendário de dias úteis. [ideia nova, necessário para a pontuação por prazo funcionar]
- Devolução de etapa com justificativa.
### Pontos e níveis dos escritórios
- Motor de pontos: ganhos (+1, +2, +5, +10, +1, +3), perdas (-1, -3, -3, -10, -2, -2), teto de 30 pontos por mês de validações simples, janela móvel de 6 meses.
- Níveis (nome do primeiro nível corrigido pelo Luis em 19/11/2026: é Starter, nunca foi Participante): Starter (0 a 29), Bronze (30 a 79), Prata (80 a 149), Ouro (150 a 249), Platinum (250 ou mais). Ouro e Platinum exigem 90% das validações sem erro confirmado.
- Todos os números guardados como configuração, com mudança agendada e aviso de 30 dias. [ideia nova: agendamento]
- Suspensão, observação de 90 dias, exclusão e quarentena de 15 dias ao voltar.
- Selo de nível para o escritório exibir nos canais dele (a confirmar com o CRC).
Decisão do Luis em 19/11/2026: são seis níveis de escritório, nesta ordem, do mais baixo ao mais alto: Starter, Bronze, Prata, Ouro, Black e Platinum (o topo). As faixas de pontos de cada um, com o Black incluído, ficam para definir. Os níveis são só dos escritórios; as faixas de faturamento do empresário são outra coisa e ainda não têm nome.
Regra de direcionamento (decisão do Luis em 19/11/2026): a faixa de faturamento do empresário casa com o nível do escritório. Lógica: quanto maior o faturamento da empresa, mais caro é o contrato contábil; por isso cada nível de escritório recebe indicações de empresas até certa faixa de faturamento, e quem sobe de nível passa a receber empresas de faturamento maior. Formato das frases para o código e para os textos do app, sempre em tom positivo, nunca punitivo: "Escritórios que contribuem com até 30 validações estão no nível Starter e recebem indicações de empresas com faturamento de até X". Uma frase por nível; os valores de X e as contagens por nível ainda serão definidos pelo Luis. Esta regra é para o Claude Code construir o pipeline; o texto da apresentação ao CRC é outro.
### Indicações de empresários
- Rodízio automático por região, depois por nível adequado ao porte, por ordem de fila; ninguém recebe duas seguidas se houver outro elegível.
- O empresário aceita ou escolhe outro. O escritório só vê os dados depois do aceite.
- Registro de cada indicação para o relatório trimestral.
### Contestações e comitê
- Abertura em até 10 dias corridos com fonte oficial; decisão em até 15 dias; devolução de pontos se aceita; tudo auditável.
### Estudantes e horas complementares
- Cadastro com instituição e matrícula; e-mail automático à instituição; vínculo pendente até confirmação.
- Registro de atividades e pontos; baixa de horas desfazível com justificativa.
- Declaração de horas em PDF que o estudante baixa pronta, para o Luis assinar como contador. [ideia nova]
- Satisfação com a instituição e consentimento para ofertas (ver seção 8 sobre o risco).
### Transparência pública (sem login)
- Regras, tabela de níveis, pontuação atual de cada escritório, relatório trimestral e lista de mudanças de regra agendadas.
- Relatório exportável para o Supervisor CRC. [ideia nova]
### Auditoria
- Log que só recebe inclusões: data, hora, perfil, usuário e ação. Não pode ser editado nem apagado. Visível ao Supervisor CRC.
### Cadastro e perfil
- Campos por tipo de usuário conforme o documento de perfis; validação de CNPJ e registro no CRC antes da ativação; o usuário escolhe o que fica visível (só pode restringir, nunca ampliar).
- Cadastro de Empresário, Estudante e Supervisor CRC ainda é proposta (a confirmar).
### Painel do Administrador
- Usuários, cadastros pendentes de validação, configurações, regras e agendamentos, chaves de bots e IA, saúde do sistema (filas paradas, prazos vencendo, erros). [ideia nova: painel de saúde]
## 5. Manutenção e operação
- Código: tudo no GitHub, commit e push ao fim de cada tarefa. Deploy só com testes passando.
- Banco de dados: Supabase (o Luis já conhece); toda mudança é migração versionada; backup automático e teste de restauração antes do lançamento.
- Segurança: permissões por linha no banco; chaves fora do código; duas etapas para administrador; rotação das chaves dos bots. [ideia nova: rotação]
- LGPD: só o dado necessário; o usuário vê, corrige e apaga o que informou; consentimentos registrados; revisar com advogado de proteção de dados antes de lançar a parte de ofertas a alunos.
- Conteúdo: as regras da reforma mudam toda semana; nada é afirmado de memória, sempre com fonte e data.
- Custo: o app é gratuito, então custo de operação baixo importa; medir uso e custo por mês. [ideia nova]
- Monitoramento: alerta ao Administrador quando uma etapa trava ou um prazo vence. [ideia nova]
- Responsável por tudo isso: o Administrador.
## 6. Regras inegociáveis
- Nenhuma informação publicada sem o aval de um escritório validador.
- Ninguém altera pontos à mão, nem o Administrador.
- Rodízio de indicações automático e público. Nas palavras do Luis (19/11/2026): os matches entre empresários e escritórios ou contadores autônomos são sempre via regra de sistema; nenhum administrador tem liberdade para alterar uma indicação. Isso existe para gerar confiabilidade.
- Log de auditoria imutável.
- Imparcialidade: sem marca, sem serviço pago, sem opinião política.
- Mudança de regra só com 30 dias de aviso.
- Permissões garantidas no banco de dados.
## 7. Decisões em aberto (para o Luis)
- Sete ou oito perfis: o documento diz sete, a tabela lista oito.
- Tecnologias finais (proposta: Next.js, Supabase e Vercel).
- O que entra na primeira entrega.
- Campos de cadastro de Empresário e Estudante (o do Supervisor CRC já foi decidido: inclui o registro no CRC).
- Como as horas complementares são emitidas (a declaração em PDF resolve?).
- Onde ficam as chaves dos bots e da IA.
- O que acontece com uma atualização que nenhum escritório valida no prazo.
## 8. Riscos, cada um com a saída
- Ofertas de outras faculdades a alunos insatisfeitos pode pesar contra a imparcialidade na frente do CRC. Saída: deixar fora da primeira versão e decidir depois da apresentação.
- Indicação de clientes por nível pode esbarrar nas normas de publicidade da profissão contábil. Saída: confirmar com o CRC antes de ligar a função; até lá, o rodízio pode ficar pronto mas desligado.
- Poucos escritórios no início deixa a fila vazia. Saída: o app funciona só com consulta e validação; indicações ligam quando houver pelo menos 3 escritórios por região.
- Perder o código de novo. Saída: push ao fim de cada tarefa, sem exceção.
## 9. Sugestão de primeira entrega
- Login e cadastro por perfil, com validação de CNPJ e CRC.
- Conteúdo publicado com selo de validação e fonte.
- Ciclo de validação completo (as quatro etapas) com fila e prazos.
- Motor de pontos e níveis com página pública de transparência.
- Painel do Administrador e log de auditoria.
Ficam para depois: indicações (prontas, mas desligadas até o CRC confirmar), horas complementares com instituição, satisfação e ofertas, relatório trimestral.
## 10. Tela de login e cadastro por perfil
Uma única tela de entrada para todos. O que muda é o cadastro, que depende do perfil escolhido. Bots e IA open source não passam por aqui: usam chaves de acesso criadas pelo Administrador.
Regra de senha (decisão do Luis em 19/11/2026, vale para todos os perfis): campos "Criar senha" e "Repetir senha"; de 8 a 10 caracteres; sem exigência de letra, número, maiúscula ou minúscula. Esta regra substitui a linha de senha da tabela de login abaixo.
Perfil Supervisor (decisão de 19/11/2026): o nome do perfil é "Supervisor"; ele é um membro do CRC. Cadastro: nome completo, número de registro no CRC, cargo no conselho, e-mail institucional do CRC, telefone, criar e repetir senha.
### Tela de login
Elemento
Regra
E-mail e senha
Campos obrigatórios. Senha com mínimo de 8 caracteres, letras e números. [ideia nova]
Entrar com Google
Opcional, como no Provador. Depois do Google, o usuário ainda completa o cadastro do perfil dele. [ideia nova]
Esqueci minha senha
Envia link por e-mail, válido por 1 hora. [ideia nova]
Verificação em duas etapas
Obrigatória para Administrador. Opcional para os demais.
Criar conta
Leva à escolha do perfil.
Depois do login
Cada perfil cai na própria tela inicial (caixa de tarefas). Conta ainda não ativada vê a tela "aguardando validação" com o motivo.
Bloqueio
5 tentativas erradas bloqueiam por 15 minutos. Toda entrada fica no log de auditoria. [ideia nova]
Avisos
Texto fixo: o app é gratuito, imparcial e não substitui o contador. Link para a política de privacidade (LGPD).
### Escolha do perfil (passo 1 do cadastro)
O usuário escolhe um, e só um: Escritório de contabilidade (com a opção "Sou contador autônomo"), Empresário, Estudante, Instituição de ensino ou Supervisor CRC. Administrador não se cadastra: é criado pelo próprio sistema. Depois de ativada, a conta não troca de perfil; para outro perfil, outra conta com outro e-mail. [ideia nova]
### Escritório de contabilidade
Decisão do Luis em 19/11/2026 (substitui a tabela abaixo): cadastro do Escritório em duas etapas.
Etapa 1, identificação: razão social, nome fantasia, telefone, e-mail principal, nome do usuário (quem acessa é uma pessoa, não a empresa), CNPJ, registro da organização contábil no CRC, criar e repetir senha. O contador autônomo tem cadastro separado (registro profissional no CRC é outro número).
Etapa 2, última fase, título na tela: "Nos ajude a direcionar melhor oportunidades para você". Todos os campos opcionais e só por seleção, sem texto livre e sem classificação por IA (decisão do Luis: selecionar é mais seguro):
- Quantidade de funcionários (mede a capacidade de atendimento).
- Especialidades (lista corrigida pelo Luis em 19/11/2026: sem consultoria, que não é nicho, e sem RH): fiscal, contábil, departamento pessoal, societário e abertura de empresas, planejamento tributário.
- Segmentos que atende: comércio, indústria, serviços, agronegócio, saúde, construção, tecnologia, outros.
- Regimes que atende: MEI, Simples, Lucro Presumido, Lucro Real.
- Porte dos clientes que atende.
- Região de atuação: estado e cidades.
- Atendimento: presencial, remoto ou os dois.
Regra do rodízio: só região e nível cortam. Especialidades e segmentos são desempate: quem marcou o que o empresário precisa sobe na fila. Nenhuma dessas respostas elimina um escritório.
Como captar (decisão de 19/11/2026): funcionários em botões de faixa (até 5, 6 a 20, 21 a 50, mais de 50); especialidades, segmentos, regimes e porte em lista com caixas de marcar; cidades por busca na lista; atendimento em três botões (presencial, remoto, os dois). Atendimento remoto não corta por região: recebe indicação de qualquer cidade; só o presencial fica preso à região.
Abrangência (decisão de 19/11/2026): o app é limitado ao Espírito Santo, porque o CRC é regional. Estado fixo em ES em todos os cadastros. Abrir para outros estados agora complica e pode desestimular o CRC-ES.
Contador autônomo (perfil próprio, decisão do Luis em 19/11/2026): cadastro: nome completo, número de registro profissional no CRC (obrigatório), e-mail, telefone, endereço, faixa de faturamento mensal (sempre de um valor a outro, nunca exato), criar e repetir senha. Sem data de nascimento. Etapa 2 opcional, igual à do escritório: especialidades (fiscal, contábil, departamento pessoal, societário, planejamento tributário), segmentos, regimes, porte de clientes, atendimento presencial, online ou os dois. Mesmas permissões, pontos, níveis e fila de indicações do escritório.
Campo
Obrigatório
Validação
Visível aos outros
Sou contador autônomo (sim ou não)
Sim
Muda os campos abaixo
Sempre
CNPJ
Sim para escritório, opcional para autônomo
Formato e dígitos; consulta à base da Receita [ideia nova]
Sempre
Razão social (escritório) ou nome completo (autônomo)
Sim
Texto
O usuário escolhe
Nome fantasia
Não
Texto
O usuário escolhe
Registro no CRC: da organização (escritório) ou profissional (autônomo)
Sim
Formato; conferido pelo Administrador antes da ativação
Sempre
Telefone
Sim
Formato
O usuário escolhe
E-mail
Sim
Confirmação por link
O usuário escolhe
Região de atuação (estado e cidades)
Sim [ideia nova, necessário para o rodízio por região]
Lista
Sempre
Senha
Sim
Regra de senha
Nunca
Aceite dos termos e das regras de pontuação
Sim
Registro com data e hora
Nunca
Depois, no perfil: foto da fachada, endereço, site e áreas de atuação, todos opcionais.
O que acontece depois: conta fica "aguardando validação". O Administrador confere o registro no CRC e ativa. O escritório entra no nível Participante, com zero pontos.
### Empresário (campos ainda em proposta, a confirmar)
Decisão do Luis em 19/11/2026 (substitui a tabela abaixo): cadastro do Empresário: razão social, nome fantasia, CNPJ, porte da empresa, natureza jurídica, regime tributário, nome do responsável pela conta, telefone, e-mail, endereço, preferência de atendimento (presencial ou online), criar e repetir senha, e tudo o que servir para direcionar o atendimento depois (segmento e quantidade de funcionários, por seleção). Faturamento é dado sensível: entra por faixa, nunca o valor exato, e as faixas seguem os limites legais: a primeira vai até o limite do MEI (cerca de 81 mil por ano) e se chama Starter; a segunda vai até o sublimite do Simples Nacional, a partir do qual ICMS e ISS são pagos por fora do Simples (valor a confirmar com fonte oficial: o Luis citou "300 e poucos mil"; o sublimite conhecido é 3,6 milhões por ano). Demais faixas e nomes a definir.
Campo
Obrigatório
Validação
Visível aos outros
CNPJ
Sim
Formato e dígitos; consulta à Receita [ideia nova]
O usuário escolhe
Razão social
Sim
Texto
O usuário escolhe
Nome fantasia
Não
Texto
O usuário escolhe
Porte (MEI, micro, pequena, média, grande)
Sim [ideia nova, define o nível de escritório que pode ser indicado]
Lista
Só para o escritório indicado, após o aceite
Regime tributário atual
Sim [ideia nova, filtra o conteúdo]
Lista
Só para o escritório indicado, após o aceite
Atividade principal (CNAE)
Não
Lista
Só para o escritório indicado, após o aceite
Estado e cidade
Sim [ideia nova, para a indicação por região]
Lista
Só para o escritório indicado
Nome do responsável, telefone e e-mail
Sim
E-mail confirmado por link
O usuário escolhe
Senha e aceite dos termos
Sim
Regra de senha; registro
Nunca
O que acontece depois: conta ativa na hora, após confirmar o e-mail. Cai na tela de conteúdo filtrado pelo regime e porte dele.
### Estudante (campos ainda em proposta, a confirmar)
Decisão do Luis em 19/11/2026 (substitui a tabela abaixo): os campos do cadastro de Estudante são: matrícula, nome completo, e-mail, telefone, instituição de ensino, data de início do curso, período do curso e curso. O curso é escolhido numa lista pré-definida, sem texto livre: Ciências Contábeis, Ciências Sociais, Administração e os demais cursos que façam sentido com o objetivo do app. A tela tem os botões tradicionais: X para fechar e cancelar, Registrar, Esqueci a senha e Novo usuário. Observação do Luis: o contador e o escritório têm registros diferentes no CRC (profissional e organização contábil), por isso são cadastros separados; a separação também é questão de oportunidade.
Campo
Obrigatório
Validação
Visível aos outros
Nome completo
Sim
Texto
O usuário escolhe (nome e foto)
E-mail
Sim
Confirmação por link
Nunca
Instituição de ensino
Sim
Escolhe na lista das instituições cadastradas; se não estiver, informa o nome e fica como "instituição pendente" [ideia nova]
Só para a instituição
Número de matrícula
Sim
Texto
Só para a instituição
Curso e semestre
Não
Lista
Só para a instituição
Telefone
Sim
Formato
Nunca
Senha e aceite dos termos
Sim
Regra de senha; registro
Nunca
O que acontece depois (pipeline da faculdade): ao se registrar, o app envia e-mail automático ao endereço oficial da instituição com nome, matrícula e instituição informada. A instituição confirma pelo link do e-mail. Até lá, o aluno usa o app normalmente, mas fica com vínculo pendente, sem baixa de horas. Depois da confirmação, passa a aparecer para a instituição. Se a instituição recusar, o aluno é avisado e pode corrigir a instituição ou a matrícula. [ideia nova: a recusa]
### Instituição de ensino
Campo
Obrigatório
Validação
Visível aos outros
CNPJ
Sim
Formato e dígitos; consulta à Receita [ideia nova]
Sempre
Razão social
Sim
Texto
O usuário escolhe
Nome fantasia
Sim
Texto
O usuário escolhe
E-mail oficial (valida os alunos)
Sim
Confirmação por link; deve ser do domínio da instituição [ideia nova]
Nunca
Nome, cargo e e-mail do responsável
Sim [ideia nova]
E-mail confirmado
Nunca
Telefone
Sim
Formato
O usuário escolhe
Senha e aceite dos termos
Sim
Regra de senha; registro
Nunca
Depois, no perfil: logotipo ou foto, opcional.
O que acontece depois: conta fica "aguardando validação". O Administrador confere o CNPJ e o e-mail oficial e ativa. A partir daí a instituição recebe os e-mails de vínculo dos alunos.
### Supervisor CRC
Campo
Obrigatório
Validação
Visível aos outros
Nome completo
Sim
Texto
Nome e cargo
Número do registro no CRC (decisão de 19/11/2026)
Sim
Formato; conferido pelo Administrador antes da ativação
Nunca
Cargo no conselho
Sim
Texto
Nome e cargo
E-mail
Sim
Confirmação por link
Nunca
Telefone
Sim
Formato
Nunca
Senha e aceite dos termos
Sim
Regra de senha; registro
Nunca
Depois, no perfil: foto, opcional.
O que acontece depois: conta fica "aguardando validação". O Administrador confere o registro e o cargo com o CRC e ativa. A presença do supervisor passa a ser pública no app. Uma só conta de supervisor por vez. [ideia nova]
### Regras gerais do cadastro
- Prova de vínculo com a empresa ou escritório (discutido em 19/11/2026, a confirmar pelo Luis): dados da Receita são públicos, então copiar CNPJ e nome de sócio não prova nada. Regra proposta: o responsável entra pelo login gov.br, que já traz a identidade verificada pelo governo; o CPF completo dele é cruzado com o quadro de sócios do CNPJ na Receita. Quem é sócio é validado na hora. Funcionário que não é sócio fica pendente até um sócio já validado aprovar. Em caso de dúvida, envio de documento (contrato social) para o Administrador conferir.
- Validação com a Receita (decisão do Luis, 19/11/2026, vale para todos os cadastros com CNPJ: escritório, contador autônomo quando informar CNPJ, empresário e instituição de ensino): o CNPJ e os dados informados (razão social, natureza jurídica, porte, regime quando disponível) são conferidos na base da Receita Federal antes de a conta ser ativada. Há um tempo de validação: a conta fica "aguardando validação" até a conferência terminar, com prazo máximo definido pelo Luis (sugestão: até 2 dias úteis); passado o prazo sem resposta da Receita, o Administrador valida manualmente. Divergência entre o informado e a Receita bloqueia a ativação e avisa o usuário para corrigir.
- Todo cadastro passa pela tela "confirme seu e-mail": o usuário recebe um código ou link por e-mail ou por SMS, à escolha dele, antes de qualquer outra coisa (decisão do Luis, 19/11/2026).
- O cadastro pede todos os dados de uma vez; a visibilidade é escolhida depois, dentro da plataforma, e só pode restringir o que a matriz de permissões já autoriza.
- O e-mail de acesso e o registro no CRC ficam sempre guardados, mesmo quando o usuário escolhe não exibir.
- Contas "aguardando validação" recebem um e-mail quando são ativadas ou recusadas, com o motivo. [ideia nova]
- Dados pessoais: só o necessário, com a finalidade escrita ao lado do campo. O usuário vê, corrige e apaga o que informou.
- Fotos com tamanho e formato limitados.
- Todo cadastro, ativação e recusa entra no log de auditoria.
## 11. Aba de informações do usuário (Luis, 19/11/2026)
Todo perfil tem, dentro do app, uma aba com as próprias informações, com estas funções:
- Atualizar as informações: o empresário pode trocar de regime tributário, porte ou endereço e não pode ficar preso ao que informou no cadastro; o escritório atualiza equipe, especialidades e região. Toda alteração fica registrada com data.
- Logo da empresa ou do escritório: facultativo.
- Escolher o que fica visível para os outros perfis, dentro do que a matriz de permissões permite.
- Cancelar o cadastro: o próprio usuário cancela a conta. Os dados pessoais são apagados conforme a LGPD; o histórico de validações e pontos fica no log de forma anônima, para não quebrar a auditoria das atualizações já publicadas (proposta, a confirmar pelo Luis).
- Resgate seus leads (só escritório e contador autônomo): área onde ele vê os leads a que tem direito pelo nível e pelo rodízio, o saldo de verificações disponível e solicita o resgate. Cada lead resgatado desconta um ponto do total de verificações. Histórico dos resgates com data.
