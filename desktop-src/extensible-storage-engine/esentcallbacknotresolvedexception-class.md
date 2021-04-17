---
description: 'Saiba mais sobre: classe EsentCallbackNotResolvedException'
title: Classe EsentCallbackNotResolvedException
TOCTitle: EsentCallbackNotResolvedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcallbacknotresolvedexception(v=EXCHG.10)
ms:contentKeyID: 55107258
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a730ce6779f41fb348a7e9685dd9ffc132897824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790493"
---
# <a name="esentcallbacknotresolvedexception-class"></a><span data-ttu-id="5d3df-103">Classe EsentCallbackNotResolvedException</span><span class="sxs-lookup"><span data-stu-id="5d3df-103">EsentCallbackNotResolvedException class</span></span>

<span data-ttu-id="5d3df-104">Classe base para JET_err. CallbackNotResolved exceções.</span><span class="sxs-lookup"><span data-stu-id="5d3df-104">Base class for JET_err.CallbackNotResolved exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5d3df-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="5d3df-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5d3df-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5d3df-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5d3df-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5d3df-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5d3df-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="5d3df-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5d3df-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5d3df-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5d3df-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="5d3df-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="5d3df-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="5d3df-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="5d3df-112">Microsoft. ISAM. ESENT. Interop. EsentCallbackNotResolvedException</span><span class="sxs-lookup"><span data-stu-id="5d3df-112">Microsoft.Isam.Esent.Interop.EsentCallbackNotResolvedException</span></span>  

<span data-ttu-id="5d3df-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d3df-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d3df-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5d3df-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3df-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d3df-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCallbackNotResolvedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCallbackNotResolvedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCallbackNotResolvedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="5d3df-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="5d3df-116">Thread safety</span></span>

<span data-ttu-id="5d3df-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="5d3df-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5d3df-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="5d3df-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d3df-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d3df-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d3df-120">Referência</span><span class="sxs-lookup"><span data-stu-id="5d3df-120">Reference</span></span>

[<span data-ttu-id="5d3df-121">Membros do EsentCallbackNotResolvedException</span><span class="sxs-lookup"><span data-stu-id="5d3df-121">EsentCallbackNotResolvedException members</span></span>](./esentcallbacknotresolvedexception-members.md)

[<span data-ttu-id="5d3df-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5d3df-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
