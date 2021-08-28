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
ms.openlocfilehash: 3ddf6f7b2ef129ab620a61616d975c8b8470022e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470782"
---
# <a name="jet_retinfo-structure"></a>Estrutura de JET_RETINFO


_**Aplica-se a:** Windows | Windows Servidor_

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


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
