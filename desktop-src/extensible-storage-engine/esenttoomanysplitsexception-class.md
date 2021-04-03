---
description: 'Saiba mais sobre: classe EsentTooManySplitsException'
title: Classe EsentTooManySplitsException
TOCTitle: EsentTooManySplitsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanysplitsexception(v=EXCHG.10)
ms:contentKeyID: 55103177
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManySplitsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fea122e5a5f40dd1a435a82f68d86766dc5518ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922750"
---
# <a name="esenttoomanysplitsexception-class"></a><span data-ttu-id="b5262-103">Classe EsentTooManySplitsException</span><span class="sxs-lookup"><span data-stu-id="b5262-103">EsentTooManySplitsException class</span></span>

<span data-ttu-id="b5262-104">Classe base para JET_err. TooManySplits exceções.</span><span class="sxs-lookup"><span data-stu-id="b5262-104">Base class for JET_err.TooManySplits exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b5262-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="b5262-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b5262-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b5262-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b5262-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b5262-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b5262-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="b5262-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b5262-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b5262-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b5262-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b5262-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b5262-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="b5262-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="b5262-112">Microsoft. ISAM. ESENT. Interop. EsentTooManySplitsException</span><span class="sxs-lookup"><span data-stu-id="b5262-112">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>  

<span data-ttu-id="b5262-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5262-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5262-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5262-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5262-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5262-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManySplitsException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentTooManySplitsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManySplitsException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="b5262-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="b5262-116">Thread safety</span></span>

<span data-ttu-id="b5262-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b5262-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b5262-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b5262-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5262-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5262-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5262-120">Referência</span><span class="sxs-lookup"><span data-stu-id="b5262-120">Reference</span></span>

[<span data-ttu-id="b5262-121">Membros do EsentTooManySplitsException</span><span class="sxs-lookup"><span data-stu-id="b5262-121">EsentTooManySplitsException members</span></span>](./esenttoomanysplitsexception-members.md)

[<span data-ttu-id="b5262-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b5262-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
