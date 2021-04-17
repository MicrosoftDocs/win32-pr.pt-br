---
description: 'Saiba mais sobre: classe EsentFragmentationException'
title: Classe EsentFragmentationException
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105769634"
---
# <a name="esentfragmentationexception-class"></a><span data-ttu-id="d0ff6-103">Classe EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-103">EsentFragmentationException class</span></span>

<span data-ttu-id="d0ff6-104">Classe base para exceções de fragmentação.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-104">Base class for Fragmentation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d0ff6-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="d0ff6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d0ff6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d0ff6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d0ff6-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d0ff6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d0ff6-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d0ff6-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d0ff6-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="d0ff6-111">Microsoft. ISAM. ESENT. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            

<span data-ttu-id="d0ff6-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0ff6-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0ff6-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0ff6-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ff6-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0ff6-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="d0ff6-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="d0ff6-115">Thread safety</span></span>

<span data-ttu-id="d0ff6-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d0ff6-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="d0ff6-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0ff6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0ff6-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0ff6-119">Referência</span><span class="sxs-lookup"><span data-stu-id="d0ff6-119">Reference</span></span>

[<span data-ttu-id="d0ff6-120">Membros do EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-120">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="d0ff6-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d0ff6-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="d0ff6-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="d0ff6-122">Derived types</span></span>

[<span data-ttu-id="d0ff6-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="d0ff6-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d0ff6-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d0ff6-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d0ff6-125">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d0ff6-126">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d0ff6-127">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="d0ff6-128">Microsoft. ISAM. ESENT. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-128">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            [<span data-ttu-id="d0ff6-129">Microsoft. ISAM. ESENT. Interop. EsentLogSectorSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-129">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchException</span></span>](./esentlogsectorsizemismatchexception-class.md)  
            [<span data-ttu-id="d0ff6-130">Microsoft. ISAM. ESENT. Interop. EsentLogSequenceEndDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-130">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException</span></span>](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [<span data-ttu-id="d0ff6-131">Microsoft. ISAM. ESENT. Interop. EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-131">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>](./esentlogsequenceendexception-class.md)  
            [<span data-ttu-id="d0ff6-132">Microsoft. ISAM. ESENT. Interop. EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-132">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>](./esentoutofautoincrementvaluesexception-class.md)  
            [<span data-ttu-id="d0ff6-133">Microsoft. ISAM. ESENT. Interop. EsentOutOfDbtimeValuesException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-133">Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException</span></span>](./esentoutofdbtimevaluesexception-class.md)  
            [<span data-ttu-id="d0ff6-134">Microsoft. ISAM. ESENT. Interop. EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-134">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>](./esentoutoflongvalueidsexception-class.md)  
            [<span data-ttu-id="d0ff6-135">Microsoft. ISAM. ESENT. Interop. EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-135">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>](./esentoutofobjectidsexception-class.md)  
            [<span data-ttu-id="d0ff6-136">Microsoft. ISAM. ESENT. Interop. EsentOutOfSequentialIndexValuesException</span><span class="sxs-lookup"><span data-stu-id="d0ff6-136">Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException</span></span>](./esentoutofsequentialindexvaluesexception-class.md)