---
description: 'Saiba mais sobre: estrutura de JET_BKINFO'
title: Estrutura de JET_BKINFO
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171358"
---
# <a name="jet_bkinfo-structure"></a>Estrutura de JET_BKINFO


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>Estrutura de JET_BKINFO

A estrutura de **JET_BKINFO** contém uma coleção de dados sobre um evento de backup específico.

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

A ID deste backup.

**logtimeMark**

A hora deste evento de backup.

**bklogtimeMark**

A hora desse evento de backup, com bits adicionais para indicar um backup de instantâneo.

**Windows Vista: o bklogtimeMark** é introduzido no Windows Vista.

**genLow**

O número de geração de log baixo associado a este evento de backup.

**genHigh**

O número de geração de log alto associado a este evento de backup.

### <a name="remarks"></a>Comentários

Essa estrutura é usada dentro da estrutura de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) para representar dados sobre o evento de backup do banco de dado.

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
