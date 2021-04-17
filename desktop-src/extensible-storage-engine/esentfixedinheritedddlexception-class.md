---
description: 'Saiba mais sobre: classe EsentFixedInheritedDDLException'
title: Classe EsentFixedInheritedDDLException
TOCTitle: EsentFixedInheritedDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfixedinheritedddlexception(v=EXCHG.10)
ms:contentKeyID: 55101724
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f8638b396848503819635860b7472a8af684c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797607"
---
# <a name="esentfixedinheritedddlexception-class"></a><span data-ttu-id="51905-103">Classe EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="51905-103">EsentFixedInheritedDDLException class</span></span>

<span data-ttu-id="51905-104">Classe base para JET_err. FixedInheritedDDL exceções.</span><span class="sxs-lookup"><span data-stu-id="51905-104">Base class for JET_err.FixedInheritedDDL exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="51905-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="51905-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="51905-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="51905-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="51905-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="51905-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="51905-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="51905-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="51905-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="51905-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="51905-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="51905-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="51905-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="51905-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="51905-112">Microsoft. ISAM. ESENT. Interop. EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="51905-112">Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException</span></span>  

<span data-ttu-id="51905-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="51905-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="51905-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="51905-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="51905-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="51905-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFixedInheritedDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFixedInheritedDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFixedInheritedDDLException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="51905-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="51905-116">Thread safety</span></span>

<span data-ttu-id="51905-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="51905-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="51905-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="51905-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="51905-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="51905-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51905-120">Referência</span><span class="sxs-lookup"><span data-stu-id="51905-120">Reference</span></span>

[<span data-ttu-id="51905-121">Membros do EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="51905-121">EsentFixedInheritedDDLException members</span></span>](./esentfixedinheritedddlexception-members.md)

[<span data-ttu-id="51905-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="51905-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
