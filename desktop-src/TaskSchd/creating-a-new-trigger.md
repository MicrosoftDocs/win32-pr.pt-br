---
title: Criando um novo gatilho
description: Para criar um gatilho, você deve usar três interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366376"
---
# <a name="creating-a-new-trigger"></a>Criando um novo gatilho

Para criar um gatilho, você deve usar três interfaces. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornece o método [**IScheduledWorkItem:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar o objeto Trigger, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fornece o método [**ITaskTrigger:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para definir os critérios para o gatilho, e a interface com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fornece um método **Save** para salvar o novo gatilho no disco.

O procedimento a seguir descreve como criar um novo gatilho.

**Para criar um novo gatilho**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar um objeto de gatilho. (Observe que [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) é herdado de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Defina uma estrutura de [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Observe que os membros wBeginDay, wBeginMonth e wBeginYear do **\_ gatilho de tarefa** devem ser definidos como um dia, mês e ano válidos, respectivamente.
5.  Chame o [**gatilho ITaskTrigger::**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) setpara definir os critérios do gatilho.
6.  Salve a tarefa com o novo gatilho em disco usando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão com suporte da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
7.  Chame o [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar todos os recursos. (Observe que **Release** é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Para obter um exemplo de código de                       | Consulte                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Criando um novo gatilho para uma tarefa existente | [Exemplo de código C/C++: Criando um gatilho de tarefa](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 