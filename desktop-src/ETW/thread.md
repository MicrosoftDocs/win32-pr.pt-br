---
description: Essa classe é a classe pai para eventos de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Classe Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: c4af87462607b675e46b3459a811925fbefe3ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172349"
---
# <a name="thread-class"></a><span data-ttu-id="7e757-104">Classe Thread</span><span class="sxs-lookup"><span data-stu-id="7e757-104">Thread class</span></span>

<span data-ttu-id="7e757-105">Essa classe é a classe pai para eventos de thread.</span><span class="sxs-lookup"><span data-stu-id="7e757-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="7e757-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="7e757-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e757-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e757-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="7e757-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7e757-108">Members</span></span>

<span data-ttu-id="7e757-109">A classe **thread** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="7e757-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e757-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e757-110">Remarks</span></span>

<span data-ttu-id="7e757-111">Para habilitar eventos de thread em uma sessão de log de kernel NT, especifique o sinalizador de **thread do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="7e757-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="7e757-112">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de thread chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ThreadGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="7e757-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="7e757-113">Use os tipos de evento a seguir para identificar o evento de thread real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="7e757-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="7e757-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="7e757-114">Event type</span></span>                                                      | <span data-ttu-id="7e757-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e757-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e757-116">**Evento \_ de Tipo de rastreamento \_ \_ end**(o valor do tipo de evento é 2)</span><span class="sxs-lookup"><span data-stu-id="7e757-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="7e757-117">Finalizar evento de thread.</span><span class="sxs-lookup"><span data-stu-id="7e757-117">End thread event.</span></span> <span data-ttu-id="7e757-118">A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7e757-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="7e757-119">**Evento \_ de \_ \_ Início do tipo de rastreamento**(o valor do tipo de evento é 1)</span><span class="sxs-lookup"><span data-stu-id="7e757-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="7e757-120">Iniciar evento de thread.</span><span class="sxs-lookup"><span data-stu-id="7e757-120">Start thread event.</span></span> <span data-ttu-id="7e757-121">A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7e757-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="7e757-122">Valor do tipo de evento, 3</span><span class="sxs-lookup"><span data-stu-id="7e757-122">Event type value, 3</span></span>                                             | <span data-ttu-id="7e757-123">Iniciar evento de thread de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="7e757-123">Start data collection thread event.</span></span> <span data-ttu-id="7e757-124">Enumera os threads que estão sendo executados no momento em que a sessão do kernel é iniciada.</span><span class="sxs-lookup"><span data-stu-id="7e757-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="7e757-125">A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7e757-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="7e757-126">Valor do tipo de evento, 4</span><span class="sxs-lookup"><span data-stu-id="7e757-126">Event type value, 4</span></span>                                             | <span data-ttu-id="7e757-127">Evento de thread de coleta de dados final.</span><span class="sxs-lookup"><span data-stu-id="7e757-127">End data collection thread event.</span></span> <span data-ttu-id="7e757-128">Enumera os threads que estão sendo executados no momento em que a sessão do kernel termina.</span><span class="sxs-lookup"><span data-stu-id="7e757-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="7e757-129">A [**classe \_ TypeGroup1 do thread**](thread-typegroup1.md) do MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="7e757-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="7e757-130">Eventos de início de processo e thread podem ser registrados no contexto do processo ou thread pai.</span><span class="sxs-lookup"><span data-stu-id="7e757-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="7e757-131">Como resultado, os membros **ProcessId** e **ThreadID** do [**cabeçalho de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) podem não corresponder ao processo e ao thread que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="7e757-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="7e757-132">É por isso que esses eventos contêm os identificadores de processo e thread nos dados de evento (além daqueles no cabeçalho do evento).</span><span class="sxs-lookup"><span data-stu-id="7e757-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e757-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e757-133">Requirements</span></span>



| <span data-ttu-id="7e757-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e757-134">Requirement</span></span> | <span data-ttu-id="7e757-135">Valor</span><span class="sxs-lookup"><span data-stu-id="7e757-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e757-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e757-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7e757-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e757-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e757-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e757-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7e757-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7e757-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e757-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e757-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e757-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="7e757-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="7e757-142">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="7e757-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="7e757-143">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="7e757-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="7e757-144">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7e757-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="7e757-145">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="7e757-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
