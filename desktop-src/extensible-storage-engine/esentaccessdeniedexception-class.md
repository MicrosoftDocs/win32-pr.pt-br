---
description: 'Saiba mais sobre: classe EsentAccessDeniedException'
title: Classe EsentAccessDeniedException
TOCTitle: EsentAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101035
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d81979a93bfa2ad3801047e5ec5cac9796bcda8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759925"
---
# <a name="esentaccessdeniedexception-class"></a><span data-ttu-id="d9556-103">Classe EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d9556-103">EsentAccessDeniedException class</span></span>

<span data-ttu-id="d9556-104">Classe base para JET_err. AccessDenied exceções.</span><span class="sxs-lookup"><span data-stu-id="d9556-104">Base class for JET_err.AccessDenied exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d9556-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="d9556-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d9556-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d9556-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d9556-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d9556-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d9556-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="d9556-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d9556-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d9556-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d9556-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d9556-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d9556-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d9556-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="d9556-112">Microsoft. ISAM. ESENT. Interop. EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d9556-112">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>  

<span data-ttu-id="d9556-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9556-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9556-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9556-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9556-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9556-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAccessDeniedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAccessDeniedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="d9556-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="d9556-116">Thread safety</span></span>

<span data-ttu-id="d9556-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="d9556-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d9556-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="d9556-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9556-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9556-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9556-120">Referência</span><span class="sxs-lookup"><span data-stu-id="d9556-120">Reference</span></span>

[<span data-ttu-id="d9556-121">Membros do EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d9556-121">EsentAccessDeniedException members</span></span>](./esentaccessdeniedexception-members.md)

[<span data-ttu-id="d9556-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d9556-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
