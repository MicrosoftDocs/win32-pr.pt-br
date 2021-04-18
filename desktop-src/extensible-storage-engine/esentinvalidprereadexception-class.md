---
description: 'Saiba mais sobre: classe EsentInvalidPrereadException'
title: Classe EsentInvalidPrereadException
TOCTitle: EsentInvalidPrereadException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidPrereadException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidprereadexception(v=EXCHG.10)
ms:contentKeyID: 55102086
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidPrereadException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidPrereadException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cba624b2159f84e0fcb94d54c53992b91aee9b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807860"
---
# <a name="esentinvalidprereadexception-class"></a><span data-ttu-id="ae9b2-103">Classe EsentInvalidPrereadException</span><span class="sxs-lookup"><span data-stu-id="ae9b2-103">EsentInvalidPrereadException class</span></span>

<span data-ttu-id="ae9b2-104">Classe base para JET_err. InvalidPreread exceções.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-104">Base class for JET_err.InvalidPreread exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ae9b2-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="ae9b2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ae9b2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ae9b2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ae9b2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ae9b2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ae9b2-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="ae9b2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ae9b2-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ae9b2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ae9b2-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="ae9b2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ae9b2-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="ae9b2-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="ae9b2-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidPrereadException</span><span class="sxs-lookup"><span data-stu-id="ae9b2-112">Microsoft.Isam.Esent.Interop.EsentInvalidPrereadException</span></span>  

<span data-ttu-id="ae9b2-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ae9b2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ae9b2-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ae9b2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9b2-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae9b2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidPrereadException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidPrereadException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidPrereadException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="ae9b2-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="ae9b2-116">Thread safety</span></span>

<span data-ttu-id="ae9b2-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ae9b2-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae9b2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae9b2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae9b2-120">Referência</span><span class="sxs-lookup"><span data-stu-id="ae9b2-120">Reference</span></span>

[<span data-ttu-id="ae9b2-121">Membros do EsentInvalidPrereadException</span><span class="sxs-lookup"><span data-stu-id="ae9b2-121">EsentInvalidPrereadException members</span></span>](./esentinvalidprereadexception-members.md)

[<span data-ttu-id="ae9b2-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ae9b2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
