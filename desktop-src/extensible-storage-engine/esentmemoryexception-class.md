---
description: 'Saiba mais sobre: classe EsentMemoryException'
title: Classe EsentMemoryException
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103837567"
---
# <a name="esentmemoryexception-class"></a><span data-ttu-id="c19f8-103">Classe EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="c19f8-103">EsentMemoryException class</span></span>

<span data-ttu-id="c19f8-104">Classe base para exceções de memória.</span><span class="sxs-lookup"><span data-stu-id="c19f8-104">Base class for Memory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c19f8-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="c19f8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c19f8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c19f8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c19f8-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c19f8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c19f8-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="c19f8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c19f8-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c19f8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c19f8-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c19f8-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c19f8-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="c19f8-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="c19f8-112">Microsoft. ISAM. ESENT. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="c19f8-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              

<span data-ttu-id="c19f8-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c19f8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c19f8-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c19f8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c19f8-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c19f8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="c19f8-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="c19f8-116">Thread safety</span></span>

<span data-ttu-id="c19f8-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="c19f8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c19f8-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="c19f8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c19f8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c19f8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c19f8-120">Referência</span><span class="sxs-lookup"><span data-stu-id="c19f8-120">Reference</span></span>

[<span data-ttu-id="c19f8-121">Membros do EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="c19f8-121">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="c19f8-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c19f8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="c19f8-123">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="c19f8-123">Derived types</span></span>

[<span data-ttu-id="c19f8-124">System.Object</span><span class="sxs-lookup"><span data-stu-id="c19f8-124">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c19f8-125">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c19f8-125">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c19f8-126">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="c19f8-126">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c19f8-127">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c19f8-127">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c19f8-128">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c19f8-128">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c19f8-129">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="c19f8-129">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="c19f8-130">Microsoft. ISAM. ESENT. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="c19f8-130">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              [<span data-ttu-id="c19f8-131">Microsoft. ISAM. ESENT. Interop. EsentOutOfBuffersException</span><span class="sxs-lookup"><span data-stu-id="c19f8-131">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>](./esentoutofbuffersexception-class.md)  
              [<span data-ttu-id="c19f8-132">Microsoft. ISAM. ESENT. Interop. EsentOutOfCursorsException</span><span class="sxs-lookup"><span data-stu-id="c19f8-132">Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException</span></span>](./esentoutofcursorsexception-class.md)  
              [<span data-ttu-id="c19f8-133">Microsoft. ISAM. ESENT. Interop. EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="c19f8-133">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>](./esentoutoffilehandlesexception-class.md)  
              [<span data-ttu-id="c19f8-134">Microsoft. ISAM. ESENT. Interop. EsentOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="c19f8-134">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>](./esentoutofmemoryexception-class.md)  
              [<span data-ttu-id="c19f8-135">Microsoft. ISAM. ESENT. Interop. EsentOutOfSessionsException</span><span class="sxs-lookup"><span data-stu-id="c19f8-135">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>](./esentoutofsessionsexception-class.md)  
              [<span data-ttu-id="c19f8-136">Microsoft. ISAM. ESENT. Interop. EsentOutOfThreadsException</span><span class="sxs-lookup"><span data-stu-id="c19f8-136">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>](./esentoutofthreadsexception-class.md)  
              [<span data-ttu-id="c19f8-137">Microsoft. ISAM. ESENT. Interop. EsentTooManyMempoolEntriesException</span><span class="sxs-lookup"><span data-stu-id="c19f8-137">Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException</span></span>](./esenttoomanymempoolentriesexception-class.md)  
              [<span data-ttu-id="c19f8-138">Microsoft. ISAM. ESENT. Interop. EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="c19f8-138">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>](./esenttoomanyopenindexesexception-class.md)  
              [<span data-ttu-id="c19f8-139">Microsoft. ISAM. ESENT. Interop. EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="c19f8-139">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>](./esenttoomanysortsexception-class.md)