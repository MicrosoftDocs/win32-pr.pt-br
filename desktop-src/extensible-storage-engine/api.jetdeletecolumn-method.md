---
description: 'Saiba mais sobre: método API. JetDeleteColumn'
title: Método API. JetDeleteColumn
TOCTitle: 'JetDeleteColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn(v=EXCHG.10)
ms:contentKeyID: 55100684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0801ffae0429b0c1d16d452d4170bdc6ce74937f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090155"
---
# <a name="apijetdeletecolumn-method"></a>Método API. JetDeleteColumn

Exclui uma coluna de uma tabela de banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetDeleteColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As StringApi.JetDeleteColumn(sesid, tableid, _
    column)
```

``` csharp
public static void JetDeleteColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Um cursor na tabela da qual excluir a coluna.

<!-- end list -->

  - coluna  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O nome da coluna a ser excluída.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
