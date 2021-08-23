---
title: Exemplo de recuperação de cadeias de caracteres de gatilho
description: Você pode recuperar as cadeias de caracteres de gatilho de um gatilho conhecido usando a interface IScheduledWorkItem ou ITaskTrigger, dependendo do tipo de objeto com o qual você está trabalhando.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- recuperando cadeias de caracteres de gatilho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a05f95f19aaa68927059c87f7a73f162266454137fbe088923b25dce7ed3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002374"
---
# <a name="retrieving-trigger-strings-example"></a>Exemplo de recuperação de cadeias de caracteres de gatilho

Você pode recuperar as cadeias de caracteres de gatilho de um gatilho conhecido usando a interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ou [**ITaskTrigger,**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) dependendo do tipo de objeto com o qual você está trabalhando.

Ao trabalhar com um [*objeto de*](t.md)tarefa , use os métodos da interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) para recuperar as cadeias de caracteres de gatilho de um item de trabalho.

Quando você estiver trabalhando com um objeto [*de*](t.md)gatilho de tarefa , use os métodos da interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar a cadeia de caracteres de gatilho do gatilho.

O exemplo a seguir mostra como usar [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) para exibir as cadeias de caracteres de todos os gatilhos associados a uma tarefa conhecida.

O procedimento a seguir descreve como recuperar as cadeias de caracteres de gatilho de uma tarefa.

**Para recuperar as cadeias de caracteres de gatilho de uma tarefa**

1.  Chame [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar a biblioteca COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um Agendador de Tarefas objeto. (Este exemplo presume que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto de tarefa. (Observe que este exemplo obtém a tarefa "Tarefa de Teste".)
3.  Chame **ITask::GetTriggerCount** para descobrir quantos gatilhos estão associados a uma tarefa. (Observe que [**GetTriggerCount é**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) [**um método IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado [**por ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
4.  Exibe as cadeias de caracteres de gatilho, chamando **ITask::GetTriggerString para** cada gatilho associado à tarefa. (Observe que [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) é [**um método IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado [**por ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
5.  Libere todos os recursos. Chame [**CoTaskMemFree para**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) liberar as cadeias de caracteres de gatilho e **ITask::Release** para liberar a interface [**ITask.**](/windows/desktop/api/Mstask/nn-mstask-itask) (Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um [**método IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por **ITask**.)



| Para um exemplo de código de                                                         | Consulte                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Recuperando uma cadeia de caracteres de gatilho para todos os gatilhos associados a uma tarefa conhecida | [Exemplo de código: recuperando cadeias de caracteres de gatilho](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 