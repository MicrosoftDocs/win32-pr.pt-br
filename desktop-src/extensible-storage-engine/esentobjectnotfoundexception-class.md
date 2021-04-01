---
description: 'Saiba mais sobre: classe EsentObjectNotFoundException'
title: Classe EsentObjectNotFoundException
TOCTitle: EsentObjectNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobjectnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55102350
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d30eb09898142b25549ff4318059b4a373c31d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164722"
---
# <a name="esentobjectnotfoundexception-class"></a><span data-ttu-id="dd91f-103">Classe EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="dd91f-103">EsentObjectNotFoundException class</span></span>

<span data-ttu-id="dd91f-104">Classe base para JET_err. ObjectNotFound exceções.</span><span class="sxs-lookup"><span data-stu-id="dd91f-104">Base class for JET_err.ObjectNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dd91f-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="dd91f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dd91f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dd91f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dd91f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="dd91f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dd91f-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="dd91f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dd91f-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="dd91f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dd91f-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="dd91f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="dd91f-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="dd91f-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="dd91f-112">Microsoft. ISAM. ESENT. Interop. EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="dd91f-112">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>  

<span data-ttu-id="dd91f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd91f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd91f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dd91f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd91f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd91f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentObjectNotFoundException _
    Inherits EsentStateException
'Usage
Dim instance As EsentObjectNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentObjectNotFoundException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="dd91f-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="dd91f-116">Thread safety</span></span>

<span data-ttu-id="dd91f-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="dd91f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dd91f-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="dd91f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd91f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd91f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd91f-120">Referência</span><span class="sxs-lookup"><span data-stu-id="dd91f-120">Reference</span></span>

[<span data-ttu-id="dd91f-121">Membros do EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="dd91f-121">EsentObjectNotFoundException members</span></span>](./esentobjectnotfoundexception-members.md)

[<span data-ttu-id="dd91f-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dd91f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
