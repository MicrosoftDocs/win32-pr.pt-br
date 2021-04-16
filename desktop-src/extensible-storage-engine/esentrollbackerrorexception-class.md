---
description: 'Saiba mais sobre: classe EsentRollbackErrorException'
title: Classe EsentRollbackErrorException
TOCTitle: EsentRollbackErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackerrorexception(v=EXCHG.10)
ms:contentKeyID: 55102663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e56e3e829b8c44ff6325ed877606fb44471f6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765141"
---
# <a name="esentrollbackerrorexception-class"></a><span data-ttu-id="43096-103">Classe EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="43096-103">EsentRollbackErrorException class</span></span>

<span data-ttu-id="43096-104">Classe base para JET_err. RollbackError exceções.</span><span class="sxs-lookup"><span data-stu-id="43096-104">Base class for JET_err.RollbackError exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="43096-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="43096-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="43096-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="43096-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="43096-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="43096-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="43096-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="43096-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="43096-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="43096-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="43096-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="43096-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="43096-111">Microsoft. ISAM. ESENT. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="43096-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="43096-112">Microsoft. ISAM. ESENT. Interop. EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="43096-112">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>  

<span data-ttu-id="43096-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43096-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43096-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43096-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43096-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43096-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackErrorException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentRollbackErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackErrorException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="43096-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="43096-116">Thread safety</span></span>

<span data-ttu-id="43096-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="43096-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="43096-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="43096-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="43096-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="43096-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43096-120">Referência</span><span class="sxs-lookup"><span data-stu-id="43096-120">Reference</span></span>

[<span data-ttu-id="43096-121">Membros do EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="43096-121">EsentRollbackErrorException members</span></span>](./esentrollbackerrorexception-members.md)

[<span data-ttu-id="43096-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="43096-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
