# Oficina Mecanica - Diagrama de Casos de Uso

#  Caso de Uso 1 — Acessar o Sistema

## Atores
- Cliente  
- Mecânico Responsável  
- Atendente da Oficina

## Condições Necessárias
- Usuário deve possuir cadastro.
- Conexão com a internet disponível.

## Resultado Esperado
- Usuário autenticado.
- Sessão iniciada no sistema.

## Fluxo Principal
1. O usuário abre o sistema e informa e-mail e senha.  
2. Seleciona a opção **Entrar**.  
3. O sistema verifica as credenciais no banco de dados.  
4. Se estiverem corretas, a autenticação é concluída.  
5. A tela inicial adequada ao perfil do usuário é exibida.

## Fluxo Alternativo — Credenciais inválidas
1. O sistema detecta senha incorreta.  
2. Exibe a mensagem: *"Senha inválida"*.  
3. O usuário seleciona **Esqueci minha senha**.  
4. O sistema envia link ou código de redefinição.  
5. O usuário cria uma nova senha.  
6. O fluxo retorna para o passo 1 do fluxo principal.

---

#  Caso de Uso 2 — Consultar Ordem de Serviço (OS)

## Atores
- Cliente

## Condições Necessárias
- Cliente autenticado.


## Resultado Esperado
- Informações da OS exibidas.

## Fluxo Principal
1. O cliente acessa o menu **Minhas Ordens de Serviço**.  
2. O sistema exibe a lista de ordens registradas.  
3. O sistema apresenta:  
   - recebido
   - em analise  
   - aguardando aprovação  
   - em serviço
   - finalizado/pronto para retirada 
4. O cliente finaliza a consulta e retorna ao menu.

## Fluxo Alternativo — Nenhuma OS registrada
1. O sistema não encontra nenhuma OS associada ao cliente.  
2. Exibe: *"Nenhuma Ordem de Serviço foi encontrada"*.  
3. Cliente retorna à tela inicial.

---

#  Caso de Uso 3 — Avaliar Orçamento

## Atores
- Cliente  
- Mecânico Responsável

## Condições Necessárias
- Cliente deve estar logado.  
- Orçamento cadastrado e aguardando decisão do cliente.

## Resultado Esperado
- Orçamento aprovado ou rejeitado.
- Mecânico notificado da decisão.

## Fluxo Principal — Aprovar Orçamento
1. O cliente acessa **Orçamentos Pendentes**.  
2. Seleciona o orçamento da OS desejada.  
3. Analisa os detalhes: peças, valores e fotos.  
4. Seleciona **Aprovar**.  
5. O sistema grava a aprovação.  
6. O mecânico é notificado.

## Fluxo Alternativo — Rejeição do orçamento
1. Cliente escolhe a opção **Não aprovar**.  
2. Sistema exibe campo para justificativa.  
3. Cliente confirma a recusa.  
4. Sistema registra a rejeição.  
5. Mecânico recebe notificação para revisão do orçamento.

---

#  Caso de Uso 4 — Solicitar Cancelamento de Serviço

## Atores
- Cliente  
- Atendente

## Condições Necessárias
- Ordem de Serviço deve estar ativa.  
- Serviço não pode estar concluído ou entregue.

## Resultado Esperado
- Ordem de serviço cancelada com sucesso (quando permitido).  
- Cliente apto a abrir novo agendamento/serviço.

## Fluxo Principal
1. Cliente acessa **Cancelar Serviço**.  
2. Seleciona a OS desejada.  
3. O sistema solicita confirmação.  
4. Cliente confirma o cancelamento.  
5. O sistema registra o cancelamento.  
6. O mecânico e a recepção são notificados.

## Fluxo Alternativo — Cancelamento indisponível
1. O sistema verifica que o prazo para cancelamento expirou ou o serviço já está quase finalizado.  
2. Exibe a mensagem:  
   *"Não é possível cancelar esta OS devido ao estágio atual do serviço."*  
3. O cliente retorna ao menu principal.
