---
description: 'Saiba mais sobre: método EsentResource. Dispose (booliano)'
title: Método EsentResource. Dispose (booliano)
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
ms.openlocfilehash: cf74291bf4c54ffa1d61c28bf7caff1e8c2b231b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172115"
---
# <a name="esentresourcedispose-method-boolean"></a><span data-ttu-id="eb0e6-103">Método EsentResource. Dispose (booliano)</span><span class="sxs-lookup"><span data-stu-id="eb0e6-103">EsentResource.Dispose method (Boolean)</span></span>

<span data-ttu-id="eb0e6-104">Chamado por Dispose e o finalizador.</span><span class="sxs-lookup"><span data-stu-id="eb0e6-104">Called by Dispose and the finalizer.</span></span>

<span data-ttu-id="eb0e6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb0e6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb0e6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb0e6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0e6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb0e6-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="eb0e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb0e6-108">Parameters</span></span>

  - <span data-ttu-id="eb0e6-109">isdisposição</span><span class="sxs-lookup"><span data-stu-id="eb0e6-109">isDisposing</span></span>  
    <span data-ttu-id="eb0e6-110">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="eb0e6-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
    
    <span data-ttu-id="eb0e6-111">True se chamado de Dispose.</span><span class="sxs-lookup"><span data-stu-id="eb0e6-111">True if called from Dispose.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb0e6-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb0e6-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb0e6-113">Referência</span><span class="sxs-lookup"><span data-stu-id="eb0e6-113">Reference</span></span>

[<span data-ttu-id="eb0e6-114">Classe EsentResource</span><span class="sxs-lookup"><span data-stu-id="eb0e6-114">EsentResource class</span></span>](./esentresource-class.md)

[<span data-ttu-id="eb0e6-115">Membros do EsentResource</span><span class="sxs-lookup"><span data-stu-id="eb0e6-115">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="eb0e6-116">Descartar sobrecarga</span><span class="sxs-lookup"><span data-stu-id="eb0e6-116">Dispose overload</span></span>](./esentresource.dispose-method.md)

[<span data-ttu-id="eb0e6-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="eb0e6-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
