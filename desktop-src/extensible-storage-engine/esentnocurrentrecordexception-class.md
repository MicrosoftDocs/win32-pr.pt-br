---
description: 'Saiba mais sobre: classe EsentNoCurrentRecordException'
title: Classe EsentNoCurrentRecordException
TOCTitle: EsentNoCurrentRecordException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnocurrentrecordexception(v=EXCHG.10)
ms:contentKeyID: 55102290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed58890ccd410101ecc6e6f38fafa0d254f4c2d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780320"
---
# <a name="esentnocurrentrecordexception-class"></a><span data-ttu-id="2025a-103">Classe EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="2025a-103">EsentNoCurrentRecordException class</span></span>

<span data-ttu-id="2025a-104">Classe base para JET_err. NoCurrentRecord exceções.</span><span class="sxs-lookup"><span data-stu-id="2025a-104">Base class for JET_err.NoCurrentRecord exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2025a-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="2025a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2025a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2025a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2025a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2025a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2025a-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="2025a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2025a-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2025a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2025a-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="2025a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2025a-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="2025a-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="2025a-112">Microsoft. ISAM. ESENT. Interop. EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="2025a-112">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>  

<span data-ttu-id="2025a-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2025a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2025a-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2025a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2025a-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2025a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoCurrentRecordException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoCurrentRecordException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoCurrentRecordException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="2025a-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="2025a-116">Thread safety</span></span>

<span data-ttu-id="2025a-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="2025a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2025a-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="2025a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2025a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2025a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2025a-120">Referência</span><span class="sxs-lookup"><span data-stu-id="2025a-120">Reference</span></span>

[<span data-ttu-id="2025a-121">Membros do EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="2025a-121">EsentNoCurrentRecordException members</span></span>](./esentnocurrentrecordexception-members.md)

[<span data-ttu-id="2025a-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2025a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
