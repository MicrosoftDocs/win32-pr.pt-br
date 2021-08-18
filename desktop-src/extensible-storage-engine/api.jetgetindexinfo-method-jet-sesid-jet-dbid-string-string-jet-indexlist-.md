---
description: 'Saiba mais sobre: Método Api.JetGetIndexInfo (JET_SESID, JET_DBID, cadeia de caracteres, cadeia de caracteres, JET_INDEXLIST)'
title: Método Api.JetGetIndexInfo (JET_SESID, JET_DBID, cadeia de caracteres, cadeia de caracteres, JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1e12b64655b4c2db3d378f9bcde985fd3684cdb8beb24ac6ad9ecddc84f8b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983310"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a>Método Api.JetGetIndexInfo (JET_SESID, JET_DBID, cadeia de caracteres, cadeia de caracteres, JET_INDEXLIST)

**OBSERVAÇÃO: essa API agora está obsoleta.**

Recupera informações sobre índices em uma tabela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    O banco de dados a ser usado.

<!-- end list -->

  - tablename  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    O nome da tabela sobre a que recuperar informações de índice.

<!-- end list -->

  - ignorado  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Este parâmetro é ignorado.

<!-- end list -->

  - indexlist  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)  
    
    Preenchido com informações sobre índices na tabela.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga JetGetIndexInfo](./api.jetgetindexinfo-method.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
