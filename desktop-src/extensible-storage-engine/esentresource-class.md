---
description: 'Saiba mais sobre: classe EsentResource'
title: Classe EsentResource
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787644"
---
# <a name="esentresource-class"></a><span data-ttu-id="cd9ab-103">Classe EsentResource</span><span class="sxs-lookup"><span data-stu-id="cd9ab-103">EsentResource class</span></span>

<span data-ttu-id="cd9ab-104">Essa é a classe base para todos os objetos de recurso de ESENT.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-104">This is the base class for all esent resource objects.</span></span> <span data-ttu-id="cd9ab-105">As subclasses dessa classe podem alocar e liberar recursos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-105">Subclasses of this class can allocate and release unmanaged resources.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cd9ab-106">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="cd9ab-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="cd9ab-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="cd9ab-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="cd9ab-108">Microsoft. ISAM. ESENT. Interop. EsentResource</span><span class="sxs-lookup"><span data-stu-id="cd9ab-108">Microsoft.Isam.Esent.Interop.EsentResource</span></span>  
    [<span data-ttu-id="cd9ab-109">Microsoft. ISAM. ESENT. Interop. Session</span><span class="sxs-lookup"><span data-stu-id="cd9ab-109">Microsoft.Isam.Esent.Interop.Session</span></span>](./session-class.md)  
    [<span data-ttu-id="cd9ab-110">Microsoft. ISAM. ESENT. Interop. Table</span><span class="sxs-lookup"><span data-stu-id="cd9ab-110">Microsoft.Isam.Esent.Interop.Table</span></span>](./table-class.md)  
    [<span data-ttu-id="cd9ab-111">Microsoft. ISAM. ESENT. Interop. Transaction</span><span class="sxs-lookup"><span data-stu-id="cd9ab-111">Microsoft.Isam.Esent.Interop.Transaction</span></span>](./transaction-class.md)  
    [<span data-ttu-id="cd9ab-112">Microsoft. ISAM. ESENT. Interop. Update</span><span class="sxs-lookup"><span data-stu-id="cd9ab-112">Microsoft.Isam.Esent.Interop.Update</span></span>](./update-class.md)  
    [<span data-ttu-id="cd9ab-113">Microsoft. ISAM. ESENT. Interop. Windows8. DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="cd9ab-113">Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback</span></span>](./durablecommitcallback-class.md)  

<span data-ttu-id="cd9ab-114">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cd9ab-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cd9ab-115">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cd9ab-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9ab-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd9ab-116">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a><span data-ttu-id="cd9ab-117">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="cd9ab-117">Thread safety</span></span>

<span data-ttu-id="cd9ab-118">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cd9ab-119">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="cd9ab-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd9ab-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd9ab-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cd9ab-121">Referência</span><span class="sxs-lookup"><span data-stu-id="cd9ab-121">Reference</span></span>

[<span data-ttu-id="cd9ab-122">Membros do EsentResource</span><span class="sxs-lookup"><span data-stu-id="cd9ab-122">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="cd9ab-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cd9ab-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
