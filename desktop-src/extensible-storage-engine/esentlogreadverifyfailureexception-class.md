---
description: 'Saiba mais sobre: classe EsentLogReadVerifyFailureException'
title: Classe EsentLogReadVerifyFailureException
TOCTitle: EsentLogReadVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogreadverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 937d3fa0b721b66d072817ba12c2cf8ba97d5cdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798505"
---
# <a name="esentlogreadverifyfailureexception-class"></a><span data-ttu-id="10e44-103">Classe EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="10e44-103">EsentLogReadVerifyFailureException class</span></span>

<span data-ttu-id="10e44-104">Classe base para JET_err. LogReadVerifyFailure exceções.</span><span class="sxs-lookup"><span data-stu-id="10e44-104">Base class for JET_err.LogReadVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="10e44-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="10e44-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="10e44-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="10e44-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="10e44-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="10e44-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="10e44-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="10e44-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="10e44-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="10e44-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="10e44-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="10e44-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="10e44-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="10e44-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="10e44-112">Microsoft. ISAM. ESENT. Interop. EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="10e44-112">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>  

<span data-ttu-id="10e44-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10e44-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10e44-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10e44-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10e44-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="10e44-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogReadVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogReadVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogReadVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="10e44-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="10e44-116">Thread safety</span></span>

<span data-ttu-id="10e44-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="10e44-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="10e44-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="10e44-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="10e44-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="10e44-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10e44-120">Referência</span><span class="sxs-lookup"><span data-stu-id="10e44-120">Reference</span></span>

[<span data-ttu-id="10e44-121">Membros do EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="10e44-121">EsentLogReadVerifyFailureException members</span></span>](./esentlogreadverifyfailureexception-members.md)

[<span data-ttu-id="10e44-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="10e44-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
