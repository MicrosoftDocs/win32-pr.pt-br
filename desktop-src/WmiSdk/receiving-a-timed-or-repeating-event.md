---
description: Um evento cronometrado ou repetitivo é um evento que ocorre em uma data e hora específicas, ou repetidamente em intervalos regulares. Por exemplo, um evento pode ocorrer à meia-noite em apenas 2 de dezembro de 2015, ou uma vez por semana às terças-feiras às 2:31 PM.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Recebendo um evento cronometrado ou repetido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165220"
---
# <a name="receiving-a-timed-or-repeating-event"></a><span data-ttu-id="d485e-104">Recebendo um evento cronometrado ou repetido</span><span class="sxs-lookup"><span data-stu-id="d485e-104">Receiving a Timed or Repeating Event</span></span>

<span data-ttu-id="d485e-105">Um evento cronometrado ou repetitivo é um evento que ocorre em uma data e hora específicas, ou repetidamente em intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="d485e-105">A timed or repeating event is an event that occurs at one specific time and date, or repeatedly at regular intervals.</span></span> <span data-ttu-id="d485e-106">Por exemplo, um evento pode ocorrer à meia-noite em apenas 2 de dezembro de 2015, ou uma vez por semana às terças-feiras às 2:31 PM.</span><span class="sxs-lookup"><span data-stu-id="d485e-106">For example, an event can occur at midnight on only December 2, 2015, or one time each week on Tuesdays at 2:31 PM.</span></span>

<span data-ttu-id="d485e-107">A tabela a seguir lista as diferentes classes que são usadas para criar um evento cronometrado ou repetido.</span><span class="sxs-lookup"><span data-stu-id="d485e-107">The following table lists the different classes that are used to create a timed or repeating event.</span></span>



| <span data-ttu-id="d485e-108">Classe</span><span class="sxs-lookup"><span data-stu-id="d485e-108">Class</span></span>                                                                                            | <span data-ttu-id="d485e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d485e-109">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d485e-110">[**Win32 \_ Localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [ **\_ UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span><span class="sxs-lookup"><span data-stu-id="d485e-110">[**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span></span> | <span data-ttu-id="d485e-111">Modelo de evento padrão da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d485e-111">Standard Microsoft event model.</span></span><br/> <span data-ttu-id="d485e-112">Para obter mais informações, consulte [criando um evento de timer com Win32 \_ localtime ou Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="d485e-112">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span><br/> |
| [<span data-ttu-id="d485e-113">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="d485e-113">**\_\_TimerInstruction**</span></span>](--timerinstruction.md)                                               | <span data-ttu-id="d485e-114">Técnica herdada.</span><span class="sxs-lookup"><span data-stu-id="d485e-114">Legacy technique.</span></span><br/> <span data-ttu-id="d485e-115">Para obter mais informações, consulte [criando um evento de timer com \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="d485e-115">For more information, see [Creating a Timer Event with \_TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span></span><br/>                                             |



 

<span data-ttu-id="d485e-116">Se você quiser agendar uma tarefa ou trabalho para ocorrer em um momento específico ou repetidamente, use a classe [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) e seus métodos.</span><span class="sxs-lookup"><span data-stu-id="d485e-116">If you want to schedule a task or job to occur at a specific time or repeatedly, use the [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) class and its methods.</span></span> <span data-ttu-id="d485e-117">Essa classe representa um trabalho criado com o comando AT em uma janela de comando de **Iniciar** e **executar**, ou das **tarefas agendadas** no **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="d485e-117">This class represents a job created with the AT command in a command window from **Start** and then **Run**, or from the **Scheduled Tasks** in **Control Panel**.</span></span>

 

