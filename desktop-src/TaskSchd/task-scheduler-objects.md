---
title: Agendador de Tarefas objetos de script
description: Os objetos de script descritos nos tópicos a seguir fornecem acesso programático à funcionalidade disponível no Agendador de Tarefas para Visual Basic e Visual Basic desenvolvedores de script.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência, objetos de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acf9d74ae2bf586941f3b93a6c2cbb3a84836144
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104162955"
---
# <a name="task-scheduler-scripting-objects"></a>Agendador de Tarefas objetos de script

Os objetos de script descritos nos tópicos a seguir fornecem acesso programático à funcionalidade disponível no Agendador de Tarefas para Visual Basic e Visual Basic desenvolvedores de script.


Os seguintes objetos são introduzidos no Agendador de Tarefas 2,0.



| Objeto                                                         | Descrição                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ação**](action.md)                                       | Fornece as propriedades comuns que são herdadas por todos os objetos de ação.                                                                                                                                                                              |
| [**Açãocollection**](actioncollection.md)                   | Contém as ações executadas pela tarefa.                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | Representa um gatilho que inicia uma tarefa quando o sistema é inicializado.                                                                                                                                                                                    |
| [**Comhandleaction**](comhandleraction.md)                   | Representa uma ação que dispara um manipulador.                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | Representa um gatilho que inicia uma tarefa com base em uma agenda diária.                                                                                                                                                                                    |
| [**Emailaction**](emailaction.md)                             | Representa uma ação que envia uma mensagem de email.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Representa um gatilho que inicia uma tarefa quando ocorre um evento do sistema.                                                                                                                                                                                   |
| [**Execaction**](execaction.md)                               | Representa uma ação que executa uma operação de linha de comando.                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | Especifica como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | Representa um gatilho que inicia uma tarefa quando ocorre uma condição ociosa.                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | Representa um gatilho que inicia uma tarefa quando um usuário faz logon.                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | Representa um gatilho que inicia uma tarefa em uma agenda mensal de dia da semana.                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | Representa um gatilho que inicia uma tarefa com base em um agendamento mensal.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Fornece as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.                                                                                                                                                               |
| [**Beneficiário**](principal.md)                                 | Fornece as credenciais de segurança para um principal.                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | Fornece os métodos que são usados para executar a tarefa imediatamente, obter qualquer instância em execução da tarefa, obter ou definir as credenciais que são usadas para registrar a tarefa e as propriedades que descrevem a tarefa.                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | Contém todas as tarefas que são registradas.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Fornece as informações administrativas que podem ser usadas para descrever a tarefa. Essas informações incluem detalhes como uma descrição da tarefa, o autor da tarefa, a data em que a tarefa é registrada e o descritor de segurança da tarefa. |
| [**RegistrationTrigger**](registrationtrigger.md)             | Representa um gatilho que inicia uma tarefa quando a tarefa é registrada.                                                                                                                                                                                  |
| [**RepetitionPattern**](repetitionpattern.md)                 | Define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | Fornece os métodos para obter informações e controlar uma tarefa em execução.                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | Usado para recuperar uma tarefa em execução.                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | Usado para disparar tarefas para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.                                                                                                                   |
| [**Permessageaction**](showmessageaction.md)                 | Representa uma ação que mostra uma caixa de mensagem quando uma tarefa é ativada.                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | Define todos os componentes de uma tarefa, como as configurações de tarefa, gatilhos, ações e informações de registro.                                                                                                                                     |
| [**TaskFolder**](taskfolder.md)                               | Fornece os métodos que são usados para registrar (criar) tarefas na pasta, remover tarefas da pasta e criar ou remover subpastas da pasta.                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | Conta o número de pastas na coleção e recupera uma pasta especificada da coleção.                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | Cria um par de nome-valor no qual o nome está associado ao valor.                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | Contém uma coleção de pares nome-valor do objeto [**TaskNamedValuePair**](tasknamedvaluepair.md) .                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | Fornece acesso ao serviço de Agendador de Tarefas para gerenciar tarefas registradas.                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | Fornece as configurações que os serviços de Agendador de Tarefas usam para executar a tarefa.                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | Define as variáveis de tarefa que podem ser passadas como parâmetros para manipuladores de tarefas e executáveis externos que são iniciados por tarefas.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Representa um gatilho que inicia uma tarefa quando o gatilho é ativado.                                                                                                                                                                                |
| [**Of**](trigger.md)                                     | Fornece as propriedades comuns que são herdadas por todos os objetos de gatilho.                                                                                                                                                                             |
| [**Disparador**](triggercollection.md)                 | Usado para adicionar, remover e recuperar os gatilhos de uma tarefa.                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | Representa um gatilho que inicia uma tarefa com base em uma agenda semanal.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Agendador de Tarefas](task-scheduler-reference.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 




