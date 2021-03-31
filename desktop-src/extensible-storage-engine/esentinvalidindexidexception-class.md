---
description: 'Saiba mais sobre: classe EsentInvalidIndexIdException'
title: Classe EsentInvalidIndexIdException
TOCTitle: EsentInvalidIndexIdException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidIndexIdException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidindexidexception(v=EXCHG.10)
ms:contentKeyID: 55101962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidIndexIdException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidIndexIdException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d101f9ea68e23505126ca0ad8bf32d8843e53a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663089"
---
# <a name="esentinvalidindexidexception-class"></a><span data-ttu-id="3b4f7-103">Classe EsentInvalidIndexIdException</span><span class="sxs-lookup"><span data-stu-id="3b4f7-103">EsentInvalidIndexIdException class</span></span>

<span data-ttu-id="3b4f7-104">Classe base para JET_err. InvalidIndexId exceções.</span><span class="sxs-lookup"><span data-stu-id="3b4f7-104">Base class for JET_err.InvalidIndexId exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3b4f7-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="3b4f7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3b4f7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3b4f7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3b4f7-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3b4f7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3b4f7-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="3b4f7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3b4f7-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3b4f7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3b4f7-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="3b4f7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3b4f7-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="3b4f7-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="3b4f7-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidIndexIdException</span><span class="sxs-lookup"><span data-stu-id="3b4f7-112">Microsoft.Isam.Esent.Interop.EsentInvalidIndexIdException</span></span>  

<span data-ttu-id="3b4f7-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b4f7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b4f7-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b4f7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4f7-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b4f7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidIndexIdException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidIndexIdException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidIndexIdException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="3b4f7-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="3b4f7-116">Thread safety</span></span>

<span data-ttu-id="3b4f7-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3b4f7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3b4f7-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3b4f7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b4f7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b4f7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b4f7-120">Referência</span><span class="sxs-lookup"><span data-stu-id="3b4f7-120">Reference</span></span>

[<span data-ttu-id="3b4f7-121">Membros do EsentInvalidIndexIdException</span><span class="sxs-lookup"><span data-stu-id="3b4f7-121">EsentInvalidIndexIdException members</span></span>](./esentinvalidindexidexception-members.md)

[<span data-ttu-id="3b4f7-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3b4f7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
