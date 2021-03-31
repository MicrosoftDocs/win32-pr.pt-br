---
description: 'Saiba mais sobre: classe EsentKeyTooBigException'
title: Classe EsentKeyTooBigException
TOCTitle: EsentKeyTooBigException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyTooBigException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeytoobigexception(v=EXCHG.10)
ms:contentKeyID: 55102046
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyTooBigException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyTooBigException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0aafd4a5c5460d74b3f7e3c000b47508de2f1ca0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172257"
---
# <a name="esentkeytoobigexception-class"></a><span data-ttu-id="bcfed-103">Classe EsentKeyTooBigException</span><span class="sxs-lookup"><span data-stu-id="bcfed-103">EsentKeyTooBigException class</span></span>

<span data-ttu-id="bcfed-104">Classe base para JET_err. KeyTooBig exceções.</span><span class="sxs-lookup"><span data-stu-id="bcfed-104">Base class for JET_err.KeyTooBig exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bcfed-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="bcfed-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bcfed-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bcfed-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bcfed-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bcfed-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bcfed-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="bcfed-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bcfed-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="bcfed-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bcfed-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="bcfed-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="bcfed-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="bcfed-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="bcfed-112">Microsoft. ISAM. ESENT. Interop. EsentKeyTooBigException</span><span class="sxs-lookup"><span data-stu-id="bcfed-112">Microsoft.Isam.Esent.Interop.EsentKeyTooBigException</span></span>  

<span data-ttu-id="bcfed-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bcfed-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bcfed-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bcfed-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bcfed-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcfed-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyTooBigException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentKeyTooBigException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyTooBigException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="bcfed-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="bcfed-116">Thread safety</span></span>

<span data-ttu-id="bcfed-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bcfed-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bcfed-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="bcfed-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcfed-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcfed-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bcfed-120">Referência</span><span class="sxs-lookup"><span data-stu-id="bcfed-120">Reference</span></span>

[<span data-ttu-id="bcfed-121">Membros do EsentKeyTooBigException</span><span class="sxs-lookup"><span data-stu-id="bcfed-121">EsentKeyTooBigException members</span></span>](./esentkeytoobigexception-members.md)

[<span data-ttu-id="bcfed-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bcfed-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
