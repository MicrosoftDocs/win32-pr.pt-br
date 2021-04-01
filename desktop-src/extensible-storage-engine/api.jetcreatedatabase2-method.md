---
description: 'Saiba mais sobre: método API. JetCreateDatabase2'
title: Método API. JetCreateDatabase2
TOCTitle: 'JetCreateDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatedatabase2(v=EXCHG.10)
ms:contentKeyID: 55100671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8293a7c98451b0fd8bc46fbc13dde6b477a0ad09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646649"
---
# <a name="apijetcreatedatabase2-method"></a>Método API. JetCreateDatabase2

Cria e anexa um arquivo de banco de dados com um tamanho máximo de banco de dados especificado.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetCreateDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As CreateDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim dbid As JET_DBID
Dim grbit As CreateDatabaseGrbitApi.JetCreateDatabase2(sesid, database, _
    maxPages, dbid, grbit)
```

``` csharp
public static void JetCreateDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    out JET_DBID dbid,
    CreateDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - Banco de Dados  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O caminho para o arquivo de banco de dados a ser criado.

<!-- end list -->

  - maxPages  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O tamanho máximo, em páginas de banco de dados, do banco de dados. Passar 0 significa que não há um máximo imposto.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Retorna o DBID do novo banco de dados.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. ESENT. Interop. CreateDatabaseGrbit](./createdatabasegrbit-enumeration.md)  
    
    Opções de criação de banco de dados.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
