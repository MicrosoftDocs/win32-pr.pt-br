---
description: 'Saiba mais sobre: estrutura de JET_RECPOS'
title: Estrutura de JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793383"
---
# <a name="jet_recpos-structure"></a>Estrutura de JET_RECPOS


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_recpos-structure"></a>Estrutura de JET_RECPOS

A estrutura de **JET_RECPOS** contém uma coleção de inteiros que representam uma posição fracionária dentro de um índice. **centriesLT** é o número de entradas de índice menor que a chave de índice atual. **centriesInRange** é o número de entradas de índice iguais à chave atual. **centriesInRange** não tem suporte e sempre é retornado como 1. **centriesTotal** é o número de entradas de índice no índice. Todos os valores são aproximações sem nenhuma garantia de precisão.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura de [JET_RETINFO](./jet-retinfo-structure.md) , em bytes. Esse valor confirma a presença dos campos a seguir.

**centriesLT**

O número aproximado de entradas de índice menores que a chave atual.

**centriesInRange**

O número aproximado de entradas de índice iguais à chave atual. Esse campo é sempre definido como 1, independentemente do número de entradas de índice que são realmente iguais à chave atual.

**centriesTotal**

O número aproximado de entradas no índice.

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

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
