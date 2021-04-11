---
title: Criando um exemplo de gatilho de ociosidade
description: Para criar um gatilho ocioso, você deve especificar um gatilho ocioso ao criar o gatilho e deve definir o tempo ocioso para a tarefa. Para obter informações sobre condições ociosas, consulte condições de ociosidade da tarefa.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294323"
---
# <a name="creating-an-idle-trigger-example"></a>Criando um exemplo de gatilho de ociosidade

Para criar um gatilho ocioso, você deve especificar um gatilho ocioso ao criar o gatilho e deve definir o tempo ocioso para a tarefa. Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).

Depois de criar o gatilho de ociosidade, chame [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para salvar o novo gatilho em disco.

O procedimento a seguir descreve como criar um gatilho ocioso para uma tarefa conhecida.

**Para criar um gatilho ocioso para uma tarefa conhecida**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) para definir por quanto tempo o sistema deve permanecer ocioso antes que o gatilho seja acionado. (Observe que **SetIdleWait** é herdado de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Defina a estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) e chame [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) para criar o gatilho ocioso. (Observe que **CreateTrigger** é herdado de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
5.  Salve a tarefa com o novo gatilho de ociosidade em disco usando [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão com suporte da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
6.  Chame **ITask:: Release** para liberar todos os recursos. (Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Para obter um exemplo de código de                         | Consulte                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Criando um gatilho ocioso para uma tarefa existente | [Exemplo de código C/C++: Criando um gatilho ocioso](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 