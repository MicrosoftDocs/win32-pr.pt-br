---
description: 'Saiba mais sobre: classe EsentTooManyInstancesException'
title: Classe EsentTooManyInstancesException
TOCTitle: EsentTooManyInstancesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyinstancesexception(v=EXCHG.10)
ms:contentKeyID: 55103084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecd20f6a05a17d4bd21623732a4e716e82c9b1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798014"
---
# <a name="esenttoomanyinstancesexception-class"></a><span data-ttu-id="e5ea3-103">Classe EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-103">EsentTooManyInstancesException class</span></span>

<span data-ttu-id="e5ea3-104">Classe base para JET_err. TooManyInstances exceções.</span><span class="sxs-lookup"><span data-stu-id="e5ea3-104">Base class for JET_err.TooManyInstances exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e5ea3-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="e5ea3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e5ea3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e5ea3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e5ea3-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e5ea3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e5ea3-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e5ea3-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e5ea3-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="e5ea3-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="e5ea3-112">Microsoft. ISAM. ESENT. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="e5ea3-113">Microsoft. ISAM. ESENT. Interop. EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-113">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>  

<span data-ttu-id="e5ea3-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5ea3-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5ea3-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5ea3-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ea3-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5ea3-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyInstancesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyInstancesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyInstancesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="e5ea3-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="e5ea3-117">Thread safety</span></span>

<span data-ttu-id="e5ea3-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e5ea3-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e5ea3-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e5ea3-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5ea3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5ea3-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5ea3-121">Referência</span><span class="sxs-lookup"><span data-stu-id="e5ea3-121">Reference</span></span>

[<span data-ttu-id="e5ea3-122">Membros do EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="e5ea3-122">EsentTooManyInstancesException members</span></span>](./esenttoomanyinstancesexception-members.md)

[<span data-ttu-id="e5ea3-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e5ea3-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
