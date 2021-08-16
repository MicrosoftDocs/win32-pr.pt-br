---
description: 'Saiba mais sobre: estrutura JET_BKINFO dados'
title: estrutura JET_BKINFO de JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 9f391d711c6d10c50cfdb26314be6ee709ff481bda0ce370faa28d514422444c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487861"
---
# <a name="jet_bkinfo-structure"></a>estrutura JET_BKINFO de JET_BKINFO


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_bkinfo-structure"></a>estrutura JET_BKINFO de JET_BKINFO

A **JET_BKINFO** contém uma coleção de dados sobre um evento de backup específico.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Membros

**lgposMark**

A ID desse backup.

**logtimeMark**

A hora desse evento de backup.

**bklogtimeMark**

A hora desse evento de backup, com bits adicionais para indicar um backup de instantâneo.

**Windows Vista: bklogtimeMark** é introduzido no Windows Vista.

**genLow**

O número de geração de log baixo associado a esse evento de backup.

**genHigh**

O número de geração de log alto associado a esse evento de backup.

### <a name="remarks"></a>Comentários

Essa estrutura é usada dentro da estrutura [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) para representar dados sobre o evento de backup de banco de dados.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
