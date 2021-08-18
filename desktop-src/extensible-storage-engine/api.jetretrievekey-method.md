---
description: 'Saiba mais sobre: Método Api.JetRetrieveKey'
title: Método Api.JetRetrieveKey
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 161840971181db3594257b1ae2440c3c1c06b35a871b21c4cbeddad56527a9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118783897"
---
# <a name="apijetretrievekey-method"></a>Método Api.JetRetrieveKey

Recupera a chave para a entrada de índice na posição atual de um cursor. Consulte também [RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - Tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    O cursor do onde recuperar a chave.

<!-- end list -->

  - data  
    Tipo: \[\]  
    
    O buffer no que recuperar a chave.

<!-- end list -->

  - dataSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    O tamanho do buffer.

<!-- end list -->

  - actualDataSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Retorna o tamanho real dos dados.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)  
    
    Recuperar opções de chave.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
