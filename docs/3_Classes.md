***Aluno***:
RF01, RF04, RF05, RF06, RF10
- idAluno
- nome
- cpf
- email
- telefone
- endereco
- rfid
- status
- contratarPlano()
- agendarAula()
- cancelarAgendamento()
- atualizarStatus()
- registrarAcesso()
- receberNotificacao()

***Plano***:
RF01, RF02, RF04
- idPlano
- nome
- tipo
- valor
- ativo
- ativar()
- desativar()
- alterarPreco()
- vincularModalidade()

***Pagamento***:
RF03, RF04, RF09
- idPagamento
- data
- valor
- formaPagamento
- status
- registrarPagamento()
- gerarBoleto()
- estornar()
- validarTransacao()

***Acesso***:
RF05, RF09
- idAcesso
- dataHora
- autorizado
- validarEntrada()
- bloquearAcesso()
- registrarTentativaInvalida()

***Aula***:
RF06, RF07, RF09
- idAula
- nome
- horario
- capacidadeMaxima
- verificarVagas()
- alterarHorario()
- definirInstrutor()

***Agendamento***:
RF06, RF10
- idAgendamento
- dataReserva
- status
- confirmar()
- cancelar()

***Presença***:
RF07
- idPresenca
- data
- presente
- registrar()
- abonarFalta()

***Avaliação Física***:
RF08, RF10
- idAvaliacao
- data
- peso
- imc
- percentualGordura
- observacoes
- anexo
- gerarResultado()
- gerarPdf()
- compararEvolucao()

***Notificação***:
RF10
- idNotificacao
- tipo
- dataEnvio
- status
- mensagem
- enviar()
- marcarConcluido()
- agendarEnvio()

***Funcionário (Abstrata)***:
- nome
- realizarLogin()
- alterarSenha()

***Instrutor***:
RF07, RF08
- idInstrutor
- nome
- especialidade
- registrarPresenca()
- realizarAvaliacao()
- prescreverTreino()

***Recepcionista***:
RF01, RF03
- idRecepcionista
- nome
- receberPagamento()
- cadastrarAluno()
- abrirCaixa()

***Gerente***:
RF02, RF09
- idGerente
- nome
- emitirRelatorios()
- gerenciarPlanos()
- analisarFaturamento()
