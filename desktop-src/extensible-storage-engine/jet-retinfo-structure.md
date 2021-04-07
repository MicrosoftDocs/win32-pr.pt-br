---
description: 'Saiba mais sobre: estrutura de JET_RETINFO'
title: Estrutura de JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827313"
---
# <a name="jet_retinfo-structure"></a>Estrutura de JET_RETINFO


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_retinfo-structure"></a>Estrutura de JET_RETINFO

A estrutura de **JET_RETINFO** contém parâmetros de entrada e saída opcionais para [JetRetrieveColumn](./jetretrievecolumn-function.md). Um ponteiro nulo pode ser passado onde um ponteiro para essa estrutura, de outra forma, seria passado. Passar um ponteiro NULL é o mesmo que passar **JET_RETINFO** com **cbStruct** definido como sizeof (JET_RETINFO), **ibLongValue** definido como 0 (zero) e **itagSequence** definido como 1.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>Membros

**cbStruct**

Deve ser definido como o tamanho da estrutura de **JET_RETINFO** , em bytes, e serve para confirmar a presença dos campos a seguir.

**ibLongValue**

O deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md). Observe que a quantidade de dados recuperados desse deslocamento é menor do que o tamanho do buffer de saída e do tamanho dos dados no valor real após esse deslocamento.

**itagSequence**

Descreve o número de sequência do valor em uma coluna com vários valores. Observe que a matriz de valores é baseada em um. O primeiro valor é Sequence 1, e não 0. Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como o **itagSequence**

Com uma coluna que pode conter vários valores, só é possível usar um número de sequência maior que 1 em [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 em [JetSetColumn](./jetsetcolumn-function.md). Na implementação atual do mecanismo, qualquer coluna criada com JET_bitColumnTagged pode conter vários valores. Colunas criadas com JET_bitColumnMultiValued diferem de colunas marcadas com vários valores apenas na forma como são indexadas. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter mais informações.

**columnidNextTagged**

Retorna o columnid da coluna undeleted, multi-Value ou esparso, quando todas as colunas marcadas são recuperadas passando 0 como columnid para [JetRetrieveColumn](./jetretrievecolumn-function.md).

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
