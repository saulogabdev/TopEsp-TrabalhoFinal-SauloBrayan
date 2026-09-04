# Casos de Uso - AquaCare

## UC-01 - Cadastrar usuário

**Ator:** Aquarista
**Pré-condição:** O usuário não deve estar cadastrado no sistema com um mesmo e-mail.

**Fluxo principal:**
1. O usuário acessa a tela de cadastro
2. O usuário insere nome, e-mail e senha
3. O usuário confirma cadastro
4. O sistema valida e salva os dados

**Fluxo alternativo:**
Se os dados informados forem inválidos (campos vazios, e-mail já cadastrado ou senha fora do padrão), o sistema exibe uma mensagem de erro e solicita a correção das informações.

---

## UC-02 - Realizar Login

**Ator:** Aquarista
**Pré-condição:** O usuário deve estar cadastrado.

**Fluxo principal:**
1. O usuário acessa a tela de login
2. O usuário insere e-mail e senha
3. O usuário confirma login
4. O sistema valida os dados
5. O sistema permite o acesso

**Fluxo alternativo:**
Se os dados estiverem incorretos, o sistema exibe mensagem de erro e solicita a correção das informações.

---

## UC-03 - Cadastrar Aquário

**Ator:** Aquarista
**Pré-condição:** O usuário deve estar logado em sua conta.

**Fluxo principal:**
1. O usuário acessa a tela de cadastro de aquário
2. O sistema apresenta o formulário de cadastro
3. O usuário informa os dados (nome, foto (opcional), tipo do aquário, litragem, data de montagem e descrição (opcional))
4. O usuário confirma
5. O sistema salva os dados

**Fluxo alternativo:**
Se os dados estiverem incorretos (letras na litragem, etc.) ou faltando, o sistema apresenta um erro e solicita a correção.

---

## UC-04 - Editar Aquário

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter cadastrado algum aquário.

**Fluxo principal:**
1. O usuário acessa a tela de edição do aquário
2. O sistema apresenta o formulário de edição
3. O usuário altera os dados que desejar (nome, foto (opcional), tipo do aquário, litragem, data de montagem e descrição (opcional))
4. O usuário confirma
5. O sistema salva os dados

**Fluxo alternativo:**
Se os dados estiverem incorretos (letras na litragem, etc.) ou faltando, o sistema apresenta um erro e solicita a correção.

---

## UC-05 - Visualizar Aquário

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter cadastrado algum aquário.

**Fluxo principal:**
1. O usuário acessa a tela principal
2. O usuário seleciona qual aquário deseja visualizar
3. O sistema apresenta as informações do aquário (espécies, informações, etc.)

**Fluxo alternativo:**
Se o usuário não tiver cadastrado um aquário, a tela principal apenas mostrará um atalho para adicionar um aquário.

---

## UC-06 - Excluir Aquário

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter cadastrado algum aquário.

**Fluxo principal:**
1. O usuário acessa a tela principal
2. O usuário seleciona o aquário desejado e clica em "Excluir"
3. O sistema apresenta uma tela de confirmação
4. O usuário aceita
5. O sistema exclui o aquário

**Fluxo alternativo:**
Se o usuário não tiver cadastrado um aquário, a tela principal apenas mostrará um atalho para adicionar um aquário.

---

## UC-07 - Associar Espécies

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter cadastrado algum aquário.

**Fluxo principal:**
1. O usuário acessa a tela principal
2. O usuário seleciona o aquário
3. O usuário clica em "Adicionar Espécie"
4. O usuário seleciona a espécie
5. O usuário confirma
6. O sistema valida a associação e salva os dados

**Fluxo alternativo:**
Se o sistema verificar que a espécie é incompatível com outra espécie já adicionada, ele mostra uma tela de aviso e não adiciona a espécie.

---

## UC-08 - Desassociar Espécies

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter espécies cadastradas em algum aquário.

**Fluxo principal:**
1. O usuário acessa a tela principal
2. O usuário seleciona o aquário
3. O usuário vai até a aba "Gerenciar Espécies do Aquário"
4. O usuário escolhe a espécie e clica no ícone de lixeira
5. O usuário confirma
6. O sistema desassocia a espécie

**Fluxo alternativo:**
Se o usuário não tiver adicionado nenhuma espécie, a aba apenas terá um atalho para associar espécies.

---

## UC-09 - Cadastrar Espécies

**Ator:** Administrador
**Pré-condição:** O usuário não deve ter adicionado uma espécie com o mesmo nome.

**Fluxo principal:**
1. O usuário acessa a tela de espécies
2. O usuário seleciona o atalho "Cadastrar Espécie"
3. O usuário informa os dados da espécie
4. O usuário confirma
5. O sistema cadastra a espécie

**Fluxo alternativo:**
Se os dados estiverem inválidos ou faltando, o sistema apresenta um erro e solicita a correção.

---

## UC-10 - Excluir Espécies

**Ator:** Administrador
**Pré-condição:** O usuário deve ter adicionado alguma espécie ao sistema.

**Fluxo principal:**
1. O usuário acessa a tela de espécies
2. O usuário seleciona a espécie desejada
3. O usuário vai até o atalho "Excluir Espécie"
4. O usuário confirma
5. O sistema exclui a espécie

**Fluxo alternativo:**
Se os dados estiverem inválidos ou faltando, o sistema apresenta um erro e solicita a correção.

---

## UC-11 - Verificar Compatibilidade

**Ator:** Sistema
**Pré-condição:** O aquário deve possuir pelo menos uma espécie cadastrada.

**Fluxo principal:**
1. O usuário cadastra ou adiciona uma espécie a um aquário
2. O sistema identifica a alteração nas espécies do aquário
3. O sistema recupera todas as espécies cadastradas no aquário
4. O sistema analisa a compatibilidade entre as espécies
5. O sistema registra o resultado da análise
6. O sistema apresenta ao usuário possíveis incompatibilidades

**Fluxo alternativo:**
Se o aquário possuir menos de uma espécie cadastrada, o sistema não realiza a análise.

---

## UC-12 - Registrar Parâmetros

**Ator:** Aquarista
**Pré-condição:** O usuário deve possuir um aquário cadastrado.

**Fluxo principal:**
1. O usuário seleciona um aquário
2. O usuário acessa a tela de registro de parâmetros
3. O usuário acessa a tela de criar registro
4. O sistema apresenta o formulário de registro
5. O usuário insere os dados (temperatura, pH, gH, kH, amônia, nitrito, nitrato, etc.)
6. O usuário confirma os dados
7. O sistema salva o registro

**Fluxo alternativo:**
Se o usuário colocar valores inválidos ou deixar todos os campos vazios, o sistema apresentará um erro e solicitará uma correção.

---

## UC-13 - Editar Parâmetros

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter parâmetros registrados em algum aquário.

**Fluxo principal:**
1. O usuário seleciona um aquário
2. O usuário acessa a tela de registro de parâmetros
3. O usuário acessa a tela de edição de parâmetros
4. O sistema apresenta o formulário de atualização
5. O usuário altera os dados (temperatura, pH, gH, kH, amônia, nitrito, nitrato, etc.)
6. O usuário confirma os dados
7. O sistema salva o registro

**Fluxo alternativo:**
Se o usuário colocar valores inválidos ou deixar todos os campos vazios, o sistema apresentará um erro e solicitará uma correção.

---

## UC-14 - Visualizar Parâmetros

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter parâmetros registrados em algum aquário.

**Fluxo principal:**
1. O usuário seleciona um aquário
2. O usuário acessa a tela de registro de parâmetros
3. O sistema mostra os parâmetros

**Fluxo alternativo:**
Se o usuário não tiver feito nenhum registro de parâmetros, o sistema avisará que não há nenhum registro feito.

---

## UC-15 - Excluir Parâmetros

**Ator:** Aquarista
**Pré-condição:** O usuário deve ter parâmetros registrados em algum aquário.

**Fluxo principal:**
1. O usuário seleciona um aquário
2. O usuário acessa a tela de registro de parâmetros
3. O usuário acessa a tela de excluir registro
4. O usuário seleciona o registro de parâmetro escolhido
5. O usuário confirma
6. O sistema exclui o registro

**Fluxo alternativo:**
Se o usuário não tiver feito nenhum registro de parâmetros, o sistema avisará que não há nenhum registro feito.

---

## UC-16 - Analisar Parâmetros

**Ator:** Sistema
**Pré-condição:**
- O aquário deve ter no mínimo um registro de parâmetros.
- O aquário deve possuir espécies cadastradas.

**Fluxo principal:**
1. O usuário faz um registro de parâmetros
2. O sistema recupera os parâmetros registrados
3. O sistema recupera as espécies cadastradas no aquário
4. O sistema compara os parâmetros com as faixas ideais de cada espécie
5. O sistema avalia se os parâmetros estão adequados
6. O sistema registra o resultado da análise
7. O sistema apresenta ao usuário o resultado da análise

**Fluxo alternativo:**
- Se não houver espécies cadastradas, o sistema não realiza a análise.
- Se os parâmetros registrados forem insuficientes, o sistema informa que não é possível realizar a análise completa.

---

## UC-17 - Diagnosticar Aquário

**Ator:** Sistema
**Pré-condição:**
- O aquário deve possuir parâmetros registrados.
- O aquário deve possuir espécies cadastradas.

**Fluxo principal:**
1. O sistema identifica uma atualização dos dados do aquário (parâmetros ou espécies)
2. O sistema recupera os parâmetros registrados
3. O sistema recupera as espécies cadastradas
4. O sistema analisa os dados disponíveis (parâmetros, compatibilidade e outros critérios definidos)
5. O sistema classifica o estado do aquário (ex: saudável, alerta ou crítico)
6. O sistema registra o diagnóstico
7. O sistema apresenta o resultado ao usuário

**Fluxo alternativo:**
- Se não houver dados suficientes para análise, o sistema informa que não é possível gerar o diagnóstico.
- Se houver problemas graves (ex: parâmetros muito fora do ideal), o sistema classifica diretamente como crítico.

---

## UC-18 - Visualizar Histórico de Parâmetros

**Ator:** Aquarista
**Pré-condição:** Ter um ou mais registros de parâmetros.

**Fluxo principal:**
1. O usuário seleciona um aquário
2. O usuário acessa a tela de registros de parâmetros
3. O sistema recupera os registros de parâmetros do aquário
4. O sistema apresenta o histórico dos parâmetros ao usuário

**Fluxo alternativo:**
Se não houver registros de parâmetros, o sistema informa que não há dados disponíveis para exibição.

---

## UC-20 - Recomendar Espécies

**Ator:** Sistema
**Pré-condição:** O usuário deve estar logado em uma conta.

**Fluxo principal:**
1. O usuário acessa a funcionalidade de recomendação de espécies
2. O sistema apresenta um formulário de parâmetros
3. O usuário insere os dados (pH, temperatura, amônia, etc.)
4. O sistema analisa os parâmetros informados
5. O sistema identifica espécies compatíveis com os parâmetros
6. O sistema apresenta ao usuário a lista de espécies recomendadas

**Fluxo alternativo:**
Se não houver parâmetros suficientes, o sistema informa que não é possível gerar recomendações.

---

## UC-21 - Recomendar Parâmetros

**Ator:** Aquarista
**Pré-condição:** O usuário deve estar logado em uma conta.

**Fluxo principal:**
1. O usuário acessa a funcionalidade de recomendação de parâmetros
2. O sistema apresenta uma lista de espécies
3. O usuário seleciona as espécies
4. O sistema analisa a compatibilidade das espécies selecionadas
5. O sistema calcula a faixa de parâmetro ideal para o conjunto de espécies informado
6. O sistema apresenta ao usuário as faixas de parâmetros recomendadas

**Fluxo alternativo:**
Se o usuário não selecionar nenhuma espécie, o sistema informa que é necessário selecionar no mínimo uma espécie.

---

## UC-22 - Dimensionar Equipamentos do Aquário

**Ator:** Sistema
**Pré-condição:** O usuário deve possuir um aquário cadastrado.

**Fluxo principal:**
1. O usuário seleciona um aquário
2. O usuário acessa a funcionalidade de dimensionamento de equipamentos
3. O sistema recupera as informações do aquário
4. O sistema calcula a potência do termostato recomendada
5. O sistema calcula a vazão do filtro recomendada
6. O sistema apresenta ao usuário as recomendações

---

## UC-23 - Criar Lembrete

**Ator:** Aquarista
**Pré-condição:** O usuário deve possuir um aquário cadastrado.

**Fluxo principal:**
1. O usuário seleciona um aquário
2. O usuário acessa a funcionalidade de lembretes
3. O usuário inicia a criação de um novo lembrete
4. O sistema apresenta o formulário de criação
5. O usuário informa os dados do lembrete (tipo, data, horário, descrição, entre outros)
6. O usuário confirma os dados
7. O sistema salva o lembrete

**Fluxo alternativo:**
Se os dados informados forem inválidos ou incompletos, o sistema exibe uma mensagem de erro e solicita a correção.

---

## UC-24 - Enviar Notificações de Lembretes

**Ator:** Sistema
**Pré-condição:** O usuário deve possuir no mínimo um lembrete criado.

**Fluxo principal:**
1. O sistema verifica os lembretes cadastrados
2. O sistema identifica os lembretes com horário que corresponde ao momento atual
3. O sistema dispara a notificação ao usuário
4. O sistema registra o envio da notificação

**Fluxo alternativo:**
Se não houver lembretes para o horário atual, o sistema não realiza nenhuma ação.