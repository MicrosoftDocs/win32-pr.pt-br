---
title: Recuperando exemplos de propriedade de item de trabalho
description: Para recuperar as propriedades de um item de trabalho, chame ITaskScheduler Activate para recuperar a interface do objeto de item de trabalho e, em seguida, chame o método apropriado para recuperar a propriedade de tarefa em que você está interessado.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- Recuperando propriedades do item de trabalho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3519f3f995e4a5c49a58f0c8be590b34a82381bfd534b61bac6ff8aba05de33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059974"
---
# <a name="retrieving-work-item-property-examples"></a>Recuperando exemplos de propriedade de item de trabalho

Para recuperar as propriedades de um item de trabalho, chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar a interface do objeto de item de trabalho e, em seguida, chame o método apropriado para recuperar a propriedade de tarefa em que você está interessado. Atualmente, os únicos itens de trabalho válidos são tarefas.

Os exemplos de código listados na parte inferior desta página mostram como recuperar as propriedades que se aplicam a todos os itens de trabalho. Para outras propriedades que são exclusivas de tarefas, consulte [definindo exemplos de propriedade de tarefa](setting-task-property-examples.md).

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.

 

Observe que, se você estiver recuperando uma propriedade de cadeia de caracteres (como comentário para um item de trabalho), deverá chamar [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.

O procedimento a seguir descreve como recuperar uma propriedade de tarefa.

**Para recuperar uma propriedade de tarefa**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que as tarefas são atualmente o único tipo válido de item de trabalho.)
3.  Chame o método apropriado para recuperar a propriedade em que você está interessado.
4.  Processe a propriedade conforme necessário. (Esses exemplos simplesmente imprimem a propriedade na tela.)
5.  Se a propriedade retornada for uma cadeia de caracteres, chame [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória alocada para a cadeia de caracteres retornada.



| Para obter um exemplo de código de                                                                        | Consulte                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Recuperando as informações da conta de uma tarefa conhecida                                           | [Exemplo de código do C/C++: Recuperando Informações da conta da tarefa](c-c-code-example-retrieving-task-account-information.md)       |
| Recuperando a cadeia de caracteres de comentário de uma tarefa conhecida                                                | [Exemplo de código C/C++: Recuperando um comentário de tarefa](c-c-code-example-retrieving-a-task-comment.md)                           |
| Recuperando o nome do criador da tarefa e exibindo-o na tela               | [Exemplo de código do C/C++: Recuperando o criador da tarefa](c-c-code-example-retrieving-the-task-creator.md)                       |
| Recuperando o último código de saída retornado por uma tarefa conhecida                                       | [Exemplo de código do C/C++: Recuperando o código de saída da tarefa](c-c-code-example-retrieving-task-exit-code.md)                           |
| Recuperando o tempo ocioso de espera da tarefa e exibindo-o na tela                    | [Exemplo de código do C/C++: Recuperando a tarefa ocioso – tempo de espera](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Recuperando a hora em que a tarefa foi executada pela última vez e exibindo-a na tela                    | [Exemplo de código C/C++: Recuperando o tempo de MostRecentRun da tarefa](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Recuperando a próxima vez que a tarefa estiver agendada para ser executada e exibir essa hora na tela | [Exemplo de código C/C++: Recuperando o tempo de NextRun da tarefa](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Recuperar os tempos de execução da tarefa e exibi-los na tela                       | [Exemplo de código do C/C++: Recuperando tempos de execução da tarefa](c-c-code-example-retrieving-task-run-times.md)                           |
| Recuperando o status atual da tarefa e exibindo-o na tela                    | [Exemplo de código do C/C++: Recuperando o status da tarefa](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 