---
description: 'Saiba mais sobre: método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, Cadeia de caracteres JET_OBJECTINFO)'
title: Método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, String JET_OBJECTINFO)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_objtyp,System.String,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100733
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffa80b7a3a1815d16d28682f45d553945988f4af1bbec3a05cba3a8592efb624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042584"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objtyp-string-jet_objectinfo"></a>Método API. JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, String JET_OBJECTINFO)

Recupera informações sobre objetos de banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    objtyp As JET_objtyp, _
    objectName As String, _
    <OutAttribute> ByRef objectinfo As JET_OBJECTINFO _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objtyp As JET_objtyp
Dim objectName As String
Dim objectinfo As JET_OBJECTINFOApi.JetGetObjectInfo(sesid, dbid, _
    objtyp, objectName, objectinfo)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_objtyp objtyp,
    string objectName,
    out JET_OBJECTINFO objectinfo
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    O banco de dados a ser usado.

<!-- end list -->

  - objtyp  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_objtyp](./jet-objtyp-enumeration.md)  
    
    O tipo do objeto.

<!-- end list -->

  - objectName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O nome do objeto sobre o qual recuperar informações.

<!-- end list -->

  - ObjectInfo  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)  
    
    Preenchido com informações sobre os objetos no banco de dados.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetGetObjectInfo](./api.jetgetobjectinfo-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
