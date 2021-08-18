---
description: 'Saiba mais sobre: estrutura JET_RETINFO dados'
title: estrutura JET_RETINFO dados
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
ms.openlocfilehash: a04ee087f036bf0d6a9e0bb4c9c558dbfe3ae5a8fc8e875973ef2930e7ba911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038724"
---
# <a name="jet_retinfo-structure"></a>estrutura JET_RETINFO dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_retinfo-structure"></a>estrutura JET_RETINFO dados

A **estrutura JET_RETINFO** contém parâmetros opcionais de entrada e saída para [JetRetrieveColumn](./jetretrievecolumn-function.md). Um ponteiro nulo pode ser passado para onde um ponteiro para essa estrutura seria passado de outra forma. Passar um ponteiro nulo é o mesmo que passar **JET_RETINFO** **com cbStruct** definido como sizeof(JET_RETINFO), **ibLongValue** definido como 0 (zero) e **itagSequence** definido como 1.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>Membros

**Cbstruct**

Deve ser definido como o tamanho da **estrutura JET_RETINFO,** em bytes, e serve para confirmar a presença dos campos a seguir.

**ibLongValue**

O deslocamento para o primeiro byte a ser recuperado de uma coluna do [tipo JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md). Observe que a quantidade de dados recuperados desse deslocamento é a menor do tamanho do buffer de saída e o tamanho dos dados no valor real após esse deslocamento.

**itagSequence**

Descreve o número de sequência de valor em uma coluna com vários valores. Observe que a matriz de valores é baseada em um. O primeiro valor é a sequência 1, não 0. Se a coluna de registro tiver apenas um valor, 1 deverá ser passado como **itagSequence**

Com uma coluna que pode conter vários valores, só é possível usar um número de sequência maior que 1 em [JetSetColumn](./jetsetcolumn-function.md) e [JetRetrieveColumn](./jetretrievecolumn-function.md) ou 0 em [JetSetColumn](./jetsetcolumn-function.md). Na implementação atual do mecanismo, qualquer coluna que foi criada com JET_bitColumnTagged pode conter vários valores. As colunas criadas com JET_bitColumnMultiValued são diferentes das colunas marcadas com vários valores apenas da maneira como são indexadas. Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter mais informações.

**columnidNextTagged**

Retorna a columnid da coluna marcada, com valor múltiplo ou esparso recuperada quando todas as colunas marcadas são recuperadas passando 0 como a columnid para [JetRetrieveColumn.](./jetretrievecolumn-function.md)

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
