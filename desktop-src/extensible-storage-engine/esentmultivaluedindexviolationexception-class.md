---
description: 'Saiba mais sobre: classe EsentMultiValuedIndexViolationException'
title: Classe EsentMultiValuedIndexViolationException
TOCTitle: EsentMultiValuedIndexViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedindexviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cafb4ce44f3b0600997e9d715f882e95869f65b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813497"
---
# <a name="esentmultivaluedindexviolationexception-class"></a><span data-ttu-id="e4c39-103">Classe EsentMultiValuedIndexViolationException</span><span class="sxs-lookup"><span data-stu-id="e4c39-103">EsentMultiValuedIndexViolationException class</span></span>

<span data-ttu-id="e4c39-104">Classe base para JET_err. MultiValuedIndexViolation exceções.</span><span class="sxs-lookup"><span data-stu-id="e4c39-104">Base class for JET_err.MultiValuedIndexViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e4c39-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="e4c39-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e4c39-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e4c39-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e4c39-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e4c39-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e4c39-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="e4c39-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e4c39-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e4c39-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e4c39-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e4c39-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e4c39-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="e4c39-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e4c39-112">Microsoft. ISAM. ESENT. Interop. EsentMultiValuedIndexViolationException</span><span class="sxs-lookup"><span data-stu-id="e4c39-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException</span></span>  

<span data-ttu-id="e4c39-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4c39-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4c39-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4c39-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c39-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4c39-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedIndexViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMultiValuedIndexViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedIndexViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e4c39-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="e4c39-116">Thread safety</span></span>

<span data-ttu-id="e4c39-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e4c39-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e4c39-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e4c39-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4c39-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4c39-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4c39-120">Referência</span><span class="sxs-lookup"><span data-stu-id="e4c39-120">Reference</span></span>

[<span data-ttu-id="e4c39-121">Membros do EsentMultiValuedIndexViolationException</span><span class="sxs-lookup"><span data-stu-id="e4c39-121">EsentMultiValuedIndexViolationException members</span></span>](./esentmultivaluedindexviolationexception-members.md)

[<span data-ttu-id="e4c39-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e4c39-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
