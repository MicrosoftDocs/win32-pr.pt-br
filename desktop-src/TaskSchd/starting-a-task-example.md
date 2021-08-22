---
title: Iniciando um exemplo de tarefa
description: Para iniciar uma tarefa, chame o método Run da interface ITask. Run é um método assíncrono que tenta executar a tarefa e retorna assim que a tarefa é iniciada. O serviço de Agendador de Tarefas deve estar em execução para que esse método tenha sucesso.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4176bf793e72acd3930d6e1e5cbc3d73e91c1d558e342a5a9804aa8f87526cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139329"
---
# <a name="starting-a-task-example"></a>Iniciando um exemplo de tarefa

Para iniciar uma tarefa, chame o método [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) da interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . **Run** é um método assíncrono que tenta executar a tarefa e retorna assim que a tarefa é iniciada. O serviço de Agendador de Tarefas deve estar em execução para que esse método tenha sucesso.

O procedimento a seguir descreve como iniciar uma tarefa.

**Para iniciar uma tarefa**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que este exemplo obtém a tarefa "Test Task".)
3.  Chame [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) para iniciar a tarefa. Observe que esse método é herdado pela interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
4.  Continue o processamento conforme necessário.
5.  Chame **ITask:: Release** para liberar recursos e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) para não inicializar com. Este exemplo chama [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para liberar o ponteiro para a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Observe que **Release** é um método [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) herdado por **ITask**.)



| Para obter um exemplo de código de    | Consulte                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Executando uma tarefa existente | [Exemplo de código C/C++: iniciando uma tarefa](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 