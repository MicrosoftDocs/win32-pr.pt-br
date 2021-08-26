---
description: a estrutura PERFINFO do \_ DSHOW \_ STREAMTRACE contém dados para um evento de rastreamento de DirectShow do tipo GUID \_ STREAMTRACE.
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
ms.openlocfilehash: e17d013d90b133f9c6819b8d9ddf4b5970582cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476993"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>Estrutura do PERFINFO \_ DShow \_ STREAMTRACE

a `PERFINFO_DSHOW_STREAMTRACE` estrutura contém dados para um evento de rastreamento de DirectShow do tipo GUID \_ STREAMTRACE.

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




| Identificador de evento | Descrição | 
|------------------|-------------|
| PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION | Registrado quando o filtro de <a href="mpeg-2-demultiplexer.md">demultiplexador MPEG-2</a> converte um carimbo de data/hora de apresentação (PTS) para transmitir o tempo.<ul><li><strong>dados</strong>[0]: hora de início convertida.</li><li><strong>dados</strong>[1]: hora de parada convertida.</li><li><strong>dados</strong>[2]. Identificador de fluxo para o pino de entrada.</li><li><strong>dados</strong>[3]: pts que foi convertido.</li></ul> | 
| PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE | Registrado quando MPEG-2 demultiplexador recebe um exemplo.<ul><li><strong>dados</strong>[0]: hora atual retornada por <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE | Registrado quando o VMR agenda uma amostra para renderização, imediatamente antes de o VMR chamar <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: aconselhetime</strong></a>.<ul><li><strong>dados</strong>[0]: tempo de referência quando o streaming começou, que corresponde ao tempo zero do fluxo.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE | Registrado quando o VMR inicia uma operação de decodificação — ou seja, quando o decodificador chama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator:: BeginFrame</strong></a>. Nenhum dado do evento. | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE | Registrado quando o VMR inicia uma operação de desentrelaçamento ou composição de vídeo. Nenhum dado do evento. | 
| PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME | Registrado quando o VMR descarta um quadro; por exemplo, se um exemplo estava atrasado.<ul><li><strong>dados</strong>[0]: hora de início da amostra.</li><li><strong>dados</strong>[1]: hora de término da amostra.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_END_ADVISE | Registrado quando o VMR recebe uma notificação de aviso do relógio de referência. Nenhum dado do evento. | 
| PERFINFO_STREAMTRACE_VMR_END_DECODE | Registrado quando o VMR termina uma operação de decodificação — ou seja, quando o decodificador chama <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator:: endframe</strong></a>. Nenhum dado do evento. | 
| PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE | Registrado quando o VMR conclui uma operação de desentrelaçamento ou composição de vídeo. Nenhum dado do evento. | 
| PERFINFO_STREAMTRACE_VMR_RECEIVE | Registrado quando o VMR recebe um novo exemplo. Nenhum dado do evento. | 
| PERFINFO_STREAMTRACE_VMR_RENDER_TIME | Registrado quando o VMR termina de renderizando um quadro.<ul><li><strong>Data</strong>[0]: tempo necessário para renderizar este quadro.</li><li><strong>dados</strong>[1]: média em execução de tempos de renderização de quadros.</li></ul> | 




 

para registrar esse evento em um filtro de DirectShow, use a função **PERFLOG \_ STREAMTRACE** , que é definida no arquivo de cabeçalho Dxmperf. h. esse cabeçalho é incluído no DirectShow classes base.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Perfstruct. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Estruturas](directshow-structures.md)
</dt> <dt>

[Rastreamento de eventos no DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUIDs de evento de rastreamento](trace-guids.md)
</dt> </dl>

 

 
