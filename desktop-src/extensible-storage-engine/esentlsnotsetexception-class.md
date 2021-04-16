---
description: 'Saiba mais sobre: classe EsentLSNotSetException'
title: Classe EsentLSNotSetException
TOCTitle: EsentLSNotSetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLSNotSetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlsnotsetexception(v=EXCHG.10)
ms:contentKeyID: 55102236
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLSNotSetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLSNotSetException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93671eeaa4172429e2243dee293188e907c0d2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754287"
---
# <a name="esentlsnotsetexception-class"></a><span data-ttu-id="7f304-103">Classe EsentLSNotSetException</span><span class="sxs-lookup"><span data-stu-id="7f304-103">EsentLSNotSetException class</span></span>

<span data-ttu-id="7f304-104">Classe base para JET_err. LSNotSet exceções.</span><span class="sxs-lookup"><span data-stu-id="7f304-104">Base class for JET_err.LSNotSet exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7f304-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="7f304-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7f304-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7f304-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7f304-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7f304-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7f304-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="7f304-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7f304-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7f304-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7f304-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="7f304-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7f304-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="7f304-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="7f304-112">Microsoft. ISAM. ESENT. Interop. EsentLSNotSetException</span><span class="sxs-lookup"><span data-stu-id="7f304-112">Microsoft.Isam.Esent.Interop.EsentLSNotSetException</span></span>  

<span data-ttu-id="7f304-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f304-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f304-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7f304-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f304-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f304-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLSNotSetException _
    Inherits EsentStateException
'Usage
Dim instance As EsentLSNotSetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLSNotSetException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="7f304-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="7f304-116">Thread safety</span></span>

<span data-ttu-id="7f304-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7f304-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7f304-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="7f304-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f304-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f304-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f304-120">Referência</span><span class="sxs-lookup"><span data-stu-id="7f304-120">Reference</span></span>

[<span data-ttu-id="7f304-121">Membros do EsentLSNotSetException</span><span class="sxs-lookup"><span data-stu-id="7f304-121">EsentLSNotSetException members</span></span>](./esentlsnotsetexception-members.md)

[<span data-ttu-id="7f304-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7f304-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
