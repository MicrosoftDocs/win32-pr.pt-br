---
description: 'Saiba mais sobre: estrutura de JET_LOGTIME'
title: Estrutura de JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103664131"
---
# <a name="jet_logtime-structure"></a>Estrutura de JET_LOGTIME


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_logtime-structure"></a>Estrutura de JET_LOGTIME

A estrutura de **JET_LOGTIME** contém elementos da data e hora de um evento.

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>Membros

**bSeconds**

A hora do evento em segundos. Esse valor pode ser de 0 a 59. 0 é usado quando a estrutura é nula.

**bMinutes**

A hora do evento em minutos. Esse valor pode ser de 0 a 59. 0 é usado quando a estrutura é nula.

**bHours**

A hora do evento em horas. Esse valor pode ser de 0 a 23. 0 é usado quando a estrutura é nula.

**bDay**

O dia do mês do evento. Esse valor pode ser de 0 a 31. 0 é usado quando a estrutura é nula.

**bMonth**

O mês do ano do evento. Esse valor pode ser de 0 a 12. 0 é usado quando a estrutura é nula.

**bYear**

O ano do evento (offset de 1900). Para obter o ano real, adicione 1900 a esse valor. 0 é usado quando a estrutura é nula.

**bFiller1**

Esse campo deve ser ignorado.

**fTimeIsUTC**

A hora está no formato UTC.

**fUnused**

Esse campo deve ser ignorado.

**bFiller2**

Esse campo deve ser ignorado.

### <a name="remarks"></a>Comentários

Essa estrutura destina-se principalmente ao uso na depuração.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
