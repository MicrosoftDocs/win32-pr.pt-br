---
description: 'Saiba mais sobre: classe EsentFatalException'
title: Classe EsentFatalException
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172426"
---
# <a name="esentfatalexception-class"></a><span data-ttu-id="23420-103">Classe EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="23420-103">EsentFatalException class</span></span>

<span data-ttu-id="23420-104">Classe base para exceções fatais.</span><span class="sxs-lookup"><span data-stu-id="23420-104">Base class for Fatal exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="23420-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="23420-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="23420-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="23420-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="23420-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="23420-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="23420-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="23420-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="23420-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="23420-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="23420-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="23420-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="23420-111">Microsoft. ISAM. ESENT. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="23420-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            

<span data-ttu-id="23420-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23420-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="23420-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="23420-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23420-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="23420-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="23420-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="23420-115">Thread safety</span></span>

<span data-ttu-id="23420-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="23420-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="23420-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="23420-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="23420-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="23420-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23420-119">Referência</span><span class="sxs-lookup"><span data-stu-id="23420-119">Reference</span></span>

[<span data-ttu-id="23420-120">Membros do EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="23420-120">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="23420-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="23420-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="23420-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="23420-122">Derived types</span></span>

[<span data-ttu-id="23420-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="23420-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="23420-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="23420-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="23420-125">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="23420-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="23420-126">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="23420-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="23420-127">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="23420-127">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="23420-128">Microsoft. ISAM. ESENT. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="23420-128">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            [<span data-ttu-id="23420-129">Microsoft. ISAM. ESENT. Interop. EsentInstanceUnavailableDueToFatalLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="23420-129">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException</span></span>](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [<span data-ttu-id="23420-130">Microsoft. ISAM. ESENT. Interop. EsentInstanceUnavailableException</span><span class="sxs-lookup"><span data-stu-id="23420-130">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>](./esentinstanceunavailableexception-class.md)  
            [<span data-ttu-id="23420-131">Microsoft. ISAM. ESENT. Interop. EsentLogDisabledDueToRecoveryFailureException</span><span class="sxs-lookup"><span data-stu-id="23420-131">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [<span data-ttu-id="23420-132">Microsoft. ISAM. ESENT. Interop. EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="23420-132">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>](./esentrollbackerrorexception-class.md)  
            [<span data-ttu-id="23420-133">Microsoft. ISAM. ESENT. Interop. EsentSectorSizeNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="23420-133">Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException</span></span>](./esentsectorsizenotsupportedexception-class.md)  
            [<span data-ttu-id="23420-134">Microsoft. ISAM. ESENT. Interop. EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="23420-134">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>](./esentunloadableosfunctionalityexception-class.md)