---
description: 'Saiba mais sobre: classe EsentCommittedLogFilesMissingException'
title: Classe EsentCommittedLogFilesMissingException
TOCTitle: EsentCommittedLogFilesMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcommittedlogfilesmissingexception(v=EXCHG.10)
ms:contentKeyID: 55101361
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 937534d550ff13fce4240411ce486e6d789ef957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783730"
---
# <a name="esentcommittedlogfilesmissingexception-class"></a><span data-ttu-id="2e7f9-103">Classe EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="2e7f9-103">EsentCommittedLogFilesMissingException class</span></span>

<span data-ttu-id="2e7f9-104">Classe base para exceções de JET_err. CommittedLogFilesMissing.</span><span class="sxs-lookup"><span data-stu-id="2e7f9-104">Base class for JET_err.CommittedLogFilesMissing exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2e7f9-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="2e7f9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2e7f9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e7f9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2e7f9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2e7f9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2e7f9-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="2e7f9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2e7f9-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2e7f9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2e7f9-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="2e7f9-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="2e7f9-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2e7f9-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="2e7f9-112">Microsoft. ISAM. ESENT. Interop. EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="2e7f9-112">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>  

<span data-ttu-id="2e7f9-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e7f9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e7f9-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2e7f9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7f9-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e7f9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCommittedLogFilesMissingException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCommittedLogFilesMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCommittedLogFilesMissingException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="2e7f9-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="2e7f9-116">Thread safety</span></span>

<span data-ttu-id="2e7f9-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="2e7f9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2e7f9-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="2e7f9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e7f9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e7f9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e7f9-120">Referência</span><span class="sxs-lookup"><span data-stu-id="2e7f9-120">Reference</span></span>

[<span data-ttu-id="2e7f9-121">Membros do EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="2e7f9-121">EsentCommittedLogFilesMissingException members</span></span>](./esentcommittedlogfilesmissingexception-members.md)

[<span data-ttu-id="2e7f9-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2e7f9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
