---
description: A estrutura PERFINFO do \_ DShow \_ AVREND contém dados para um evento de rastreamento do tipo Guid \_ VIDEOREND. O VMR registra esse evento imediatamente antes de renderizar um quadro.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Estrutura de PERFINFO_DSHOW_AVREND (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 49cc76f4db1a5fae76678ee2d81f3e2fff0a6c5ca3d5c5532adebaec23f48215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050706"
---
# <a name="perfinfo_dshow_avrend-structure"></a>Estrutura do PERFINFO \_ DShow \_ AVREND

A `PERFINFO_DSHOW_AVREND` estrutura contém dados para um evento de rastreamento do tipo Guid \_ VIDEOREND.

O VMR registra esse evento imediatamente antes de renderizar um quadro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a>Membros

<dl> <dt>

**cycleCounter**
</dt> <dd>

Contagem de ciclos de relógio mais recente (instrução RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Tempo de referência atual, conforme retornado pelo método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

</dd> <dt>

**exemplo de**
</dt> <dd>

Hora de início do exemplo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para habilitar esse evento, você deve definir o \_ sinalizador DXMPERF VIDEOREND no parâmetro *EnableFlag* ao chamar **EnableTrace**. esse sinalizador é definido no arquivo de cabeçalho Dxmperf. h, que é incluído no DirectShow classes base.

para registrar esse evento em um filtro de DirectShow, use a macro **PERFLOG \_ VIDEOREND** , que é definida em Dxmperf. h.

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

 

 




