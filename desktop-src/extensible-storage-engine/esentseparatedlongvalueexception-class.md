---
description: 'Saiba mais sobre: classe EsentSeparatedLongValueException'
title: Classe EsentSeparatedLongValueException
TOCTitle: EsentSeparatedLongValueException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentseparatedlongvalueexception(v=EXCHG.10)
ms:contentKeyID: 55107331
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35977f8b27914799097188030f6b91afd055d08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011273"
---
# <a name="esentseparatedlongvalueexception-class"></a><span data-ttu-id="9b984-103">Classe EsentSeparatedLongValueException</span><span class="sxs-lookup"><span data-stu-id="9b984-103">EsentSeparatedLongValueException class</span></span>

<span data-ttu-id="9b984-104">Classe base para JET_err. SeparatedLongValue exceções.</span><span class="sxs-lookup"><span data-stu-id="9b984-104">Base class for JET_err.SeparatedLongValue exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9b984-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="9b984-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9b984-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9b984-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9b984-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="9b984-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9b984-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="9b984-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9b984-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9b984-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9b984-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="9b984-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="9b984-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="9b984-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="9b984-112">Microsoft. ISAM. ESENT. Interop. EsentSeparatedLongValueException</span><span class="sxs-lookup"><span data-stu-id="9b984-112">Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException</span></span>  

<span data-ttu-id="9b984-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9b984-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9b984-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9b984-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9b984-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b984-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSeparatedLongValueException _
    Inherits EsentStateException
'Usage
Dim instance As EsentSeparatedLongValueException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSeparatedLongValueException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="9b984-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="9b984-116">Thread safety</span></span>

<span data-ttu-id="9b984-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9b984-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9b984-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9b984-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b984-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b984-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9b984-120">Referência</span><span class="sxs-lookup"><span data-stu-id="9b984-120">Reference</span></span>

[<span data-ttu-id="9b984-121">Membros do EsentSeparatedLongValueException</span><span class="sxs-lookup"><span data-stu-id="9b984-121">EsentSeparatedLongValueException members</span></span>](./esentseparatedlongvalueexception-members.md)

[<span data-ttu-id="9b984-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9b984-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
