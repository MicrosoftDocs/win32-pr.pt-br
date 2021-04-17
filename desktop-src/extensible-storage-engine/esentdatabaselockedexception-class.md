---
description: 'Saiba mais sobre: classe EsentDatabaseLockedException'
title: Classe EsentDatabaseLockedException
TOCTitle: EsentDatabaseLockedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaselockedexception(v=EXCHG.10)
ms:contentKeyID: 55101527
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97001b234c845d6453818aeeb5a930d090382278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813535"
---
# <a name="esentdatabaselockedexception-class"></a><span data-ttu-id="a1208-103">Classe EsentDatabaseLockedException</span><span class="sxs-lookup"><span data-stu-id="a1208-103">EsentDatabaseLockedException class</span></span>

<span data-ttu-id="a1208-104">Classe base para JET_err. DatabaseLocked exceções.</span><span class="sxs-lookup"><span data-stu-id="a1208-104">Base class for JET_err.DatabaseLocked exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a1208-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="a1208-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a1208-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a1208-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a1208-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a1208-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a1208-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="a1208-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a1208-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a1208-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a1208-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a1208-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a1208-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a1208-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a1208-112">Microsoft. ISAM. ESENT. Interop. EsentDatabaseLockedException</span><span class="sxs-lookup"><span data-stu-id="a1208-112">Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException</span></span>  

<span data-ttu-id="a1208-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a1208-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a1208-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a1208-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a1208-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1208-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLockedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseLockedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLockedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a1208-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="a1208-116">Thread safety</span></span>

<span data-ttu-id="a1208-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a1208-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a1208-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a1208-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1208-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1208-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a1208-120">Referência</span><span class="sxs-lookup"><span data-stu-id="a1208-120">Reference</span></span>

[<span data-ttu-id="a1208-121">Membros do EsentDatabaseLockedException</span><span class="sxs-lookup"><span data-stu-id="a1208-121">EsentDatabaseLockedException members</span></span>](./esentdatabaselockedexception-members.md)

[<span data-ttu-id="a1208-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a1208-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
