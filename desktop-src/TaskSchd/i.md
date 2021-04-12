---
title: I (Agendador de Tarefas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499201"
---
# <a name="i-task-scheduler"></a>I (Agendador de Tarefas)

A B C D [E](e.md) F G H i J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condições ociosas**
</dt> <dd>

Um período de tempo no qual não há nenhuma entrada do usuário no computador. As condições ociosas são associadas à hora de início agendada para a tarefa.

Essas condições são definidas chamando [**IScheduledWorkItem:: SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**gatilhos ociosos**
</dt> <dd>

Um gatilho baseado em evento que é acionado quando o computador fica ocioso por um período de tempo específico.

Gatilhos ociosos são criados definindo o \_ \_ membro de tipo de gatilho de tarefa da estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) para o \_ gatilho de evento de tarefa \_ \_ em \_ ociosidade.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tempo de espera ocioso**
</dt> <dd>

O intervalo de tempo (em minutos) usado por um gatilho ocioso ou uma condição ociosa. Os gatilhos ociosos são gatilhos baseados em eventos que não estão associados a um horário agendado. As condições ociosas são associadas à hora de início agendada para a tarefa.

O tempo ocioso é definido por uma chamada para [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).

</dd> </dl>

 

 




