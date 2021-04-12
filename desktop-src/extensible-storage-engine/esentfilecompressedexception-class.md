---
description: 'Saiba mais sobre: classe EsentFileCompressedException'
title: Classe EsentFileCompressedException
TOCTitle: EsentFileCompressedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileCompressedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilecompressedexception(v=EXCHG.10)
ms:contentKeyID: 55101678
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileCompressedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileCompressedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17bc3a37cc6d7366319c2a526b3636b9857282aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297317"
---
# <a name="esentfilecompressedexception-class"></a><span data-ttu-id="a9805-103">Classe EsentFileCompressedException</span><span class="sxs-lookup"><span data-stu-id="a9805-103">EsentFileCompressedException class</span></span>

<span data-ttu-id="a9805-104">Classe base para JET_err. Exceções compactadas.</span><span class="sxs-lookup"><span data-stu-id="a9805-104">Base class for JET_err.FileCompressed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a9805-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="a9805-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a9805-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a9805-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a9805-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a9805-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a9805-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="a9805-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a9805-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a9805-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a9805-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a9805-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a9805-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a9805-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a9805-112">Microsoft. ISAM. ESENT. Interop. EsentFileCompressedException</span><span class="sxs-lookup"><span data-stu-id="a9805-112">Microsoft.Isam.Esent.Interop.EsentFileCompressedException</span></span>  

<span data-ttu-id="a9805-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a9805-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a9805-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a9805-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a9805-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9805-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileCompressedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFileCompressedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileCompressedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a9805-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="a9805-116">Thread safety</span></span>

<span data-ttu-id="a9805-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a9805-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a9805-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a9805-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9805-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9805-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a9805-120">Referência</span><span class="sxs-lookup"><span data-stu-id="a9805-120">Reference</span></span>

[<span data-ttu-id="a9805-121">Membros do EsentFileCompressedException</span><span class="sxs-lookup"><span data-stu-id="a9805-121">EsentFileCompressedException members</span></span>](./esentfilecompressedexception-members.md)

[<span data-ttu-id="a9805-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a9805-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
