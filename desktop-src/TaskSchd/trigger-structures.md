---
title: Estruturas de gatilho para Agendador de Tarefas 1,0
description: Agendador de Tarefas 1,0 usa várias estruturas para definir os critérios de um gatilho.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005650"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Estruturas de gatilho para Agendador de Tarefas 1,0

Agendador de Tarefas 1,0 usa várias estruturas para definir os critérios de um gatilho.

> [!Note]  
> Para obter mais informações sobre Agendador de Tarefas gatilhos 2,0, consulte [interfaces de gatilho](trigger-interfaces.md).

 

## <a name="task-scheduler-10-structures"></a>Estruturas Agendador de Tarefas 1,0

A ilustração a seguir mostra a estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Ele tem três membros necessários (**wBeginYear**, **wBeginMonth** e **wBeginDay**) que devem ser definidos ao criar um novo gatilho. (Para ir para a página de referência dessa estrutura, clique no nome da estrutura na ilustração.)

![estrutura do gatilho de tarefa](images/tsktri1.png)

Lembre-se de que o membro **TriggerType** usa a enumeração de [**\_ \_ tipo de gatilho de tarefa**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e o membro de **tipo** usa uma estrutura de **\_ \_ União de gatilho de tarefa** . A enumeração do **\_ \_ tipo de gatilho de tarefa** é usada para especificar o tipo de gatilho (tipos de gatilho baseados em eventos e em tempo). A estrutura de [**\_ \_ União do tipo de gatilho**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) é usada para combinar as estruturas [**diária**](/windows/desktop/api/Mstask/ns-mstask-daily), [**semanal**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (dia do mês) e [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (dia da semana) usadas para especificar quando um gatilho baseado em tempo será acionado.

Se **TriggerType** especificar um gatilho baseado em tempo único ou um gatilho baseado em evento, o membro de **tipo** será ignorado. A estrutura de [**\_ \_ União do tipo de gatilho**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) será usada somente se o membro **TriggerType** especificar um gatilho diário, semanal, dia-de-mês ou dia da semana mensal.

Além disso, a configuração do membro de **tipo** indica qual membro da estrutura [**de \_ \_ União de tipo de gatilho**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) é usado. A ilustração a seguir mostra a relação entre os valores da enumeração de [**\_ \_ tipo de gatilho de tarefa**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e os membros da estrutura de **\_ \_ estrutura do tipo de gatilho** . (Para saltar para as páginas de referência dessas estruturas, clique no nome da estrutura na ilustração.)

![relação entre os valores de enumeração do tipo de gatilho de tarefa e os membros da estrutura de estrutura do tipo de gatilho](images/tsktri3.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gatilhos de tarefa](task-triggers.md)
</dt> <dt>

[Tipos de gatilho](trigger-types.md)
</dt> <dt>

[Interfaces de gatilho](trigger-interfaces.md)
</dt> </dl>

 

 




