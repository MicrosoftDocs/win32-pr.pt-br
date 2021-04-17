---
description: 'Saiba mais sobre: classe EsentOutOfBuffersException'
title: Classe EsentOutOfBuffersException
TOCTitle: EsentOutOfBuffersException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofbuffersexception(v=EXCHG.10)
ms:contentKeyID: 55102398
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fc8c5d22a6dc4d33d855d6d98a78e8ce7d33ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798279"
---
# <a name="esentoutofbuffersexception-class"></a><span data-ttu-id="92c77-103">Classe EsentOutOfBuffersException</span><span class="sxs-lookup"><span data-stu-id="92c77-103">EsentOutOfBuffersException class</span></span>

<span data-ttu-id="92c77-104">Classe base para JET_err. OutOfBuffers exceções.</span><span class="sxs-lookup"><span data-stu-id="92c77-104">Base class for JET_err.OutOfBuffers exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="92c77-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="92c77-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="92c77-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="92c77-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="92c77-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="92c77-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="92c77-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="92c77-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="92c77-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="92c77-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="92c77-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="92c77-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="92c77-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="92c77-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="92c77-112">Microsoft. ISAM. ESENT. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="92c77-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="92c77-113">Microsoft. ISAM. ESENT. Interop. EsentOutOfBuffersException</span><span class="sxs-lookup"><span data-stu-id="92c77-113">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>  

<span data-ttu-id="92c77-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92c77-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92c77-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="92c77-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92c77-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92c77-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfBuffersException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfBuffersException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfBuffersException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="92c77-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="92c77-117">Thread safety</span></span>

<span data-ttu-id="92c77-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="92c77-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="92c77-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="92c77-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="92c77-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="92c77-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92c77-121">Referência</span><span class="sxs-lookup"><span data-stu-id="92c77-121">Reference</span></span>

[<span data-ttu-id="92c77-122">Membros do EsentOutOfBuffersException</span><span class="sxs-lookup"><span data-stu-id="92c77-122">EsentOutOfBuffersException members</span></span>](./esentoutofbuffersexception-members.md)

[<span data-ttu-id="92c77-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="92c77-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
