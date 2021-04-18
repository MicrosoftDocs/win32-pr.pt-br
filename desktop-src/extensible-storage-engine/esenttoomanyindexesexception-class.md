---
description: 'Saiba mais sobre: classe EsentTooManyIndexesException'
title: Classe EsentTooManyIndexesException
TOCTitle: EsentTooManyIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103060
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a1d895f61b3ad1f25b8992b43da1fd14f29f22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767806"
---
# <a name="esenttoomanyindexesexception-class"></a><span data-ttu-id="ec74a-103">Classe EsentTooManyIndexesException</span><span class="sxs-lookup"><span data-stu-id="ec74a-103">EsentTooManyIndexesException class</span></span>

<span data-ttu-id="ec74a-104">Classe base para JET_err. TooManyIndexes exceções.</span><span class="sxs-lookup"><span data-stu-id="ec74a-104">Base class for JET_err.TooManyIndexes exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ec74a-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="ec74a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ec74a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ec74a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ec74a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ec74a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ec74a-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="ec74a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ec74a-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ec74a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ec74a-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="ec74a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ec74a-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="ec74a-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="ec74a-112">Microsoft. ISAM. ESENT. Interop. EsentTooManyIndexesException</span><span class="sxs-lookup"><span data-stu-id="ec74a-112">Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException</span></span>  

<span data-ttu-id="ec74a-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec74a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec74a-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ec74a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec74a-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec74a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyIndexesException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyIndexesException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="ec74a-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="ec74a-116">Thread safety</span></span>

<span data-ttu-id="ec74a-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ec74a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ec74a-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ec74a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec74a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec74a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec74a-120">Referência</span><span class="sxs-lookup"><span data-stu-id="ec74a-120">Reference</span></span>

[<span data-ttu-id="ec74a-121">Membros do EsentTooManyIndexesException</span><span class="sxs-lookup"><span data-stu-id="ec74a-121">EsentTooManyIndexesException members</span></span>](./esenttoomanyindexesexception-members.md)

[<span data-ttu-id="ec74a-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ec74a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
