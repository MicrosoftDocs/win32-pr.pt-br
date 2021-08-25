---
description: 'Saiba mais sobre: Método Api.JetSetSessionContext'
title: Método Api.JetSetSessionContext
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5530988aff70589493645afb2bf0b78da63470a1f48d1619913fbfdf8d8c8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977596"
---
# <a name="apijetsetsessioncontext-method"></a>Método Api.JetSetSessionContext

Associa uma sessão ao thread atual usando o alça de contexto determinado. Essa associação substitui o requisito de mecanismo padrão de que uma transação para uma determinada sessão deve ocorrer inteiramente no mesmo thread. Use [JetResetSessionContext(JET_SESID) para](./api.jetresetsessioncontext-method.md) remover a associação.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão na qual definir o contexto.

<!-- end list -->

  - contexto  
    Tipo: [System.IntPtr](/dotnet/api/system.intptr)  
    
    O contexto a ser definido.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
