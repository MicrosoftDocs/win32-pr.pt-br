---
description: 'Saiba mais sobre: classe EsentApiException'
title: Classe EsentApiException
TOCTitle: EsentApiException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentApiException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101032
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentApiException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b01747d2ecb197ce99617b8c9206d4fada8c2a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171757"
---
# <a name="esentapiexception-class"></a><span data-ttu-id="fd976-103">Classe EsentApiException</span><span class="sxs-lookup"><span data-stu-id="fd976-103">EsentApiException class</span></span>

<span data-ttu-id="fd976-104">Classe base para exceções de API.</span><span class="sxs-lookup"><span data-stu-id="fd976-104">Base class for API exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fd976-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="fd976-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fd976-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fd976-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fd976-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="fd976-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fd976-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="fd976-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fd976-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="fd976-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="fd976-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="fd976-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>  
          [<span data-ttu-id="fd976-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="fd976-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
          [<span data-ttu-id="fd976-112">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="fd976-112">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
          [<span data-ttu-id="fd976-113">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="fd976-113">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  

<span data-ttu-id="fd976-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fd976-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fd976-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fd976-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fd976-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd976-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentApiException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentApiException
```

``` csharp
[SerializableAttribute]
public abstract class EsentApiException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="fd976-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="fd976-117">Thread safety</span></span>

<span data-ttu-id="fd976-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="fd976-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fd976-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="fd976-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd976-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd976-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fd976-121">Referência</span><span class="sxs-lookup"><span data-stu-id="fd976-121">Reference</span></span>

[<span data-ttu-id="fd976-122">Membros do EsentApiException</span><span class="sxs-lookup"><span data-stu-id="fd976-122">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="fd976-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fd976-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
