---
description: 'Saiba mais sobre: classe EsentInvalidBookmarkException'
title: Classe EsentInvalidBookmarkException
TOCTitle: EsentInvalidBookmarkException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidBookmarkException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidbookmarkexception(v=EXCHG.10)
ms:contentKeyID: 55101901
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidBookmarkException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidBookmarkException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79878d5740f15935ec86ed82e6507fdc8d6d46fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171081"
---
# <a name="esentinvalidbookmarkexception-class"></a><span data-ttu-id="9e05c-103">Classe EsentInvalidBookmarkException</span><span class="sxs-lookup"><span data-stu-id="9e05c-103">EsentInvalidBookmarkException class</span></span>

<span data-ttu-id="9e05c-104">Classe base para JET_err. InvalidBookmark exceções.</span><span class="sxs-lookup"><span data-stu-id="9e05c-104">Base class for JET_err.InvalidBookmark exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9e05c-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="9e05c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9e05c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9e05c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9e05c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="9e05c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9e05c-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="9e05c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9e05c-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9e05c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9e05c-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="9e05c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="9e05c-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="9e05c-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="9e05c-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidBookmarkException</span><span class="sxs-lookup"><span data-stu-id="9e05c-112">Microsoft.Isam.Esent.Interop.EsentInvalidBookmarkException</span></span>  

<span data-ttu-id="9e05c-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9e05c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9e05c-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9e05c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9e05c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e05c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidBookmarkException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidBookmarkException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidBookmarkException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="9e05c-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="9e05c-116">Thread safety</span></span>

<span data-ttu-id="9e05c-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9e05c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9e05c-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9e05c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e05c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e05c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9e05c-120">Referência</span><span class="sxs-lookup"><span data-stu-id="9e05c-120">Reference</span></span>

[<span data-ttu-id="9e05c-121">Membros do EsentInvalidBookmarkException</span><span class="sxs-lookup"><span data-stu-id="9e05c-121">EsentInvalidBookmarkException members</span></span>](./esentinvalidbookmarkexception-members.md)

[<span data-ttu-id="9e05c-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9e05c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
