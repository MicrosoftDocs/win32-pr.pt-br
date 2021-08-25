---
title: Exemplo de página Recuperar uma Tarefa
description: Para recuperar uma página de tarefas, você deve chamar ITask QueryInterface para recuperar a interface IProvideTaskPage e, em seguida, chamar IProvideTaskPage GetPage. O método GetPage retorna um handle para a página, que pode ser usado para exibir a página solicitada.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- recuperação da página de tarefas Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d619f76b4de416fe2bef9faa679851c613df05e427d6203a6a91936644ad07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872266"
---
# <a name="retrieving-a-task-page-example"></a>Exemplo de página Recuperar uma Tarefa

Para recuperar uma página de tarefas, você deve chamar **ITask::QueryInterface** para recuperar a interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e, em seguida, chamar [**IProvideTaskPage::GetPage.**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) O **método GetPage** retorna um handle para a página, que pode ser usado para exibir a página solicitada.

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são liberadas depois que não são mais necessárias.

 

O procedimento a seguir descreve como criar um novo gatilho.

**Para criar um novo gatilho**

1.  Chame [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar a biblioteca COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um Agendador de Tarefas objeto. (Este exemplo presume que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto de tarefa. (Observe que este exemplo obtém a tarefa "Tarefa de Teste".)
3.  Chame **ITask::QueryInterface** para recuperar a interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) e [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) para recuperar a página.
4.  Usando o alça de página retornado, exibe a página.



| Para um exemplo de código de                                   | Consulte                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Recuperando e exibindo a página Tarefa de uma tarefa conhecida | [Recuperando uma página de tarefa](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 