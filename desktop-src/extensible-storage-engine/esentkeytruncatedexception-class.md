---
description: 'Saiba mais sobre: classe EsentKeyTruncatedException'
title: Classe EsentKeyTruncatedException
TOCTitle: EsentKeyTruncatedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeytruncatedexception(v=EXCHG.10)
ms:contentKeyID: 55102126
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ba38f11d6e78383bb313a9ae798b79efb2bfd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747250"
---
# <a name="esentkeytruncatedexception-class"></a><span data-ttu-id="b1c47-103">Classe EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="b1c47-103">EsentKeyTruncatedException class</span></span>

<span data-ttu-id="b1c47-104">Classe base para JET_err. Exceções de keytruncate.</span><span class="sxs-lookup"><span data-stu-id="b1c47-104">Base class for JET_err.KeyTruncated exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b1c47-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="b1c47-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b1c47-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b1c47-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b1c47-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b1c47-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b1c47-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="b1c47-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b1c47-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b1c47-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b1c47-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b1c47-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b1c47-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="b1c47-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="b1c47-112">Microsoft. ISAM. ESENT. Interop. EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="b1c47-112">Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException</span></span>  

<span data-ttu-id="b1c47-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1c47-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b1c47-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1c47-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1c47-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1c47-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyTruncatedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentKeyTruncatedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyTruncatedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="b1c47-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="b1c47-116">Thread safety</span></span>

<span data-ttu-id="b1c47-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b1c47-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b1c47-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b1c47-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1c47-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1c47-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1c47-120">Referência</span><span class="sxs-lookup"><span data-stu-id="b1c47-120">Reference</span></span>

[<span data-ttu-id="b1c47-121">Membros do EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="b1c47-121">EsentKeyTruncatedException members</span></span>](./esentkeytruncatedexception-members.md)

[<span data-ttu-id="b1c47-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b1c47-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
