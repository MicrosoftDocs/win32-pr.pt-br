---
description: 'Saiba mais sobre: classe EsentOperationException'
title: Classe EsentOperationException
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105761570"
---
# <a name="esentoperationexception-class"></a><span data-ttu-id="622dd-103">Classe EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="622dd-103">EsentOperationException class</span></span>

<span data-ttu-id="622dd-104">Classe base para exceções de operação.</span><span class="sxs-lookup"><span data-stu-id="622dd-104">Base class for Operation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="622dd-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="622dd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="622dd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="622dd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="622dd-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="622dd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="622dd-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="622dd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="622dd-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="622dd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="622dd-110">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="622dd-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          

<span data-ttu-id="622dd-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="622dd-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="622dd-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="622dd-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="622dd-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="622dd-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="622dd-114">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="622dd-114">Thread safety</span></span>

<span data-ttu-id="622dd-115">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="622dd-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="622dd-116">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="622dd-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="622dd-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="622dd-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="622dd-118">Referência</span><span class="sxs-lookup"><span data-stu-id="622dd-118">Reference</span></span>

[<span data-ttu-id="622dd-119">Membros do EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="622dd-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="622dd-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="622dd-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="622dd-121">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="622dd-121">Derived types</span></span>

[<span data-ttu-id="622dd-122">System.Object</span><span class="sxs-lookup"><span data-stu-id="622dd-122">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="622dd-123">System. Exception</span><span class="sxs-lookup"><span data-stu-id="622dd-123">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="622dd-124">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="622dd-124">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="622dd-125">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="622dd-125">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="622dd-126">Microsoft. ISAM. ESENT. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="622dd-126">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          [<span data-ttu-id="622dd-127">Microsoft. ISAM. ESENT. Interop. EsentBackupAbortByServerException</span><span class="sxs-lookup"><span data-stu-id="622dd-127">Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException</span></span>](./esentbackupabortbyserverexception-class.md)  
          [<span data-ttu-id="622dd-128">Microsoft. ISAM. ESENT. Interop. EsentCheckpointDepthTooDeepException</span><span class="sxs-lookup"><span data-stu-id="622dd-128">Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException</span></span>](./esentcheckpointdepthtoodeepexception-class.md)  
          [<span data-ttu-id="622dd-129">Microsoft. ISAM. ESENT. Interop. EsentClientRequestToStopJetServiceException</span><span class="sxs-lookup"><span data-stu-id="622dd-129">Microsoft.Isam.Esent.Interop.EsentClientRequestToStopJetServiceException</span></span>](./esentclientrequesttostopjetserviceexception-class.md)  
          [<span data-ttu-id="622dd-130">Microsoft. ISAM. ESENT. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="622dd-130">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
          [<span data-ttu-id="622dd-131">Microsoft. ISAM. ESENT. Interop. EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="622dd-131">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>](./esentinitinprogressexception-class.md)  
          [<span data-ttu-id="622dd-132">Microsoft. ISAM. ESENT. Interop. EsentInternalErrorException</span><span class="sxs-lookup"><span data-stu-id="622dd-132">Microsoft.Isam.Esent.Interop.EsentInternalErrorException</span></span>](./esentinternalerrorexception-class.md)  
          [<span data-ttu-id="622dd-133">Microsoft. ISAM. ESENT. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="622dd-133">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
          [<span data-ttu-id="622dd-134">Microsoft. ISAM. ESENT. Interop. EsentNTSystemCallFailedException</span><span class="sxs-lookup"><span data-stu-id="622dd-134">Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException</span></span>](./esentntsystemcallfailedexception-class.md)  
          [<span data-ttu-id="622dd-135">Microsoft. ISAM. ESENT. Interop. EsentOSSnapshotTimeOutException</span><span class="sxs-lookup"><span data-stu-id="622dd-135">Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException</span></span>](./esentossnapshottimeoutexception-class.md)  
          [<span data-ttu-id="622dd-136">Microsoft. ISAM. ESENT. Interop. EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="622dd-136">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>](./esentrecordnotdeletedexception-class.md)  
          [<span data-ttu-id="622dd-137">Microsoft. ISAM. ESENT. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="622dd-137">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
          [<span data-ttu-id="622dd-138">Microsoft. ISAM. ESENT. Interop. EsentTermInProgressException</span><span class="sxs-lookup"><span data-stu-id="622dd-138">Microsoft.Isam.Esent.Interop.EsentTermInProgressException</span></span>](./esentterminprogressexception-class.md)  
          [<span data-ttu-id="622dd-139">Microsoft. ISAM. ESENT. Interop. EsentUnicodeLanguageValidationFailureException</span><span class="sxs-lookup"><span data-stu-id="622dd-139">Microsoft.Isam.Esent.Interop.EsentUnicodeLanguageValidationFailureException</span></span>](./esentunicodelanguagevalidationfailureexception-class.md)  
          [<span data-ttu-id="622dd-140">Microsoft. ISAM. ESENT. Interop. EsentUnicodeTranslationFailException</span><span class="sxs-lookup"><span data-stu-id="622dd-140">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException</span></span>](./esentunicodetranslationfailexception-class.md)