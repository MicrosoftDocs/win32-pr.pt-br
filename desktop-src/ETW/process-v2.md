---
description: Classe Process_V2-essa classe é a classe pai para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Classe Process_V2
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
ms.openlocfilehash: 77d700e7847d0ad19a019985a4e19343ce8f383d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106294"
---
# <a name="process_v2-class"></a><span data-ttu-id="4e54b-104">\_Classe Process v2</span><span class="sxs-lookup"><span data-stu-id="4e54b-104">Process\_V2 class</span></span>

<span data-ttu-id="4e54b-105">Essa classe é a classe pai para eventos de processo.</span><span class="sxs-lookup"><span data-stu-id="4e54b-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="4e54b-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="4e54b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e54b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e54b-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="4e54b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4e54b-108">Members</span></span>

<span data-ttu-id="4e54b-109">A classe **process** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="4e54b-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e54b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e54b-110">Remarks</span></span>

<span data-ttu-id="4e54b-111">Para habilitar eventos de processo em uma sessão de log do kernel NT, especifique o sinalizador de **processo do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="4e54b-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="4e54b-112">Você também pode especificar o seguinte sinalizador:</span><span class="sxs-lookup"><span data-stu-id="4e54b-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="4e54b-113">**\_contadores de \_ processo de sinalizador de rastreamento de eventos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4e54b-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="4e54b-114">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de processo chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ProcessGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="4e54b-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="4e54b-115">Use os tipos de evento a seguir para identificar o evento de processo real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="4e54b-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="4e54b-116">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="4e54b-116">Event type</span></span>                                                      | <span data-ttu-id="4e54b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e54b-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e54b-118">**Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)</span><span class="sxs-lookup"><span data-stu-id="4e54b-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="4e54b-119">Encerrar o evento de processo.</span><span class="sxs-lookup"><span data-stu-id="4e54b-119">End process event.</span></span> <span data-ttu-id="4e54b-120">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e54b-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="4e54b-121">**Evento \_ de \_ \_ Início do tipo de rastreamento**(o valor do tipo de evento é 1)</span><span class="sxs-lookup"><span data-stu-id="4e54b-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="4e54b-122">Iniciar o evento de processo.</span><span class="sxs-lookup"><span data-stu-id="4e54b-122">Start process event.</span></span> <span data-ttu-id="4e54b-123">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e54b-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="4e54b-124">Valor do tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="4e54b-124">Event type value, 3</span></span>                                             | <span data-ttu-id="4e54b-125">Iniciar evento de processo de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="4e54b-125">Start data collection process event.</span></span> <span data-ttu-id="4e54b-126">Enumera os processos que estão sendo executados no momento em que a sessão do kernel é iniciada.</span><span class="sxs-lookup"><span data-stu-id="4e54b-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="4e54b-127">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e54b-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="4e54b-128">Valor do tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="4e54b-128">Event type value, 4</span></span>                                             | <span data-ttu-id="4e54b-129">Evento de processo de coleta de dados final.</span><span class="sxs-lookup"><span data-stu-id="4e54b-129">End data collection process event.</span></span> <span data-ttu-id="4e54b-130">Enumera os processos que estão sendo executados no momento em que a sessão do kernel termina.</span><span class="sxs-lookup"><span data-stu-id="4e54b-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="4e54b-131">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e54b-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="4e54b-132">Valor do tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="4e54b-132">Event type value, 32</span></span>                                            | <span data-ttu-id="4e54b-133">Evento de contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="4e54b-133">Performance counters event.</span></span> <span data-ttu-id="4e54b-134">A classe MOF do [**processo \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e54b-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="4e54b-135">Valor do tipo de evento, 33</span><span class="sxs-lookup"><span data-stu-id="4e54b-135">Event type value, 33</span></span>                                            | <span data-ttu-id="4e54b-136">Encerramento dos contadores de desempenho no início da sessão.</span><span class="sxs-lookup"><span data-stu-id="4e54b-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="4e54b-137">A classe MOF do [**processo \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e54b-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="4e54b-138">Valor do tipo de evento, 39</span><span class="sxs-lookup"><span data-stu-id="4e54b-138">Event type value, 39</span></span>                                            | <span data-ttu-id="4e54b-139">Evento de processo extinto.</span><span class="sxs-lookup"><span data-stu-id="4e54b-139">Defunct process event.</span></span> <span data-ttu-id="4e54b-140">A classe [**process \_ TypeGroup1**](process-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="4e54b-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="4e54b-141">Eventos de início de processo e thread podem ser registrados no contexto do processo ou thread pai.</span><span class="sxs-lookup"><span data-stu-id="4e54b-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="4e54b-142">Como resultado, os membros **ProcessId** e **ThreadID** do [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="4e54b-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="4e54b-143">É por isso que esses eventos contêm os identificadores de processo e thread nos dados de evento (além daqueles no cabeçalho do evento).</span><span class="sxs-lookup"><span data-stu-id="4e54b-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e54b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e54b-144">Requirements</span></span>



| <span data-ttu-id="4e54b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e54b-145">Requirement</span></span> | <span data-ttu-id="4e54b-146">Valor</span><span class="sxs-lookup"><span data-stu-id="4e54b-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="4e54b-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e54b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4e54b-148">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="4e54b-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="4e54b-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e54b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4e54b-150">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e54b-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e54b-151">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4e54b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e54b-152">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="4e54b-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="4e54b-153">**Processar**</span><span class="sxs-lookup"><span data-stu-id="4e54b-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="4e54b-154">**TypeGroup1 de processo \_**</span><span class="sxs-lookup"><span data-stu-id="4e54b-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="4e54b-155">**V0 de processo \_**</span><span class="sxs-lookup"><span data-stu-id="4e54b-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="4e54b-156">**Processo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="4e54b-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
