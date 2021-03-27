---
description: Essa classe é a classe pai para eventos UDP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Classe UdpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502067"
---
# <a name="udpip-class"></a><span data-ttu-id="3afb6-104">Classe UdpIp</span><span class="sxs-lookup"><span data-stu-id="3afb6-104">UdpIp class</span></span>

<span data-ttu-id="3afb6-105">Essa classe é a classe pai para eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="3afb6-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="3afb6-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="3afb6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3afb6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3afb6-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="3afb6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3afb6-108">Members</span></span>

<span data-ttu-id="3afb6-109">A classe **UdpIp** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="3afb6-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3afb6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3afb6-110">Remarks</span></span>

<span data-ttu-id="3afb6-111">Para habilitar eventos UDP/IP em uma sessão de log de kernel NT, especifique o sinalizador **\_ \_ \_ \_ tcpip de rede sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="3afb6-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="3afb6-112">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos UDP/IP chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**UdpIpGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="3afb6-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="3afb6-113">Use os seguintes tipos de evento para identificar o evento de rede (UDP/IP) real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="3afb6-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="3afb6-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="3afb6-114">Event type</span></span>                                                         | <span data-ttu-id="3afb6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3afb6-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3afb6-116">**Evento \_ de Tipo de rastreamento \_ \_ Receive**(o valor do tipo de evento é 11)</span><span class="sxs-lookup"><span data-stu-id="3afb6-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="3afb6-117">Receber evento para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="3afb6-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="3afb6-118">A classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="3afb6-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="3afb6-119">**Evento \_ de Tipo de rastreamento \_ \_ Send**(o valor do tipo de evento é 10)</span><span class="sxs-lookup"><span data-stu-id="3afb6-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="3afb6-120">Enviar evento para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="3afb6-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="3afb6-121">A classe [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="3afb6-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="3afb6-122">Valor do tipo de evento, 17</span><span class="sxs-lookup"><span data-stu-id="3afb6-122">Event type value, 17</span></span>                                               | <span data-ttu-id="3afb6-123">Evento Fail.</span><span class="sxs-lookup"><span data-stu-id="3afb6-123">Fail event.</span></span> <span data-ttu-id="3afb6-124">A classe [**UdpIp \_ Fail**](udpip-fail.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="3afb6-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="3afb6-125">Valor do tipo de evento, 26</span><span class="sxs-lookup"><span data-stu-id="3afb6-125">Event type value, 26</span></span>                                               | <span data-ttu-id="3afb6-126">Enviar evento para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="3afb6-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="3afb6-127">A classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="3afb6-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="3afb6-128">Valor do tipo de evento, 27</span><span class="sxs-lookup"><span data-stu-id="3afb6-128">Event type value, 27</span></span>                                               | <span data-ttu-id="3afb6-129">Receber evento para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="3afb6-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="3afb6-130">A classe [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="3afb6-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="3afb6-131">Você pode rastrear eventos de rede para um processo de origem e de destino usando a propriedade **ProcessId** .</span><span class="sxs-lookup"><span data-stu-id="3afb6-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="3afb6-132">Como alguns eventos de rede são registrados por threads separados, talvez você não possa usar os membros **ProcessId** e **ThreadID** do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar o processo ou thread que originou as atividades de rede.</span><span class="sxs-lookup"><span data-stu-id="3afb6-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="3afb6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3afb6-133">Requirements</span></span>



| <span data-ttu-id="3afb6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3afb6-134">Requirement</span></span> | <span data-ttu-id="3afb6-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3afb6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3afb6-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3afb6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3afb6-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3afb6-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3afb6-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3afb6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3afb6-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3afb6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3afb6-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3afb6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3afb6-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="3afb6-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="3afb6-142">**Falha de UdpIp \_**</span><span class="sxs-lookup"><span data-stu-id="3afb6-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="3afb6-143">**UdpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="3afb6-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="3afb6-144">**UdpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="3afb6-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="3afb6-145">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="3afb6-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="3afb6-146">**UdpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="3afb6-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
