---
description: 'Saiba mais sobre: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105753507"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_grbit"></a>JET_GRBIT

O tipo de dados **JET_GRBIT** é um grupo de bits que contém constantes específicas para as funções e estruturas nas quais ele é usado.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipos de dados

JET_GRBIT

Em geral, as constantes usadas como valores para esse tipo de dados refletem o nome do elemento de API no qual elas são usadas. Por exemplo, todas as constantes passadas para [JetRetrieveColumn](./jetretrievecolumn-function.md) começam com "JET_bitRetrieve". Da mesma forma, todas as constantes passadas para [JetSetColumn](./jetsetcolumn-function.md) começam com "JET_bitSet".

Um valor de zero faz com que o parâmetro seja ignorado.

### <a name="remarks"></a>Comentários

Para obter mais informações, consulte a função ou estrutura específica. As opções geralmente são passadas como um conjunto de sinalizadores que podem ser combinados.

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

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
