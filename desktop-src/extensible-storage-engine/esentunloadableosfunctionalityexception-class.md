---
description: 'Saiba mais sobre: classe EsentUnloadableOSFunctionalityException'
title: Classe EsentUnloadableOSFunctionalityException
TOCTitle: EsentUnloadableOSFunctionalityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunloadableosfunctionalityexception(v=EXCHG.10)
ms:contentKeyID: 55107333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81b1151be5020a07f92582e762c6e6597138d9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760190"
---
# <a name="esentunloadableosfunctionalityexception-class"></a><span data-ttu-id="3b188-103">Classe EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="3b188-103">EsentUnloadableOSFunctionalityException class</span></span>

<span data-ttu-id="3b188-104">Classe base para JET_err. UnloadableOSFunctionality exceções.</span><span class="sxs-lookup"><span data-stu-id="3b188-104">Base class for JET_err.UnloadableOSFunctionality exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3b188-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="3b188-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3b188-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3b188-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3b188-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3b188-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3b188-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="3b188-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3b188-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3b188-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3b188-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="3b188-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="3b188-111">Microsoft. ISAM. ESENT. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="3b188-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="3b188-112">Microsoft. ISAM. ESENT. Interop. EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="3b188-112">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>  

<span data-ttu-id="3b188-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b188-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b188-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b188-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b188-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b188-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnloadableOSFunctionalityException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentUnloadableOSFunctionalityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnloadableOSFunctionalityException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="3b188-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="3b188-116">Thread safety</span></span>

<span data-ttu-id="3b188-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3b188-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3b188-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3b188-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b188-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b188-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b188-120">Referência</span><span class="sxs-lookup"><span data-stu-id="3b188-120">Reference</span></span>

[<span data-ttu-id="3b188-121">Membros do EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="3b188-121">EsentUnloadableOSFunctionalityException members</span></span>](./esentunloadableosfunctionalityexception-members.md)

[<span data-ttu-id="3b188-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3b188-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
