---
description: 'Saiba mais sobre: propriedade IndexInfo.Keys'
title: Propriedade IndexInfo.Keys
TOCTitle: 'Keys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.Keys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.keys(v=EXCHG.10)
ms:contentKeyID: 55103265
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.Keys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.Keys
- Microsoft.Isam.Esent.Interop.IndexInfo.get_Keys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c10deabe07a261f84ae3d321fce0120792309eaf48f9623aed0021a62c85585e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980596"
---
# <a name="indexinfokeys-property"></a>Propriedade IndexInfo.Keys

Obtém o número de chaves exclusivas no índice. Esse valor não é atual e só é atualizado por Api.JetComputeStats.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property Keys As Integer
    Get
'Usage
Dim instance As IndexInfo
Dim value As Integer

value = instance.Keys
```

``` csharp
public int Keys { get; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe IndexInfo](./indexinfo-class.md)

[Membros indexInfo](./indexinfo-members.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
