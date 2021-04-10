---
description: 'Saiba mais sobre: classe EsentTooManyOpenIndexesException'
title: Classe EsentTooManyOpenIndexesException
TOCTitle: EsentTooManyOpenIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopenindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103106
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 681f9a8ec67b9b9c82babcc3814833a1a3dbb0d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171367"
---
# <a name="esenttoomanyopenindexesexception-class"></a><span data-ttu-id="6424a-103">Classe EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="6424a-103">EsentTooManyOpenIndexesException class</span></span>

<span data-ttu-id="6424a-104">Classe base para JET_err. TooManyOpenIndexes exceções.</span><span class="sxs-lookup"><span data-stu-id="6424a-104">Base class for JET_err.TooManyOpenIndexes exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6424a-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="6424a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6424a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6424a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6424a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="6424a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6424a-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="6424a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6424a-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="6424a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6424a-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="6424a-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="6424a-111">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="6424a-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="6424a-112">Microsoft. ISAM. ESENT. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="6424a-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="6424a-113">Microsoft. ISAM. ESENT. Interop. EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="6424a-113">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>  

<span data-ttu-id="6424a-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6424a-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6424a-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6424a-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6424a-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="6424a-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenIndexesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyOpenIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenIndexesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="6424a-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="6424a-117">Thread safety</span></span>

<span data-ttu-id="6424a-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="6424a-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6424a-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="6424a-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6424a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6424a-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6424a-121">Referência</span><span class="sxs-lookup"><span data-stu-id="6424a-121">Reference</span></span>

[<span data-ttu-id="6424a-122">Membros do EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="6424a-122">EsentTooManyOpenIndexesException members</span></span>](./esenttoomanyopenindexesexception-members.md)

[<span data-ttu-id="6424a-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6424a-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
