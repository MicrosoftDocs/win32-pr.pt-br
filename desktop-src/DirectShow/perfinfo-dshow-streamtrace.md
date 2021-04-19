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
# <a name="perfinfo_dshow_streamtrace-structure"></a>Estrutura do PERFINFO \_ DShow \_ STREAMTRACE

A `PERFINFO_DSHOW_STREAMTRACE` estrutura contém dados para um evento de rastreamento do DirectShow do tipo Guid \_ STREAMTRACE.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>Membros

<dl> <dt>

**id**
</dt> <dd>

Identificador de evento. Consulte Observações.

</dd> <dt>

**reservado**
</dt> <dd>

Reservado. Definido como zero.

</dd> <dt>

**dshowClock**
</dt> <dd>

Transmita o tempo para esse evento, em unidades de 100 a nanossegundos. Esse valor é opcional e pode ser zero.

</dd> <dt>

**data**
</dt> <dd>

Dados de evento opcionais que consistem em quatro valores de **ULONGLONG** . O significado desses dados depende do identificador de evento.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os identificadores de evento a seguir são definidos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificador de evento</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</td>
<td>Registrado quando o filtro de <a href="mpeg-2-demultiplexer.md">demultiplexador MPEG-2</a> converte um carimbo de data/hora de apresentação (PTS) para transmitir o tempo.
<ul>
<li><strong>dado</strong>[0]: Converted start time.</li>
<li><strong>dado</strong>[1]: Converted stop time.</li>
<li><strong>dados</strong>[2]. Identificador de fluxo para o pino de entrada.</li>
<li><strong>dado</strong>[3]: PTS that was converted.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</td>
<td>Registrado quando MPEG-2 demultiplexador recebe um exemplo.
<ul>
<li><strong>dados</strong> [0]: Current time returned by  do <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</td>
<td>Registrado quando o VMR agenda uma amostra para renderização, imediatamente antes de o VMR chamar <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: aconselhetime</strong></a>.
<ul>
<li><strong>dado</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</td>
<td>Registrado quando o VMR inicia uma operação de decodificação — ou seja, quando o decodificador chama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator:: BeginFrame</strong></a>. Nenhum dado do evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</td>
<td>Registrado quando o VMR inicia uma operação de desentrelaçamento ou composição de vídeo. Nenhum dado do evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</td>
<td>Registrado quando o VMR descarta um quadro; por exemplo, se um exemplo estava atrasado.
<ul>
<li><strong>dado</strong>[0]: Sample start time.</li>
<li><strong>dado</strong>[1]: Sample end time.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_ADVISE</td>
<td>Registrado quando o VMR recebe uma notificação de aviso do relógio de referência. Nenhum dado do evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_END_DECODE</td>
<td>Registrado quando o VMR termina uma operação de decodificação — ou seja, quando o decodificador chama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator:: endframe</strong></a>. Nenhum dado do evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</td>
<td>Registrado quando o VMR conclui uma operação de desentrelaçamento ou composição de vídeo. Nenhum dado do evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_RECEIVE</td>
<td>Registrado quando o VMR recebe um novo exemplo. Nenhum dado do evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_RENDER_TIME</td>
<td>Registrado quando o VMR termina de renderizando um quadro.
<ul>
<li><strong>dado</strong>[0]: Time that it took to render this frame.</li>
<li><strong>dado</strong>[1]: Running average of frame rendering times.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Para registrar esse evento de um filtro do DirectShow, use a função **PERFLOG \_ STREAMTRACE** , que é definida no arquivo de cabeçalho Dxmperf. h. Esse cabeçalho está incluído nas classes base do DirectShow.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Perfstruct. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do DirectShow](directshow-structures.md)
</dt> <dt>

[Rastreamento de eventos no DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUIDs de evento de rastreamento](trace-guids.md)
</dt> </dl>

 

 
