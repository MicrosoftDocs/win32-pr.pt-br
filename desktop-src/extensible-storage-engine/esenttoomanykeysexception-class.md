---
description: 'Saiba mais sobre: classe EsentTooManyKeysException'
title: Classe EsentTooManyKeysException
TOCTitle: EsentTooManyKeysException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyKeysException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanykeysexception(v=EXCHG.10)
ms:contentKeyID: 55103066
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyKeysException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyKeysException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d90152c0d811566681599033ffc950d1f880cc2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788846"
---
# <a name="esenttoomanykeysexception-class"></a><span data-ttu-id="f187b-103">Classe EsentTooManyKeysException</span><span class="sxs-lookup"><span data-stu-id="f187b-103">EsentTooManyKeysException class</span></span>

<span data-ttu-id="f187b-104">Classe base para JET_err. TooManyKeys exceções.</span><span class="sxs-lookup"><span data-stu-id="f187b-104">Base class for JET_err.TooManyKeys exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f187b-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="f187b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f187b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f187b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f187b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f187b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f187b-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="f187b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f187b-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f187b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f187b-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f187b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f187b-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="f187b-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="f187b-112">Microsoft. ISAM. ESENT. Interop. EsentTooManyKeysException</span><span class="sxs-lookup"><span data-stu-id="f187b-112">Microsoft.Isam.Esent.Interop.EsentTooManyKeysException</span></span>  

<span data-ttu-id="f187b-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f187b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f187b-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f187b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f187b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f187b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyKeysException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyKeysException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyKeysException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="f187b-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="f187b-116">Thread safety</span></span>

<span data-ttu-id="f187b-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="f187b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f187b-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="f187b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f187b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f187b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f187b-120">Referência</span><span class="sxs-lookup"><span data-stu-id="f187b-120">Reference</span></span>

[<span data-ttu-id="f187b-121">Membros do EsentTooManyKeysException</span><span class="sxs-lookup"><span data-stu-id="f187b-121">EsentTooManyKeysException members</span></span>](./esenttoomanykeysexception-members.md)

[<span data-ttu-id="f187b-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f187b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
