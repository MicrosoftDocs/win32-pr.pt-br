---
title: Editando um item de trabalho usando páginas de propriedades
description: Você pode editar as propriedades de um item de trabalho usando a interface gráfica do usuário fornecida pelo serviço Agendador de Tarefas.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- editando itens de trabalho Agendador de Tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0121a9e3100922ecdd1d529aa81b498d377724959abb5c3380337df82817e338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100426"
---
# <a name="editing-a-work-item-using-property-pages"></a>Editando um item de trabalho usando páginas de propriedades

Você pode editar as propriedades de um item de trabalho usando a interface gráfica do usuário fornecida pelo serviço Agendador de Tarefas. (Atualmente, os únicos itens de trabalho válidos são tarefas.)

O procedimento a seguir descreve como editar uma tarefa usando suas páginas de propriedades.

**Para editar uma tarefa usando suas páginas de propriedades**

1.  Chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um objeto Agendador de tarefas. (Esses exemplos pressupõem que o serviço Agendador de Tarefas está em execução.)
2.  Chame [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obter a interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) do objeto Task. (Observe que as tarefas são atualmente o único tipo válido de item de trabalho.)
3.  Chame [**IScheduledWorkItem:: EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) para exibir as páginas de propriedades da tarefa.
4.  Edite as propriedades da tarefa conforme necessário e clique em OK para aceitar os novos valores e remover as páginas de propriedades exibidas.



| Para obter um exemplo de código de                                                                                      | Consulte                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Exibindo as páginas de propriedades de uma tarefa conhecida e permitindo que um usuário edite as propriedades do item de trabalho | [Exemplo de código do C/C++: editando um item de trabalho](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Agendador de Tarefas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 