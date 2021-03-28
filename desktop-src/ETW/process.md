---
description: Essa classe é a classe pai para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Classe Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: b014262044db9e227bec5af2b351d1392c243c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968110"
---
# <a name="process-class"></a><span data-ttu-id="11c00-104">Classe Process</span><span class="sxs-lookup"><span data-stu-id="11c00-104">Process class</span></span>

<span data-ttu-id="11c00-105">Essa classe é a classe pai para eventos de processo.</span><span class="sxs-lookup"><span data-stu-id="11c00-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="11c00-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="11c00-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c00-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11c00-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="11c00-108">Membros</span><span class="sxs-lookup"><span data-stu-id="11c00-108">Members</span></span>

<span data-ttu-id="11c00-109">A classe **process** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="11c00-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="11c00-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="11c00-110">Remarks</span></span>

<span data-ttu-id="11c00-111">Para habilitar eventos de processo em uma sessão de log do kernel NT, especifique o sinalizador de **processo do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="11c00-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="11c00-112">Você também pode especificar o seguinte sinalizador:</span><span class="sxs-lookup"><span data-stu-id="11c00-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="11c00-113">**\_contadores de \_ processo de sinalizador de rastreamento de eventos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="11c00-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="11c00-114">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de processo chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="11c00-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="11c00-115">Use os tipos de evento a seguir para identificar o evento de processo real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="11c00-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="11c00-116">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="11c00-116">Event type</span></span>                                                      | <span data-ttu-id="11c00-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="11c00-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c00-118">**Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)</span><span class="sxs-lookup"><span data-stu-id="11c00-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="11c00-119">Encerrar o evento de processo.</span><span class="sxs-lookup"><span data-stu-id="11c00-119">End process event.</span></span> <span data-ttu-id="11c00-120">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="11c00-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="11c00-121">**Evento \_ de \_ \_ Início do tipo de rastreamento**(o valor do tipo de evento é 1)</span><span class="sxs-lookup"><span data-stu-id="11c00-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="11c00-122">Iniciar o evento de processo.</span><span class="sxs-lookup"><span data-stu-id="11c00-122">Start process event.</span></span> <span data-ttu-id="11c00-123">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="11c00-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="11c00-124">Valor do tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="11c00-124">Event type value, 3</span></span>                                             | <span data-ttu-id="11c00-125">Iniciar evento de processo de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="11c00-125">Start data collection process event.</span></span> <span data-ttu-id="11c00-126">Enumera os processos que estão sendo executados no momento em que a sessão do kernel é iniciada.</span><span class="sxs-lookup"><span data-stu-id="11c00-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="11c00-127">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="11c00-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="11c00-128">Valor do tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="11c00-128">Event type value, 4</span></span>                                             | <span data-ttu-id="11c00-129">Evento de processo de coleta de dados final.</span><span class="sxs-lookup"><span data-stu-id="11c00-129">End data collection process event.</span></span> <span data-ttu-id="11c00-130">Enumera os processos que estão sendo executados no momento em que a sessão do kernel termina.</span><span class="sxs-lookup"><span data-stu-id="11c00-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="11c00-131">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="11c00-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="11c00-132">Eventos de início de processo e thread podem ser registrados no contexto do processo ou thread pai.</span><span class="sxs-lookup"><span data-stu-id="11c00-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="11c00-133">Como resultado, os membros **ProcessId** e **ThreadID** do [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="11c00-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="11c00-134">É por isso que esses eventos contêm os identificadores de processo e thread nos dados de evento (além daqueles no cabeçalho do evento).</span><span class="sxs-lookup"><span data-stu-id="11c00-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="11c00-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c00-135">Requirements</span></span>



| <span data-ttu-id="11c00-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c00-136">Requirement</span></span> | <span data-ttu-id="11c00-137">Valor</span><span class="sxs-lookup"><span data-stu-id="11c00-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="11c00-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11c00-138">Minimum supported client</span></span><br/> | <span data-ttu-id="11c00-139">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="11c00-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="11c00-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11c00-140">Minimum supported server</span></span><br/> | <span data-ttu-id="11c00-141">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="11c00-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11c00-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="11c00-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c00-143">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="11c00-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="11c00-144">**TypeGroup1 de processo \_**</span><span class="sxs-lookup"><span data-stu-id="11c00-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="11c00-145">**V0 de processo \_**</span><span class="sxs-lookup"><span data-stu-id="11c00-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="11c00-146">**Processo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="11c00-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="11c00-147">**Processo \_ v2**</span><span class="sxs-lookup"><span data-stu-id="11c00-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
