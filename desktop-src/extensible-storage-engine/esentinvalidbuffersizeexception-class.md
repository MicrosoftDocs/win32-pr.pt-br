---
description: 'Saiba mais sobre: classe EsentInvalidBufferSizeException'
title: Classe EsentInvalidBufferSizeException
TOCTitle: EsentInvalidBufferSizeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidbuffersizeexception(v=EXCHG.10)
ms:contentKeyID: 55101912
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0dc693135124ba5d2979fa0f1a7ff80fcca27600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828806"
---
# <a name="esentinvalidbuffersizeexception-class"></a><span data-ttu-id="1fa45-103">Classe EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="1fa45-103">EsentInvalidBufferSizeException class</span></span>

<span data-ttu-id="1fa45-104">Classe base para JET_err. InvalidBufferSize exceções.</span><span class="sxs-lookup"><span data-stu-id="1fa45-104">Base class for JET_err.InvalidBufferSize exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1fa45-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="1fa45-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1fa45-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fa45-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1fa45-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1fa45-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1fa45-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="1fa45-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1fa45-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1fa45-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1fa45-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1fa45-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1fa45-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="1fa45-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="1fa45-112">Microsoft. ISAM. ESENT. Interop. EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="1fa45-112">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>  

<span data-ttu-id="1fa45-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fa45-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1fa45-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1fa45-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa45-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fa45-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidBufferSizeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentInvalidBufferSizeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidBufferSizeException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="1fa45-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="1fa45-116">Thread safety</span></span>

<span data-ttu-id="1fa45-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="1fa45-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1fa45-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="1fa45-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fa45-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fa45-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fa45-120">Referência</span><span class="sxs-lookup"><span data-stu-id="1fa45-120">Reference</span></span>

[<span data-ttu-id="1fa45-121">Membros do EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="1fa45-121">EsentInvalidBufferSizeException members</span></span>](./esentinvalidbuffersizeexception-members.md)

[<span data-ttu-id="1fa45-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1fa45-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
