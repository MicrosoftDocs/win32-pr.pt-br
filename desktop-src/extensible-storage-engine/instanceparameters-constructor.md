---
description: 'Saiba mais sobre: Construtor Instanceparameters'
title: Construtor instanceparameters
TOCTitle: 'InstanceParameters constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.InstanceParameters.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.instanceparameters(v=EXCHG.10)
ms:contentKeyID: 55107431
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.InstanceParameters
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 147cc3c68856744dc904d9dc730e44ad5c83b8593723b345e317f9c9602512b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618196"
---
# <a name="instanceparameters-constructor"></a>Construtor instanceparameters

Inicializa uma nova instância da classe Instanceparameters.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New InstanceParameters(instance)
```

``` csharp
public InstanceParameters(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância na qual definir parâmetros. Se isso for JET_INSTANCE. Nil, as configurações afetam as configurações padrão de instâncias futuras.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe instanceparameters](./instanceparameters-class.md)

[Membros de instanceparameters](./instanceparameters-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
