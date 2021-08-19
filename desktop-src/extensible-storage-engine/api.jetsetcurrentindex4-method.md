---
description: 'Saiba mais sobre: método API. JetSetCurrentIndex4'
title: Método API. JetSetCurrentIndex4
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53b35384607e988c2456f4d48f93b49b6974b138e4a71ef8916b174a92a61611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118497880"
---
# <a name="apijetsetcurrentindex4-method"></a>Método API. JetSetCurrentIndex4

Define o índice atual de um cursor.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor no qual definir o índice.

<!-- end list -->

  - índice  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O nome do índice a ser selecionado. Se isso for nulo ou vazio, o índice primário será selecionado.

<!-- end list -->

  - indexid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    A ID do índice a ser selecionado. Essa ID pode ser obtida usando JetGetIndexInfo ou JetGetTableIndexInfo com a opção [IndexID](./jet-idxinfo-enumeration.md) .

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)  
    
    Definir opções de índice.

<!-- end list -->

  - itagSequence  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Número de sequência do valor de coluna com valores múltiplos que será usado para posicionar o cursor no novo índice. Esse parâmetro só é usado em conjunto com [nomove](./setcurrentindexgrbit-enumeration.md). Quando esse parâmetro não estiver presente ou estiver definido como zero, seu valor será presumido como 1.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
