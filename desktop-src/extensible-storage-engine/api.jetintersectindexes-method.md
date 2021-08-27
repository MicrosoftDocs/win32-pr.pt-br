---
description: 'Saiba mais sobre: método API. JetIntersectIndexes'
title: Método API. JetIntersectIndexes
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b2e9e259d9c90a3067931fbba425ab1b21e5c2a36a73563f593d3b280a40496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978026"
---
# <a name="apijetintersectindexes-method"></a>Método API. JetIntersectIndexes

Computa a interseção entre vários conjuntos de entradas de índice de índices secundários diferentes na mesma tabela. Essa operação é útil para localizar o conjunto de registros em uma tabela que corresponde a dois ou mais critérios que podem ser expressos usando intervalos de índice. Consulte também [IntersectIndexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - ranges  
    Escreva \[\]  
    
    Um índice varia para interseção. O tableids nos intervalos deve ter intervalos de índice definidos neles. Use [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) para criar um intervalo de índice.

<!-- end list -->

  - numRanges  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O número de intervalos de índice.

<!-- end list -->

  - registros da  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RECORDLIST](./jet-recordlist-class.md)  
    
    Retorna informações sobre a tabela temporária que contém os resultados da interseção.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)  
    
    Opções de interseção.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
