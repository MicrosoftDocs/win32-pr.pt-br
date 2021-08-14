---
description: 'Saiba mais sobre: JET_PCWSTR'
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 3958baa23228bdf32807cc4fdc07a471e625d553f57672e318a062038923b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473886"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_pcwstr"></a>JET_PCWSTR

O **JET_PCWSTR** de dados contém uma cadeia de caracteres **Unicode** constante terminada em nulo (char \* ).

**Windows Vista: JET_PCWSTR** é introduzido no Windows Vista.

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>Tipos de dados

JET_PCWSTR

Cadeia de caracteres Unicode constante terminada em nulo (char \* ).

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>

