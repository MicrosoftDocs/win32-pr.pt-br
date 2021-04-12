---
description: 'Saiba mais sobre: classe EsentInvalidOperationException'
title: Classe EsentInvalidOperationException
TOCTitle: EsentInvalidOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102007
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidOperationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccf4c4fe3b980251c91d11387af02c56cc23772f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297747"
---
# <a name="esentinvalidoperationexception-class"></a><span data-ttu-id="7d793-103">Classe EsentInvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="7d793-103">EsentInvalidOperationException class</span></span>

<span data-ttu-id="7d793-104">Classe base para JET_err. InvalidOperation exceções.</span><span class="sxs-lookup"><span data-stu-id="7d793-104">Base class for JET_err.InvalidOperation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7d793-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="7d793-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7d793-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7d793-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7d793-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7d793-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7d793-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="7d793-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7d793-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7d793-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7d793-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="7d793-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7d793-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="7d793-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="7d793-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="7d793-112">Microsoft.Isam.Esent.Interop.EsentInvalidOperationException</span></span>  

<span data-ttu-id="7d793-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d793-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d793-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d793-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d793-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d793-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidOperationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidOperationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidOperationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="7d793-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="7d793-116">Thread safety</span></span>

<span data-ttu-id="7d793-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7d793-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7d793-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7d793-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d793-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d793-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d793-120">Referência</span><span class="sxs-lookup"><span data-stu-id="7d793-120">Reference</span></span>

[<span data-ttu-id="7d793-121">Membros do EsentInvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="7d793-121">EsentInvalidOperationException members</span></span>](./esentinvalidoperationexception-members.md)

[<span data-ttu-id="7d793-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7d793-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
