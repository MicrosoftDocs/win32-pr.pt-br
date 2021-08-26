---
description: A estrutura PERFINFO \_ DSHOW \_ AUDIOBREAK contém dados para um evento de rastreamento do tipo GUID \_ AUDIOBREAK. O filtro Do renderador DirectSound registra esse evento quando há uma quebra no fluxo de áudio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: PERFINFO_DSHOW_AUDIOBREAK estrutura (Perfstruct.h)
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
ms.openlocfilehash: c7b8f83fffaa718c27e0333d864a564282228c0943f4d77fb653dc1800a6ddd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928186"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>Estrutura AUDIOBREAK PERFINFO \_ DSHOW \_

A `PERFINFO_DSHOW_AUDIOBREAK` estrutura contém dados para um evento de rastreamento do tipo GUID \_ AUDIOBREAK.

O [filtro Do renderador DirectSound](directsound-renderer-filter.md) registra esse evento quando há uma quebra no fluxo de áudio.

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

Contagem de ciclo de relógio mais recente (instrução RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Posição de gravação atual no buffer DirectSound.

</dd> <dt>

**sampleTime**
</dt> <dd>

Início da quebra de áudio no buffer DirectSound.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Duração da quebra, em milissegundos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para habilitar esse evento, você deve definir o sinalizador AUDIOBREAK BIT no parâmetro \_ *EnableFlag* ao chamar **EnableTrace**. Esse sinalizador é definido no arquivo de header Dxmperf.h, que está incluído nas classes DirectShow base.

Para registrar esse evento em um DirectShow, use a macro **PERFLOG \_ AUDIOBREAK,** que é definida em Dxmperf.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Perfstruct.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Estruturas](directshow-structures.md)
</dt> <dt>

[Rastreamento de eventos em DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUIDs de evento de rastreamento](trace-guids.md)
</dt> </dl>

 

 




