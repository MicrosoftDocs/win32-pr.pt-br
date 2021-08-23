---
description: 'Saiba mais sobre: Método Api.JetBeginTransaction'
title: Método Api.JetBeginTransaction
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7dfd2e5b9c2aeac93d2099580dce69e8ca66db54b03d33477fbb0c4a918f20f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983616"
---
# <a name="apijetbegintransaction-method"></a>Método Api.JetBeginTransaction

Faz com que uma sessão insira uma transação ou crie um novo ponto de salvar em uma transação existente.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão para a que iniciar a transação.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
