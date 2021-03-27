---
description: Essa classe é a classe pai para eventos de falha de página. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: Classe PageFault_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967422"
---
# <a name="pagefault_v2-class"></a><span data-ttu-id="7f434-104">\_Classe falhadepágina v2</span><span class="sxs-lookup"><span data-stu-id="7f434-104">PageFault\_V2 class</span></span>

<span data-ttu-id="7f434-105">Essa classe é a classe pai para eventos de falha de página.</span><span class="sxs-lookup"><span data-stu-id="7f434-105">This class is the parent class for page fault events.</span></span>

<span data-ttu-id="7f434-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="7f434-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f434-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f434-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="7f434-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7f434-108">Members</span></span>

<span data-ttu-id="7f434-109">A classe **falhadepágina \_ v2** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="7f434-109">The **PageFault\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f434-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f434-110">Remarks</span></span>

<span data-ttu-id="7f434-111">Para habilitar todos os eventos de falha de página em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ \_ falhas de página do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="7f434-111">To enable all page fault events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="7f434-112">Você também pode especificar os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="7f434-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="7f434-113">**\_falhas de \_ memória do sinalizador de rastreamento de \_ \_ eventos \_**</span><span class="sxs-lookup"><span data-stu-id="7f434-113">**EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS**</span></span>
-   <span data-ttu-id="7f434-114">**\_ \_ alocação virtual do sinalizador de rastreamento de \_ eventos \_**</span><span class="sxs-lookup"><span data-stu-id="7f434-114">**EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC**</span></span>

<span data-ttu-id="7f434-115">Os consumidores de rastreamento de eventos podem implementar processamento especial para todos os eventos de falha de página chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**PageFaultGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="7f434-115">Event trace consumers can implement special processing for all page fault events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PageFaultGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="7f434-116">Use os tipos de evento a seguir para identificar o evento de memória real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="7f434-116">Use the following event types to identify the actual memory event when consuming events.</span></span>



| <span data-ttu-id="7f434-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="7f434-117">Event type</span></span>                                                     | <span data-ttu-id="7f434-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f434-118">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f434-119">\_ \_ Tipo de rastreamento \_ de evento mm \_ vaca (o valor do tipo de evento é 12)</span><span class="sxs-lookup"><span data-stu-id="7f434-119">EVENT\_TRACE\_TYPE\_MM\_COW(Event type value is 12)</span></span><br/> | <span data-ttu-id="7f434-120">Evento de cópia em gravação.</span><span class="sxs-lookup"><span data-stu-id="7f434-120">Copy-on-write event.</span></span> <span data-ttu-id="7f434-121">A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-121">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="7f434-122">Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-122">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>     |
| <span data-ttu-id="7f434-123">\_ \_ Tipo de rastreamento \_ de evento mm \_ DZF (o valor do tipo de evento é 11)</span><span class="sxs-lookup"><span data-stu-id="7f434-123">EVENT\_TRACE\_TYPE\_MM\_DZF(Event type value is 11)</span></span><br/> | <span data-ttu-id="7f434-124">Evento de falha de demanda zero.</span><span class="sxs-lookup"><span data-stu-id="7f434-124">Demand zero fault event.</span></span> <span data-ttu-id="7f434-125">A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-125">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="7f434-126">Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-126">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span> |
| <span data-ttu-id="7f434-127">\_ \_ Tipo de rastreamento \_ de evento mm \_ GPF (o valor do tipo de evento é 13)</span><span class="sxs-lookup"><span data-stu-id="7f434-127">EVENT\_TRACE\_TYPE\_MM\_GPF(Event type value is 13)</span></span><br/> | <span data-ttu-id="7f434-128">Evento de falha de página de proteção.</span><span class="sxs-lookup"><span data-stu-id="7f434-128">Guard page fault event.</span></span> <span data-ttu-id="7f434-129">A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-129">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="7f434-130">Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-130">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="7f434-131">\_ \_ Tipo de rastreamento \_ de evento mm \_ HPF (o valor do tipo de evento é 14)</span><span class="sxs-lookup"><span data-stu-id="7f434-131">EVENT\_TRACE\_TYPE\_MM\_HPF(Event type value is 14)</span></span><br/> | <span data-ttu-id="7f434-132">Evento de falha de página de hardware.</span><span class="sxs-lookup"><span data-stu-id="7f434-132">Hard page fault event.</span></span> <span data-ttu-id="7f434-133">A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-133">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="7f434-134">Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-134">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>   |
| <span data-ttu-id="7f434-135">\_ \_ Tipo de rastreamento \_ de evento mm \_ TF (o valor do tipo de evento é 10)</span><span class="sxs-lookup"><span data-stu-id="7f434-135">EVENT\_TRACE\_TYPE\_MM\_TF(Event type value is 10)</span></span><br/>  | <span data-ttu-id="7f434-136">Evento de falha de transição.</span><span class="sxs-lookup"><span data-stu-id="7f434-136">Transition fault event.</span></span> <span data-ttu-id="7f434-137">A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-137">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="7f434-138">Antes do Windows Vista, a classe [**falhadepágina \_ TransitionFault**](pagefault-transitionfault.md) MOF define o evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-138">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="7f434-139">\_ \_ Tipo de rastreamento \_ de evento mm \_ AV (o valor do tipo de evento é 15)</span><span class="sxs-lookup"><span data-stu-id="7f434-139">EVENT\_TRACE\_TYPE\_MM\_AV(Event type value is 15)</span></span><br/>  | <span data-ttu-id="7f434-140">Evento de violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="7f434-140">Access violation event.</span></span> <span data-ttu-id="7f434-141">A classe [**falhadepágina \_ TypeGroup1**](pagefault-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-141">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                           |
| <span data-ttu-id="7f434-142">Valor do tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="7f434-142">Event type value, 32</span></span>                                           | <span data-ttu-id="7f434-143">Evento de falha de página de hardware. A classe [**falhadepágina \_ HardFault**](pagefault-hardfault.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-143">Hard page fault event.The [**PageFault\_HardFault**](pagefault-hardfault.md) MOF class defines the event data for this event.</span></span>                                                                                                                               |
| <span data-ttu-id="7f434-144">Valor do tipo de evento, 105</span><span class="sxs-lookup"><span data-stu-id="7f434-144">Event type value, 105</span></span>                                          | <span data-ttu-id="7f434-145">Carregamento de imagem no evento de arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="7f434-145">Image load in page file event.</span></span> <span data-ttu-id="7f434-146">A classe [**falhadepágina \_ ImageLoadBacked**](pagefault-imageloadbacked.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-146">The [**PageFault\_ImageLoadBacked**](pagefault-imageloadbacked.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="7f434-147">Valor do tipo de evento, 98</span><span class="sxs-lookup"><span data-stu-id="7f434-147">Event type value, 98</span></span>                                           | <span data-ttu-id="7f434-148">Evento de alocação virtual.</span><span class="sxs-lookup"><span data-stu-id="7f434-148">Virtual allocation event.</span></span> <span data-ttu-id="7f434-149">A classe do [**VirtualAlloc**](pagefault-virtualalloc.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-149">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="7f434-150">Valor do tipo de evento, 99</span><span class="sxs-lookup"><span data-stu-id="7f434-150">Event type value, 99</span></span>                                           | <span data-ttu-id="7f434-151">Evento livre virtual.</span><span class="sxs-lookup"><span data-stu-id="7f434-151">Virtual free event.</span></span> <span data-ttu-id="7f434-152">A classe do [**VirtualAlloc**](pagefault-virtualalloc.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7f434-152">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                      |



 

<span data-ttu-id="7f434-153">Você pode usar os membros **ProcessId** e **ThreadID** do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar o processo ou thread com falha.</span><span class="sxs-lookup"><span data-stu-id="7f434-153">You can use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the faulting process or thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f434-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f434-154">Requirements</span></span>



| <span data-ttu-id="7f434-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f434-155">Requirement</span></span> | <span data-ttu-id="7f434-156">Valor</span><span class="sxs-lookup"><span data-stu-id="7f434-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f434-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f434-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7f434-158">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f434-158">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7f434-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f434-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7f434-160">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f434-160">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
