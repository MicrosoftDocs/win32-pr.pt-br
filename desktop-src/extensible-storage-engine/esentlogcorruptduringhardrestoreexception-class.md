---
description: 'Saiba mais sobre: classe EsentLogCorruptDuringHardRestoreException'
title: Classe EsentLogCorruptDuringHardRestoreException
TOCTitle: EsentLogCorruptDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: daeabeae72916781e01640cd0de10c737b53e5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171896"
---
# <a name="esentlogcorruptduringhardrestoreexception-class"></a><span data-ttu-id="f26a8-103">Classe EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="f26a8-103">EsentLogCorruptDuringHardRestoreException class</span></span>

<span data-ttu-id="f26a8-104">Classe base para JET_err. LogCorruptDuringHardRestore exceções.</span><span class="sxs-lookup"><span data-stu-id="f26a8-104">Base class for JET_err.LogCorruptDuringHardRestore exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f26a8-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="f26a8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f26a8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f26a8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f26a8-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f26a8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f26a8-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="f26a8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f26a8-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f26a8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f26a8-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="f26a8-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="f26a8-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="f26a8-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="f26a8-112">Microsoft. ISAM. ESENT. Interop. EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="f26a8-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>  

<span data-ttu-id="f26a8-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f26a8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f26a8-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f26a8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f26a8-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="f26a8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="f26a8-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="f26a8-116">Thread safety</span></span>

<span data-ttu-id="f26a8-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="f26a8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f26a8-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="f26a8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f26a8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f26a8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f26a8-120">Referência</span><span class="sxs-lookup"><span data-stu-id="f26a8-120">Reference</span></span>

[<span data-ttu-id="f26a8-121">Membros do EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="f26a8-121">EsentLogCorruptDuringHardRestoreException members</span></span>](./esentlogcorruptduringhardrestoreexception-members.md)

[<span data-ttu-id="f26a8-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f26a8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
