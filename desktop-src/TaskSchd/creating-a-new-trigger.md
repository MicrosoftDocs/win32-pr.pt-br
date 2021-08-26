---
title: Criando um novo gatilho
description: Para criar um gatilho, você deve usar três interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0111fe8c45fdac5618407500b2168bf09c4ec01c5d68e78342f14d6bf103ff78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100436"
---
# <a name="creating-a-new-trigger"></a>Criando um novo gatilho

Para criar um gatilho, você deve usar três interfaces. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornece o método [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar o objeto de gatilho, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fornece o método [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para definir os critérios para o gatilho e **a** interface COM [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fornece um método Save para salvar o novo gatilho no disco.

O procedimento a seguir descreve como criar um novo gatilho.

**Para criar um novo gatilho**

1.  Chame [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar a biblioteca COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um Agendador de Tarefas objeto. (Este exemplo presume que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto de tarefa. (Observe que este exemplo obtém a tarefa "Tarefa de Teste".)
3.  Chame [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar um objeto de gatilho. (Observe que [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) é herdado [**de IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Defina uma [**estrutura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Observe que os membros wBeginDay, wBeginMonth e wBeginYear do **TASK \_ TRIGGER** devem ser definidos como um dia, mês e ano válidos, respectivamente.
5.  Chame [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) para definir os critérios de gatilho.
6.  Salve a tarefa com o novo gatilho no disco usando [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface COM padrão com suporte pela interface [**ITask.)**](/windows/desktop/api/Mstask/nn-mstask-itask)
7.  Chame [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar todos os recursos. (Observe que **Release** é um [**método IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Para um exemplo de código de                       | Consulte                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Criando um novo gatilho para uma tarefa existente | [Exemplo de código C/C++: criando um gatilho de tarefa](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 