---
description: 'Saiba mais sobre: estrutura de JET_ENUMCOLUMNID'
title: Estrutura de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 21f28e160f1c31dac909e02bf64acba0ae230305
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479639"
---
# <a name="jet_enumcolumnid-structure"></a>Estrutura de JET_ENUMCOLUMNID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_enumcolumnid-structure"></a>Estrutura de JET_ENUMCOLUMNID

A estrutura de **JET_ENUMCOLUMNID** enumera um conjunto específico de colunas e, opcionalmente, um conjunto específico de vários valores para essas colunas quando a função [JetEnumerateColumns](./jetenumeratecolumns-function.md) é usada. [JetEnumerateColumns](./jetenumeratecolumns-function.md) retorna uma matriz de estruturas de **JET_ENUMCOLUMNID** .

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Membros

**columnid**

A ID da coluna a ser enumerada.

Se a ID da coluna for 0 (zero), a enumeração dessa coluna será ignorada e um slot correspondente na matriz de saída de estruturas de [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) será gerado com um estado de coluna de JET_wrnColumnSkipped.

**ctagSequence**

Opcionalmente, identifica uma matriz de valores de coluna (por índice baseado em um) para enumerar para a ID de coluna especificada.

Se **ctagSequence** for 0 (zero), **rgtagSequence** será ignorado e todos os valores de coluna para a ID de coluna especificada serão enumerados.

Se um elemento de **rgtagSequence** for 0 (zero), a enumeração desse valor de coluna (por índice baseado em um) será ignorada. Um slot correspondente na matriz de saída da estrutura de **JET_ENUMCOLUMNID** será gerado com um valor de status de coluna de JET_wrnColumnSkipped.

**rgtagSequence**

Uma matriz de índices baseados em um na matriz de valores de coluna para uma determinada coluna. Um único elemento é um **itagSequence** que é definido em [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Um **itagSequence** de 0 (zero) significa "ignorar". Um **itagSequence** de 1 significa retornar o primeiro valor de coluna da coluna, 2 significa o segundo e assim por diante.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
