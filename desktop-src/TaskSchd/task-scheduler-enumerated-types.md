---
title: Agendador de Tarefas tipos enumerados
description: Lista as enumerações usadas pelas APIs de Agendador de Tarefas.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência, tipos enumerados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104499191"
---
# <a name="task-scheduler-enumerated-types"></a>Agendador de Tarefas tipos enumerados

Descreve os tipos enumerados que definem as constantes que são usadas pelas APIs de Agendador de Tarefas.


Os seguintes tipos enumerados são introduzidos no Agendador de Tarefas 2,0.



| Enumeração                                                                  | Descrição                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**\_tipo de ação da tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | Define o tipo de ações que uma tarefa pode executar.                                                             |
| [**compatibilidade de tarefas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | Define quais versões do Agendador de Tarefas ou o comando AT com o qual a tarefa é compatível.                      |
| [**criação de tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | Define como o serviço de Agendador de Tarefas cria, atualiza ou desabilita a tarefa.                                   |
| [**\_sinalizadores de enumeração de tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | Define como o Agendador de Tarefas enumera por meio de tarefas registradas.                                              |
| [**\_política de instâncias de tarefas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | Define como o Agendador de Tarefas trata as instâncias existentes da tarefa quando ele inicia uma nova instância da tarefa. |
| [**TIPO de logon da tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | Define qual técnica de logon é necessária para executar uma tarefa.                                                          |
| [**TIPO de PROCESSTOKENSID de tarefa \_**](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | Define os tipos de SID de processo que podem ser usados pelas tarefas.                                                         |
| [**\_sinalizadores de execução de tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | Define como uma tarefa é executada.                                                                                       |
| [**\_tipo de runlevel de tarefa \_**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | Define sinalizadores de elevação de LUA que especificam com que nível de privilégio a tarefa será executada.                         |
| [**\_tipo de \_ alteração de estado da sessão de tarefa \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | Define os tipos de Terminal Server alteração de estado de sessão que você pode usar para disparar uma tarefa a ser iniciada.               |
| [**estado da tarefa \_**](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | Define os diferentes Estados em que uma tarefa registrada pode estar.                                                   |
| [**Gatilho de tarefa \_ \_ TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | Define o tipo de gatilhos que podem ser usados pelas tarefas.                                                          |



 


> [!WARNING]
> As enumerações Agendador de Tarefas 1,0 estão disponíveis apenas nos sistemas operacionais Windows 2000, Windows XP e Windows Server 2003. Eles foram preteridos no Windows Vista e podem ser removidos completamente no futuro. Use as enumerações Agendador de Tarefas 2,0 listadas acima em vez disso.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[Referência de Agendador de Tarefas](task-scheduler-reference.md)
</dt> </dl>

 

 




