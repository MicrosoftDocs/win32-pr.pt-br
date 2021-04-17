---
description: 'Saiba mais sobre: classe EsentFileAccessDeniedException'
title: Classe EsentFileAccessDeniedException
TOCTitle: EsentFileAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101658
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afb92cc5fad314763ef2d679035b727f38b8305a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784187"
---
# <a name="esentfileaccessdeniedexception-class"></a><span data-ttu-id="0b667-103">Classe EsentFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="0b667-103">EsentFileAccessDeniedException class</span></span>

<span data-ttu-id="0b667-104">Classe base para JET_err. FileAccessDenied exceções.</span><span class="sxs-lookup"><span data-stu-id="0b667-104">Base class for JET_err.FileAccessDenied exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0b667-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="0b667-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0b667-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0b667-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0b667-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0b667-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0b667-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="0b667-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0b667-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0b667-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0b667-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="0b667-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="0b667-111">Microsoft. ISAM. ESENT. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="0b667-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="0b667-112">Microsoft. ISAM. ESENT. Interop. EsentFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="0b667-112">Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException</span></span>  

<span data-ttu-id="0b667-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b667-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b667-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b667-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b667-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b667-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileAccessDeniedException _
    Inherits EsentIOException
'Usage
Dim instance As EsentFileAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileAccessDeniedException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="0b667-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="0b667-116">Thread safety</span></span>

<span data-ttu-id="0b667-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0b667-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0b667-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="0b667-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b667-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b667-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b667-120">Referência</span><span class="sxs-lookup"><span data-stu-id="0b667-120">Reference</span></span>

[<span data-ttu-id="0b667-121">Membros do EsentFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="0b667-121">EsentFileAccessDeniedException members</span></span>](./esentfileaccessdeniedexception-members.md)

[<span data-ttu-id="0b667-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0b667-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
