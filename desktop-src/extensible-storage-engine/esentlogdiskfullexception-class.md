---
description: 'Saiba mais sobre: classe EsentLogDiskFullException'
title: Classe EsentLogDiskFullException
TOCTitle: EsentLogDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55102101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a237a8d21aab32114708a5cb59545ed827e05bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296847"
---
# <a name="esentlogdiskfullexception-class"></a><span data-ttu-id="7aabd-103">Classe EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="7aabd-103">EsentLogDiskFullException class</span></span>

<span data-ttu-id="7aabd-104">Classe base para JET_err. LogDiskFull exceções.</span><span class="sxs-lookup"><span data-stu-id="7aabd-104">Base class for JET_err.LogDiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7aabd-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="7aabd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7aabd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7aabd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7aabd-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7aabd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7aabd-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="7aabd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7aabd-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7aabd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7aabd-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="7aabd-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="7aabd-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="7aabd-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="7aabd-112">Microsoft. ISAM. ESENT. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="7aabd-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="7aabd-113">Microsoft. ISAM. ESENT. Interop. EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="7aabd-113">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>  

<span data-ttu-id="7aabd-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7aabd-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7aabd-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7aabd-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7aabd-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aabd-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentLogDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="7aabd-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="7aabd-117">Thread safety</span></span>

<span data-ttu-id="7aabd-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7aabd-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7aabd-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7aabd-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7aabd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7aabd-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7aabd-121">Referência</span><span class="sxs-lookup"><span data-stu-id="7aabd-121">Reference</span></span>

[<span data-ttu-id="7aabd-122">Membros do EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="7aabd-122">EsentLogDiskFullException members</span></span>](./esentlogdiskfullexception-members.md)

[<span data-ttu-id="7aabd-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7aabd-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
