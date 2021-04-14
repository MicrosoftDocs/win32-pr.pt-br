---
description: 'Saiba mais sobre: classe EsentDiskException'
title: Classe EsentDiskException
TOCTitle: EsentDiskException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101517
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22c2e2e2f829b6fcc6967e6e58692613243549c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370757"
---
# <a name="esentdiskexception-class"></a><span data-ttu-id="ac4bd-103">Classe EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-103">EsentDiskException class</span></span>

<span data-ttu-id="ac4bd-104">Classe base para exceções de disco.</span><span class="sxs-lookup"><span data-stu-id="ac4bd-104">Base class for Disk exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ac4bd-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="ac4bd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ac4bd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ac4bd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ac4bd-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ac4bd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ac4bd-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ac4bd-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ac4bd-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="ac4bd-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="ac4bd-112">Microsoft. ISAM. ESENT. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>  
              [<span data-ttu-id="ac4bd-113">Microsoft. ISAM. ESENT. Interop. EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>](./esentdiskfullexception-class.md)  
              [<span data-ttu-id="ac4bd-114">Microsoft. ISAM. ESENT. Interop. EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-114">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>](./esentlogdiskfullexception-class.md)  

<span data-ttu-id="ac4bd-115">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac4bd-115">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac4bd-116">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac4bd-116">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4bd-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac4bd-117">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDiskException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentDiskException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDiskException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="ac4bd-118">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="ac4bd-118">Thread safety</span></span>

<span data-ttu-id="ac4bd-119">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ac4bd-119">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ac4bd-120">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ac4bd-120">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac4bd-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac4bd-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac4bd-122">Referência</span><span class="sxs-lookup"><span data-stu-id="ac4bd-122">Reference</span></span>

[<span data-ttu-id="ac4bd-123">Membros do EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="ac4bd-123">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="ac4bd-124">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ac4bd-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
