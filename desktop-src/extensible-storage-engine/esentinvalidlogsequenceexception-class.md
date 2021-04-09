---
description: 'Saiba mais sobre: classe EsentInvalidLogSequenceException'
title: Classe EsentInvalidLogSequenceException
TOCTitle: EsentInvalidLogSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogsequenceexception(v=EXCHG.10)
ms:contentKeyID: 55107285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8803298a3202ea151bcb42e5490931c0aba2705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922582"
---
# <a name="esentinvalidlogsequenceexception-class"></a><span data-ttu-id="bc7fb-103">Classe EsentInvalidLogSequenceException</span><span class="sxs-lookup"><span data-stu-id="bc7fb-103">EsentInvalidLogSequenceException class</span></span>

<span data-ttu-id="bc7fb-104">Classe base para JET_err. InvalidLogSequence exceções.</span><span class="sxs-lookup"><span data-stu-id="bc7fb-104">Base class for JET_err.InvalidLogSequence exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bc7fb-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="bc7fb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bc7fb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bc7fb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bc7fb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bc7fb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bc7fb-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="bc7fb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bc7fb-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="bc7fb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bc7fb-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="bc7fb-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="bc7fb-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="bc7fb-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="bc7fb-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidLogSequenceException</span><span class="sxs-lookup"><span data-stu-id="bc7fb-112">Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException</span></span>  

<span data-ttu-id="bc7fb-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc7fb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bc7fb-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc7fb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc7fb-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc7fb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogSequenceException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentInvalidLogSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogSequenceException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="bc7fb-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="bc7fb-116">Thread safety</span></span>

<span data-ttu-id="bc7fb-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bc7fb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bc7fb-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bc7fb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc7fb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc7fb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc7fb-120">Referência</span><span class="sxs-lookup"><span data-stu-id="bc7fb-120">Reference</span></span>

[<span data-ttu-id="bc7fb-121">Membros do EsentInvalidLogSequenceException</span><span class="sxs-lookup"><span data-stu-id="bc7fb-121">EsentInvalidLogSequenceException members</span></span>](./esentinvalidlogsequenceexception-members.md)

[<span data-ttu-id="bc7fb-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bc7fb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
