---
description: 'Saiba mais sobre: método API. JetSetColumnDefaultValue'
title: Método API. JetSetColumnDefaultValue
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 643e056acc99aba255b1c94b2d72337ccaf9f7668caf9c937f08dce7f9214ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084945"
---
# <a name="apijetsetcolumndefaultvalue-method"></a>Método API. JetSetColumnDefaultValue

Altera o valor padrão de uma coluna existente.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    O banco de dados que contém a coluna.

<!-- end list -->

  - tableName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O nome da tabela que contém a coluna.

<!-- end list -->

  - columnName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O nome da coluna.

<!-- end list -->

  - data  
    Escreva \[\]  
    
    O novo valor padrão.

<!-- end list -->

  - dataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Tamanho do novo valor padrão.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)  
    
    Opções de valor padrão da coluna.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
