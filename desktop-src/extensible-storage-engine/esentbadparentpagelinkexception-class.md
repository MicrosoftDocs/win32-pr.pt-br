---
description: 'Saiba mais sobre: classe EsentBadParentPageLinkException'
title: Classe EsentBadParentPageLinkException
TOCTitle: EsentBadParentPageLinkException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadparentpagelinkexception(v=EXCHG.10)
ms:contentKeyID: 55101090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffcfab55b6acda192252faeb43493dfba3978b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798410"
---
# <a name="esentbadparentpagelinkexception-class"></a><span data-ttu-id="ffc32-103">Classe EsentBadParentPageLinkException</span><span class="sxs-lookup"><span data-stu-id="ffc32-103">EsentBadParentPageLinkException class</span></span>

<span data-ttu-id="ffc32-104">Classe base para JET_err. BadParentPageLink exceções.</span><span class="sxs-lookup"><span data-stu-id="ffc32-104">Base class for JET_err.BadParentPageLink exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ffc32-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="ffc32-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ffc32-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ffc32-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ffc32-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ffc32-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ffc32-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="ffc32-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ffc32-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ffc32-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ffc32-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="ffc32-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="ffc32-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="ffc32-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="ffc32-112">Microsoft. ISAM. ESENT. Interop. EsentBadParentPageLinkException</span><span class="sxs-lookup"><span data-stu-id="ffc32-112">Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException</span></span>  

<span data-ttu-id="ffc32-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ffc32-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ffc32-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ffc32-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc32-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffc32-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadParentPageLinkException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadParentPageLinkException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadParentPageLinkException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="ffc32-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="ffc32-116">Thread safety</span></span>

<span data-ttu-id="ffc32-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ffc32-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ffc32-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="ffc32-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffc32-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffc32-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ffc32-120">Referência</span><span class="sxs-lookup"><span data-stu-id="ffc32-120">Reference</span></span>

[<span data-ttu-id="ffc32-121">Membros do EsentBadParentPageLinkException</span><span class="sxs-lookup"><span data-stu-id="ffc32-121">EsentBadParentPageLinkException members</span></span>](./esentbadparentpagelinkexception-members.md)

[<span data-ttu-id="ffc32-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ffc32-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
