---
description: Classe TcpIp-essa classe é a classe pai para eventos TCP/IP. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: Classe TcpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105724"
---
# <a name="tcpip-class"></a><span data-ttu-id="9fe0c-104">Classe TcpIp</span><span class="sxs-lookup"><span data-stu-id="9fe0c-104">TcpIp class</span></span>

<span data-ttu-id="9fe0c-105">Essa classe é a classe pai para eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="9fe0c-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe0c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fe0c-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="9fe0c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9fe0c-108">Members</span></span>

<span data-ttu-id="9fe0c-109">A classe **tcpip** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fe0c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fe0c-110">Remarks</span></span>

<span data-ttu-id="9fe0c-111">Para habilitar eventos TCP/IP em uma sessão de log de kernel NT, especifique o sinalizador **\_ \_ \_ \_ tcpip de rede sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="9fe0c-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="9fe0c-112">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos TCP/IP chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**TcpIpGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="9fe0c-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="9fe0c-113">Use os seguintes tipos de evento para identificar o evento de rede (TCP/IP) real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="9fe0c-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="9fe0c-114">Event type</span></span>                                                            | <span data-ttu-id="9fe0c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fe0c-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe0c-116">**Evento \_ de Tipo de rastreamento \_ \_ Accept**(o valor do tipo de evento é 15)</span><span class="sxs-lookup"><span data-stu-id="9fe0c-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="9fe0c-117">Aceite o evento para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-118">A classe [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="9fe0c-119">**Evento \_ de Tipo de rastreamento \_ \_ Connect**(o valor do tipo de evento é 12)</span><span class="sxs-lookup"><span data-stu-id="9fe0c-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="9fe0c-120">Evento Connect para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-121">A classe [**tcpip \_ TypeGroup2**](tcpip-typegroup2.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="9fe0c-122">**Evento \_ de Tipo de rastreamento \_ \_ Desconectar**(o valor do tipo de evento é 13)</span><span class="sxs-lookup"><span data-stu-id="9fe0c-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="9fe0c-123">Evento de desconexão para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-124">A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="9fe0c-125">**Evento \_ de Tipo de rastreamento \_ \_ Receive**(o valor do tipo de evento é 11)</span><span class="sxs-lookup"><span data-stu-id="9fe0c-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="9fe0c-126">Receber evento para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-127">A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="9fe0c-128">**Evento \_ de \_Reconectar \_ tipo de rastreamento**(o valor do tipo de evento é 16)</span><span class="sxs-lookup"><span data-stu-id="9fe0c-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="9fe0c-129">Evento de reconexão para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-130">(Uma tentativa de conexão falhou e outra tentativa foi feita.) A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="9fe0c-131">**Evento \_ de \_Retransmissão \_ do tipo de rastreamento**(o valor do tipo de evento é 14)</span><span class="sxs-lookup"><span data-stu-id="9fe0c-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="9fe0c-132">Retransmitir evento para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-133">A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="9fe0c-134">**Evento \_ de Tipo de rastreamento \_ \_ Send**(o valor do tipo de evento é 10)</span><span class="sxs-lookup"><span data-stu-id="9fe0c-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="9fe0c-135">Enviar evento para o protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-136">A classe [**tcpip \_ SendIPV4**](tcpip-sendipv4.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="9fe0c-137">Valor do tipo de evento, 17</span><span class="sxs-lookup"><span data-stu-id="9fe0c-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="9fe0c-138">Evento Fail.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-138">Fail event.</span></span> <span data-ttu-id="9fe0c-139">A classe do MOF [**\_ falha de tcpip**](tcpip-fail.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="9fe0c-140">Valor do tipo de evento, 18</span><span class="sxs-lookup"><span data-stu-id="9fe0c-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="9fe0c-141">Evento de cópia TCP para protocolo IPv4.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="9fe0c-142">A classe [**tcpip \_ TypeGroup1**](tcpip-typegroup1.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="9fe0c-143">Valor do tipo de evento, 26</span><span class="sxs-lookup"><span data-stu-id="9fe0c-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="9fe0c-144">Enviar evento para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-145">A classe [**tcpip \_ SendIPV6**](tcpip-sendipv6.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="9fe0c-146">Valor do tipo de evento, 27</span><span class="sxs-lookup"><span data-stu-id="9fe0c-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="9fe0c-147">Receber evento para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-148">A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="9fe0c-149">Valor do tipo de evento, 28</span><span class="sxs-lookup"><span data-stu-id="9fe0c-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="9fe0c-150">Evento Connect para protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-151">A classe [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="9fe0c-152">Valor do tipo de evento, 29</span><span class="sxs-lookup"><span data-stu-id="9fe0c-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="9fe0c-153">Evento de desconexão para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-154">A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="9fe0c-155">Valor do tipo de evento, 30</span><span class="sxs-lookup"><span data-stu-id="9fe0c-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="9fe0c-156">Retransmitir evento para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-157">A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="9fe0c-158">Valor do tipo de evento, 31</span><span class="sxs-lookup"><span data-stu-id="9fe0c-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="9fe0c-159">Aceite o evento para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-160">A classe [**tcpip \_ TypeGroup4**](tcpip-typegroup4.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="9fe0c-161">Valor do tipo de evento, 32</span><span class="sxs-lookup"><span data-stu-id="9fe0c-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="9fe0c-162">Evento de reconexão para o protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-163">(Uma tentativa de conexão falhou e outra tentativa foi feita.) A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="9fe0c-164">Valor do tipo de evento, 34</span><span class="sxs-lookup"><span data-stu-id="9fe0c-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="9fe0c-165">Evento de cópia TCP para protocolo IPv6.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="9fe0c-166">A classe [**tcpip \_ TypeGroup3**](tcpip-typegroup3.md) MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="9fe0c-167">Você pode rastrear eventos de rede para um processo de origem e de destino usando a propriedade **ProcessId** .</span><span class="sxs-lookup"><span data-stu-id="9fe0c-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="9fe0c-168">Como alguns eventos de rede são registrados por threads separados, talvez você não possa usar os membros **ProcessId** e **ThreadID** do [**\_ \_ cabeçalho de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) para identificar o processo ou thread que originou as atividades de rede.</span><span class="sxs-lookup"><span data-stu-id="9fe0c-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe0c-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fe0c-169">Requirements</span></span>



| <span data-ttu-id="9fe0c-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe0c-170">Requirement</span></span> | <span data-ttu-id="9fe0c-171">Valor</span><span class="sxs-lookup"><span data-stu-id="9fe0c-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fe0c-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fe0c-172">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe0c-173">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fe0c-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fe0c-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fe0c-174">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe0c-175">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fe0c-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fe0c-176">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9fe0c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe0c-177">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-178">**Falha de TcpIp \_**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-179">**\_SendIPV4 tcpip**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-180">**\_SendIPV6 tcpip**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-181">**\_TypeGroup1 tcpip**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-182">**\_TypeGroup2 tcpip**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-183">**\_TypeGroup3 tcpip**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-184">**\_TypeGroup4 tcpip**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-185">**\_V0 tcpip**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="9fe0c-186">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="9fe0c-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
