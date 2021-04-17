---
description: 'Saiba mais sobre: classe EsentOutOfObjectIDsException'
title: Classe EsentOutOfObjectIDsException
TOCTitle: EsentOutOfObjectIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofobjectidsexception(v=EXCHG.10)
ms:contentKeyID: 55102436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18cf8d1b7c98db8f855cf970eed7be87185fc9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785032"
---
# <a name="esentoutofobjectidsexception-class"></a><span data-ttu-id="3e59c-103">Classe EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="3e59c-103">EsentOutOfObjectIDsException class</span></span>

<span data-ttu-id="3e59c-104">Classe base para JET_err. OutOfObjectIDs exceções.</span><span class="sxs-lookup"><span data-stu-id="3e59c-104">Base class for JET_err.OutOfObjectIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3e59c-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="3e59c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3e59c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3e59c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3e59c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3e59c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3e59c-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="3e59c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3e59c-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3e59c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3e59c-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="3e59c-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="3e59c-111">Microsoft. ISAM. ESENT. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="3e59c-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="3e59c-112">Microsoft. ISAM. ESENT. Interop. EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="3e59c-112">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>  

<span data-ttu-id="3e59c-113">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3e59c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3e59c-114">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3e59c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3e59c-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e59c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfObjectIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfObjectIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfObjectIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="3e59c-116">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="3e59c-116">Thread safety</span></span>

<span data-ttu-id="3e59c-117">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3e59c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3e59c-118">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="3e59c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e59c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e59c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e59c-120">Referência</span><span class="sxs-lookup"><span data-stu-id="3e59c-120">Reference</span></span>

[<span data-ttu-id="3e59c-121">Membros do EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="3e59c-121">EsentOutOfObjectIDsException members</span></span>](./esentoutofobjectidsexception-members.md)

[<span data-ttu-id="3e59c-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3e59c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
