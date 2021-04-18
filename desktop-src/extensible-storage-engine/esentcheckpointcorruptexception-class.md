---
description: 'Saiba mais sobre: classe EsentCheckpointCorruptException'
title: Classe EsentCheckpointCorruptException
TOCTitle: EsentCheckpointCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointcorruptexception(v=EXCHG.10)
ms:contentKeyID: 55101237
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0654ff85fa74cca8435ca6366e301bc3c70fc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813655"
---
# <a name="esentcheckpointcorruptexception-class"></a><span data-ttu-id="61547-103">Classe EsentCheckpointCorruptException</span><span class="sxs-lookup"><span data-stu-id="61547-103">EsentCheckpointCorruptException class</span></span>

<span data-ttu-id="61547-104">Classe base para JET_err. CheckpointCorrupt exceções.</span><span class="sxs-lookup"><span data-stu-id="61547-104">Base class for JET_err.CheckpointCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="61547-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="61547-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="61547-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="61547-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="61547-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="61547-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="61547-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="61547-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="61547-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="61547-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="61547-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="61547-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="61547-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="61547-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="61547-112">Microsoft. ISAM. ESENT. Interop. EsentCheckpointCorruptException</span><span class="sxs-lookup"><span data-stu-id="61547-112">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>  

<span data-ttu-id="61547-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61547-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61547-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61547-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61547-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="61547-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCheckpointCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="61547-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="61547-116">Thread safety</span></span>

<span data-ttu-id="61547-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="61547-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="61547-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="61547-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="61547-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="61547-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61547-120">Referência</span><span class="sxs-lookup"><span data-stu-id="61547-120">Reference</span></span>

[<span data-ttu-id="61547-121">Membros do EsentCheckpointCorruptException</span><span class="sxs-lookup"><span data-stu-id="61547-121">EsentCheckpointCorruptException members</span></span>](./esentcheckpointcorruptexception-members.md)

[<span data-ttu-id="61547-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="61547-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
