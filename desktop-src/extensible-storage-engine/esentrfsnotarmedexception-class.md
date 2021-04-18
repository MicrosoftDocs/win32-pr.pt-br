---
description: 'Saiba mais sobre: classe EsentRfsNotArmedException'
title: Classe EsentRfsNotArmedException
TOCTitle: EsentRfsNotArmedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrfsnotarmedexception(v=EXCHG.10)
ms:contentKeyID: 55102660
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c824cea5a74c1af60b39c42d9835846403fc44f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795449"
---
# <a name="esentrfsnotarmedexception-class"></a><span data-ttu-id="999d4-103">Classe EsentRfsNotArmedException</span><span class="sxs-lookup"><span data-stu-id="999d4-103">EsentRfsNotArmedException class</span></span>

<span data-ttu-id="999d4-104">Classe base para JET_err. RfsNotArmed exceções.</span><span class="sxs-lookup"><span data-stu-id="999d4-104">Base class for JET_err.RfsNotArmed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="999d4-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="999d4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="999d4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="999d4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="999d4-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="999d4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="999d4-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="999d4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="999d4-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="999d4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="999d4-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="999d4-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="999d4-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="999d4-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="999d4-112">Microsoft. ISAM. ESENT. Interop. EsentRfsNotArmedException</span><span class="sxs-lookup"><span data-stu-id="999d4-112">Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException</span></span>  

<span data-ttu-id="999d4-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="999d4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="999d4-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="999d4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="999d4-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="999d4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRfsNotArmedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentRfsNotArmedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRfsNotArmedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="999d4-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="999d4-116">Thread safety</span></span>

<span data-ttu-id="999d4-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="999d4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="999d4-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="999d4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="999d4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="999d4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="999d4-120">Referência</span><span class="sxs-lookup"><span data-stu-id="999d4-120">Reference</span></span>

[<span data-ttu-id="999d4-121">Membros do EsentRfsNotArmedException</span><span class="sxs-lookup"><span data-stu-id="999d4-121">EsentRfsNotArmedException members</span></span>](./esentrfsnotarmedexception-members.md)

[<span data-ttu-id="999d4-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="999d4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
