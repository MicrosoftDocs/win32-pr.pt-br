---
description: 'Saiba mais sobre: classe EsentDiskFullException'
title: Classe EsentDiskFullException
TOCTitle: EsentDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55101513
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28c3fb4fa06a6526cf06d0f4822ce3dcb835bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297555"
---
# <a name="esentdiskfullexception-class"></a><span data-ttu-id="0744e-103">Classe EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="0744e-103">EsentDiskFullException class</span></span>

<span data-ttu-id="0744e-104">Classe base para JET_err. DiskFull exceções.</span><span class="sxs-lookup"><span data-stu-id="0744e-104">Base class for JET_err.DiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0744e-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="0744e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0744e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0744e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0744e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0744e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0744e-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="0744e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0744e-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0744e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0744e-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="0744e-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="0744e-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="0744e-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="0744e-112">Microsoft. ISAM. ESENT. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="0744e-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="0744e-113">Microsoft. ISAM. ESENT. Interop. EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="0744e-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>  

<span data-ttu-id="0744e-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0744e-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0744e-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0744e-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0744e-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="0744e-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="0744e-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="0744e-117">Thread safety</span></span>

<span data-ttu-id="0744e-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0744e-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0744e-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0744e-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0744e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0744e-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0744e-121">Referência</span><span class="sxs-lookup"><span data-stu-id="0744e-121">Reference</span></span>

[<span data-ttu-id="0744e-122">Membros do EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="0744e-122">EsentDiskFullException members</span></span>](./esentdiskfullexception-members.md)

[<span data-ttu-id="0744e-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0744e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
