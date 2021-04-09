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
# <a name="jet_pfnrealloc-delegate"></a><span data-ttu-id="84e82-103">JET_PFNREALLOC delegado</span><span class="sxs-lookup"><span data-stu-id="84e82-103">JET_PFNREALLOC delegate</span></span>

<span data-ttu-id="84e82-104">Retorno de chamada usado pelo JetEnumerateColumns para alocar memória para seus buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="84e82-104">Callback used by JetEnumerateColumns to allocate memory for its output buffers.</span></span>

<span data-ttu-id="84e82-105">Esta API não está em conformidade com CLS.</span><span class="sxs-lookup"><span data-stu-id="84e82-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="84e82-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="84e82-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="84e82-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="84e82-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="84e82-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84e82-108">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="84e82-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84e82-109">Parameters</span></span>

  - <span data-ttu-id="84e82-110">contexto</span><span class="sxs-lookup"><span data-stu-id="84e82-110">context</span></span>  
    <span data-ttu-id="84e82-111">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="84e82-111">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="84e82-112">Contexto fornecido para JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="84e82-112">Context given to JetEnumerateColumns.</span></span>

<!-- end list -->

  - <span data-ttu-id="84e82-113">memória</span><span class="sxs-lookup"><span data-stu-id="84e82-113">memory</span></span>  
    <span data-ttu-id="84e82-114">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="84e82-114">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="84e82-115">Se for diferente de zero, um ponteiro para um bloco de memória alocado anteriormente por esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="84e82-115">If non-zero, a pointer to a memory block previously allocated by this callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="84e82-116">requestedSize</span><span class="sxs-lookup"><span data-stu-id="84e82-116">requestedSize</span></span>  
    <span data-ttu-id="84e82-117">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="84e82-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="84e82-118">O novo tamanho do bloco de memória (em bytes).</span><span class="sxs-lookup"><span data-stu-id="84e82-118">The new size of the memory block (in bytes).</span></span> <span data-ttu-id="84e82-119">Se for 0 e um bloco de memória for especificado, esse bloco de memória será liberado.</span><span class="sxs-lookup"><span data-stu-id="84e82-119">If this is 0 and a memory block is specified, that memory block will be freed.</span></span>

#### <a name="return-value"></a><span data-ttu-id="84e82-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84e82-120">Return value</span></span>

<span data-ttu-id="84e82-121">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="84e82-121">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
<span data-ttu-id="84e82-122">Um ponteiro para a memória alocada recentemente.</span><span class="sxs-lookup"><span data-stu-id="84e82-122">A pointer to newly allocated memory.</span></span> <span data-ttu-id="84e82-123">Se não for possível alocar memória, [zero](/dotnet/api/system.intptr.zero) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="84e82-123">If memory could not be allocated then [Zero](/dotnet/api/system.intptr.zero) should be returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="84e82-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="84e82-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="84e82-125">Referência</span><span class="sxs-lookup"><span data-stu-id="84e82-125">Reference</span></span>

[<span data-ttu-id="84e82-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="84e82-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
