---
title: Gatilhos ociosos para Agendador de Tarefas 1,0
description: Um gatilho ocioso é um gatilho baseado em evento que é acionado um número específico de vezes após o computador ficar ocioso. Há várias condições que definem quando um computador se torna ocioso, como quando não ocorre nenhuma entrada de teclado ou mouse.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349b6ce078479df841773661bfe07b098f95d1124a68803b8b472b226d9b5df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760082"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>Gatilhos ociosos para Agendador de Tarefas 1,0

Um gatilho ocioso é um gatilho baseado em evento que é acionado um número específico de vezes após o computador ficar ocioso. Há várias condições que definem quando um computador se torna ocioso, como quando não ocorre nenhuma entrada de teclado ou mouse.

Gatilhos ociosos são criados especificando \_ o gatilho de evento de tarefa \_ \_ em \_ ociosidade no membro de [**\_ \_ tipo de gatilho de tarefa**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) da estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . O gatilho de ociosidade é acionado quando o sistema fica ocioso pelo período de tempo ocioso especificado pelo tempo de espera de ociosidade do item de trabalho.

> [!Note]  
> Quando \_ \_ o gatilho de evento de tarefa \_ \_ está ocioso é especificado, os membros **wStartHour**, **wStartMinute** e **Type** da estrutura de [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) são ignorados.

 

Você pode definir o tempo de espera ocioso de um item de trabalho chamando o método [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) . Esse método define a quantidade de tempo (em minutos) que o sistema deve permanecer ocioso antes que o gatilho seja acionado e o item de trabalho seja executado.

Para recuperar o tempo ocioso de uma tarefa, chame o método [**IScheduledWorkItem:: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> </dl>

 

 




