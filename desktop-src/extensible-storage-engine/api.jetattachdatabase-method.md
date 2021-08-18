---
description: 'Saiba mais sobre: método API. JetAttachDatabase'
title: Método API. JetAttachDatabase
TOCTitle: 'JetAttachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100652
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f81e70898165c2aa7882675620ed217efa79739aed12469685defd27c68a45d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983666"
---
# <a name="apijetattachdatabase-method"></a>Método API. JetAttachDatabase

Anexa um arquivo de banco de dados para uso com uma instância de banco de dados. Para usar o banco de dados, será necessário abri-lo subsequentemente com [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function JetAttachDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase(sesid, _
    database, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase(
    JET_SESID sesid,
    string database,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - Banco de Dados  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O banco de dados a ser anexado.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)  
    
    Opções de anexação.

#### <a name="return-value"></a>Valor retornado

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Um código de aviso de ESENT.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
