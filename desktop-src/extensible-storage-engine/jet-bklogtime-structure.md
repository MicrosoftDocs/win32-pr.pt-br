---
description: 'Saiba mais sobre: estrutura de JET_BKLOGTIME'
title: Estrutura de JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: b34740d582e341cce3b2fd0b28203b7346a4de1d94a8586289be8ab252247943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487718"
---
# <a name="jet_bklogtime-structure"></a>Estrutura de JET_BKLOGTIME


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_bklogtime-structure"></a>Estrutura de JET_BKLOGTIME

A estrutura de **JET_BKLOGTIME** contém os elementos de data e hora de um evento. É uma extensão de [JET_LOGTIME](./jet-logtime-structure.md).

**Windows vista: JET_BKLOGTIME** é introduzido no Windows Vista.

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Membros

**bSeconds**

A hora do evento em segundos. Isso pode ser 0 (zero) a 60. 0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".

**bMinutes**

A hora do evento em minutos. Isso pode ser 0 (zero) a 60. 0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".

**bHours**

A hora do evento em horas. Isso pode ser 0 (zero) a 24. 0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".

**bDay**

O dia do mês do evento. Isso pode ser 0 (zero) a 31. 0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".

**bMonth**

O mês do ano do evento. Isso pode ser 0 (zero) a 12. 0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".

**bYear**

O ano (deslocamento de 1900) do evento. Para obter o ano real, adicione 1900 a esse valor. 0 (zero) é usado quando a estrutura de **JET_BKLOGTIME** é "NULL".

**bFiller1**

Esse campo deve ser ignorado.

**fTimeIsUTC**

A hora está no formato UTC.

**fUnused**

Esse campo deve ser ignorado.

**bFiller2**

Esse campo deve ser ignorado.

**fOSSnapshot**

Se esse evento for um backup, esse sinalizador conterá um dos seguintes valores possíveis:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>backup de streaming</p></td>
<td><p>0 (zero)</p></td>
</tr>
<tr class="even">
<td><p>backup de instantâneo</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**fReserved**

Esse campo deve ser ignorado.

### <a name="remarks"></a>Comentários

Essa estrutura é usada durante a depuração.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>requer o Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
