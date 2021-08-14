---
description: 'Saiba mais sobre: Conversão implícita de sessão (sessão para JET_SESID)'
title: Conversão implícita de sessão (sessão em JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be293636044e744ec02e3bdcddbc96b61373a35c9bddc04a03d282fcebe268d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485505"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a>Conversão implícita de sessão (sessão em JET_SESID)

Operador de conversão implícita de uma sessão em um JET_SESID. Isso permite que uma sessão seja usada com APIs que esperam um JET_SESID.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a>Parâmetros

  - sessão  
    Tipo: [Microsoft.Isam.Esent.Interop.Session](./session-class.md)  
    
    A sessão a ser convertida.

#### <a name="return-value"></a>Valor retornado

Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
O JET_SESID da sessão.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe da sessão](./session-class.md)

[Membros da sessão](./session-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
