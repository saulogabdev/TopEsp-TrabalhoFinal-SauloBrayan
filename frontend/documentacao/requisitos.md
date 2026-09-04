# Requisitos do Sistema - AquaCare

## Requisitos Funcionais

| ID | Nome do Requisito | Descrição |
|---|---|---|
| RF01 | Autenticar Usuário | O sistema deve permitir que os usuários se cadastrem e façam login com email e senha. |
| RF02 | Recuperar Senha | O sistema deve permitir ao usuário redefinir sua senha, caso tenha perdido. |
| RF03 | Gerenciar Conta | O sistema deve permitir ao usuário alterar suas informações e excluir sua conta. |
| RF04 | Gerenciar Aquário | O sistema deve permitir ao usuário cadastrar, editar e excluir aquários. |
| RF05 | Gerenciar Animal no Aquário | O sistema deve permitir ao usuário associar, editar e excluir animais em um aquário. |
| RF06 | Gerenciar Planta no Aquário | O sistema deve permitir ao usuário associar, editar e excluir plantas em um aquário. |
| RF07 | Consultar Enciclopédia de Espécies | O sistema deve disponibilizar uma enciclopédia com todas as espécies cadastradas, permitindo busca por nome, visualização de informações detalhadas e filtragens. |
| RF08 | Gerenciar Catálogo de Espécies | O sistema deve permitir que um usuário com papel de administrador (role ADMIN) cadastre, edite e exclua espécies (animais e plantas) na base de dados de referência utilizada pela enciclopédia. |
| RF09 | Verificar Compatibilidade | O sistema deve analisar a compatibilidade das espécies presentes no aquário. |
| RF10 | Gerenciar Registro de Parâmetro | O sistema deve permitir ao usuário registrar, editar e excluir as medições dos parâmetros físico-químicos relacionados a um aquário. |
| RF11 | Visualizar Histórico de Registros | O sistema deve permitir ao usuário visualizar o histórico de todos os registros de medições feitas de um aquário. |
| RF12 | Analisar Registros | O sistema deve analisar os parâmetros registrados, correlacioná-los com a fauna do aquário e exibir ação recomendada para cada parâmetro fora do tolerável. |
| RF13 | Diagnosticar Aquário | O sistema deve classificar o estado do aquário, com base na análise e na compatibilidade. |
| RF14 | Gerar Gráficos | O sistema deve gerar gráficos mostrando a variação de cada parâmetro conforme os dias. |
| RF15 | Recomendar Ações e Parâmetros | O sistema deve sugerir ações, espécies e parâmetros ideais para determinado aquário. |
| RF16 | Dimensionar Equipamento | O sistema deve recomendar o dimensionamento ideal dos equipamentos com base nas características do aquário selecionado. |
| RF17 | Gerenciar Lembrete | O sistema deve permitir ao usuário criar, editar e excluir lembretes, além de ser notificado. |
| RF18 | Notificar Lembrete | O sistema deve enviar notificações para o dispositivo do usuário alertando sobre lembretes agendados. |
