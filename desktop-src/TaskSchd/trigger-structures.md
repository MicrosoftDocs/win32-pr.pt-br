---
title: Estruturas de gatilho Agendador de Tarefas 1.0
description: Agendador de Tarefas 1.0 usa várias estruturas para definir os critérios de um gatilho.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a70688597f7684a6b6a0bedba90cb23d34135cd732aaed37cd74970867b3b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002046"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Estruturas de gatilho Agendador de Tarefas 1.0

Agendador de Tarefas 1.0 usa várias estruturas para definir os critérios de um gatilho.

> [!Note]  
> Para obter mais informações sobre Agendador de Tarefas gatilhos 2.0, consulte [Trigger Interfaces](trigger-interfaces.md).

 

## <a name="task-scheduler-10-structures"></a>Agendador de Tarefas estruturas 1.0

A ilustração a seguir mostra a [**estrutura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Ele tem três membros necessários (**wBeginYear**, **wBeginMonth** e **wBeginDay**) que devem ser definidos ao criar um novo gatilho. (Para ir para a página de referência dessa estrutura, clique no nome da estrutura na ilustração.)

![estrutura de gatilho de tarefa](images/tsktri1.png)

Esteja ciente de que o **membro TriggerType** usa a [**enumeração TASK \_ TRIGGER \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e o membro **Type** usa uma estrutura TASK **TRIGGER \_ \_ UNION.** A **\_ enumeração TASK TRIGGER \_ TYPE** é usada para especificar o tipo de gatilho (tipos de gatilho baseados em tempo e evento). A estrutura [**TRIGGER \_ TYPE \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) é usada para combinar as estruturas [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (dia do mês) e [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (dia da semana) que são usadas para especificar quando um gatilho baseado em tempo será acionado.

Se **TriggerType** especificar um gatilho baseado em tempo único ou um gatilho baseado em evento, o **membro Type** será ignorado. A [**estrutura TRIGGER TYPE \_ \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) será usada somente se o membro **TriggerType** especificar um gatilho diário, semanal, dia do mês ou mensal baseado em hora do dia da semana.

Além disso, a configuração do **membro Type** indica qual membro da estrutura TRIGGER [**TYPE \_ \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) é usado. A ilustração a seguir mostra a relação entre os valores da [**enumeração TASK \_ TRIGGER \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e os membros da estrutura **TRIGGER TYPE \_ \_ STRUCTURE.** (Para ir para as páginas de referência dessas estruturas, clique no nome da estrutura na ilustração.)

![relação entre valores de enumeração de tipo de gatilho de tarefa e membros da estrutura do tipo de gatilho](images/tsktri3.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> <dt>

[Tipos de gatilho](trigger-types.md)
</dt> <dt>

[Interfaces de gatilho](trigger-interfaces.md)
</dt> </dl>

 

 




