---
description: 'Saiba mais sobre: JET_PCSTR'
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 2786435822fefb56b09c3bb434612dc1fbf13f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172085"
---
# <a name="jet_pcstr"></a>JET_PCSTR


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_pcstr"></a>JET_PCSTR

O tipo de dados **JET_PCSTR** contém uma cadeia de caracteres **ASCII** de constante de terminação nula (Char \* ).

**Windows Vista: a JET_PCSTR** é introduzida no Windows Vista.

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a>Tipos de dados

JET_PCSTR

Cadeia de caracteres ASCII de constante terminada em nulo (Char \* ).

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>

