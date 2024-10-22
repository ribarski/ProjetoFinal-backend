# ProjetoFinal-backend
Gerenciamento de medicamentos, mapeamento de atendimentos médicos, recomendações médicas


|Camada de Apresentação|
|----------------------|

|  - Tela de Login                      |
|  - Tela de Registro                   |
|  - Tela de Medicamentos               |
|  - Tela de Atendimentos               |
|  - Tela de Recomendações              |
-----------------------------------------------------

|----------------------|
|Camada de Serviço     |
|----------------------|

|  - UsuárioService                     |
|  - TokenService                       |
|  - MedicamentoService                 |
|  - AtendimentoMedicoService           |
|  - RecomendacaoMedicaService          |
-----------------------------------------------------

|----------------------|
|Camada de Repositório |
|----------------------|

|  - UsuárioRepository                   |
|  - TokenRepository                     |
|  - MedicamentoRepository               |
|  - AtendimentoMedicoRepository         |
|  - RecomendacaoMedicaRepository        |
-----------------------------------------------------

|----------------------|
|Camada de Modelo      |
|----------------------|

|  - Usuário                             |
|     - ID                               |
|     - Nome                             |
|     - Email                            |
|                                        |
|  - Token                               |
|     - Token ID                         |
|     - Usuário ID                       |
|     - Expiração                        |
|                                        |
|  - Medicamento                         |
|     - ID                               |
|     - Nome                             |
|     - Dosagem                          |
|                                        |
|  - AtendimentoMedico                   |
|     - ID                               |
|     - Paciente                         |
|     - Data                             |
|                                        |
|  - RecomendacaoMedica                  |
|     - ID                               |
|     - Descrição                        |
|     - AtendimentoId                    |
-----------------------------------------------------

##Descrição das Camadas

##Camada de Apresentação

Interface do usuário onde as interações ocorrem, incluindo telas para login, registro, gerenciamento de medicamentos, atendimentos médicos e recomendações.

##Camada de Serviço

Contém a lógica de negócio da aplicação:
UsuárioService: Lida com operações relacionadas a usuários.
TokenService: Lida com a geração e validação de tokens.
MedicamentoService: Gerencia a lógica para medicamentos.
AtendimentoMedicoService: Gerencia a lógica para atendimentos médicos.
RecomendacaoMedicaService: Gerencia a lógica para recomendações médicas.

##Camada de Repositório

Interface para interação com a fonte de dados (banco de dados):
UsuárioRepository: Gerencia operações de usuários.
TokenRepository: Gerencia operações de tokens.
MedicamentoRepository: Gerencia operações de medicamentos.
AtendimentoMedicoRepository: Gerencia operações de atendimentos.
RecomendacaoMedicaRepository: Gerencia operações de recomendações.

##Camada de Modelo

Representa a estrutura dos dados utilizados na aplicação:
Usuário: Contém os atributos do usuário.
Token: Contém os atributos do token.
Medicamento: Contém os atributos do medicamento.
AtendimentoMedico: Contém os atributos do atendimento médico.
RecomendacaoMedica: Contém os atributos da recomendação médica.

##Conexões e Interações

As interações do usuário na Camada de Apresentação chamam serviços da Camada de Serviço, que implementam a lógica de negócio.
Os serviços acessam a Camada de Repositório para realizar operações de leitura e gravação no banco de dados.
As operações em banco de dados são realizadas sobre os dados definidos na Camada de Modelo.
