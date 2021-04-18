---
description: 'Saiba mais sobre: classe EsentRestoreInProgressException'
title: Classe EsentRestoreInProgressException
TOCTitle: EsentRestoreInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrestoreinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55102631
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0906d1ee8c196260d36da8d385a0e48e12f31018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781618"
---
# <a name="esentrestoreinprogressexception-class"></a><span data-ttu-id="04432-103">Classe EsentRestoreInProgressException</span><span class="sxs-lookup"><span data-stu-id="04432-103">EsentRestoreInProgressException class</span></span>

<span data-ttu-id="04432-104">Classe base para JET_err. RestoreInProgress exceções.</span><span class="sxs-lookup"><span data-stu-id="04432-104">Base class for JET_err.RestoreInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="04432-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="04432-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="04432-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="04432-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="04432-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="04432-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="04432-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="04432-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="04432-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="04432-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="04432-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="04432-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="04432-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="04432-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="04432-112">Microsoft. ISAM. ESENT. Interop. EsentRestoreInProgressException</span><span class="sxs-lookup"><span data-stu-id="04432-112">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>  

<span data-ttu-id="04432-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04432-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04432-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="04432-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04432-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="04432-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRestoreInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRestoreInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRestoreInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="04432-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="04432-116">Thread safety</span></span>

<span data-ttu-id="04432-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="04432-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="04432-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="04432-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="04432-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="04432-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04432-120">Referência</span><span class="sxs-lookup"><span data-stu-id="04432-120">Reference</span></span>

[<span data-ttu-id="04432-121">Membros do EsentRestoreInProgressException</span><span class="sxs-lookup"><span data-stu-id="04432-121">EsentRestoreInProgressException members</span></span>](./esentrestoreinprogressexception-members.md)

[<span data-ttu-id="04432-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="04432-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
