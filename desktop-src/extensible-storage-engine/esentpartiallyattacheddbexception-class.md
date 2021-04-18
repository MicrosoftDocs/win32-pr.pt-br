---
description: 'Saiba mais sobre: classe EsentPartiallyAttachedDBException'
title: Classe EsentPartiallyAttachedDBException
TOCTitle: EsentPartiallyAttachedDBException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpartiallyattacheddbexception(v=EXCHG.10)
ms:contentKeyID: 55107313
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96ff15d9a2becb937c88f6e0bec689e68ddc39d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778793"
---
# <a name="esentpartiallyattacheddbexception-class"></a><span data-ttu-id="7a386-103">Classe EsentPartiallyAttachedDBException</span><span class="sxs-lookup"><span data-stu-id="7a386-103">EsentPartiallyAttachedDBException class</span></span>

<span data-ttu-id="7a386-104">Classe base para JET_err. PartiallyAttachedDB exceções.</span><span class="sxs-lookup"><span data-stu-id="7a386-104">Base class for JET_err.PartiallyAttachedDB exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7a386-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="7a386-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7a386-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7a386-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7a386-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7a386-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7a386-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="7a386-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7a386-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7a386-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7a386-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="7a386-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7a386-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="7a386-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="7a386-112">Microsoft. ISAM. ESENT. Interop. EsentPartiallyAttachedDBException</span><span class="sxs-lookup"><span data-stu-id="7a386-112">Microsoft.Isam.Esent.Interop.EsentPartiallyAttachedDBException</span></span>  

<span data-ttu-id="7a386-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a386-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a386-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a386-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a386-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a386-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPartiallyAttachedDBException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentPartiallyAttachedDBException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPartiallyAttachedDBException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="7a386-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="7a386-116">Thread safety</span></span>

<span data-ttu-id="7a386-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7a386-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7a386-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7a386-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a386-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a386-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a386-120">Referência</span><span class="sxs-lookup"><span data-stu-id="7a386-120">Reference</span></span>

[<span data-ttu-id="7a386-121">Membros do EsentPartiallyAttachedDBException</span><span class="sxs-lookup"><span data-stu-id="7a386-121">EsentPartiallyAttachedDBException members</span></span>](./esentpartiallyattacheddbexception-members.md)

[<span data-ttu-id="7a386-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7a386-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
