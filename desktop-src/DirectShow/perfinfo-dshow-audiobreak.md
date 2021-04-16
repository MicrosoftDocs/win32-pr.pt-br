---
description: A estrutura PERFINFO do \_ DShow \_ AUDIOBREAK contém dados para um evento de rastreamento do tipo Guid \_ AUDIOBREAK. O filtro de renderizador do DirectSound registra esse evento quando há uma interrupção no fluxo de áudio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Estrutura de PERFINFO_DSHOW_AUDIOBREAK (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758140"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>Estrutura do PERFINFO \_ DShow \_ AUDIOBREAK

A `PERFINFO_DSHOW_AUDIOBREAK` estrutura contém dados para um evento de rastreamento do tipo Guid \_ AUDIOBREAK.

O filtro de [renderizador do DirectSound](directsound-renderer-filter.md) registra esse evento quando há uma interrupção no fluxo de áudio.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>Membros

<dl> <dt>

**cycleCounter**
</dt> <dd>

Contagem de ciclos de relógio mais recente (instrução RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Posição de gravação atual no buffer do DirectSound.

</dd> <dt>

**exemplo de**
</dt> <dd>

Início do intervalo de áudio no buffer do DirectSound.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Duração da interrupção, em milissegundos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para habilitar esse evento, você deve definir o \_ sinalizador de bit AUDIOBREAK no parâmetro *EnableFlag* ao chamar **EnableTrace**. Esse sinalizador é definido no arquivo de cabeçalho Dxmperf. h, que está incluído nas classes base do DirectShow.

Para registrar esse evento de um filtro do DirectShow, use a macro **PERFLOG \_ AUDIOBREAK** , que é definida em Dxmperf. h.

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

 

 




