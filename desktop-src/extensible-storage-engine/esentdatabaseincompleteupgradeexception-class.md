---
description: 'Saiba mais sobre: classe EsentDatabaseIncompleteUpgradeException'
title: Classe EsentDatabaseIncompleteUpgradeException
TOCTitle: EsentDatabaseIncompleteUpgradeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteupgradeexception(v=EXCHG.10)
ms:contentKeyID: 55101371
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ae6272559c537ae870794a9d5a7a76bb8672b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761691"
---
# <a name="esentdatabaseincompleteupgradeexception-class"></a><span data-ttu-id="244e9-103">Classe EsentDatabaseIncompleteUpgradeException</span><span class="sxs-lookup"><span data-stu-id="244e9-103">EsentDatabaseIncompleteUpgradeException class</span></span>

<span data-ttu-id="244e9-104">Classe base para JET_err. DatabaseIncompleteUpgrade exceções.</span><span class="sxs-lookup"><span data-stu-id="244e9-104">Base class for JET_err.DatabaseIncompleteUpgrade exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="244e9-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="244e9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="244e9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="244e9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="244e9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="244e9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="244e9-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="244e9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="244e9-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="244e9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="244e9-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="244e9-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="244e9-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="244e9-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="244e9-112">Microsoft. ISAM. ESENT. Interop. EsentDatabaseIncompleteUpgradeException</span><span class="sxs-lookup"><span data-stu-id="244e9-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>  

<span data-ttu-id="244e9-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="244e9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="244e9-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="244e9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="244e9-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="244e9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteUpgradeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseIncompleteUpgradeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteUpgradeException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="244e9-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="244e9-116">Thread safety</span></span>

<span data-ttu-id="244e9-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="244e9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="244e9-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="244e9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="244e9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="244e9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="244e9-120">Referência</span><span class="sxs-lookup"><span data-stu-id="244e9-120">Reference</span></span>

[<span data-ttu-id="244e9-121">Membros do EsentDatabaseIncompleteUpgradeException</span><span class="sxs-lookup"><span data-stu-id="244e9-121">EsentDatabaseIncompleteUpgradeException members</span></span>](./esentdatabaseincompleteupgradeexception-members.md)

[<span data-ttu-id="244e9-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="244e9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
