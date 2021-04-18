---
description: 'Saiba mais sobre: classe EsentTooManyActiveUsersException'
title: Classe EsentTooManyActiveUsersException
TOCTitle: EsentTooManyActiveUsersException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyactiveusersexception(v=EXCHG.10)
ms:contentKeyID: 55103048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2376821027d1ef51f2e96dab62c7e9a56542c61d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756955"
---
# <a name="esenttoomanyactiveusersexception-class"></a><span data-ttu-id="e3814-103">Classe EsentTooManyActiveUsersException</span><span class="sxs-lookup"><span data-stu-id="e3814-103">EsentTooManyActiveUsersException class</span></span>

<span data-ttu-id="e3814-104">Classe base para JET_err. TooManyActiveUsers exceções.</span><span class="sxs-lookup"><span data-stu-id="e3814-104">Base class for JET_err.TooManyActiveUsers exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e3814-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="e3814-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e3814-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e3814-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e3814-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e3814-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e3814-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="e3814-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e3814-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e3814-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e3814-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e3814-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e3814-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="e3814-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e3814-112">Microsoft. ISAM. ESENT. Interop. EsentTooManyActiveUsersException</span><span class="sxs-lookup"><span data-stu-id="e3814-112">Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException</span></span>  

<span data-ttu-id="e3814-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e3814-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e3814-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e3814-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e3814-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3814-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyActiveUsersException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyActiveUsersException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyActiveUsersException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e3814-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="e3814-116">Thread safety</span></span>

<span data-ttu-id="e3814-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e3814-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e3814-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="e3814-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3814-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3814-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e3814-120">Referência</span><span class="sxs-lookup"><span data-stu-id="e3814-120">Reference</span></span>

[<span data-ttu-id="e3814-121">Membros do EsentTooManyActiveUsersException</span><span class="sxs-lookup"><span data-stu-id="e3814-121">EsentTooManyActiveUsersException members</span></span>](./esenttoomanyactiveusersexception-members.md)

[<span data-ttu-id="e3814-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e3814-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
