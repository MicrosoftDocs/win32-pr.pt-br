---
description: 'Saiba mais sobre: método API. JetGetDatabaseFileInfo (cadeia de caracteres, JET_DBINFOMISC JET_DbInfo)'
title: Método API. JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,Microsoft.Isam.Esent.Interop.JET_DBINFOMISC@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d72711314312c843d9e456a5194cb6133b4f491f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090145"
---
# <a name="apijetgetdatabasefileinfo-method-string-jet_dbinfomisc-jet_dbinfo"></a>Método API. JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)

Recupera determinadas informações sobre o banco de dados especificado.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef dbinfomisc As JET_DBINFOMISC, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim dbinfomisc As JET_DBINFOMISC
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    dbinfomisc, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out JET_DBINFOMISC dbinfomisc,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a>Parâmetros

  - databaseName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O nome do arquivo do banco de dados.

<!-- end list -->

  - dbinfomisc  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)  
    
    O valor a ser recuperado.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)  
    
    Os dados específicos a serem recuperados.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetGetDatabaseFileInfo](./api.jetgetdatabasefileinfo-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
