---
description: 'Saiba mais sobre: classe EsentMultiValuedDuplicateException'
title: Classe EsentMultiValuedDuplicateException
TOCTitle: EsentMultiValuedDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102340
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fddfac316bb8ad13ff5c42abc8041e4a18c85321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757656"
---
# <a name="esentmultivaluedduplicateexception-class"></a><span data-ttu-id="b7b00-103">Classe EsentMultiValuedDuplicateException</span><span class="sxs-lookup"><span data-stu-id="b7b00-103">EsentMultiValuedDuplicateException class</span></span>

<span data-ttu-id="b7b00-104">Classe base para JET_err. MultiValuedDuplicate exceções.</span><span class="sxs-lookup"><span data-stu-id="b7b00-104">Base class for JET_err.MultiValuedDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b7b00-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="b7b00-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b7b00-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b7b00-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b7b00-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b7b00-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b7b00-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="b7b00-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b7b00-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b7b00-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b7b00-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b7b00-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b7b00-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="b7b00-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="b7b00-112">Microsoft. ISAM. ESENT. Interop. EsentMultiValuedDuplicateException</span><span class="sxs-lookup"><span data-stu-id="b7b00-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>  

<span data-ttu-id="b7b00-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7b00-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7b00-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7b00-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b00-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b00-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="b7b00-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="b7b00-116">Thread safety</span></span>

<span data-ttu-id="b7b00-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b7b00-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b7b00-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b7b00-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7b00-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7b00-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7b00-120">Referência</span><span class="sxs-lookup"><span data-stu-id="b7b00-120">Reference</span></span>

[<span data-ttu-id="b7b00-121">Membros do EsentMultiValuedDuplicateException</span><span class="sxs-lookup"><span data-stu-id="b7b00-121">EsentMultiValuedDuplicateException members</span></span>](./esentmultivaluedduplicateexception-members.md)

[<span data-ttu-id="b7b00-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b7b00-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
