---
description: 'Saiba mais sobre: método API. JetResetSessionContext'
title: Método API. JetResetSessionContext
TOCTitle: 'JetResetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a34a6c2922c0041f0720b498855b15c4aed23f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807151"
---
# <a name="apijetresetsessioncontext-method"></a>Método API. JetResetSessionContext

Desassocia uma sessão do thread atual. Isso deve ser usado em conjunto com [JetSetSessionContext (JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetResetSessionContext ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetResetSessionContext(sesid)
```

``` csharp
public static void JetResetSessionContext(
    JET_SESID sesid
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
