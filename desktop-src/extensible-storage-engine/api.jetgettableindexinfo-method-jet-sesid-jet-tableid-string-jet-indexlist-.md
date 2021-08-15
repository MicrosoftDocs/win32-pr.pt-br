---
description: 'Saiba mais sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String JET_INDEXLIST)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String JET_INDEXLIST)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100752
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9fcdc0916d09bbe2dfa9e44ec4bdc0fa3bae8e0dda2148f327ca62f28c131b8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272318"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist"></a>Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String JET_INDEXLIST)

**Observação: essa API agora está obsoleta.**

Recupera informações sobre índices em uma tabela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim indexlist As JET_INDEXLISTApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    A tabela da qual recuperar informações de índice.

<!-- end list -->

  - IndexName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Este parâmetro é ignorado.

<!-- end list -->

  - IndexList  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)  
    
    Preenchido com informações sobre índices na tabela.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetGetTableIndexInfo](./api.jetgettableindexinfo-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
