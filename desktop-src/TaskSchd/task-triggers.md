---
title: Gatilhos de tarefa
description: Um gatilho é um conjunto de critérios que, quando atendidos, inicia a execução de uma tarefa.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- Criando gatilhos Agendador de Tarefas
- Agendador de Tarefas de gatilhos
- disparadores Agendador de Tarefas, descritos
- gatilhos Agendador de Tarefas, com base no tempo
- disparadores Agendador de Tarefas, baseado em evento
- gatilhos baseados em evento Agendador de Tarefas
- gatilhos baseados em tempo Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159457"
---
# <a name="task-triggers"></a>Gatilhos de tarefa

Um gatilho é um conjunto de critérios que, quando atendidos, inicia a execução de uma tarefa. O Agendador de Tarefas fornece gatilhos baseados em tempo e em eventos que podem iniciar uma tarefa de várias maneiras diferentes. Uma determinada tarefa pode ser iniciada por um ou mais gatilhos. Uma tarefa pode ter um máximo de 48 gatilhos.

## <a name="time-based-triggers"></a>Gatilhos baseados em tempo

Os gatilhos baseados em tempo iniciam as tarefas em horários especificados. Isso inclui iniciar a tarefa uma vez em um momento específico ou iniciar a tarefa várias vezes em uma agenda diária, semanal, mensal ou mensal de dia da semana.

## <a name="event-based-triggers"></a>Gatilhos baseados em evento

Os gatilhos baseados em evento iniciam uma tarefa em resposta a determinados eventos do sistema. Por exemplo, os gatilhos baseados em evento podem ser definidos para iniciar uma tarefa quando o sistema é iniciado, quando um usuário faz logon no computador local ou quando o sistema se torna ocioso.

## <a name="multiple-triggers"></a>Vários gatilhos

Cada tarefa pode ser iniciada por um ou mais gatilhos, permitindo que a tarefa seja iniciada de várias maneiras. No entanto, vários gatilhos são implementados de forma diferente em Agendador de Tarefas 1,0 e Agendador de Tarefas 2,0.

No Agendador de Tarefas 2,0, cada gatilho é definido por uma API de gatilho separada que está associada à tarefa por meio da coleção de gatilhos.

No Agendador de Tarefas 1,0, vários gatilhos podem ser considerados como um agendamento, um conjunto de vezes em que a tarefa é iniciada. Nesse caso, o agendamento é o conjunto de vezes (especificado pela União de todos os gatilhos associados ao item de trabalho) no qual um item de trabalho será executado.

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

 

 




