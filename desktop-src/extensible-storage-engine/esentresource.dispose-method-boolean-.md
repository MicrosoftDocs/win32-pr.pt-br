---
description: 'Saiba mais sobre: Método EsentResource.Dispose (booliana)'
title: Método EsentResource.Dispose (booliana)
TOCTitle: Dispose method (Boolean)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResource.Dispose(System.Boolean)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource.dispose(v=EXCHG.10)
ms:contentKeyID: 55102624
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource.Dispose
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cc2f9fab375e2ae2b9a27611192c3db9e3bba4eb272de1dfca243d13bf7766f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119477326"
---
# <a name="esentresourcedispose-method-boolean"></a>Método EsentResource.Dispose (booliana)

Chamado por Dispose e o finalizador.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Overridable Sub Dispose ( _
    isDisposing As Boolean _
)
'Usage
Dim isDisposing As Boolean

Me.Dispose(isDisposing)
```

``` csharp
protected virtual void Dispose(
    bool isDisposing
)
```

#### <a name="parameters"></a>Parâmetros

  - isDisposing  
    Tipo: [System.Boolean](/dotnet/api/system.boolean)  
    
    True se chamado de Dispose.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe EsentResource](./esentresource-class.md)

[Membros EsentResource](./esentresource-members.md)

[Sobrecarga de descarte](./esentresource.dispose-method.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
