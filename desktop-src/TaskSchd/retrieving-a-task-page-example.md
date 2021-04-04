---
title: Recuperando um exemplo de página de tarefa
description: Para recuperar uma página de tarefas, você deve chamar ITask QueryInterface para recuperar a interface IProvideTaskPage e, em seguida, chamar IProvideTaskPage GetPage. O método GetPage retorna um identificador para a página, que pode ser usado para exibir a página solicitada.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- Recuperando a página de tarefas Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007715"
---
# <a name="retrieving-a-task-page-example"></a>Recuperando um exemplo de página de tarefa

Para recuperar uma página de tarefas, você deve chamar **ITask:: QueryInterface** para recuperar a interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e, em seguida, chamar [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage). O método **GetPage** retorna um identificador para a página, que pode ser usado para exibir a página solicitada.

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.

 

O procedimento a seguir descreve como criar um novo gatilho.

**Para criar um novo gatilho**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame **ITask:: QueryInterface** para recuperar a interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e [**IProvideTaskPage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) para recuperar a página.
4.  Usando o identificador de página retornado, exiba a página.



| Para obter um exemplo de código de                                   | Consulte                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Recuperando e exibindo a página de tarefas de uma tarefa conhecida | [Recuperando uma página de tarefas](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 