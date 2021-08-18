---
title: Criando um exemplo de gatilho ocioso
description: Para criar um gatilho ocioso, você deve especificar um gatilho ocioso ao criar o gatilho e definir o tempo ocioso para a tarefa. Para obter informações sobre condições ociosas, consulte Condições ociosas da tarefa.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac38eb3eb7520fde552f009a718fe188d247e3f9fef943f0f0f79ba6ea85970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139539"
---
# <a name="creating-an-idle-trigger-example"></a>Criando um exemplo de gatilho ocioso

Para criar um gatilho ocioso, você deve especificar um gatilho ocioso ao criar o gatilho e definir o tempo ocioso para a tarefa. Para obter informações sobre condições ociosas, consulte [Condições ociosas da tarefa](task-idle-conditions.md).

Depois de criar o gatilho ocioso, chame [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o novo gatilho no disco.

O procedimento a seguir descreve como criar um gatilho ocioso para uma tarefa conhecida.

**Para criar um gatilho ocioso para uma tarefa conhecida**

1.  Chame [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar a biblioteca COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um Agendador de Tarefas objeto. (Este exemplo presume que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto de tarefa. (Observe que este exemplo obtém a tarefa "Tarefa de Teste".)
3.  Chame [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) para definir por quanto tempo o sistema deve permanecer ocioso antes que o gatilho seja acionado. (Observe que **SetIdleWait** é herdado de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Defina a [**estrutura TASK \_ TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) e chame [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar o gatilho ocioso. (Observe que **CreateTrigger** é herdado [**de IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
5.  Salve a tarefa com o novo gatilho ocioso no disco usando [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface COM padrão com suporte pela interface [**ITask.)**](/windows/desktop/api/Mstask/nn-mstask-itask)
6.  Chame **ITask::Release para** liberar todos os recursos. (Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um [**método IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Para um exemplo de código de                         | Consulte                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Criando um gatilho ocioso para uma tarefa existente | [Exemplo de código C/C++: criando um gatilho ocioso](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 