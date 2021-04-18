---
title: Exemplo de enumeração de tarefas
description: Para enumerar tarefas, você deve chamar ITaskScheduler enum para criar um objeto de enumeração. Em seguida, use a interface IEnumWorkItems do objeto de enumeração para enumerar as tarefas na pasta tarefas agendadas.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105764752"
---
# <a name="enumerating-tasks-example"></a>Exemplo de enumeração de tarefas

Para enumerar tarefas, você deve chamar [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para criar um [*objeto de enumeração*](e.md). Em seguida, use a interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) do objeto de enumeração para enumerar as tarefas na pasta tarefas agendadas.

O procedimento a seguir descreve como enumerar as tarefas na pasta tarefas agendadas.

**Para enumerar as tarefas na pasta tarefas agendadas**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Este exemplo pressupõe que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) para obter um objeto de enumeração.
3.  Chame [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) para recuperar as tarefas. (Este exemplo tenta recuperar cinco tarefas com cada chamada.)
4.  Processe as tarefas retornadas. (Este exemplo simplesmente imprime o nome de cada tarefa na tela.
5.  Liberar recursos. Chame [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória usada para nomes.



| Para obter um exemplo de código de                                                         | Consulte                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Enumerando todas as tarefas na pasta tarefas agendadas do computador local | [Exemplo de código C/C++: enumerando tarefas](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 