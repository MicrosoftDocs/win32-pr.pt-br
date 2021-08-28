---
title: Finalizando um exemplo de tarefa
description: Você pode encerrar uma tarefa enquanto ela está em execução chamando IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2705687b5383589c297348b1b5efa805b8ab407aeaef1c8c1213b1f9f6b0e894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354768"
---
# <a name="terminating-a-task-example"></a>Finalizando um exemplo de tarefa

Você pode encerrar uma tarefa enquanto ela está em execução chamando [**IScheduledWorkItem:: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).

O procedimento a seguir descreve como encerrar uma tarefa se ela estiver em execução.

**Para encerrar uma tarefa se ela estiver em execução**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame **ITask:: GetStatus** para descobrir se a tarefa está em execução. (Observe que [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
4.  Verifique o status da tarefa e, em seguida, chame **ITask:: Terminate** se a tarefa estiver em execução. (Observe que [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Para obter um exemplo de código de                | Consulte                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Verificando o status de uma tarefa conhecida | [Exemplo de código do C/C++: finalizando uma tarefa](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 