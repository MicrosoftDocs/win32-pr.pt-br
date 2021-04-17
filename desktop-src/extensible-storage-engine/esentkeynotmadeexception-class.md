---
description: 'Saiba mais sobre: classe EsentKeyNotMadeException'
title: Classe EsentKeyNotMadeException
TOCTitle: EsentKeyNotMadeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeynotmadeexception(v=EXCHG.10)
ms:contentKeyID: 55102115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e77be995e6f06aaa7058455f9e0f64bd9721f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763098"
---
# <a name="esentkeynotmadeexception-class"></a><span data-ttu-id="e8fbe-103">Classe EsentKeyNotMadeException</span><span class="sxs-lookup"><span data-stu-id="e8fbe-103">EsentKeyNotMadeException class</span></span>

<span data-ttu-id="e8fbe-104">Classe base para JET_err. KeyNotMade exceções.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-104">Base class for JET_err.KeyNotMade exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e8fbe-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="e8fbe-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e8fbe-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e8fbe-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e8fbe-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e8fbe-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e8fbe-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="e8fbe-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e8fbe-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e8fbe-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e8fbe-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e8fbe-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e8fbe-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="e8fbe-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e8fbe-112">Microsoft. ISAM. ESENT. Interop. EsentKeyNotMadeException</span><span class="sxs-lookup"><span data-stu-id="e8fbe-112">Microsoft.Isam.Esent.Interop.EsentKeyNotMadeException</span></span>  

<span data-ttu-id="e8fbe-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8fbe-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8fbe-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8fbe-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fbe-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8fbe-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyNotMadeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentKeyNotMadeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyNotMadeException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e8fbe-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="e8fbe-116">Thread safety</span></span>

<span data-ttu-id="e8fbe-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e8fbe-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e8fbe-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8fbe-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8fbe-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8fbe-120">Referência</span><span class="sxs-lookup"><span data-stu-id="e8fbe-120">Reference</span></span>

[<span data-ttu-id="e8fbe-121">Membros do EsentKeyNotMadeException</span><span class="sxs-lookup"><span data-stu-id="e8fbe-121">EsentKeyNotMadeException members</span></span>](./esentkeynotmadeexception-members.md)

[<span data-ttu-id="e8fbe-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e8fbe-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
