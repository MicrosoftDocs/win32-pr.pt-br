---
description: Preterido. Representa um instante no tempo, normalmente expresso como uma data e hora do dia e um calendário correspondente.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Estrutura CALDATETIME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 700e11f27b673d9ff706483cc4abcf2f06cd7d8bb779ef8eaf9b51a6d81b4068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822826"
---
# <a name="caldatetime-structure"></a>Estrutura CALDATETIME

Preterido. Representa um instante no tempo, normalmente expresso como uma data e hora do dia e um calendário correspondente.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a>Membros

<dl> <dt>

**CalId**
</dt> <dd>

O [identificador de calendário](calendar-identifiers.md) para o instante no tempo.

</dd> <dt>

**Era**
</dt> <dd>

As informações de era para o instantâneo no tempo.

</dd> <dt>

**Ano**
</dt> <dd>

O ano para o instantâneo no tempo.

</dd> <dt>

**Mês**
</dt> <dd>

O mês do instantâneo no tempo.

</dd> <dt>

**Day**
</dt> <dd>

O dia do instante no tempo.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

O dia da semana para o instante no tempo.

</dd> <dt>

**Hora**
</dt> <dd>

A hora do instante no tempo.

</dd> <dt>

**Minuto**
</dt> <dd>

O minuto para o instante no tempo.

</dd> <dt>

**Segundo**
</dt> <dd>

O segundo para o instantâneo no tempo.

</dd> <dt>

**Carrapato**
</dt> <dd>

O tique para o instante no tempo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de suporte a idiomas nacionais](national-language-support-structures.md)
</dt> </dl>

 

 




