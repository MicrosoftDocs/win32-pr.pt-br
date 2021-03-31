---
description: 'Saiba mais sobre: classe EsentMustCommitDistributedTransactionToLevel0Exception'
title: Classe EsentMustCommitDistributedTransactionToLevel0Exception
TOCTitle: EsentMustCommitDistributedTransactionToLevel0Exception class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmustcommitdistributedtransactiontolevel0exception(v=EXCHG.10)
ms:contentKeyID: 55102329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 660610563676276bb3387fcbb8e9b5959df03067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921304"
---
# <a name="esentmustcommitdistributedtransactiontolevel0exception-class"></a><span data-ttu-id="3b4a9-103">Classe EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="3b4a9-103">EsentMustCommitDistributedTransactionToLevel0Exception class</span></span>

<span data-ttu-id="3b4a9-104">Classe base para JET_err. MustCommitDistributedTransactionToLevel0 exceções.</span><span class="sxs-lookup"><span data-stu-id="3b4a9-104">Base class for JET_err.MustCommitDistributedTransactionToLevel0 exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3b4a9-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="3b4a9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3b4a9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3b4a9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3b4a9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3b4a9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3b4a9-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="3b4a9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3b4a9-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3b4a9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3b4a9-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="3b4a9-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3b4a9-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="3b4a9-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="3b4a9-112">Microsoft. ISAM. ESENT. Interop. EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="3b4a9-112">Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception</span></span>  

<span data-ttu-id="3b4a9-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b4a9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b4a9-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b4a9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4a9-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b4a9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMustCommitDistributedTransactionToLevel0Exception _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentMustCommitDistributedTransactionToLevel0Exception
```

``` csharp
[SerializableAttribute]
public sealed class EsentMustCommitDistributedTransactionToLevel0Exception : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="3b4a9-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="3b4a9-116">Thread safety</span></span>

<span data-ttu-id="3b4a9-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3b4a9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3b4a9-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3b4a9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b4a9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b4a9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b4a9-120">Referência</span><span class="sxs-lookup"><span data-stu-id="3b4a9-120">Reference</span></span>

[<span data-ttu-id="3b4a9-121">Membros do EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="3b4a9-121">EsentMustCommitDistributedTransactionToLevel0Exception members</span></span>](./esentmustcommitdistributedtransactiontolevel0exception-members.md)

[<span data-ttu-id="3b4a9-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3b4a9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
