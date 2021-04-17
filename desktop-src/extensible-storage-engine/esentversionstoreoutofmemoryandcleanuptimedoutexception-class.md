---
description: 'Saiba mais sobre: classe EsentVersionStoreOutOfMemoryAndCleanupTimedOutException'
title: Classe EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
TOCTitle: EsentVersionStoreOutOfMemoryAndCleanupTimedOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreoutofmemoryandcleanuptimedoutexception(v=EXCHG.10)
ms:contentKeyID: 55103240
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 58cfb5343bd4de471dc73cb0fa5a57729dde5b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761587"
---
# <a name="esentversionstoreoutofmemoryandcleanuptimedoutexception-class"></a><span data-ttu-id="64b32-103">Classe EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span><span class="sxs-lookup"><span data-stu-id="64b32-103">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException class</span></span>

<span data-ttu-id="64b32-104">Classe base para JET_err. VersionStoreOutOfMemoryAndCleanupTimedOut exceções.</span><span class="sxs-lookup"><span data-stu-id="64b32-104">Base class for JET_err.VersionStoreOutOfMemoryAndCleanupTimedOut exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="64b32-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="64b32-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="64b32-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="64b32-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="64b32-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="64b32-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="64b32-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="64b32-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="64b32-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="64b32-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="64b32-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="64b32-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="64b32-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="64b32-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="64b32-112">Microsoft. ISAM. ESENT. Interop. EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span><span class="sxs-lookup"><span data-stu-id="64b32-112">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span></span>  

<span data-ttu-id="64b32-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="64b32-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="64b32-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="64b32-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="64b32-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="64b32-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="64b32-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="64b32-116">Thread safety</span></span>

<span data-ttu-id="64b32-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="64b32-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="64b32-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="64b32-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="64b32-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="64b32-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="64b32-120">Referência</span><span class="sxs-lookup"><span data-stu-id="64b32-120">Reference</span></span>

[<span data-ttu-id="64b32-121">Membros do EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span><span class="sxs-lookup"><span data-stu-id="64b32-121">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException members</span></span>](./esentversionstoreoutofmemoryandcleanuptimedoutexception-members.md)

[<span data-ttu-id="64b32-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="64b32-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
