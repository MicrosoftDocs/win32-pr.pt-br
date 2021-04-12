---
title: Recuperando exemplos de propriedade de tarefa
description: Para recuperar as propriedades de uma tarefa, chame ITaskScheduler Activate para obter a interface do objeto de tarefa e, em seguida, chame o método ITask apropriado para recuperar a propriedade de tarefa em que você está interessado.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- Recuperando propriedades da tarefa Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294364"
---
# <a name="retrieving-task-property-examples"></a>Recuperando exemplos de propriedade de tarefa

Para recuperar as propriedades de uma tarefa, chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface do objeto de tarefa e, em seguida, chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para recuperar a propriedade de tarefa em que você está interessado. Os exemplos de código listados na parte inferior da página mostram como recuperar as diferentes propriedades da tarefa.

Os exemplos de código listados na parte inferior da página mostram como recuperar as propriedades que são exclusivas de objetos de tarefa. Para outras propriedades de [*item de trabalho*](w.md) que também se aplicam a tarefas, consulte [recuperando exemplos de item de trabalho](retrieving-work-item-property-examples.md).

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.

 

Observe que, se você estiver recuperando uma propriedade de cadeia de caracteres (como o nome do aplicativo, os parâmetros ou o diretório de trabalho), deverá chamar [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.

O procedimento a seguir descreve como recuperar uma propriedade de tarefa.

**Para recuperar uma propriedade de tarefa**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para recuperar a propriedade em que você está interessado.
4.  Processe a propriedade conforme necessário. (Esses exemplos imprimem a propriedade na tela.)
5.  Se a propriedade retornada for uma cadeia de caracteres, chame [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.



| Para obter um exemplo de código de                                                                                                                           | Consulte                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Recuperando o nome do aplicativo associado a uma determinada tarefa                                                                             | [Exemplo de código do C/C++: Recuperando o nome do aplicativo da tarefa](c-c-code-example-retrieving-the-task-application-name.md)   |
| Recuperando a quantidade máxima de tempo que a tarefa pode executar e exibindo esse número na tela                                                 | [Exemplo de código C/C++: Recuperando a tarefa MaxRunTime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Recuperando a cadeia de caracteres do parâmetro que é executada quando a tarefa é executada e exibindo essa cadeia de caracteres na tela                                  | [Exemplo de código do C/C++: Recuperando parâmetros da tarefa](c-c-code-example-retrieving-task-parameters.md)                       |
| Recuperando o [*nível de prioridade*](p.md) da tarefa                                                                    | [Exemplo de código do C/C++: Recuperando a prioridade da tarefa](c-c-code-example-retrieving-task-priority.md)                           |
| Recuperando o [*diretório de trabalho*](w.md) de uma tarefa e exibindo o caminho para o diretório de trabalho na tela | [Exemplo de código do C/C++: Recuperando o diretório de trabalho da tarefa](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 