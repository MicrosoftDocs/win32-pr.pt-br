---
description: 'Saiba mais sobre: classe EsentResourceException'
title: Classe EsentResourceException
TOCTitle: EsentResourceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResourceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102627
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResourceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7d4964bb4ed9c1305652d9425170bd934c9274e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170144"
---
# <a name="esentresourceexception-class"></a><span data-ttu-id="50825-103">Classe EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="50825-103">EsentResourceException class</span></span>

<span data-ttu-id="50825-104">Classe base para exceções de recurso.</span><span class="sxs-lookup"><span data-stu-id="50825-104">Base class for Resource exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="50825-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="50825-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="50825-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="50825-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="50825-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="50825-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="50825-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="50825-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="50825-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="50825-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="50825-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="50825-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="50825-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="50825-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>  
            [<span data-ttu-id="50825-112">Microsoft. ISAM. ESENT. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="50825-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
            [<span data-ttu-id="50825-113">Microsoft. ISAM. ESENT. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="50825-113">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
            [<span data-ttu-id="50825-114">Microsoft. ISAM. ESENT. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="50825-114">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
            [<span data-ttu-id="50825-115">Microsoft. ISAM. ESENT. Interop. EsentTaskDroppedException</span><span class="sxs-lookup"><span data-stu-id="50825-115">Microsoft.Isam.Esent.Interop.EsentTaskDroppedException</span></span>](./esenttaskdroppedexception-class.md)  
            [<span data-ttu-id="50825-116">Microsoft. ISAM. ESENT. Interop. EsentTooManyIOException</span><span class="sxs-lookup"><span data-stu-id="50825-116">Microsoft.Isam.Esent.Interop.EsentTooManyIOException</span></span>](./esenttoomanyioexception-class.md)  

<span data-ttu-id="50825-117">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50825-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50825-118">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="50825-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50825-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50825-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentResourceException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentResourceException
```

``` csharp
[SerializableAttribute]
public abstract class EsentResourceException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="50825-120">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="50825-120">Thread safety</span></span>

<span data-ttu-id="50825-121">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="50825-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="50825-122">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="50825-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="50825-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="50825-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50825-124">Referência</span><span class="sxs-lookup"><span data-stu-id="50825-124">Reference</span></span>

[<span data-ttu-id="50825-125">Membros do EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="50825-125">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="50825-126">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="50825-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
