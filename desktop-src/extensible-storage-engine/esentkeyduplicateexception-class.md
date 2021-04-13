---
description: 'Saiba mais sobre: classe EsentKeyDuplicateException'
title: Classe EsentKeyDuplicateException
TOCTitle: EsentKeyDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeyduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102039
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d63945d5db3ca97e858e7f02fd2b4e8a9045f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297550"
---
# <a name="esentkeyduplicateexception-class"></a><span data-ttu-id="afe2c-103">Classe EsentKeyDuplicateException</span><span class="sxs-lookup"><span data-stu-id="afe2c-103">EsentKeyDuplicateException class</span></span>

<span data-ttu-id="afe2c-104">Classe base para JET_err. Exceções de keyduplicação.</span><span class="sxs-lookup"><span data-stu-id="afe2c-104">Base class for JET_err.KeyDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="afe2c-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="afe2c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="afe2c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="afe2c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="afe2c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="afe2c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="afe2c-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="afe2c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="afe2c-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="afe2c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="afe2c-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="afe2c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="afe2c-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="afe2c-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="afe2c-112">Microsoft. ISAM. ESENT. Interop. EsentKeyDuplicateException</span><span class="sxs-lookup"><span data-stu-id="afe2c-112">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>  

<span data-ttu-id="afe2c-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afe2c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afe2c-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="afe2c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afe2c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="afe2c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentKeyDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="afe2c-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="afe2c-116">Thread safety</span></span>

<span data-ttu-id="afe2c-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="afe2c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="afe2c-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="afe2c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="afe2c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="afe2c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afe2c-120">Referência</span><span class="sxs-lookup"><span data-stu-id="afe2c-120">Reference</span></span>

[<span data-ttu-id="afe2c-121">Membros do EsentKeyDuplicateException</span><span class="sxs-lookup"><span data-stu-id="afe2c-121">EsentKeyDuplicateException members</span></span>](./esentkeyduplicateexception-members.md)

[<span data-ttu-id="afe2c-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="afe2c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
