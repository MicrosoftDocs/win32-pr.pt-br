---
title: Definindo exemplos de propriedade de item de trabalho
description: Para definir as propriedades de um item de trabalho, chame ITaskScheduler Activate para recuperar a interface do objeto de item de trabalho e, em seguida, chame o método apropriado para definir a propriedade de tarefa em que você está interessado. Atualmente, os únicos itens de trabalho válidos são tarefas.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- definindo propriedades do item de trabalho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917519"
---
# <a name="setting-work-item-property-examples"></a>Definindo exemplos de propriedade de item de trabalho

Para definir as propriedades de um item de trabalho, chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar a interface do objeto de item de trabalho e, em seguida, chame o método apropriado para definir a propriedade de tarefa em que você está interessado. Atualmente, os únicos itens de trabalho válidos são tarefas.

Os exemplos de código listados na parte inferior da página mostram como definir as propriedades que se aplicam a todos os itens de trabalho. Para outras propriedades que são exclusivas de tarefas, consulte [definindo exemplos de propriedade de tarefa](setting-task-property-examples.md).

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.

 

Nos exemplos a seguir, o objeto modificado é sempre salvo em disco por uma chamada para [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão herdada pelo objeto Task.)

O procedimento a seguir descreve como definir uma propriedade de tarefa.

**Para definir uma propriedade de tarefa**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que as tarefas são atualmente o único tipo válido de item de trabalho.)
3.  Chame o método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) apropriado para definir a propriedade em que você está interessado. Observe que os métodos **IScheduledWorkItem** são herdados pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
4.  Chame [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para armazenar o objeto de tarefa modificado em disco.



| Para obter um exemplo de código de                            | Consulte                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Definindo as informações da conta para uma tarefa conhecida | [Exemplo de código C/C++: definindo informações da conta da tarefa](c-c-code-example-setting-task-account-information.md) |
| Definindo o comentário de uma tarefa conhecida              | [Exemplo de código C/C++: definindo o comentário da tarefa](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 