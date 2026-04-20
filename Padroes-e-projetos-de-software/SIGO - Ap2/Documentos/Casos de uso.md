# Documento de Casos de Uso - SIGO

## Caso de Uso: Autenticar  
**Atores:** Usuário (Paciente, Dentista, Recepcionista)  
**Resumo:** Permite que o usuário se identifique e acesse o sistema.  
**Fluxo Principal:**  
1. Usuário informa login e senha.  
2. O sistema valida as credenciais.  
3. O sistema libera o acesso conforme o perfil.  
**Fluxos Alternativos:**  
- 2a. Login ou senha incorretos: sistema exibe mensagem de erro.  
- 2b. Usuário esqueceu a senha: sistema envia instruções para recuperação.  
**Pós-condição:** Usuário autenticado no sistema.

---

## Caso de Uso: Agendar Consulta  
**Atores:** [Paciente, Recepcionista]  
**Resumo:** Permite o agendamento de uma consulta para um paciente.  
**Fluxo Principal:**  
1. Ator informa dados da consulta (data, horário, tipo).  
2. O sistema verifica disponibilidade.  
3. O sistema agenda e confirma a consulta por email.  
**Fluxos Alternativos:**  
- 2a. Horário indisponível: sistema solicita nova escolha.  
- 2b. Paciente indisponível nas datas sugeridas: sistema oferece opções alternativas ou contato para reagendamento.  
**Pós-condição:** Consulta registrada no sistema.

---

## Caso de Uso: Confirmar Consulta  
**Atores:** [Paciente, Recepcionista]  
**Resumo:** Permite a confirmação de um agendamento já realizado.  
**Fluxo Principal:**  
1. Ator localiza a consulta.  
2. Sistema atualiza status para "Confirmada".  
**Fluxos Alternativos:**  
- 1a. Consulta não encontrada: sistema exibe mensagem de erro.  
- 2a. Confirmação via outro método (telefone, presencial): sistema registra confirmação manual.  
**Pós-condição:** Consulta confirmada.

---

## Caso de Uso: Cancelar Consulta  
**Atores:** [Paciente, Recepcionista]  
**Resumo:** Permite o cancelamento de uma consulta agendada.  
**Fluxo Principal:**  
1. Ator localiza consulta agendada.  
2. Sistema solicita confirmação do cancelamento.  
3. Consulta é cancelada.  
**Fluxos Alternativos:**  
- 1a. Consulta não encontrada: sistema exibe mensagem de erro.  
- 2a. Consulta dentro do prazo mínimo para cancelamento: sistema impede cancelamento e informa o usuário.  
**Pós-condição:** Consulta removida da agenda.

---

## Caso de Uso: Registrar Pagamento  
**Atores:** [Paciente, Recepcionista]  
**Resumo:** Permite registrar o pagamento de um procedimento.  
**Fluxo Principal:**  
1. Ator escolhe forma de pagamento.  
2. Sistema registra pagamento.  
**Fluxos Alternativos:**  
- 2a. Pagamento não aprovado (ex: cartão recusado): sistema exibe erro e solicita nova tentativa.  
**Inclusão:** Selecionar Forma de Pagamento  
**Extensão:** Aplicar Desconto (opcional)  
**Pós-condição:** Pagamento registrado no sistema.

---

## Caso de Uso: Selecionar Forma de Pagamento  
**Atores:** [Paciente, Recepcionista]  
**Resumo:** Permite definir a forma de pagamento (PIX, cartão, dinheiro, débito automático).  
**Fluxo Principal:**  
1. Ator escolhe método de pagamento.  
2. Sistema armazena a informação selecionada.  
**Observação:** Este caso está incluído em "Registrar Pagamento" para evitar redundância.

---

## Caso de Uso: Aplicar Desconto  
**Ator:** Recepcionista  
**Resumo:** Permite aplicar desconto conforme políticas da clínica.  
**Fluxo Principal:**  
1. Recepcionista informa percentual ou valor do desconto.  
2. Sistema recalcula o valor total.  
**Fluxos Alternativos:**  
- 2a. Desconto inválido ou não autorizado: sistema exibe mensagem de erro e não aplica o desconto.  
**Pós-condição:** Valor do pagamento atualizado.

---

## Caso de Uso: Cadastrar Paciente  
**Ator:** Recepcionista  
**Resumo:** Permite inserir dados de um novo paciente no sistema.  
**Fluxo Principal:**  
1. Recepcionista preenche os dados pessoais, contatos e histórico.  
2. Sistema valida e salva as informações.  
**Fluxos Alternativos:**  
- 2a. Dados inválidos ou incompletos: sistema exibe mensagem de erro e solicita correção.  
**Pós-condição:** Paciente cadastrado no sistema.

---

## Caso de Uso: Atualizar Cadastro de Paciente  
**Ator:** Recepcionista  
**Resumo:** Permite alterar dados pessoais e bancários do paciente.  
**Fluxo Principal:**  
1. Ator seleciona paciente.  
2. Sistema exibe dados atuais.  
3. Ator edita e salva alterações.  
**Fluxos Alternativos:**  
- 1a. Paciente não encontrado: sistema exibe mensagem de erro.  
- 3a. Dados editados inválidos: sistema indica erro e solicita correção.  
**Pós-condição:** Dados do paciente atualizados.

---

## Caso de Uso: Gerar Fatura  
**Ator:** Recepcionista  
**Resumo:** Gera documento detalhado de cobrança para o paciente.  
**Fluxo Principal:**  
1. Sistema calcula valores pendentes.  
2. Fatura é emitida e disponibilizada para impressão ou envio.

---

## Caso de Uso: Emitir Relatórios  
**Ator:** Recepcionista  
**Resumo:** Gera relatórios gerenciais para administração da clínica (financeiro, atendimentos, inadimplência).  
**Fluxo Principal:**  
1. Ator seleciona tipo de relatório.  
2. Sistema apresenta os dados para análise.  
**Fluxos Alternativos:**  
- 1a. Tipo de relatório inválido: sistema exibe mensagem de erro.  
- 2a. Não há dados disponíveis: sistema informa ausência de registros.

---

## Caso de Uso: Registrar Procedimento  
**Ator:** Dentista  
**Resumo:** Permite o registro detalhado de procedimentos realizados no paciente.  
**Fluxo Principal:**  
1. Dentista seleciona paciente e procedimento realizado.  
2. Sistema armazena os dados do procedimento.

---

## Caso de Uso: Gerenciar Tratamento  
**Ator:** Dentista  
**Resumo:** Permite planejar, acompanhar e ajustar tratamentos odontológicos.  
**Inclusões:**  
- Emitir Plano de Tratamento  
- Recomendar Tratamento  
**Fluxo Principal:**  
1. Dentista seleciona paciente.  
2. Sistema exibe histórico e opções de tratamento.  
**Fluxos Alternativos:**  
- 2a. Histórico do paciente incompleto ou indisponível: sistema alerta e permite cadastro complementar.  
**Pós-condição:** Tratamento atualizado no sistema.

---

## Caso de Uso: Emitir Plano de Tratamento  
**Ator:** Dentista  
**Resumo:** Gera documento com etapas, valores estimados e duração do tratamento.  
**Fluxo Principal:**  
1. Sistema monta plano com base nos dados inseridos pelo dentista.  
2. Plano é salvo e/ou impresso.  
**Pós-condição:** Plano de tratamento registrado.

---

## Caso de Uso: Recomendar Tratamento  
**Ator:** Dentista  
**Resumo:** Permite indicar tratamento com base na avaliação clínica.  
**Fluxo Principal:**  
1. Dentista escolhe opções de tratamento recomendadas.  
2. Sistema armazena recomendação para o paciente.  
**Pós-condição:** Recomendação registrada.

---

## Caso de Uso: Visualizar Histórico do Paciente  
**Atores:** [Dentista, Recepcionista]  
**Resumo:** Permite acesso ao histórico clínico e financeiro do paciente.  
**Fluxo Principal:**  
1. Ator seleciona paciente.  
2. Sistema exibe registros clínicos, financeiros e pagamentos anteriores.  
**Fluxos Alternativos:**  
- 1a. Paciente não encontrado: sistema exibe mensagem de erro.

---

## Caso de Uso: Notificar Paciente  
**Ator:** Sistema (Automatizado)  
**Resumo:** Envia notificações automáticas de consultas, pagamentos e outras ações importantes.  
**Fluxo Principal:**  
1. Sistema identifica eventos futuros (consultas agendadas, vencimentos).  
2. Notificações são enviadas via e-mail, SMS ou aplicativo móvel.  
**Fluxos Alternativos:**  
- 2a. Falha no envio: sistema registra erro e tenta reenvio posterior.  
**Pós-condição:** Paciente notificado ou tentativa registrada.

