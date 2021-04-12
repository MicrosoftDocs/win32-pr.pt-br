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
# <a name="i-task-scheduler"></a><span data-ttu-id="bb23c-103">I (Agendador de Tarefas)</span><span class="sxs-lookup"><span data-stu-id="bb23c-103">I (Task Scheduler)</span></span>

<span data-ttu-id="bb23c-104">A B C D [E](e.md) F G H i J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="bb23c-104">A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bb23c-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condições ociosas**</span><span class="sxs-lookup"><span data-stu-id="bb23c-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**idle conditions**</span></span>
</dt> <dd>

<span data-ttu-id="bb23c-106">Um período de tempo no qual não há nenhuma entrada do usuário no computador.</span><span class="sxs-lookup"><span data-stu-id="bb23c-106">A period of time in which there is no user input on the computer.</span></span> <span data-ttu-id="bb23c-107">As condições ociosas são associadas à hora de início agendada para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="bb23c-107">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="bb23c-108">Essas condições são definidas chamando [**IScheduledWorkItem:: SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span><span class="sxs-lookup"><span data-stu-id="bb23c-108">These conditions are set by calling [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span></span>

</dd> <dt>

<span data-ttu-id="bb23c-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**gatilhos ociosos**</span><span class="sxs-lookup"><span data-stu-id="bb23c-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**idle triggers**</span></span>
</dt> <dd>

<span data-ttu-id="bb23c-110">Um gatilho baseado em evento que é acionado quando o computador fica ocioso por um período de tempo específico.</span><span class="sxs-lookup"><span data-stu-id="bb23c-110">An event-based trigger that is fired when the computer becomes idle for a specific amount of time.</span></span>

<span data-ttu-id="bb23c-111">Gatilhos ociosos são criados definindo o \_ \_ membro de tipo de gatilho de tarefa da estrutura do [**\_ gatilho de tarefa**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) para o \_ gatilho de evento de tarefa \_ \_ em \_ ociosidade.</span><span class="sxs-lookup"><span data-stu-id="bb23c-111">Idle triggers are created by setting the TASK\_TRIGGER\_TYPE member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure to TASK\_EVENT\_TRIGGER\_ON\_IDLE.</span></span>

</dd> <dt>

<span data-ttu-id="bb23c-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tempo de espera ocioso**</span><span class="sxs-lookup"><span data-stu-id="bb23c-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**idle wait time**</span></span>
</dt> <dd>

<span data-ttu-id="bb23c-113">O intervalo de tempo (em minutos) usado por um gatilho ocioso ou uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="bb23c-113">The time interval (in minutes) used by an idle trigger or idle condition.</span></span> <span data-ttu-id="bb23c-114">Os gatilhos ociosos são gatilhos baseados em eventos que não estão associados a um horário agendado.</span><span class="sxs-lookup"><span data-stu-id="bb23c-114">Idle triggers are event-based triggers that are not associated with a scheduled time.</span></span> <span data-ttu-id="bb23c-115">As condições ociosas são associadas à hora de início agendada para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="bb23c-115">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="bb23c-116">O tempo ocioso é definido por uma chamada para [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span><span class="sxs-lookup"><span data-stu-id="bb23c-116">The idle time is set by a call to [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span></span>

</dd> </dl>

 

 




