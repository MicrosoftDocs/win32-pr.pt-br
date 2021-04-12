---
description: 'Saiba mais sobre: classe EsentInvalidInstanceException'
title: Classe EsentInvalidInstanceException
TOCTitle: EsentInvalidInstanceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidinstanceexception(v=EXCHG.10)
ms:contentKeyID: 55101939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ba855e89f7714b7042b882b5c8cb28eba3dca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171080"
---
# <a name="esentinvalidinstanceexception-class"></a><span data-ttu-id="b915f-103">Classe EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="b915f-103">EsentInvalidInstanceException class</span></span>

<span data-ttu-id="b915f-104">Classe base para JET_err. InvalidInstance exceções.</span><span class="sxs-lookup"><span data-stu-id="b915f-104">Base class for JET_err.InvalidInstance exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b915f-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="b915f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b915f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b915f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b915f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b915f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b915f-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="b915f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b915f-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b915f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b915f-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b915f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b915f-111">Microsoft. ISAM. ESENT. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="b915f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b915f-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="b915f-112">Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException</span></span>  

<span data-ttu-id="b915f-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b915f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b915f-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b915f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b915f-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="b915f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidInstanceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidInstanceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidInstanceException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b915f-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="b915f-116">Thread safety</span></span>

<span data-ttu-id="b915f-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b915f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b915f-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b915f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b915f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b915f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b915f-120">Referência</span><span class="sxs-lookup"><span data-stu-id="b915f-120">Reference</span></span>

[<span data-ttu-id="b915f-121">Membros do EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="b915f-121">EsentInvalidInstanceException members</span></span>](./esentinvalidinstanceexception-members.md)

[<span data-ttu-id="b915f-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b915f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
