---
description: 'Saiba mais sobre: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761223"
---
# <a name="jet_pwstr"></a>JET_PWSTR


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_pwstr"></a>JET_PWSTR

O tipo de dados **JET_PWSTR** contém uma cadeia de caracteres **Unicode** terminada em nulo (Char \* ).

**Windows Vista: a JET_PWSTR** é introduzida no Windows Vista.

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a>Tipos de dados

JET_PWSTR

Terminação nula, Cadeia de caracteres Unicode (Char \* ).

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

