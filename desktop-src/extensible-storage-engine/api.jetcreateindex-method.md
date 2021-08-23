---
description: 'Saiba mais sobre: Método Api.JetCreateIndex'
title: Método Api.JetCreateIndex
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df24e16252ec3aa837b9232859bf56726ee54b09448a57572281fab97a28c5c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670546"
---
# <a name="apijetcreateindex-method"></a>Método Api.JetCreateIndex

Cria um índice sobre dados em um banco de dados ESE. Um índice pode ser usado para localizar dados específicos rapidamente.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - Tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    A tabela na que o índice será criado.

<!-- end list -->

  - indexName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do índice a ser criado.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)  
    
    Opções de criação de índice.

<!-- end list -->

  - keyDescription  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Ponteiro para uma cadeia de caracteres terminada em nulo dupla de tokens delimitados por nulo.

<!-- end list -->

  - keyDescriptionLength  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O comprimento, em caracteres, de szKey, incluindo os dois nulos de terminação.

<!-- end list -->

  - densidade  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Densidade de árvore B+ inicial.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
