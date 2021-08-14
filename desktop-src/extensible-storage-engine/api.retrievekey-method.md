---
description: 'Saiba mais sobre: Método Api.RetrieveKey'
title: Método Api.RetrieveKey
TOCTitle: 'RetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievekey(v=EXCHG.10)
ms:contentKeyID: 55100880
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70eb4900c1b3fc4ea8b66f138db4b51328ae019c15c6fdfc05d7b786a574d5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117717840"
---
# <a name="apiretrievekey-method"></a>Método Api.RetrieveKey

Recupera a chave para a entrada de índice na posição atual de um cursor.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function RetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As RetrieveKeyGrbit _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As RetrieveKeyGrbit
Dim returnValue As Byte()

returnValue = Api.RetrieveKey(sesid, _
    tableid, grbit)
```

``` csharp
public static byte[] RetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
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

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)  
    
    Recuperar opções de chave.

#### <a name="return-value"></a>Valor retornado

Tipo: \[\]  
A chave recuperada.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
