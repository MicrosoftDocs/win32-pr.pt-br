---
description: 'Saiba mais sobre: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826811"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_columnid"></a>JET_COLUMNID

O tipo de dados **JET_COLUMNID** identifica uma coluna dentro de uma tabela.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Tipos de dados

JET_COLUMNID

Identifica uma coluna dentro de uma tabela.

### <a name="remarks"></a>Comentários

As IDs de coluna são exclusivas em uma única tabela. Depois que uma coluna tiver uma determinada ID de coluna, ela sempre terá essa ID de coluna. A restauração do backup não alterará o valor de uma ID de coluna. No entanto, se uma ou mais colunas de tabela, antes de uma coluna de tabela específica, forem excluídas, um banco de dados compacto poderá alterar o valor de uma ID de coluna.

Em alguns casos, as IDs de coluna são os únicos meios de identificar colunas. Quando uma tabela temporária é criada, suas colunas não têm nomes, mas uma matriz de IDs de coluna é retornada pela função de criação.

As colunas em tabelas diferentes podem ter a mesma ID de coluna.

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

