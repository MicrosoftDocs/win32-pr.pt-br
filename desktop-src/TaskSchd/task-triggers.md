---
title: Gatilhos de tarefa
description: Um gatilho é um conjunto de critérios que, quando atendido, inicia a execução de uma tarefa.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- criando gatilhos Agendador de Tarefas
- gatilhos Agendador de Tarefas
- gatilhos Agendador de Tarefas , descrito
- gatilhos Agendador de Tarefas , baseados em tempo
- dispara Agendador de Tarefas , baseado em evento
- gatilhos baseados em evento Agendador de Tarefas
- gatilhos baseados em tempo Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0060511556615c638eb8385a757e9c44147720b659bb11bfe4f0849e4499ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002294"
---
# <a name="task-triggers"></a>Gatilhos de tarefa

Um gatilho é um conjunto de critérios que, quando atendido, inicia a execução de uma tarefa. Agendador de Tarefas fornece gatilhos baseados em tempo e em eventos que podem iniciar uma tarefa de várias maneiras diferentes. Uma determinada tarefa pode ser iniciada por um ou mais gatilhos. Uma tarefa pode ter um máximo de 48 gatilhos.

## <a name="time-based-triggers"></a>Gatilhos baseados em tempo

Gatilhos baseados em tempo iniciam tarefas em horários especificados. Isso inclui iniciar a tarefa uma vez em um momento específico ou iniciar a tarefa várias vezes em um agendamento diário, semanal, mensal ou mensal do dia da semana.

## <a name="event-based-triggers"></a>Gatilhos baseados em eventos

Gatilhos baseados em eventos iniciam uma tarefa em resposta a determinados eventos do sistema. Por exemplo, gatilhos baseados em eventos podem ser definidos para iniciar uma tarefa quando o sistema é iniciado, quando um usuário faz login no computador local ou quando o sistema fica ocioso.

## <a name="multiple-triggers"></a>Vários gatilhos

Cada tarefa pode ser iniciada por um ou mais gatilhos, permitindo que a tarefa seja iniciada de várias maneiras. No entanto, vários gatilhos são implementados de maneira Agendador de Tarefas 1.0 e Agendador de Tarefas 2.0.

No Agendador de Tarefas 2.0, cada gatilho é definido por uma API de gatilho separada associada à tarefa por meio da coleção de gatilhos.

No Agendador de Tarefas 1.0, vários gatilhos podem ser pensados como um agendamento, um conjunto de horas em que a tarefa é iniciada. Nesse caso, o agendamento é o conjunto de horas (especificado pela união de todos os gatilhos associados ao item de trabalho) no qual um item de trabalho será executado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Repetindo uma tarefa](repeating-a-task.md)
</dt> <dt>

[Tipos de gatilho](trigger-types.md)
</dt> <dt>

[Interfaces de gatilho](trigger-interfaces.md)
</dt> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> </dl>

 

 




