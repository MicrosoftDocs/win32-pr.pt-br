---
description: 'Saiba mais sobre: estrutura de JET_SETINFO'
title: Estrutura de JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506549"
---
# <a name="jet_setinfo-structure"></a>Estrutura de JET_SETINFO


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_setinfo-structure"></a>Estrutura de JET_SETINFO

A estrutura de **JET_SETINFO** contém parâmetros de entrada opcionais para [JetSetColumn](./jetsetcolumn-function.md). Um ponteiro **nulo** pode ser passado onde um ponteiro para essa estrutura, de outra forma, seria passado. O significado de passar um **NULL** é o mesmo que passar **JET_SETINFO** com **cbStruct** definido como sizeof (JET_SETINFO), **ibLongValue** definido como 0 (zero) e **itagSequence** definido como 1.

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho, em bytes, do **JET_SETINFO**. Esse valor confirma a presença dos campos a seguir.

**ibLongValue**

O deslocamento para o primeiro byte a ser definido em uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

Descreve o número de sequência do valor em uma coluna de valores múltiplos a ser definida. A matriz de valores é baseada em um. O primeiro valor é Sequence 1, não 0 (zero). Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como **itagSequence** se esse valor estiver sendo substituído. Um valor de 0 (zero) significa adicionar uma nova instância de valor de coluna ao final da sequência de valores de coluna.

Com uma coluna que pode conter vários valores, só é possível usar um número de sequência maior que 1 em [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 em [JetSetColumn](./jetsetcolumn-function.md). Na implementação atual do mecanismo, qualquer coluna criada com JET_bitColumnTagged pode conter vários valores. Colunas criadas com JET_bitColumnMultiValued diferem de colunas marcadas com vários valores apenas na forma como são indexadas. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter mais informações.

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

[JetSetColumn](./jetsetcolumn-function.md)
