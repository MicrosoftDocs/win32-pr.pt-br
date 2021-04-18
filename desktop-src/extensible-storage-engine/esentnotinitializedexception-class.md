---
description: 'Saiba mais sobre: classe EsentNotInitializedException'
title: Classe EsentNotInitializedException
TOCTitle: EsentNotInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55102300
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInitializedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c026bf7e5e6f9cb132f5c1ca19d23f180b325906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784526"
---
# <a name="esentnotinitializedexception-class"></a><span data-ttu-id="3d869-103">Classe EsentNotInitializedException</span><span class="sxs-lookup"><span data-stu-id="3d869-103">EsentNotInitializedException class</span></span>

<span data-ttu-id="3d869-104">Classe base para JET_err. Exceções não inicializadas.</span><span class="sxs-lookup"><span data-stu-id="3d869-104">Base class for JET_err.NotInitialized exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3d869-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="3d869-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3d869-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3d869-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3d869-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3d869-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3d869-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="3d869-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3d869-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3d869-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3d869-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="3d869-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3d869-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="3d869-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="3d869-112">Microsoft. ISAM. ESENT. Interop. EsentNotInitializedException</span><span class="sxs-lookup"><span data-stu-id="3d869-112">Microsoft.Isam.Esent.Interop.EsentNotInitializedException</span></span>  

<span data-ttu-id="3d869-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d869-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d869-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d869-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d869-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d869-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInitializedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNotInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInitializedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="3d869-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="3d869-116">Thread safety</span></span>

<span data-ttu-id="3d869-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3d869-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3d869-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3d869-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d869-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d869-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d869-120">Referência</span><span class="sxs-lookup"><span data-stu-id="3d869-120">Reference</span></span>

[<span data-ttu-id="3d869-121">Membros do EsentNotInitializedException</span><span class="sxs-lookup"><span data-stu-id="3d869-121">EsentNotInitializedException members</span></span>](./esentnotinitializedexception-members.md)

[<span data-ttu-id="3d869-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3d869-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
