---
description: Essa classe de tipo de evento é usada para indicar que os eventos foram perdidos em uma sessão em tempo real. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: Classe RT_LostEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501766"
---
# <a name="rt_lostevent-class"></a><span data-ttu-id="f6b33-104">\_Classe RT LostEvent</span><span class="sxs-lookup"><span data-stu-id="f6b33-104">RT\_LostEvent class</span></span>

<span data-ttu-id="f6b33-105">Essa classe de tipo de evento é usada para indicar que os eventos foram perdidos em uma sessão em tempo real.</span><span class="sxs-lookup"><span data-stu-id="f6b33-105">This event type class is used to indicate that events were lost in a real-time session.</span></span>

<span data-ttu-id="f6b33-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="f6b33-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b33-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6b33-107">Syntax</span></span>

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a><span data-ttu-id="f6b33-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f6b33-108">Members</span></span>

<span data-ttu-id="f6b33-109">A classe **RT \_ LostEvent** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="f6b33-109">The **RT\_LostEvent** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6b33-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6b33-110">Remarks</span></span>

<span data-ttu-id="f6b33-111">O tipo de evento RTLostEvent indica que um ou mais eventos foram perdidos.</span><span class="sxs-lookup"><span data-stu-id="f6b33-111">The RTLostEvent event type indicates that one or more events were lost.</span></span> <span data-ttu-id="f6b33-112">O tipo de evento RTLostBuffer indica que um ou mais buffers foram perdidos.</span><span class="sxs-lookup"><span data-stu-id="f6b33-112">The RTLostBuffer event type indicates that one or more buffers were lost.</span></span> <span data-ttu-id="f6b33-113">Os tipos de evento RTLostEvent e RTLostBuffer são entregues antes de processar eventos do buffer.</span><span class="sxs-lookup"><span data-stu-id="f6b33-113">The RTLostEvent and RTLostBuffer event types are delivered before processing events from the buffer.</span></span>

<span data-ttu-id="f6b33-114">O RTLostFile indica que o arquivo de backup usado pelo autologger para capturar eventos foi perdido.</span><span class="sxs-lookup"><span data-stu-id="f6b33-114">The RTLostFile indicates that the backing file used by the AutoLogger to capture events was lost.</span></span>

<span data-ttu-id="f6b33-115">Os eventos perder dependem da frequência com que os eventos são registrados e de quanto tempo o consumidor gasta processando os eventos.</span><span class="sxs-lookup"><span data-stu-id="f6b33-115">Loosing events depends on the frequency with which the events are logged and how much time the consumer spends processing the events.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b33-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6b33-116">Requirements</span></span>



| <span data-ttu-id="f6b33-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b33-117">Requirement</span></span> | <span data-ttu-id="f6b33-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f6b33-118">Value</span></span> |
|-------------------------------------|------------------------------------------------|
| <span data-ttu-id="f6b33-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6b33-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b33-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6b33-120">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f6b33-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6b33-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b33-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f6b33-122">None supported</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="f6b33-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6b33-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b33-124">**\_Evento perdido**</span><span class="sxs-lookup"><span data-stu-id="f6b33-124">**Lost\_Event**</span></span>](lost-event.md)
</dt> </dl>

 

 




