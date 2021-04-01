---
description: 'Saiba mais sobre: classe EsentOutOfLongValueIDsException'
title: Classe EsentOutOfLongValueIDsException
TOCTitle: EsentOutOfLongValueIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutoflongvalueidsexception(v=EXCHG.10)
ms:contentKeyID: 55102476
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aada406390da086bc209094641a5ceca546d4932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164677"
---
# <a name="esentoutoflongvalueidsexception-class"></a><span data-ttu-id="9b06b-103">Classe EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="9b06b-103">EsentOutOfLongValueIDsException class</span></span>

<span data-ttu-id="9b06b-104">Classe base para JET_err. OutOfLongValueIDs exceções.</span><span class="sxs-lookup"><span data-stu-id="9b06b-104">Base class for JET_err.OutOfLongValueIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9b06b-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="9b06b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9b06b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9b06b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9b06b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="9b06b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9b06b-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="9b06b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9b06b-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9b06b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9b06b-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="9b06b-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="9b06b-111">Microsoft. ISAM. ESENT. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="9b06b-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="9b06b-112">Microsoft. ISAM. ESENT. Interop. EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="9b06b-112">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>  

<span data-ttu-id="9b06b-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9b06b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9b06b-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9b06b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9b06b-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b06b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfLongValueIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfLongValueIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfLongValueIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="9b06b-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="9b06b-116">Thread safety</span></span>

<span data-ttu-id="9b06b-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9b06b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9b06b-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="9b06b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b06b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b06b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9b06b-120">Referência</span><span class="sxs-lookup"><span data-stu-id="9b06b-120">Reference</span></span>

[<span data-ttu-id="9b06b-121">Membros do EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="9b06b-121">EsentOutOfLongValueIDsException members</span></span>](./esentoutoflongvalueidsexception-members.md)

[<span data-ttu-id="9b06b-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9b06b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
