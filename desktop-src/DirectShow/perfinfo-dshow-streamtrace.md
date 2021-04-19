---
description: A estrutura PERFINFO do \_ DShow \_ STREAMTRACE contém dados para um evento de rastreamento do DirectShow do tipo Guid \_ STREAMTRACE.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: Estrutura de PERFINFO_DSHOW_STREAMTRACE (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_STREAMTRACE
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 2bee4f3c11cf8462c8292cc412a6da5d9f9bfa78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767790"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a><span data-ttu-id="88599-103">Estrutura do PERFINFO \_ DShow \_ STREAMTRACE</span><span class="sxs-lookup"><span data-stu-id="88599-103">PERFINFO\_DSHOW\_STREAMTRACE structure</span></span>

<span data-ttu-id="88599-104">A `PERFINFO_DSHOW_STREAMTRACE` estrutura contém dados para um evento de rastreamento do DirectShow do tipo Guid \_ STREAMTRACE.</span><span class="sxs-lookup"><span data-stu-id="88599-104">The `PERFINFO_DSHOW_STREAMTRACE` structure contains data for a DirectShow trace event of type GUID\_STREAMTRACE.</span></span>

## <a name="syntax"></a><span data-ttu-id="88599-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88599-105">Syntax</span></span>


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a><span data-ttu-id="88599-106">Membros</span><span class="sxs-lookup"><span data-stu-id="88599-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88599-107">**id**</span><span class="sxs-lookup"><span data-stu-id="88599-107">**id**</span></span>
</dt> <dd>

<span data-ttu-id="88599-108">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="88599-108">Event identifier.</span></span> <span data-ttu-id="88599-109">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="88599-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="88599-110">**reservado**</span><span class="sxs-lookup"><span data-stu-id="88599-110">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="88599-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="88599-111">Reserved.</span></span> <span data-ttu-id="88599-112">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="88599-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="88599-113">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="88599-113">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="88599-114">Transmita o tempo para esse evento, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="88599-114">Stream time for this event, in 100-nanosecond units.</span></span> <span data-ttu-id="88599-115">Esse valor é opcional e pode ser zero.</span><span class="sxs-lookup"><span data-stu-id="88599-115">This value is optional and can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="88599-116">**data**</span><span class="sxs-lookup"><span data-stu-id="88599-116">**data**</span></span>
</dt> <dd>

<span data-ttu-id="88599-117">Dados de evento opcionais que consistem em quatro valores de **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="88599-117">Optional event data consisting of four **ULONGLONG** values.</span></span> <span data-ttu-id="88599-118">O significado desses dados depende do identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="88599-118">The meaning of this data depends on the event identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88599-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="88599-119">Remarks</span></span>

<span data-ttu-id="88599-120">Os identificadores de evento a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="88599-120">The following event identifiers are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88599-121">Identificador de evento</span><span class="sxs-lookup"><span data-stu-id="88599-121">Event identifier</span></span></th>
<th><span data-ttu-id="88599-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="88599-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88599-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span><span class="sxs-lookup"><span data-stu-id="88599-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span></span></td>
<td><span data-ttu-id="88599-124">Registrado quando o filtro de <a href="mpeg-2-demultiplexer.md">demultiplexador MPEG-2</a> converte um carimbo de data/hora de apresentação (PTS) para transmitir o tempo.</span><span class="sxs-lookup"><span data-stu-id="88599-124">Logged when the <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer</a> filter converts a presentation time stamp (PTS) to stream time.</span></span>
<ul>
<li><span data-ttu-id="88599-125"><strong>dado</strong>[0]: Converted start time.</span><span class="sxs-lookup"><span data-stu-id="88599-125"><strong>data</strong>[0]: Converted start time.</span></span></li>
<li><span data-ttu-id="88599-126"><strong>dado</strong>[1]: Converted stop time.</span><span class="sxs-lookup"><span data-stu-id="88599-126"><strong>data</strong>[1]: Converted stop time.</span></span></li>
<li><span data-ttu-id="88599-127"><strong>dados</strong>[2].</span><span class="sxs-lookup"><span data-stu-id="88599-127"><strong>data</strong>[2].</span></span> <span data-ttu-id="88599-128">Identificador de fluxo para o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="88599-128">Stream identifier for the input pin.</span></span></li>
<li><span data-ttu-id="88599-129"><strong>dado</strong>[3]: PTS that was converted.</span><span class="sxs-lookup"><span data-stu-id="88599-129"><strong>data</strong>[3]: PTS that was converted.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88599-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="88599-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span></span></td>
<td><span data-ttu-id="88599-131">Registrado quando MPEG-2 demultiplexador recebe um exemplo.</span><span class="sxs-lookup"><span data-stu-id="88599-131">Logged when MPEG-2 Demultiplexer receives a sample.</span></span>
<ul>
<li><span data-ttu-id="88599-132"><strong>dados</strong> [0]: Current time returned by  do <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="88599-132"><strong>data</strong>[0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88599-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span><span class="sxs-lookup"><span data-stu-id="88599-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span></span></td>
<td><span data-ttu-id="88599-134">Registrado quando o VMR agenda uma amostra para renderização, imediatamente antes de o VMR chamar <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: aconselhetime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="88599-134">Logged when the VMR schedules a sample for rendering, immediately before the VMR calls <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.</span></span>
<ul>
<li><span data-ttu-id="88599-135"><strong>dado</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span><span class="sxs-lookup"><span data-stu-id="88599-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88599-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span><span class="sxs-lookup"><span data-stu-id="88599-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span></span></td>
<td><span data-ttu-id="88599-137">Registrado quando o VMR inicia uma operação de decodificação — ou seja, quando o decodificador chama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator:: BeginFrame</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="88599-137">Logged when the VMR begins a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>.</span></span> <span data-ttu-id="88599-138">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="88599-138">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88599-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="88599-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span></span></td>
<td><span data-ttu-id="88599-140">Registrado quando o VMR inicia uma operação de desentrelaçamento ou composição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="88599-140">Logged when the VMR begins a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="88599-141">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="88599-141">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88599-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span><span class="sxs-lookup"><span data-stu-id="88599-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span></span></td>
<td><span data-ttu-id="88599-143">Registrado quando o VMR descarta um quadro; por exemplo, se um exemplo estava atrasado.</span><span class="sxs-lookup"><span data-stu-id="88599-143">Logged when the VMR drops a frame; for example, if a sample was late.</span></span>
<ul>
<li><span data-ttu-id="88599-144"><strong>dado</strong>[0]: Sample start time.</span><span class="sxs-lookup"><span data-stu-id="88599-144"><strong>data</strong>[0]: Sample start time.</span></span></li>
<li><span data-ttu-id="88599-145"><strong>dado</strong>[1]: Sample end time.</span><span class="sxs-lookup"><span data-stu-id="88599-145"><strong>data</strong>[1]: Sample end time.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88599-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span><span class="sxs-lookup"><span data-stu-id="88599-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span></span></td>
<td><span data-ttu-id="88599-147">Registrado quando o VMR recebe uma notificação de aviso do relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="88599-147">Logged when the VMR receives an advise notification from the reference clock.</span></span> <span data-ttu-id="88599-148">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="88599-148">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88599-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span><span class="sxs-lookup"><span data-stu-id="88599-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span></span></td>
<td><span data-ttu-id="88599-150">Registrado quando o VMR termina uma operação de decodificação — ou seja, quando o decodificador chama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator:: endframe</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="88599-150">Logged when the VMR ends a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>.</span></span> <span data-ttu-id="88599-151">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="88599-151">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88599-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="88599-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span></span></td>
<td><span data-ttu-id="88599-153">Registrado quando o VMR conclui uma operação de desentrelaçamento ou composição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="88599-153">Logged when the VMR completes a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="88599-154">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="88599-154">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88599-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="88599-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span></span></td>
<td><span data-ttu-id="88599-156">Registrado quando o VMR recebe um novo exemplo.</span><span class="sxs-lookup"><span data-stu-id="88599-156">Logged when the VMR receives a new sample.</span></span> <span data-ttu-id="88599-157">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="88599-157">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88599-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span><span class="sxs-lookup"><span data-stu-id="88599-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span></span></td>
<td><span data-ttu-id="88599-159">Registrado quando o VMR termina de renderizando um quadro.</span><span class="sxs-lookup"><span data-stu-id="88599-159">Logged when the VMR finishes rendering a frame.</span></span>
<ul>
<li><span data-ttu-id="88599-160"><strong>dado</strong>[0]: Time that it took to render this frame.</span><span class="sxs-lookup"><span data-stu-id="88599-160"><strong>data</strong>[0]: Time that it took to render this frame.</span></span></li>
<li><span data-ttu-id="88599-161"><strong>dado</strong>[1]: Running average of frame rendering times.</span><span class="sxs-lookup"><span data-stu-id="88599-161"><strong>data</strong>[1]: Running average of frame rendering times.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="88599-162">Para registrar esse evento de um filtro do DirectShow, use a função **PERFLOG \_ STREAMTRACE** , que é definida no arquivo de cabeçalho Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="88599-162">To log this event from a DirectShow filter, use the **PERFLOG\_STREAMTRACE** function, which is defined in the header file Dxmperf.h.</span></span> <span data-ttu-id="88599-163">Esse cabeçalho está incluído nas classes base do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="88599-163">This header is included in the DirectShow base classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="88599-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88599-164">Requirements</span></span>



| <span data-ttu-id="88599-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="88599-165">Requirement</span></span> | <span data-ttu-id="88599-166">Valor</span><span class="sxs-lookup"><span data-stu-id="88599-166">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88599-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88599-167">Header</span></span><br/> | <dl> <span data-ttu-id="88599-168"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="88599-168"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88599-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="88599-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88599-170">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="88599-170">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="88599-171">Rastreamento de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="88599-171">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="88599-172">GUIDs de evento de rastreamento</span><span class="sxs-lookup"><span data-stu-id="88599-172">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 
