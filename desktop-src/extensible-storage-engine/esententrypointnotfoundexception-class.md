---
description: 'Saiba mais sobre: classe EsentEntryPointNotFoundException'
title: Classe EsentEntryPointNotFoundException
TOCTitle: EsentEntryPointNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esententrypointnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101642
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7bbc8d66af82c5f232ccc94f14b81f2987748e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791436"
---
# <a name="esententrypointnotfoundexception-class"></a><span data-ttu-id="c7366-103">Classe EsentEntryPointNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c7366-103">EsentEntryPointNotFoundException class</span></span>

<span data-ttu-id="c7366-104">Classe base para JET_err. EntryPointNotFound exceções.</span><span class="sxs-lookup"><span data-stu-id="c7366-104">Base class for JET_err.EntryPointNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c7366-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="c7366-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c7366-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c7366-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c7366-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c7366-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c7366-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="c7366-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c7366-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c7366-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c7366-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="c7366-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="c7366-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="c7366-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="c7366-112">Microsoft. ISAM. ESENT. Interop. EsentEntryPointNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c7366-112">Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException</span></span>  

<span data-ttu-id="c7366-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7366-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c7366-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7366-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7366-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7366-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentEntryPointNotFoundException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentEntryPointNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentEntryPointNotFoundException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="c7366-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="c7366-116">Thread safety</span></span>

<span data-ttu-id="c7366-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="c7366-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c7366-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="c7366-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7366-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7366-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7366-120">Referência</span><span class="sxs-lookup"><span data-stu-id="c7366-120">Reference</span></span>

[<span data-ttu-id="c7366-121">Membros do EsentEntryPointNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c7366-121">EsentEntryPointNotFoundException members</span></span>](./esententrypointnotfoundexception-members.md)

[<span data-ttu-id="c7366-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c7366-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
