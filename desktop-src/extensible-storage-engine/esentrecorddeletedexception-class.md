---
description: 'Saiba mais sobre: classe EsentRecordDeletedException'
title: Classe EsentRecordDeletedException
TOCTitle: EsentRecordDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecorddeletedexception(v=EXCHG.10)
ms:contentKeyID: 55107344
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61d09fca2e154f0a5c5e9e64b85b6a855c460593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921357"
---
# <a name="esentrecorddeletedexception-class"></a><span data-ttu-id="45b4d-103">Classe EsentRecordDeletedException</span><span class="sxs-lookup"><span data-stu-id="45b4d-103">EsentRecordDeletedException class</span></span>

<span data-ttu-id="45b4d-104">Classe base para JET_err. RecordDeleted exceções.</span><span class="sxs-lookup"><span data-stu-id="45b4d-104">Base class for JET_err.RecordDeleted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="45b4d-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="45b4d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="45b4d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="45b4d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="45b4d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="45b4d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="45b4d-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="45b4d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="45b4d-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="45b4d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="45b4d-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="45b4d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="45b4d-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="45b4d-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="45b4d-112">Microsoft. ISAM. ESENT. Interop. EsentRecordDeletedException</span><span class="sxs-lookup"><span data-stu-id="45b4d-112">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>  

<span data-ttu-id="45b4d-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="45b4d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="45b4d-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="45b4d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="45b4d-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="45b4d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordDeletedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordDeletedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="45b4d-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="45b4d-116">Thread safety</span></span>

<span data-ttu-id="45b4d-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="45b4d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="45b4d-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="45b4d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="45b4d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="45b4d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="45b4d-120">Referência</span><span class="sxs-lookup"><span data-stu-id="45b4d-120">Reference</span></span>

[<span data-ttu-id="45b4d-121">Membros do EsentRecordDeletedException</span><span class="sxs-lookup"><span data-stu-id="45b4d-121">EsentRecordDeletedException members</span></span>](./esentrecorddeletedexception-members.md)

[<span data-ttu-id="45b4d-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="45b4d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
