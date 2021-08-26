---
title: I (Agendador de Tarefas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14bec8dd745aee798ebb6aa9cb296d7a0990b85b44562fb94ea844d2d5d3397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072636"
---
# <a name="i-task-scheduler"></a>I (Agendador de Tarefas)

A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condições ociosas**
</dt> <dd>

Um período em que não há entrada do usuário no computador. As condições ociosas são associadas à hora de início agendada para a tarefa.

Essas condições são definidas chamando [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**gatilhos ociosos**
</dt> <dd>

Um gatilho baseado em evento que é acionado quando o computador fica ocioso por um período específico.

Gatilhos ociosos são criados definindo o membro TASK \_ TRIGGER TYPE da estrutura TASK \_ TRIGGER como [**TASK \_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) EVENT \_ \_ TRIGGER ON \_ \_ IDLE.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tempo de espera ocioso**
</dt> <dd>

O intervalo de tempo (em minutos) usado por um gatilho ocioso ou condição ociosa. Gatilhos ociosos são gatilhos baseados em evento que não estão associados a uma hora agendada. As condições ociosas são associadas à hora de início agendada para a tarefa.

O tempo ocioso é definido por uma chamada para [**IScheduledWorkItem::SetIdleWait.**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait)

</dd> </dl>

 

 




