---
description: 'Saiba mais sobre: estrutura de JET_LGPOS'
title: Estrutura de JET_LGPOS
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: abf3ca2996e75d2abfe6fc766ec6f5bbd30054eeb9dd8406fe2747307a00c4a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109253"
---
# <a name="jet_lgpos-structure"></a>Estrutura de JET_LGPOS


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_lgpos-structure"></a>Estrutura de JET_LGPOS

A estrutura de **JET_LGPOS** contém dados internos ao mecanismo de log do mecanismo de banco de dados. Essa estrutura é considerada interna.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Membros

**IB**

Dá suporte à infraestrutura ESE e não pode ser usada no seu código.

**iSEC Partners**

Dá suporte à infraestrutura ESE e não pode ser usada no seu código.

**lGeneration**

Dá suporte à infraestrutura ESE e não pode ser usada no seu código.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
