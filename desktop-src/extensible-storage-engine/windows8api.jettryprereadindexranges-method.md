---
description: 'Saiba mais sobre: método Windows8Api. JetTryPrereadIndexRanges'
title: Método Windows8Api. JetTryPrereadIndexRanges (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9664e658254de057b0e3aa8ae86813eb996a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813317"
---
# <a name="windows8apijettryprereadindexranges-method"></a>Método Windows8Api. JetTryPrereadIndexRanges

Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    A tabela na qual os itens são relidos.

<!-- end list -->

  - indexRanges  
    Escreva \[\]  
    
    Os intervalos de chave a serem lidos.

<!-- end list -->

  - rangeIndex  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O índice do primeiro intervalo de chaves na matriz a ser lido.

<!-- end list -->

  - rangeCount  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O número máximo de intervalos de chave a serem lidos.

<!-- end list -->

  - rangesPreread  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Retorna o número de chaves que realmente são conlidas.

<!-- end list -->

  - columnsPreread  
    Escreva \[\]  
    
    Lista de IDs de coluna para colunas de valor longo a serem lidas.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)  
    
    Opções de preread. Usado para especificar a direção da subleitura.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
**\[ true \]** se alguma preread estiver concluída; caso contrário, **\[ false \]** .  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe Windows8Api](./windows8api-class.md)

[Membros do Windows8Api](./windows8api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
