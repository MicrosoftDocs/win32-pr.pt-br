---
title: Definindo exemplos de propriedade da tarefa
description: Para definir as propriedades de uma tarefa, chame ITaskScheduler Activate para recuperar a interface do objeto de tarefa e, em seguida, chame o método ITask apropriado para definir a propriedade da tarefa em que você está interessado.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- definindo propriedades da tarefa Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deac57ac28a16108eb886cc56cf697cd768ca7d2e351c4517728c2972be8582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681626"
---
# <a name="setting-task-property-examples"></a>Definindo exemplos de propriedade da tarefa

Para definir as propriedades de uma tarefa, chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para recuperar a interface do objeto de tarefa e, em seguida, chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para definir a propriedade da tarefa em que você está interessado.

Os exemplos de código listados na parte inferior da página mostram como definir as propriedades exclusivas para objetos de tarefa. Para outras [*propriedades de item de*](w.md) trabalho que também se aplicam a tarefas, consulte [Definindo exemplos](setting-work-item-property-examples.md)de propriedade de item de trabalho .

> [!Note]  
> No exemplo de código a seguir, todas as interfaces são liberadas depois que não são mais necessárias.

 

Nos exemplos a seguir, o objeto de tarefa modificado sempre é salvo em disco por uma chamada para [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) é uma interface COM padrão herdada pelo objeto de tarefa.)

O procedimento a seguir descreve como definir uma propriedade de tarefa.

**Para definir uma propriedade de tarefa**

1.  Chame [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar a biblioteca COM e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um Agendador de Tarefas objeto. (Esses exemplos pressuem que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto de tarefa. (Observe que este exemplo obtém a tarefa "Tarefa de Teste".)
3.  Chame o método [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) apropriado para definir a propriedade em que você está interessado.
4.  Chame [**IPersistFile::Save para**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) armazenar o objeto de tarefa modificado no disco.



| Para um exemplo de código de                                                                                                                                | Consulte                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Definindo o nome do aplicativo associado a uma tarefa conhecida                                                                                     | [Exemplo de código C/C++: definindo o nome do aplicativo](c-c-code-example-setting-application-name.md)   |
| Definindo o tempo de duração máximo de uma tarefa conhecida                                                                                                         | [Exemplo de código C/C++: Definindo MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| Limpar todos os parâmetros de linha de comando associados a uma tarefa conhecida                                                                                    | [Exemplo de código C/C++: definindo parâmetros de tarefa](c-c-code-example-setting-task-parameters.md)     |
| Este exemplo define a prioridade de uma tarefa de teste e salva a tarefa. Este exemplo pressu que a tarefa de teste já existe no computador local. | [Exemplo de código C/C++: definindo a prioridade da tarefa](c-c-code-example-setting-task-priority.md)         |
| Definindo [*o diretório de trabalho*](w.md) de uma tarefa conhecida                                                                  | [Exemplo de código C/C++: Definindo o diretório de trabalho](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Agendador de Tarefas exemplos 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 