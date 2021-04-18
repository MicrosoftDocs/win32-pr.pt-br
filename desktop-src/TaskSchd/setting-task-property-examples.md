---
title: Definindo exemplos de propriedade de tarefa
description: Para definir as propriedades de uma tarefa, chame ITaskScheduler Activate para recuperar a interface do objeto Task e, em seguida, chame o método ITask apropriado para definir a Propriedade Task na qual você está interessado.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- definindo as propriedades da tarefa Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105792604"
---
# <a name="setting-task-property-examples"></a>Definindo exemplos de propriedade de tarefa

Para definir as propriedades de uma tarefa, chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar a interface do objeto de tarefa e, em seguida, chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para definir a propriedade de tarefa em que você está interessado.

Os exemplos de código listados na parte inferior da página mostram como definir as propriedades que são exclusivas de objetos de tarefa. Para outras propriedades de [*item de trabalho*](w.md) que também se aplicam a tarefas, consulte [definindo exemplos de propriedade de item de trabalho](setting-work-item-property-examples.md).

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são lançadas depois que elas não são mais necessárias.

 

Nos exemplos a seguir, o objeto de tarefa modificado sempre é salvo em disco por uma chamada para [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface com padrão herdada pelo objeto Task.)

O procedimento a seguir descreve como definir uma propriedade de tarefa.

**Para definir uma propriedade de tarefa**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para definir a propriedade em que você está interessado.
4.  Chame [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) para armazenar o objeto de tarefa modificado em disco.



| Para obter um exemplo de código de                                                                                                                                | Consulte                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Definindo o nome do aplicativo associado a uma tarefa conhecida                                                                                     | [Exemplo de código C/C++: definindo o nome do aplicativo](c-c-code-example-setting-application-name.md)   |
| Definindo o tempo de execução máximo de uma tarefa conhecida                                                                                                         | [Exemplo de código C/C++: Configurando MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| Limpando todos os parâmetros de linha de comando associados a uma tarefa conhecida                                                                                    | [Exemplo de código C/C++: definindo parâmetros de tarefa](c-c-code-example-setting-task-parameters.md)     |
| Este exemplo define a prioridade de uma tarefa de teste e salva a tarefa. Este exemplo pressupõe que a tarefa de teste já existe no computador local. | [Exemplo de código C/C++: definindo a prioridade da tarefa](c-c-code-example-setting-task-priority.md)         |
| Definindo o [*diretório de trabalho*](w.md) de uma tarefa conhecida                                                                  | [Exemplo de código C/C++: definindo diretório de trabalho](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 