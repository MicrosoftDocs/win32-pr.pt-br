---
title: Interfaces Agendador de Tarefas 1,0
description: as interfaces descritas nos tópicos a seguir fornecem acesso programático à funcionalidade que está disponível no Agendador de Tarefas usado nos sistemas operacionais Windows 2000, Windows XP e Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2033c78594c0f4ef1d9f871275f425ef5189240ed7b432266464343cf86e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975026"
---
# <a name="task-scheduler-10-interfaces"></a>Interfaces Agendador de Tarefas 1,0

\[\[Essa API pode ser alterada ou não estar disponível nas versões subsequentes do sistema operacional ou produto. Use as [Interfaces Agendador de Tarefas 2,0](task-scheduler-2-0-interfaces.md) ou [Agendador de tarefas tipos enumerados 2,0](task-scheduler-2-0-enumerated-types.md) em vez disso. \]\]

as interfaces descritas nos tópicos a seguir fornecem acesso programático à funcionalidade que está disponível no Agendador de Tarefas usado nos sistemas operacionais Windows 2000, Windows XP e Windows Server 2003.

Esses tópicos contêm uma descrição da interface, uma lista das propriedades e dos métodos definidos pela interface e comentários sobre as circunstâncias especiais que devem ser observadas ao usar a interface.


As interfaces a seguir são introduzidas por Agendador de Tarefas 1,0.



| Interface                                        | Descrição                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Fornece os métodos para enumerar as tarefas na [*pasta tarefas agendadas*](s.md).                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Fornece os métodos para acessar as configurações de folha de propriedades de uma tarefa.                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Fornece os métodos para gerenciar [*itens de trabalho*](w.md)específicos.                                                                                                                                                 |
| [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Fornece os métodos para executar tarefas, obter ou definir informações de tarefas e finalizar tarefas. Ele é derivado da interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) e herda todos os métodos dessa interface. |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Fornece os métodos para agendar tarefas.                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Fornece os métodos para acessar e definir gatilhos para uma tarefa. Os gatilhos especificam os horários de início da tarefa, os critérios de repetição e outros parâmetros que controlam quando uma tarefa é executada.                                                     |



 

 

 




