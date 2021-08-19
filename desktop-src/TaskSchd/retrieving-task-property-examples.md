---
title: Recuperando exemplos de propriedade da tarefa
description: Para recuperar as propriedades de uma tarefa, chame ITaskScheduler Activate para recuperar a interface do objeto de tarefa e, em seguida, chame o método ITask apropriado para recuperar a propriedade da tarefa em que você está interessado.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- recuperando propriedades da tarefa Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e46554c32d9d30941fd837b91e80e8e20d915b0f1c68a665fd72c8f1624c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002384"
---
# <a name="retrieving-task-property-examples"></a>Recuperando exemplos de propriedade da tarefa

Para recuperar as propriedades de uma tarefa, chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar a interface do objeto de tarefa e, em seguida, chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para recuperar a propriedade da tarefa em que você está interessado. Os exemplos de código listados na parte inferior da página mostram como recuperar as diferentes propriedades da tarefa.

Os exemplos de código listados na parte inferior da página mostram como recuperar as propriedades exclusivas dos objetos de tarefa. Para outras [*propriedades de item*](w.md) de trabalho que também se aplicam a tarefas, consulte Recuperando [exemplos de item de trabalho.](retrieving-work-item-property-examples.md)

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são liberadas depois que não são mais necessárias.

 

Observe que, se você estiver recuperando uma propriedade de cadeia de caracteres (como o nome do aplicativo, os parâmetros ou o diretório de trabalho), deverá chamar [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.

O procedimento a seguir descreve como recuperar uma propriedade de tarefa.

**Para recuperar uma propriedade de tarefa**

1.  Chame [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar a biblioteca COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um Agendador de Tarefas objeto. (Esses exemplos pressuem que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto de tarefa. (Observe que este exemplo obtém a tarefa "Tarefa de Teste".)
3.  Chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para recuperar a propriedade em que você está interessado.
4.  Processe a propriedade conforme necessário. (Esses exemplos imprimem a propriedade na tela.)
5.  Se a propriedade retornada for uma cadeia de caracteres, chame [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.



| Para um exemplo de código de                                                                                                                           | Consulte                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Recuperando o nome do aplicativo associado a uma determinada tarefa                                                                             | [Exemplo de código C/C++: recuperando o nome do aplicativo de tarefa](c-c-code-example-retrieving-the-task-application-name.md)   |
| Recuperando o tempo máximo que a tarefa pode executar e exibindo esse número na tela                                                 | [Exemplo de código C/C++: recuperando a tarefa MaxRunTime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Recuperando a cadeia de caracteres de parâmetro executada quando a tarefa é executada e exibindo essa cadeia de caracteres na tela                                  | [Exemplo de código C/C++: Recuperando parâmetros de tarefa](c-c-code-example-retrieving-task-parameters.md)                       |
| Recuperando o nível [*de prioridade*](p.md) da tarefa                                                                    | [Exemplo de código C/C++: Recuperando a prioridade da tarefa](c-c-code-example-retrieving-task-priority.md)                           |
| Recuperando o diretório de [*trabalho de*](w.md) uma tarefa e exibindo o caminho para o diretório de trabalho na tela | [Exemplo de código C/C++: recuperando o diretório de trabalho da tarefa](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 