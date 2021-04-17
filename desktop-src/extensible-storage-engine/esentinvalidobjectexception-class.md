---
description: 'Saiba mais sobre: classe EsentInvalidObjectException'
title: Classe EsentInvalidObjectException
TOCTitle: EsentInvalidObjectException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidobjectexception(v=EXCHG.10)
ms:contentKeyID: 55107288
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86cf06f1f291ca6f2637e652a61b27319b4fa7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811459"
---
# <a name="esentinvalidobjectexception-class"></a><span data-ttu-id="ee0b2-103">Classe EsentInvalidObjectException</span><span class="sxs-lookup"><span data-stu-id="ee0b2-103">EsentInvalidObjectException class</span></span>

<span data-ttu-id="ee0b2-104">Classe base para JET_err. Exceções inválidas.</span><span class="sxs-lookup"><span data-stu-id="ee0b2-104">Base class for JET_err.InvalidObject exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ee0b2-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="ee0b2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ee0b2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ee0b2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ee0b2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ee0b2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ee0b2-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="ee0b2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ee0b2-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ee0b2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ee0b2-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="ee0b2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ee0b2-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="ee0b2-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="ee0b2-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidObjectException</span><span class="sxs-lookup"><span data-stu-id="ee0b2-112">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>  

<span data-ttu-id="ee0b2-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee0b2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ee0b2-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ee0b2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee0b2-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee0b2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidObjectException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidObjectException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidObjectException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="ee0b2-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="ee0b2-116">Thread safety</span></span>

<span data-ttu-id="ee0b2-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ee0b2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ee0b2-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ee0b2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee0b2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee0b2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee0b2-120">Referência</span><span class="sxs-lookup"><span data-stu-id="ee0b2-120">Reference</span></span>

[<span data-ttu-id="ee0b2-121">Membros do EsentInvalidObjectException</span><span class="sxs-lookup"><span data-stu-id="ee0b2-121">EsentInvalidObjectException members</span></span>](./esentinvalidobjectexception-members.md)

[<span data-ttu-id="ee0b2-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ee0b2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
