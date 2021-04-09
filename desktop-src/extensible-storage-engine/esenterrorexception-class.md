---
description: 'Saiba mais sobre: classe EsentErrorException'
title: Classe EsentErrorException
TOCTitle: EsentErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101648
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb05197392c1d5c8798968254b24d2d0ae677bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011232"
---
# <a name="esenterrorexception-class"></a><span data-ttu-id="b1398-103">Classe EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b1398-103">EsentErrorException class</span></span>

<span data-ttu-id="b1398-104">Classe base para exceções de erro de ESENT.</span><span class="sxs-lookup"><span data-stu-id="b1398-104">Base class for ESENT error exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b1398-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="b1398-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b1398-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b1398-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b1398-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b1398-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b1398-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="b1398-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      <span data-ttu-id="b1398-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b1398-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>  
        [<span data-ttu-id="b1398-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b1398-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
        [<span data-ttu-id="b1398-111">Microsoft. ISAM. ESENT. Interop. EsentCannotLogDuringRecoveryRedoException</span><span class="sxs-lookup"><span data-stu-id="b1398-111">Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException</span></span>](./esentcannotlogduringrecoveryredoexception-class.md)  
        [<span data-ttu-id="b1398-112">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="b1398-112">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
        [<span data-ttu-id="b1398-113">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="b1398-113">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
        [<span data-ttu-id="b1398-114">Microsoft. ISAM. ESENT. Interop. EsentPreviousVersionException</span><span class="sxs-lookup"><span data-stu-id="b1398-114">Microsoft.Isam.Esent.Interop.EsentPreviousVersionException</span></span>](./esentpreviousversionexception-class.md)  
        [<span data-ttu-id="b1398-115">Microsoft. ISAM. ESENT. Interop. EsentVersionStoreEntryTooBigException</span><span class="sxs-lookup"><span data-stu-id="b1398-115">Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException</span></span>](./esentversionstoreentrytoobigexception-class.md)  

<span data-ttu-id="b1398-116">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1398-116">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b1398-117">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1398-117">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1398-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1398-118">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Class EsentErrorException _
    Inherits EsentException
'Usage
Dim instance As EsentErrorException
```

``` csharp
[SerializableAttribute]
public class EsentErrorException : EsentException
```

## <a name="thread-safety"></a><span data-ttu-id="b1398-119">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="b1398-119">Thread safety</span></span>

<span data-ttu-id="b1398-120">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b1398-120">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b1398-121">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="b1398-121">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1398-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1398-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1398-123">Referência</span><span class="sxs-lookup"><span data-stu-id="b1398-123">Reference</span></span>

[<span data-ttu-id="b1398-124">Membros do EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b1398-124">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="b1398-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b1398-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
