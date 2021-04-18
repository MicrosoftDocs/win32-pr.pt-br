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
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780138"
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

**Dourado**
</dt> <dd>

As informações de era para o instante em tempo.

</dd> <dt>

**Year**
</dt> <dd>

O ano para o instante no tempo.

</dd> <dt>

**Mês**
</dt> <dd>

O mês para o instante no tempo.

</dd> <dt>

**Day**
</dt> <dd>

O dia para o instante no tempo.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

O dia da semana para o instante no tempo.

</dd> <dt>

**Hora**
</dt> <dd>

A hora para o instante no tempo.

</dd> <dt>

**Demorar**
</dt> <dd>

O minuto para o instante no tempo.

</dd> <dt>

**Microssegundo**
</dt> <dd>

O segundo para o instante no tempo.

</dd> <dt>

**Traços**
</dt> <dd>

O tique para o instante no tempo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de suporte ao idioma nacional](national-language-support-structures.md)
</dt> </dl>

 

 




