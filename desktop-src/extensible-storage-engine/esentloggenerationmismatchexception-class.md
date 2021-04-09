---
description: 'Saiba mais sobre: classe EsentLogGenerationMismatchException'
title: Classe EsentLogGenerationMismatchException
TOCTitle: EsentLogGenerationMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentloggenerationmismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102125
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a878330a00147e1d4f24e7882776ad827d97a50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091704"
---
# <a name="esentloggenerationmismatchexception-class"></a><span data-ttu-id="0bcf9-103">Classe EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="0bcf9-103">EsentLogGenerationMismatchException class</span></span>

<span data-ttu-id="0bcf9-104">Classe base para JET_err. LogGenerationMismatch exceções.</span><span class="sxs-lookup"><span data-stu-id="0bcf9-104">Base class for JET_err.LogGenerationMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0bcf9-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="0bcf9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0bcf9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0bcf9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0bcf9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0bcf9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0bcf9-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="0bcf9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0bcf9-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0bcf9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0bcf9-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0bcf9-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0bcf9-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="0bcf9-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="0bcf9-112">Microsoft. ISAM. ESENT. Interop. EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="0bcf9-112">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>  

<span data-ttu-id="0bcf9-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0bcf9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0bcf9-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0bcf9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcf9-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bcf9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogGenerationMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentLogGenerationMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogGenerationMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="0bcf9-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="0bcf9-116">Thread safety</span></span>

<span data-ttu-id="0bcf9-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0bcf9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0bcf9-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0bcf9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0bcf9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bcf9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0bcf9-120">Referência</span><span class="sxs-lookup"><span data-stu-id="0bcf9-120">Reference</span></span>

[<span data-ttu-id="0bcf9-121">Membros do EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="0bcf9-121">EsentLogGenerationMismatchException members</span></span>](./esentloggenerationmismatchexception-members.md)

[<span data-ttu-id="0bcf9-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0bcf9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
