---
description: 'Saiba mais sobre: classe EsentOutOfThreadsException'
title: Classe EsentOutOfThreadsException
TOCTitle: EsentOutOfThreadsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofthreadsexception(v=EXCHG.10)
ms:contentKeyID: 55102450
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05a1427383a12c286ba37eee6f4ddfcd0b655350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922865"
---
# <a name="esentoutofthreadsexception-class"></a><span data-ttu-id="bde73-103">Classe EsentOutOfThreadsException</span><span class="sxs-lookup"><span data-stu-id="bde73-103">EsentOutOfThreadsException class</span></span>

<span data-ttu-id="bde73-104">Classe base para JET_err. OutOfThreads exceções.</span><span class="sxs-lookup"><span data-stu-id="bde73-104">Base class for JET_err.OutOfThreads exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bde73-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="bde73-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bde73-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bde73-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bde73-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bde73-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bde73-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="bde73-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bde73-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="bde73-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bde73-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="bde73-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="bde73-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="bde73-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="bde73-112">Microsoft. ISAM. ESENT. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="bde73-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="bde73-113">Microsoft. ISAM. ESENT. Interop. EsentOutOfThreadsException</span><span class="sxs-lookup"><span data-stu-id="bde73-113">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>  

<span data-ttu-id="bde73-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bde73-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bde73-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bde73-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bde73-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="bde73-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfThreadsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfThreadsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfThreadsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="bde73-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="bde73-117">Thread safety</span></span>

<span data-ttu-id="bde73-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bde73-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bde73-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bde73-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bde73-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="bde73-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bde73-121">Referência</span><span class="sxs-lookup"><span data-stu-id="bde73-121">Reference</span></span>

[<span data-ttu-id="bde73-122">Membros do EsentOutOfThreadsException</span><span class="sxs-lookup"><span data-stu-id="bde73-122">EsentOutOfThreadsException members</span></span>](./esentoutofthreadsexception-members.md)

[<span data-ttu-id="bde73-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bde73-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
