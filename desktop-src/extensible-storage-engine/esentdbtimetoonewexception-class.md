---
description: 'Saiba mais sobre: classe EsentDbTimeTooNewException'
title: Classe EsentDbTimeTooNewException
TOCTitle: EsentDbTimeTooNewException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdbtimetoonewexception(v=EXCHG.10)
ms:contentKeyID: 55101468
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de09cf8f20aca58c6e32fdf23766f416bf93f227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165152"
---
# <a name="esentdbtimetoonewexception-class"></a><span data-ttu-id="49a53-103">Classe EsentDbTimeTooNewException</span><span class="sxs-lookup"><span data-stu-id="49a53-103">EsentDbTimeTooNewException class</span></span>

<span data-ttu-id="49a53-104">Classe base para JET_err. DbTimeTooNew exceções.</span><span class="sxs-lookup"><span data-stu-id="49a53-104">Base class for JET_err.DbTimeTooNew exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="49a53-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="49a53-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="49a53-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="49a53-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="49a53-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="49a53-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="49a53-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="49a53-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="49a53-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="49a53-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="49a53-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="49a53-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="49a53-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="49a53-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="49a53-112">Microsoft. ISAM. ESENT. Interop. EsentDbTimeTooNewException</span><span class="sxs-lookup"><span data-stu-id="49a53-112">Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException</span></span>  

<span data-ttu-id="49a53-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49a53-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="49a53-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="49a53-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49a53-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="49a53-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDbTimeTooNewException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDbTimeTooNewException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDbTimeTooNewException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="49a53-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="49a53-116">Thread safety</span></span>

<span data-ttu-id="49a53-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="49a53-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="49a53-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="49a53-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="49a53-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="49a53-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49a53-120">Referência</span><span class="sxs-lookup"><span data-stu-id="49a53-120">Reference</span></span>

[<span data-ttu-id="49a53-121">Membros do EsentDbTimeTooNewException</span><span class="sxs-lookup"><span data-stu-id="49a53-121">EsentDbTimeTooNewException members</span></span>](./esentdbtimetoonewexception-members.md)

[<span data-ttu-id="49a53-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="49a53-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
