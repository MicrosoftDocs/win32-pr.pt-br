---
description: Você pode usar o modelo padrão de eventos intrínsecos e filtros de eventos em combinação com as \_ classes Win32 localtime ou Win32 \_ UTCTime para receber uma notificação cronometrada.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Criando um evento de temporizador com Win32_LocalTime ou Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171451"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a><span data-ttu-id="aa76f-103">Criando um evento de temporizador com Win32 \_ localtime ou Win32 \_ UTCTime</span><span class="sxs-lookup"><span data-stu-id="aa76f-103">Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime</span></span>

<span data-ttu-id="aa76f-104">Você pode usar o modelo padrão de eventos intrínsecos e filtros de eventos em combinação com as classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) para receber uma notificação cronometrada.</span><span class="sxs-lookup"><span data-stu-id="aa76f-104">You can use the standard model of intrinsic events and event filters in combination with the [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes to receive a timed notification.</span></span> <span data-ttu-id="aa76f-105">O método intrínseco é uma maneira recomendada de gerar eventos cronometrados, pois é consistente com o restante do modelo de evento da Microsoft e dá suporte a condições de agendamento complexas.</span><span class="sxs-lookup"><span data-stu-id="aa76f-105">The intrinsic method is a recommended way of generating timed events, as it is consistent with the rest of the Microsoft event model and supports complex scheduling conditions.</span></span>

<span data-ttu-id="aa76f-106">As classes [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) e [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) são classes singleton no namespace raiz \\ cimv2 que representam o relógio do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa76f-106">The [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) and [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes are singleton classes in the root\\cimv2 namespace that represent the system clock.</span></span> <span data-ttu-id="aa76f-107">Quando consultado, o **Win32 \_ localtime** retorna a hora atual no momento da recuperação de dados em um relógio de 24 horas com referência local.</span><span class="sxs-lookup"><span data-stu-id="aa76f-107">When queried, **Win32\_LocalTime** returns the current time at the moment of data retrieval in a 24-hour clock with local reference.</span></span> <span data-ttu-id="aa76f-108">A classe **Win32 \_ UTCTime** retorna a hora atual com referência UTC.</span><span class="sxs-lookup"><span data-stu-id="aa76f-108">The **Win32\_UTCTime** class returns the current time with UTC reference.</span></span>

<span data-ttu-id="aa76f-109">**Para gerar eventos cronometrados ou repetidos com Win32 \_ localtime ou Win32 \_ UTCTime**</span><span class="sxs-lookup"><span data-stu-id="aa76f-109">**To generate timed or repeating events with Win32\_LocalTime or Win32\_UTCTime**</span></span>

-   <span data-ttu-id="aa76f-110">Configure um filtro de eventos de notificação intrínseco para [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) ou [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que solicita a notificação para uma data e hora específicas.</span><span class="sxs-lookup"><span data-stu-id="aa76f-110">Set up an intrinsic notification event filter for [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) that requests notification for a specific date and time.</span></span>

<span data-ttu-id="aa76f-111">Por exemplo, se a hora local em horário de verão é de 4 horas</span><span class="sxs-lookup"><span data-stu-id="aa76f-111">For example, if the local time under Daylight Savings Time is 4 P.M.</span></span> <span data-ttu-id="aa76f-112">e o local é GMT-8, o [**Win32 \_ localtime. hora**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) retorna 16 e o [**Win32 \_ UTCTime. Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) retorna 23.</span><span class="sxs-lookup"><span data-stu-id="aa76f-112">and the location is GMT -8, then [**Win32\_LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) returns 16 and [**Win32\_UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) returns 23.</span></span>

<span data-ttu-id="aa76f-113">O exemplo de código a seguir descreve como criar um filtro de eventos que sinaliza um evento repetido todos os dias à meia-noite.</span><span class="sxs-lookup"><span data-stu-id="aa76f-113">The following code example describes how to create an event filter that signals a repeating event every day at midnight.</span></span>

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
