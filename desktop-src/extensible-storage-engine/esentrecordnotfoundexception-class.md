---
description: 'Saiba mais sobre: classe EsentRecordNotFoundException'
title: Classe EsentRecordNotFoundException
TOCTitle: EsentRecordNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55102528
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c013bda1ba0592b2137e4bc428ccf4bc195fc6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798476"
---
# <a name="esentrecordnotfoundexception-class"></a><span data-ttu-id="8152b-103">Classe EsentRecordNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8152b-103">EsentRecordNotFoundException class</span></span>

<span data-ttu-id="8152b-104">Classe base para JET_err. RecordNotFound exceções.</span><span class="sxs-lookup"><span data-stu-id="8152b-104">Base class for JET_err.RecordNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8152b-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="8152b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8152b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8152b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8152b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8152b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8152b-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="8152b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8152b-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8152b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8152b-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="8152b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8152b-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="8152b-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="8152b-112">Microsoft. ISAM. ESENT. Interop. EsentRecordNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8152b-112">Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException</span></span>  

<span data-ttu-id="8152b-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8152b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8152b-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8152b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8152b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="8152b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNotFoundException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNotFoundException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="8152b-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="8152b-116">Thread safety</span></span>

<span data-ttu-id="8152b-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="8152b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8152b-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="8152b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8152b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8152b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8152b-120">Referência</span><span class="sxs-lookup"><span data-stu-id="8152b-120">Reference</span></span>

[<span data-ttu-id="8152b-121">Membros do EsentRecordNotFoundException</span><span class="sxs-lookup"><span data-stu-id="8152b-121">EsentRecordNotFoundException members</span></span>](./esentrecordnotfoundexception-members.md)

[<span data-ttu-id="8152b-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8152b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
