---
title: Estruturas de Agendador de Tarefas e uniões
description: Lista as estruturas e uniões usadas pelas APIs Agendador de Tarefas 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência, estruturas e uniões
- gatilhos Agendador de Tarefas, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159426"
---
# <a name="task-scheduler-structures-and-unions"></a>Estruturas de Agendador de Tarefas e uniões

Esta seção descreve as estruturas e as uniões usadas pelas APIs de Agendador de Tarefas.

Todas as estruturas e uniões abaixo são usadas pelo Agendador de Tarefas 1,0.



| Name                                               | Descrição                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**DIÁRIO**](/windows/desktop/api/Mstask/ns-mstask-daily)                             | Define o intervalo, em dias, no qual uma tarefa é executada.                                                                          |
| [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | Define o dia do mês em que a tarefa será executada.                                                                                 |
| [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | Define as datas em que a tarefa é executada por mês, semana e dia da semana.                                                     |
| [**gatilho de tarefa \_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | Define os horários para executar um [*item de trabalho*](w.md)agendado.                                                  |
| [**tipo de gatilho \_ \_ Union**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | Define o agendamento de invocação do gatilho dentro do membro de **tipo** de uma estrutura de [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . |
| [**QUINZENAL**](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | Define o intervalo, em semanas, entre as invocações de uma tarefa.                                                                  |



 

 

 




