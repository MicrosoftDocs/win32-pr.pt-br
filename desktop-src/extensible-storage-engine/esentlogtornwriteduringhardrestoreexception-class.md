---
description: 'Saiba mais sobre: classe EsentLogTornWriteDuringHardRestoreException'
title: Classe EsentLogTornWriteDuringHardRestoreException
TOCTitle: EsentLogTornWriteDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogtornwriteduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e0ce33334dfc45bcdc2e643a78b8cca9197f3855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165127"
---
# <a name="esentlogtornwriteduringhardrestoreexception-class"></a><span data-ttu-id="cbdd8-103">Classe EsentLogTornWriteDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="cbdd8-103">EsentLogTornWriteDuringHardRestoreException class</span></span>

<span data-ttu-id="cbdd8-104">Classe base para JET_err. LogTornWriteDuringHardRestore exceções.</span><span class="sxs-lookup"><span data-stu-id="cbdd8-104">Base class for JET_err.LogTornWriteDuringHardRestore exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cbdd8-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="cbdd8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="cbdd8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="cbdd8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="cbdd8-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="cbdd8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="cbdd8-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="cbdd8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="cbdd8-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="cbdd8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="cbdd8-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="cbdd8-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="cbdd8-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="cbdd8-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="cbdd8-112">Microsoft. ISAM. ESENT. Interop. EsentLogTornWriteDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="cbdd8-112">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException</span></span>  

<span data-ttu-id="cbdd8-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cbdd8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cbdd8-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cbdd8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cbdd8-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbdd8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogTornWriteDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogTornWriteDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogTornWriteDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="cbdd8-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="cbdd8-116">Thread safety</span></span>

<span data-ttu-id="cbdd8-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="cbdd8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cbdd8-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="cbdd8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbdd8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbdd8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cbdd8-120">Referência</span><span class="sxs-lookup"><span data-stu-id="cbdd8-120">Reference</span></span>

[<span data-ttu-id="cbdd8-121">Membros do EsentLogTornWriteDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="cbdd8-121">EsentLogTornWriteDuringHardRestoreException members</span></span>](./esentlogtornwriteduringhardrestoreexception-members.md)

[<span data-ttu-id="cbdd8-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cbdd8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
