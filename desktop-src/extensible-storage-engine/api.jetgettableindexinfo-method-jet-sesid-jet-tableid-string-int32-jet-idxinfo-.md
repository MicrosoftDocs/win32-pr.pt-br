---
description: 'Saiba mais sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100742
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
ms.openlocfilehash: 28a3baab31c9d819dbef2fa6654504341bf0a86824ee4a2bd23ac5d081028763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786750"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-int32-jet_idxinfo"></a>Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)

Recupera informações sobre índices em uma tabela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As Integer
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out int result,
    JET_IdxInfo infoLevel
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
    
    O nome do índice.

<!-- end list -->

  - result  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Preenchido com informações sobre índices na tabela.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)  
    
    O tipo de informações a serem recuperadas.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetGetTableIndexInfo](./api.jetgettableindexinfo-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
