---
title: Exemplo de recuperação de cadeias de caracteres de gatilho
description: Você pode recuperar as cadeias de caracteres de gatilho de um gatilho conhecido usando a interface IScheduledWorkItem ou ITaskTrigger, dependendo do tipo de objeto com o qual você está trabalhando.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- Recuperando cadeias de caracteres de gatilho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105792606"
---
# <a name="retrieving-trigger-strings-example"></a>Exemplo de recuperação de cadeias de caracteres de gatilho

Você pode recuperar as cadeias de caracteres de gatilho de um gatilho conhecido usando a interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ou [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , dependendo do tipo de objeto com o qual você está trabalhando.

Ao trabalhar com um [*objeto de tarefa*](t.md), use os métodos da interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) para recuperar as cadeias de caracteres de gatilho de um item de trabalho.

Quando você estiver trabalhando com um [*objeto de gatilho de tarefa*](t.md), use os métodos da interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) para recuperar a cadeia de caracteres do gatilho.

O exemplo a seguir mostra como usar [**IScheduledWorkItem:: Gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) para exibir as cadeias de caracteres de todos os gatilhos associados a uma tarefa conhecida.

O procedimento a seguir descreve como recuperar as cadeias de caracteres de gatilho de uma tarefa.

**Para recuperar as cadeias de caracteres de gatilho de uma tarefa**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame **ITask:: GetTriggerCount** para descobrir quantos gatilhos estão associados a uma tarefa. (Observe que [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
4.  Exiba as cadeias de caracteres do gatilho, chamando **ITask:: Gettriggerstring** para cada gatilho associado à tarefa. (Observe que [**Gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) é um método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) herdado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
5.  Libere todos os recursos. Chame [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar as cadeias de caracteres de gatilho e **ITask:: Release** para liberar a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Observe que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por **ITask**.)



| Para obter um exemplo de código de                                                         | Consulte                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Recuperando uma cadeia de caracteres de gatilho para todos os gatilhos associados a uma tarefa conhecida | [Exemplo de código: Recuperando cadeias de caracteres de gatilho](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 