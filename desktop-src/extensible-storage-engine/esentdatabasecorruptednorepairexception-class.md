---
description: 'Saiba mais sobre: classe EsentDatabaseCorruptedNoRepairException'
title: Classe EsentDatabaseCorruptedNoRepairException
TOCTitle: EsentDatabaseCorruptedNoRepairException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasecorruptednorepairexception(v=EXCHG.10)
ms:contentKeyID: 55101445
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1db5ebfb204e5b74a34e5fe52e7a5cc81260f194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501857"
---
# <a name="esentdatabasecorruptednorepairexception-class"></a><span data-ttu-id="6dc6d-103">Classe EsentDatabaseCorruptedNoRepairException</span><span class="sxs-lookup"><span data-stu-id="6dc6d-103">EsentDatabaseCorruptedNoRepairException class</span></span>

<span data-ttu-id="6dc6d-104">Classe base para JET_err. DatabaseCorruptedNoRepair exceções.</span><span class="sxs-lookup"><span data-stu-id="6dc6d-104">Base class for JET_err.DatabaseCorruptedNoRepair exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6dc6d-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="6dc6d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6dc6d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6dc6d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6dc6d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="6dc6d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6dc6d-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="6dc6d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6dc6d-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="6dc6d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6dc6d-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="6dc6d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6dc6d-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="6dc6d-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="6dc6d-112">Microsoft. ISAM. ESENT. Interop. EsentDatabaseCorruptedNoRepairException</span><span class="sxs-lookup"><span data-stu-id="6dc6d-112">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedNoRepairException</span></span>  

<span data-ttu-id="6dc6d-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6dc6d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6dc6d-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6dc6d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc6d-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dc6d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseCorruptedNoRepairException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseCorruptedNoRepairException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseCorruptedNoRepairException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="6dc6d-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="6dc6d-116">Thread safety</span></span>

<span data-ttu-id="6dc6d-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="6dc6d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6dc6d-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="6dc6d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dc6d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6dc6d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6dc6d-120">Referência</span><span class="sxs-lookup"><span data-stu-id="6dc6d-120">Reference</span></span>

[<span data-ttu-id="6dc6d-121">Membros do EsentDatabaseCorruptedNoRepairException</span><span class="sxs-lookup"><span data-stu-id="6dc6d-121">EsentDatabaseCorruptedNoRepairException members</span></span>](./esentdatabasecorruptednorepairexception-members.md)

[<span data-ttu-id="6dc6d-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6dc6d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
