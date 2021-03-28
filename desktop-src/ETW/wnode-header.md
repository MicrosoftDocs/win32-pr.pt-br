---
description: A \_ estrutura de cabeçalho WNODE é um membro da estrutura de propriedades de rastreamento de eventos \_ \_ .
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
title: Estrutura de WNODE_HEADER (Wmistr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WNODE_HEADER
api_type:
- HeaderDef
api_location:
- Wmistr.h
ms.openlocfilehash: 6a2ed615d2b67cbd47a817234a14b7cf1221f601
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "104968762"
---
# <a name="wnode_header-structure"></a><span data-ttu-id="4a0b8-103">\_Estrutura de cabeçalho WNODE</span><span class="sxs-lookup"><span data-stu-id="4a0b8-103">WNODE\_HEADER structure</span></span>

<span data-ttu-id="4a0b8-104">A estrutura de **\_ cabeçalho WNODE** é um membro da estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-104">The **WNODE\_HEADER** structure is a member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a0b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a0b8-105">Syntax</span></span>


```C++
typedef struct _WNODE_HEADER {
  ULONG BufferSize;
  ULONG ProviderId;
  union {
    ULONG64 HistoricalContext;
    struct {
      ULONG Version;
      ULONG Linkage;
    };
  };
  union {
    HANDLE        KernelHandle;
    LARGE_INTEGER TimeStamp;
  };
  GUID  Guid;
  ULONG ClientContext;
  ULONG Flags;
} WNODE_HEADER, *PWNODE_HEADER;
```



## <a name="members"></a><span data-ttu-id="4a0b8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4a0b8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a0b8-107">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-107">**BufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-108">Tamanho total da memória alocada, em bytes, para as propriedades da sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-108">Total size of memory allocated, in bytes, for the event tracing session properties.</span></span> <span data-ttu-id="4a0b8-109">O tamanho da memória deve incluir o espaço para a estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) , além da cadeia de caracteres do nome da sessão e da cadeia de caracteres do nome do arquivo de log que seguem a estrutura na memória.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-109">The size of memory must include the room for the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure plus the session name string and log file name string that follow the structure in memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-110">**ProviderId**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-110">**ProviderId**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-111">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-111">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-112">**HistoricalContext**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-112">**HistoricalContext**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-113">Na saída, o identificador para a sessão de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-113">On output, the handle to the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-114">**Versão**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-114">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-115">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-116">**Vinculação**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-116">**Linkage**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-117">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-117">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-118">**KernelHandle**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-118">**KernelHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-119">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-119">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-120">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-120">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-121">Hora em que as informações nesta estrutura foram atualizadas, em intervalos de 100 a nanossegundos desde a meia-noite, 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-121">Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-122">**Volume**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-122">**Guid**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-123">O GUID que você define para a sessão.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-123">The GUID that you define for the session.</span></span>

<span data-ttu-id="4a0b8-124">Para uma sessão do NT kernel Logger, defina esse membro como **SystemTraceControlGuid**.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-124">For an NT Kernel Logger session, set this member to **SystemTraceControlGuid**.</span></span>

<span data-ttu-id="4a0b8-125">Se esse membro for definido como **SystemTraceControlGuid** ou **GlobalLoggerGuid**, o agente será um agente de log do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-125">If this member is set to **SystemTraceControlGuid** or **GlobalLoggerGuid**, the logger will be a system logger.</span></span>

<span data-ttu-id="4a0b8-126">Para uma sessão de agente de log particular, defina esse membro como o GUID do provedor que você vai habilitar para a sessão.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-126">For a private logger session, set this member to the provider's GUID that you are going to enable for the session.</span></span>

<span data-ttu-id="4a0b8-127">Se você iniciar uma sessão que não seja um agente de log de kernel ou uma sessão de agente particular, não será necessário especificar um GUID de sessão.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-127">If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID.</span></span> <span data-ttu-id="4a0b8-128">Se você não especificar um GUID, o ETW criará um para você.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-128">If you do not specify a GUID, ETW creates one for you.</span></span> <span data-ttu-id="4a0b8-129">Você precisará especificar um GUID de sessão somente se quiser alterar as permissões padrão associadas a uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-129">You need to specify a session GUID only if you want to change the default permissions associated with a specific session.</span></span> <span data-ttu-id="4a0b8-130">Para obter detalhes, consulte a função EventAccessControl.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-130">For details, see the EventAccessControl function.</span></span>

<span data-ttu-id="4a0b8-131">Não é possível iniciar mais de uma sessão com o mesmo GUID de sessão.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-131">You cannot start more than one session with the same session GUID.</span></span>

<span data-ttu-id="4a0b8-132">**Antes do Windows Vista:** Você pode iniciar mais de uma sessão com o mesmo GUID de sessão.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-132">**Prior to Windows Vista:** You can start more than one session with the same session GUID.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-133">**ClientContext**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-133">**ClientContext**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-134">Resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-134">Clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="4a0b8-135">O padrão é o contador de desempenho de consulta (QPC).</span><span class="sxs-lookup"><span data-stu-id="4a0b8-135">The default is Query performance counter (QPC).</span></span>

<span data-ttu-id="4a0b8-136">**Antes do Windows Vista:** O padrão é hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-136">**Prior to Windows Vista:** The default is system time.</span></span>

<span data-ttu-id="4a0b8-137">**Antes do Windows 10, versão 1703:** Não mais do que 2 tipos de relógio distintos podem ser usados simultaneamente por qualquer agente de log do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-137">**Prior to Windows 10, version 1703:** No more than 2 distinct clock types can be used simultaneously by any system loggers.</span></span>

<span data-ttu-id="4a0b8-138">**A partir do Windows 10, versão 1703:** A restrição de tipo de relógio foi removida.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-138">**Starting with Windows 10, version 1703:** The clock type restriction has been removed.</span></span> <span data-ttu-id="4a0b8-139">Todos os três tipos de relógio agora podem ser usados simultaneamente por agentes de log do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-139">All three clock types can now be used simultaneously by system loggers.</span></span>

<span data-ttu-id="4a0b8-140">Você pode especificar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-140">You can specify one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a0b8-141">Valor</span><span class="sxs-lookup"><span data-stu-id="4a0b8-141">Value</span></span></th>
<th><span data-ttu-id="4a0b8-142">Significado</span><span class="sxs-lookup"><span data-stu-id="4a0b8-142">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="4a0b8-143"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="4a0b8-143"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="4a0b8-144">Contador de desempenho de consulta (QPC).</span><span class="sxs-lookup"><span data-stu-id="4a0b8-144">Query performance counter (QPC).</span></span> <span data-ttu-id="4a0b8-145">O contador QPC fornece um carimbo de data/hora de alta resolução que não é afetado pelos ajustes no relógio do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-145">The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock.</span></span> <span data-ttu-id="4a0b8-146">O carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-146">The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API.</span></span> <span data-ttu-id="4a0b8-147">Para obter mais informações sobre as características desse carimbo de data/hora, consulte <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">adquirindo carimbos de data/hora de alta resolução</a>.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-147">For more information on the characteristics of this time stamp, see <a href="/windows/win32/sysinfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</span></span><br/> <span data-ttu-id="4a0b8-148">Você deve usar essa resolução se tiver taxas de eventos altas ou se o consumidor mesclar eventos de buffers diferentes.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-148">You should use this resolution if you have high event rates or if the consumer merges events from different buffers.</span></span> <span data-ttu-id="4a0b8-149">Nesses casos, a precisão e a estabilidade do carimbo de data/hora do QPC permitem maior precisão na ordenação dos eventos de diferentes buffers.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-149">In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers.</span></span> <span data-ttu-id="4a0b8-150">No entanto, o carimbo de data/hora de QPC não refletirá as atualizações no relógio do sistema, por exemplo, se o relógio do sistema for ajustado para frente devido à sincronização com um servidor NTP enquanto o rastreamento estiver em andamento, os carimbos de hora QPC no rastreamento continuarão a refletir o tempo como se nenhuma atualização tivesse ocorrido.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-150">However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.</span></span><br/> <span data-ttu-id="4a0b8-151">Para determinar a resolução, use o membro <strong>PerfFreq</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> ao consumir o evento.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-151">To determine the resolution, use the <strong>PerfFreq</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="4a0b8-152">Para converter o carimbo de data/hora de um evento em unidades 100-NS, use a seguinte fórmula de conversão:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-152">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="4a0b8-153">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart \* 10000000,0/logfileHeader. PerfFreq. QuadPart</span><span class="sxs-lookup"><span data-stu-id="4a0b8-153">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart \* 10000000.0 / logfileHeader.PerfFreq.QuadPart</span></span><br/> <span data-ttu-id="4a0b8-154">Observe que, em computadores mais antigos, o carimbo de data/hora pode não ser preciso, pois o contador às vezes pula para frente devido a erros de hardware.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-154">Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="4a0b8-155"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="4a0b8-155"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="4a0b8-156">Hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-156">System time.</span></span> <span data-ttu-id="4a0b8-157">A hora do sistema fornece um carimbo de data/hora que controla as alterações no relógio do sistema, por exemplo, se o relógio do sistema for ajustado para frente devido à sincronização com um servidor NTP enquanto o rastreamento estiver em andamento, os carimbos de hora do sistema no rastreamento também serão encaminhados para corresponder à nova configuração do relógio do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-157">The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock.</span></span> <br/>
<ul>
<li><span data-ttu-id="4a0b8-158">Em sistemas anteriores ao Windows 10, o carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API GetSystemTimeAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-158">On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</span></span></li>
<li><span data-ttu-id="4a0b8-159">No Windows 10 ou posterior, o carimbo de data/hora armazenado no evento é equivalente ao valor retornado da API GetSystemTimePreciseAsFileTime.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-159">On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</span></span></li>
</ul>
<span data-ttu-id="4a0b8-160">Antes do Windows 10, a resolução desse carimbo de data/hora foi a resolução de um tique de relógio do sistema, conforme indicado pelo membro TimerResolution de TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-160">Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER.</span></span> <span data-ttu-id="4a0b8-161">A partir do Windows 10, a resolução desse carimbo de data/hora é a resolução do contador de desempenho, conforme indicado pelo membro PerfFreq de TRACE_LOGFILE_HEADER.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-161">Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.</span></span><br/> <span data-ttu-id="4a0b8-162">Para converter o carimbo de data/hora de um evento em unidades 100-NS, use a seguinte fórmula de conversão:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-162">To convert an event’s time stamp into 100-ns units, use the following conversion formula:</span></span> <br/> <span data-ttu-id="4a0b8-163">scaledTimestamp = eventRecord. EventHeader. TimeStamp. QuadPart</span><span class="sxs-lookup"><span data-stu-id="4a0b8-163">scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart</span></span><br/> <span data-ttu-id="4a0b8-164">Observe que quando os eventos são capturados em um sistema que executa um so anterior ao Windows 10, se o volume de eventos for alto, a resolução do tempo do sistema poderá não ser suficiente para determinar a sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-164">Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events.</span></span> <span data-ttu-id="4a0b8-165">Nesse caso, um conjunto de eventos terá o mesmo carimbo de data/hora, mas a ordem na qual o ETW entrega os eventos pode não estar correta.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-165">In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct.</span></span> <span data-ttu-id="4a0b8-166">A partir do Windows 10, o carimbo de data/hora é capturado com precisão adicional, embora alguma instabilidade ainda possa ocorrer nos casos em que o relógio do sistema foi ajustado enquanto o rastreamento estava sendo capturado.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-166">Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="4a0b8-167"><dt>Beta</dt> </span><span class="sxs-lookup"><span data-stu-id="4a0b8-167"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="4a0b8-168">Contador de ciclo de CPU.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-168">CPU cycle counter.</span></span> <span data-ttu-id="4a0b8-169">O contador de CPU fornece o carimbo de data e hora de resolução mais alto e consome menos recursos para recuperar.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-169">The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve.</span></span> <span data-ttu-id="4a0b8-170">No entanto, o contador de CPU não é confiável e não deve ser usado na produção.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-170">However, the CPU counter is unreliable and should not be used in production.</span></span> <span data-ttu-id="4a0b8-171">Por exemplo, em alguns computadores, os temporizadores mudarão a frequência devido a alterações térmicas e de energia, além de serem interrompidos em alguns Estados.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-171">For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.</span></span><br/> <span data-ttu-id="4a0b8-172">Para determinar a resolução, use o membro <strong>CpuSpeedInMHz</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> ao consumir o evento.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-172">To determine the resolution, use the <strong>CpuSpeedInMHz</strong> member of <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> when consuming the event.</span></span><br/> <span data-ttu-id="4a0b8-173">Se o hardware não oferecer suporte a esse tipo de relógio, o ETW usará a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-173">If your hardware does not support this clock type, ETW uses system time.</span></span><br/> <span data-ttu-id="4a0b8-174"><strong>Windows Server 2003, Windows XP com SP1 e Windows XP:</strong> Esse valor não tem suporte, foi introduzido no Windows Server 2003 com SP1 e no Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-174"><strong>Windows Server 2003, Windows XP with SP1 and Windows XP:</strong> This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4a0b8-175">**Windows 2000:** Não há suporte para o membro **ClientContext** .</span><span class="sxs-lookup"><span data-stu-id="4a0b8-175">**Windows 2000:** The **ClientContext** member is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4a0b8-176">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-176">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4a0b8-177">Deve conter **\_ \_ \_ GUID rastreado do sinalizador WNODE** para indicar que a estrutura contém informações de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-177">Must contain **WNODE\_FLAG\_TRACED\_GUID** to indicate that the structure contains event tracing information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a0b8-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a0b8-178">Remarks</span></span>

<span data-ttu-id="4a0b8-179">Certifique-se de inicializar a memória dessa estrutura para zero antes de definir os membros.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-179">Be sure to initialize the memory for this structure to zero before setting any members.</span></span>

<span data-ttu-id="4a0b8-180">Para converter um carimbo de data/hora ETW em um FILETIME, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-180">To convert an ETW timestamp into a FILETIME, use the following procedure:</span></span>

<dl> 1. <span data-ttu-id="4a0b8-181">Para cada arquivo de sessão ou de log sendo processado (ou seja, para cada log de rastreamento de evento \_ \_ ), verifique o campo logfile. ProcessTraceMode para determinar se o \_ sinalizador de carimbo de \_ data/hora bruto do modo de rastreamento do processo \_ \_ está definido.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-181">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.ProcessTraceMode field to determine whether the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag is set.</span></span> <span data-ttu-id="4a0b8-182">Por padrão, esse sinalizador não é definido.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-182">By default, this flag is not set.</span></span> <span data-ttu-id="4a0b8-183">Se esse sinalizador não for definido, o tempo de execução do ETW converterá automaticamente o carimbo de data/hora de cada registro de evento \_ em um FILETIME antes de enviar o registro de evento \_ para a função EventRecordCallback, portanto, nenhum processamento adicional será necessário.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-183">If this flag is not set, the ETW runtime will automatically convert the timestamp of each EVENT\_RECORD into a FILETIME before sending the EVENT\_RECORD to your EventRecordCallback function, so no additional processing is needed.</span></span> <span data-ttu-id="4a0b8-184">As etapas a seguir só devem ser usadas se o rastreamento estiver sendo processado com o \_ \_ sinalizador de \_ carimbo de \_ data/hora bruto do modo de rastreamento do processo.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-184">The following steps should only be used if the trace is being processed with the PROCESS\_TRACE\_MODE\_RAW\_TIMESTAMP flag set.</span></span>  
2. <span data-ttu-id="4a0b8-185">Para cada arquivo de sessão ou de log sendo processado (ou seja, para cada log de rastreamento de evento \_ \_ ), verifique o campo logfile. LogfileHeader. ReservedFlags para determinar a escala de carimbo de data/hora do arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-185">For each session or log file being processed (i.e. for each EVENT\_TRACE\_LOGFILE), check the logFile.LogfileHeader.ReservedFlags field to determine the time stamp scale for the log file.</span></span> <span data-ttu-id="4a0b8-186">Com base no valor de ReservedFlags, siga uma destas etapas para determinar o valor a ser usado para timeStampScale nas etapas restantes:</span><span class="sxs-lookup"><span data-stu-id="4a0b8-186">Based on the value of ReservedFlags, follow one of these steps to determine the value to use for timeStampScale in the remaining steps:</span></span> <dl> <span data-ttu-id="4a0b8-187">a.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-187">a.</span></span> <span data-ttu-id="4a0b8-188">Se ReservedFlags = = 1 (QPC): DOUBLE timeStampScale = 10000000,0/logFile. LogfileHeader. PerfFreq. QuadPart;</span><span class="sxs-lookup"><span data-stu-id="4a0b8-188">If ReservedFlags == 1 (QPC): DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;</span></span>  
<span data-ttu-id="4a0b8-189">b.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-189">b.</span></span> <span data-ttu-id="4a0b8-190">Se ReservedFlags = = 2 (hora do sistema): timeStampScale duplo = 1,0;</span><span class="sxs-lookup"><span data-stu-id="4a0b8-190">If ReservedFlags == 2 (System time): DOUBLE timeStampScale = 1.0;</span></span>  
<span data-ttu-id="4a0b8-191">Observe que as etapas restantes são desnecessárias para eventos que usam a hora do sistema, pois os eventos já fornecem seus carimbos de data/hora em unidades FILETIME.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-191">Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units.</span></span> <span data-ttu-id="4a0b8-192">As etapas restantes funcionarão, mas serão desnecessárias e apresentarão um pequeno erro de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-192">The remaining steps will work but are unnecessary and will introduce a small rounding error.</span></span>  
<span data-ttu-id="4a0b8-193">c.</span><span class="sxs-lookup"><span data-stu-id="4a0b8-193">c.</span></span> <span data-ttu-id="4a0b8-194">Se ReservedFlags = = 3 (contador de ciclo de CPU): DOUBLE timeStampScale = 10,0/logFile. LogfileHeader. CpuSpeedInMHz;</span><span class="sxs-lookup"><span data-stu-id="4a0b8-194">If ReservedFlags == 3 (CPU cycle counter): DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;</span></span>  
</dl> </dd> 3. On the FIRST call to your EventRecordCallback function for a particular log file, use data from the logFile (EVENT\_TRACE\_LOGFILE) and from the eventRecord (EVENT\_RECORD) to compute the timeStampBase that will be used for the remaining events in the log file: INT64 timeStampBase = logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
4. For each eventRecord (EVENT\_RECORD), convert the event’s timestamp into FILETIME as follows, using the timeStampScale and timeStampBase values calculated in steps 2 and 3: INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale \* eventRecord.EventHeader.TimeStamp.QuadPart);  
</dl>

## <a name="requirements"></a><span data-ttu-id="4a0b8-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a0b8-195">Requirements</span></span>



| <span data-ttu-id="4a0b8-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a0b8-196">Requirement</span></span> | <span data-ttu-id="4a0b8-197">Valor</span><span class="sxs-lookup"><span data-stu-id="4a0b8-197">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a0b8-198">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a0b8-198">Minimum supported client</span></span><br/> | <span data-ttu-id="4a0b8-199">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4a0b8-199">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                   |
| <span data-ttu-id="4a0b8-200">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a0b8-200">Minimum supported server</span></span><br/> | <span data-ttu-id="4a0b8-201">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4a0b8-201">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                         |
| <span data-ttu-id="4a0b8-202">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a0b8-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a0b8-203"><dt>Wmistr. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a0b8-203"><dt>Wmistr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a0b8-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a0b8-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a0b8-205">*ControlCallback*</span><span class="sxs-lookup"><span data-stu-id="4a0b8-205">*ControlCallback*</span></span>](/windows/win32/api/evntrace/nc-evntrace-wmidprequest)
</dt> <dt>

[<span data-ttu-id="4a0b8-206">**\_Propriedades de rastreamento de eventos \_**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-206">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="4a0b8-207">**GetTraceLoggerHandle**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-207">**GetTraceLoggerHandle**</span></span>](/windows/win32/api/evntrace/nf-evntrace-gettraceloggerhandle)
</dt> <dt>

[<span data-ttu-id="4a0b8-208">**\_inteiro grande**</span><span class="sxs-lookup"><span data-stu-id="4a0b8-208">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)
</dt> </dl>

 

 
