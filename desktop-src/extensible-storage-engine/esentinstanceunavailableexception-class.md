---
description: 'Saiba mais sobre: classe EsentInstanceUnavailableException'
title: Classe EsentInstanceUnavailableException
TOCTitle: EsentInstanceUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinstanceunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3761965a836182480ec934be344322f5b5c6a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815504"
---
# <a name="esentinstanceunavailableexception-class"></a><span data-ttu-id="963cd-103">Classe EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="963cd-103">EsentInstanceUnavailableException class</span></span>

<span data-ttu-id="963cd-104">Classe base para JET_err. InstanceUnavailable exceções.</span><span class="sxs-lookup"><span data-stu-id="963cd-104">Base class for JET_err.InstanceUnavailable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="963cd-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="963cd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="963cd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="963cd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="963cd-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="963cd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="963cd-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="963cd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="963cd-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="963cd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="963cd-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="963cd-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="963cd-111">Microsoft. ISAM. ESENT. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="963cd-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="963cd-112">Microsoft. ISAM. ESENT. Interop. EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="963cd-112">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>  

<span data-ttu-id="963cd-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="963cd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="963cd-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="963cd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="963cd-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="963cd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInstanceUnavailableException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentInstanceUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInstanceUnavailableException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="963cd-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="963cd-116">Thread safety</span></span>

<span data-ttu-id="963cd-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="963cd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="963cd-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="963cd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="963cd-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="963cd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="963cd-120">Referência</span><span class="sxs-lookup"><span data-stu-id="963cd-120">Reference</span></span>

[<span data-ttu-id="963cd-121">Membros do EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="963cd-121">EsentInstanceUnavailableException members</span></span>](./esentinstanceunavailableexception-members.md)

[<span data-ttu-id="963cd-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="963cd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
