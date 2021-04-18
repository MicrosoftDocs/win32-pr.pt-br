---
description: 'Saiba mais sobre: classe EsentSystemParamsAlreadySetException'
title: Classe EsentSystemParamsAlreadySetException
TOCTitle: EsentSystemParamsAlreadySetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsystemparamsalreadysetexception(v=EXCHG.10)
ms:contentKeyID: 55103003
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38aec2e2ca60a59e45ae3f43f390a1b7fdf2553a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763446"
---
# <a name="esentsystemparamsalreadysetexception-class"></a><span data-ttu-id="1ec35-103">Classe EsentSystemParamsAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="1ec35-103">EsentSystemParamsAlreadySetException class</span></span>

<span data-ttu-id="1ec35-104">Classe base para exceções de JET_err.SystemParamsAlreadySet.</span><span class="sxs-lookup"><span data-stu-id="1ec35-104">Base class for JET_err.SystemParamsAlreadySet exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1ec35-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="1ec35-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1ec35-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ec35-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1ec35-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1ec35-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1ec35-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="1ec35-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1ec35-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1ec35-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1ec35-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1ec35-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1ec35-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="1ec35-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="1ec35-112">Microsoft. ISAM. ESENT. Interop. EsentSystemParamsAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="1ec35-112">Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException</span></span>  

<span data-ttu-id="1ec35-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ec35-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ec35-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ec35-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec35-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ec35-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSystemParamsAlreadySetException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSystemParamsAlreadySetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSystemParamsAlreadySetException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="1ec35-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="1ec35-116">Thread safety</span></span>

<span data-ttu-id="1ec35-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="1ec35-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1ec35-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="1ec35-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ec35-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ec35-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ec35-120">Referência</span><span class="sxs-lookup"><span data-stu-id="1ec35-120">Reference</span></span>

[<span data-ttu-id="1ec35-121">Membros do EsentSystemParamsAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="1ec35-121">EsentSystemParamsAlreadySetException members</span></span>](./esentsystemparamsalreadysetexception-members.md)

[<span data-ttu-id="1ec35-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1ec35-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
