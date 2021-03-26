---
description: Essa classe é a classe pai para eventos de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Classe Thread_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: f28b68a2aac5f2d5293f94ed2bab366d238ae662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828892"
---
# <a name="thread_v2-class"></a><span data-ttu-id="1e454-104">Classe de thread \_ v2</span><span class="sxs-lookup"><span data-stu-id="1e454-104">Thread\_V2 class</span></span>

<span data-ttu-id="1e454-105">Essa classe é a classe pai para eventos de thread.</span><span class="sxs-lookup"><span data-stu-id="1e454-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="1e454-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="1e454-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e454-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e454-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1e454-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1e454-108">Members</span></span>

<span data-ttu-id="1e454-109">A classe **thread \_ v2** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="1e454-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e454-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e454-110">Remarks</span></span>

<span data-ttu-id="1e454-111">Para habilitar eventos de thread em uma sessão de log de kernel NT, especifique o sinalizador de **thread do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="1e454-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="1e454-112">Você também pode especificar os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="1e454-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="1e454-113">**sinalizador de rastreamento de eventos \_ \_ \_ CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="1e454-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="1e454-114">**\_Dispatcher do \_ sinalizador de rastreamento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="1e454-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="1e454-115">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de thread chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="1e454-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="1e454-116">Use os tipos de evento a seguir para identificar o evento de thread real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="1e454-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="1e454-117">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="1e454-117">Event type</span></span>                                                      | <span data-ttu-id="1e454-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e454-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e454-119">**Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)</span><span class="sxs-lookup"><span data-stu-id="1e454-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="1e454-120">Finalizar evento de thread.</span><span class="sxs-lookup"><span data-stu-id="1e454-120">End thread event.</span></span> <span data-ttu-id="1e454-121">A classe MOF do [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="1e454-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="1e454-122">**Evento \_ de \_ \_ Início do tipo de rastreamento**(o valor do tipo de evento é 1)</span><span class="sxs-lookup"><span data-stu-id="1e454-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="1e454-123">Iniciar evento de thread.</span><span class="sxs-lookup"><span data-stu-id="1e454-123">Start thread event.</span></span> <span data-ttu-id="1e454-124">A classe MOF do [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="1e454-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="1e454-125">Valor do tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="1e454-125">Event type value, 3</span></span>                                             | <span data-ttu-id="1e454-126">Iniciar evento de thread de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="1e454-126">Start data collection thread event.</span></span> <span data-ttu-id="1e454-127">Enumera os threads que estão sendo executados no momento em que a sessão do kernel é iniciada.</span><span class="sxs-lookup"><span data-stu-id="1e454-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="1e454-128">A classe MOF do [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="1e454-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1e454-129">Valor do tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="1e454-129">Event type value, 4</span></span>                                             | <span data-ttu-id="1e454-130">Evento de thread de coleta de dados final.</span><span class="sxs-lookup"><span data-stu-id="1e454-130">End data collection thread event.</span></span> <span data-ttu-id="1e454-131">Enumera os threads que estão sendo executados no momento em que a sessão do kernel termina.</span><span class="sxs-lookup"><span data-stu-id="1e454-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="1e454-132">A classe MOF do [**thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="1e454-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="1e454-133">Valor do tipo de evento, 36</span><span class="sxs-lookup"><span data-stu-id="1e454-133">Event type value, 36</span></span>                                            | <span data-ttu-id="1e454-134">Evento de alternância de contexto.</span><span class="sxs-lookup"><span data-stu-id="1e454-134">Context switch event.</span></span> <span data-ttu-id="1e454-135">A classe MOF [**CSwitch**](cswitch.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="1e454-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="1e454-136">Valor do tipo de evento, 50</span><span class="sxs-lookup"><span data-stu-id="1e454-136">Event type value, 50</span></span>                                            | <span data-ttu-id="1e454-137">Evento de thread pronto.</span><span class="sxs-lookup"><span data-stu-id="1e454-137">Ready thread event.</span></span> <span data-ttu-id="1e454-138">A classe MOF [**ReadyThread**](readythread.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="1e454-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="1e454-139">Eventos de início de processo e thread podem ser registrados no contexto do processo ou thread pai.</span><span class="sxs-lookup"><span data-stu-id="1e454-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="1e454-140">Como resultado, os membros **ProcessId** e **ThreadID** do [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="1e454-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="1e454-141">É por isso que esses eventos contêm os identificadores de processo e thread nos dados de evento (além daqueles no cabeçalho do evento).</span><span class="sxs-lookup"><span data-stu-id="1e454-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e454-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e454-142">Requirements</span></span>



| <span data-ttu-id="1e454-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e454-143">Requirement</span></span> | <span data-ttu-id="1e454-144">Valor</span><span class="sxs-lookup"><span data-stu-id="1e454-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e454-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e454-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1e454-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e454-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e454-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e454-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1e454-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e454-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e454-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e454-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e454-150">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="1e454-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="1e454-151">**CSwitch**</span><span class="sxs-lookup"><span data-stu-id="1e454-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="1e454-152">**Processo**</span><span class="sxs-lookup"><span data-stu-id="1e454-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="1e454-153">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="1e454-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="1e454-154">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="1e454-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="1e454-155">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1e454-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
