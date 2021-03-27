---
description: Essa classe é a classe pai para eventos de contador de desempenho. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Classe PerfInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967439"
---
# <a name="perfinfo-class"></a><span data-ttu-id="6bc8c-104">Classe PerfInfo</span><span class="sxs-lookup"><span data-stu-id="6bc8c-104">PerfInfo class</span></span>

<span data-ttu-id="6bc8c-105">Essa classe é a classe pai para eventos de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-105">This class is the parent class for performance counter events.</span></span>

<span data-ttu-id="6bc8c-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bc8c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bc8c-107">Syntax</span></span>

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="6bc8c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6bc8c-108">Members</span></span>

<span data-ttu-id="6bc8c-109">A classe **PerfInfo** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-109">The **PerfInfo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bc8c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bc8c-110">Remarks</span></span>

<span data-ttu-id="6bc8c-111">Para habilitar eventos de DPC (chamada de procedimento deferida) em uma sessão de log do kernel NT, especifique o sinalizador de DPC do sinalizador de rastreamento de eventos no membro **EnableFlags** de uma [](/windows/win32/api/evntrace/nf-evntrace-starttracea) estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função StartTrace. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6bc8c-111">To enable deferred procedure call (DPC) events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="6bc8c-112">Você também pode especificar um ou mais dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="6bc8c-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="6bc8c-113">**\_interrupção do \_ sinalizador de rastreamento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="6bc8c-113">**EVENT\_TRACE\_FLAG\_INTERRUPT**</span></span>
-   <span data-ttu-id="6bc8c-114">**\_perfil do \_ sinalizador de rastreamento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="6bc8c-114">**EVENT\_TRACE\_FLAG\_PROFILE**</span></span>
-   <span data-ttu-id="6bc8c-115">**sinalizador de rastreamento de eventos \_ \_ \_ SYSTEMCALL**</span><span class="sxs-lookup"><span data-stu-id="6bc8c-115">**EVENT\_TRACE\_FLAG\_SYSTEMCALL**</span></span>

<span data-ttu-id="6bc8c-116">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos DPC chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="6bc8c-116">Event trace consumers can implement special processing for DPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PerfInfoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="6bc8c-117">Use os tipos de evento a seguir para identificar o evento real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-117">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="6bc8c-118">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="6bc8c-118">Event type</span></span>           | <span data-ttu-id="6bc8c-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bc8c-119">Description</span></span>                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc8c-120">Valor do tipo de evento, 46</span><span class="sxs-lookup"><span data-stu-id="6bc8c-120">Event type value, 46</span></span> | <span data-ttu-id="6bc8c-121">Exemplo de evento de perfil.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-121">Sampled profile event.</span></span> <span data-ttu-id="6bc8c-122">A classe MOF [**SampledProfile**](sampledprofile.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-122">The [**SampledProfile**](sampledprofile.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="6bc8c-123">Valor do tipo de evento, 51</span><span class="sxs-lookup"><span data-stu-id="6bc8c-123">Event type value, 51</span></span> | <span data-ttu-id="6bc8c-124">Evento de entrada de chamada do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-124">System call enter event.</span></span> <span data-ttu-id="6bc8c-125">A classe MOF [**SysCallEnter**](syscallenter.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-125">The [**SysCallEnter**](syscallenter.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="6bc8c-126">Valor do tipo de evento, 52</span><span class="sxs-lookup"><span data-stu-id="6bc8c-126">Event type value, 52</span></span> | <span data-ttu-id="6bc8c-127">Evento de saída de chamada do sistema.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-127">System call exit event.</span></span> <span data-ttu-id="6bc8c-128">A classe MOF [**SysCallExit**](syscallexit.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-128">The [**SysCallExit**](syscallexit.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="6bc8c-129">Valor do tipo de evento, 66</span><span class="sxs-lookup"><span data-stu-id="6bc8c-129">Event type value, 66</span></span> | <span data-ttu-id="6bc8c-130">Evento de DPC threaded.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-130">Threaded DPC event.</span></span> <span data-ttu-id="6bc8c-131">A classe do MOF [**DPC**](dpc.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-131">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                          |
| <span data-ttu-id="6bc8c-132">Valor do tipo de evento, 67</span><span class="sxs-lookup"><span data-stu-id="6bc8c-132">Event type value, 67</span></span> | <span data-ttu-id="6bc8c-133">Evento da rotina de serviço de interrupção (ISR).</span><span class="sxs-lookup"><span data-stu-id="6bc8c-133">Interrupt service routine (ISR) event.</span></span> <span data-ttu-id="6bc8c-134">A classe do MOF do [**ISR**](isr.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-134">The [**ISR**](isr.md) MOF class defines the event data for this event.</span></span>       |
| <span data-ttu-id="6bc8c-135">Valor do tipo de evento, 68</span><span class="sxs-lookup"><span data-stu-id="6bc8c-135">Event type value, 68</span></span> | <span data-ttu-id="6bc8c-136">Evento DPC.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-136">DPC event.</span></span> <span data-ttu-id="6bc8c-137">A classe do MOF [**DPC**](dpc.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-137">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="6bc8c-138">Valor do tipo de evento, 69</span><span class="sxs-lookup"><span data-stu-id="6bc8c-138">Event type value, 69</span></span> | <span data-ttu-id="6bc8c-139">Evento de timer de DPC.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-139">DPC timer event.</span></span> <span data-ttu-id="6bc8c-140">A classe do MOF [**DPC**](dpc.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6bc8c-140">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="6bc8c-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bc8c-141">Requirements</span></span>



| <span data-ttu-id="6bc8c-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bc8c-142">Requirement</span></span> | <span data-ttu-id="6bc8c-143">Valor</span><span class="sxs-lookup"><span data-stu-id="6bc8c-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6bc8c-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc8c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6bc8c-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6bc8c-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6bc8c-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc8c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6bc8c-147">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6bc8c-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
