---
description: 'Saiba mais sobre: JET_PFNREALLOC delegado'
title: JET_PFNREALLOC delegado
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922846"
---
# <a name="jet_pfnrealloc-delegate"></a>JET_PFNREALLOC delegado

Retorno de chamada usado pelo JetEnumerateColumns para alocar memória para seus buffers de saída.

Esta API não está em conformidade com CLS. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a>Parâmetros

  - contexto  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexto fornecido para JetEnumerateColumns.

<!-- end list -->

  - memória  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Se for diferente de zero, um ponteiro para um bloco de memória alocado anteriormente por esse retorno de chamada.

<!-- end list -->

  - requestedSize  
    Tipo: [System. UInt32](/dotnet/api/system.uint32)  
    
    O novo tamanho do bloco de memória (em bytes). Se for 0 e um bloco de memória for especificado, esse bloco de memória será liberado.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
Um ponteiro para a memória alocada recentemente. Se não for possível alocar memória, [zero](/dotnet/api/system.intptr.zero) deverá ser retornado.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
