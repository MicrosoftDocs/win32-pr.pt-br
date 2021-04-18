---
description: 'Saiba mais sobre: classe EsentInconsistentException'
title: Classe EsentInconsistentException
TOCTitle: EsentInconsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInconsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b963e5b0d3f400a860f7742bb76a183b67bd7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105812805"
---
# <a name="esentinconsistentexception-class"></a><span data-ttu-id="548d7-103">Classe EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="548d7-103">EsentInconsistentException class</span></span>

<span data-ttu-id="548d7-104">Classe base para exceções inconsistentes.</span><span class="sxs-lookup"><span data-stu-id="548d7-104">Base class for Inconsistent exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="548d7-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="548d7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="548d7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="548d7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="548d7-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="548d7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="548d7-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="548d7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="548d7-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="548d7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="548d7-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="548d7-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="548d7-111">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="548d7-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            

<span data-ttu-id="548d7-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="548d7-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="548d7-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="548d7-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="548d7-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="548d7-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentInconsistentException _
    Inherits EsentDataException
'Usage
Dim instance As EsentInconsistentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentInconsistentException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="548d7-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="548d7-115">Thread safety</span></span>

<span data-ttu-id="548d7-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="548d7-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="548d7-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="548d7-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="548d7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="548d7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="548d7-119">Referência</span><span class="sxs-lookup"><span data-stu-id="548d7-119">Reference</span></span>

[<span data-ttu-id="548d7-120">Membros do EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="548d7-120">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="548d7-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="548d7-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="548d7-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="548d7-122">Derived types</span></span>

[<span data-ttu-id="548d7-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="548d7-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="548d7-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="548d7-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="548d7-125">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="548d7-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="548d7-126">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="548d7-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="548d7-127">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="548d7-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="548d7-128">Microsoft. ISAM. ESENT. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="548d7-128">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>  
            [<span data-ttu-id="548d7-129">Microsoft. ISAM. ESENT. Interop. EsentAttachedDatabaseMismatchException</span><span class="sxs-lookup"><span data-stu-id="548d7-129">Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException</span></span>](./esentattacheddatabasemismatchexception-class.md)  
            [<span data-ttu-id="548d7-130">Microsoft. ISAM. ESENT. Interop. EsentBadCheckpointSignatureException</span><span class="sxs-lookup"><span data-stu-id="548d7-130">Microsoft.Isam.Esent.Interop.EsentBadCheckpointSignatureException</span></span>](./esentbadcheckpointsignatureexception-class.md)  
            [<span data-ttu-id="548d7-131">Microsoft. ISAM. ESENT. Interop. EsentBadLogSignatureException</span><span class="sxs-lookup"><span data-stu-id="548d7-131">Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException</span></span>](./esentbadlogsignatureexception-class.md)  
            [<span data-ttu-id="548d7-132">Microsoft. ISAM. ESENT. Interop. EsentBadLogVersionException</span><span class="sxs-lookup"><span data-stu-id="548d7-132">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>](./esentbadlogversionexception-class.md)  
            [<span data-ttu-id="548d7-133">Microsoft. ISAM. ESENT. Interop. EsentCheckpointFileNotFoundException</span><span class="sxs-lookup"><span data-stu-id="548d7-133">Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException</span></span>](./esentcheckpointfilenotfoundexception-class.md)  
            [<span data-ttu-id="548d7-134">Microsoft. ISAM. ESENT. Interop. EsentConsistentTimeMismatchException</span><span class="sxs-lookup"><span data-stu-id="548d7-134">Microsoft.Isam.Esent.Interop.EsentConsistentTimeMismatchException</span></span>](./esentconsistenttimemismatchexception-class.md)  
            [<span data-ttu-id="548d7-135">Microsoft. ISAM. ESENT. Interop. EsentDatabaseDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="548d7-135">Microsoft.Isam.Esent.Interop.EsentDatabaseDirtyShutdownException</span></span>](./esentdatabasedirtyshutdownexception-class.md)  
            [<span data-ttu-id="548d7-136">Microsoft. ISAM. ESENT. Interop. EsentDatabaseIncompleteIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="548d7-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>](./esentdatabaseincompleteincrementalreseedexception-class.md)  
            [<span data-ttu-id="548d7-137">Microsoft. ISAM. ESENT. Interop. EsentDatabaseLogSetMismatchException</span><span class="sxs-lookup"><span data-stu-id="548d7-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException</span></span>](./esentdatabaselogsetmismatchexception-class.md)  
            [<span data-ttu-id="548d7-138">Microsoft. ISAM. ESENT. Interop. EsentDbTimeTooNewException</span><span class="sxs-lookup"><span data-stu-id="548d7-138">Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException</span></span>](./esentdbtimetoonewexception-class.md)  
            [<span data-ttu-id="548d7-139">Microsoft. ISAM. ESENT. Interop. EsentDbTimeTooOldException</span><span class="sxs-lookup"><span data-stu-id="548d7-139">Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException</span></span>](./esentdbtimetoooldexception-class.md)  
            [<span data-ttu-id="548d7-140">Microsoft. ISAM. ESENT. Interop. EsentEndingRestoreLogTooLowException</span><span class="sxs-lookup"><span data-stu-id="548d7-140">Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException</span></span>](./esentendingrestorelogtoolowexception-class.md)  
            [<span data-ttu-id="548d7-141">Microsoft. ISAM. ESENT. Interop. EsentExistingLogFileHasBadSignatureException</span><span class="sxs-lookup"><span data-stu-id="548d7-141">Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException</span></span>](./esentexistinglogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="548d7-142">Microsoft. ISAM. ESENT. Interop. EsentExistingLogFileIsNotContiguousException</span><span class="sxs-lookup"><span data-stu-id="548d7-142">Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException</span></span>](./esentexistinglogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="548d7-143">Microsoft. ISAM. ESENT. Interop. EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="548d7-143">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>](./esentfileinvalidtypeexception-class.md)  
            [<span data-ttu-id="548d7-144">Microsoft. ISAM. ESENT. Interop. EsentGivenLogFileHasBadSignatureException</span><span class="sxs-lookup"><span data-stu-id="548d7-144">Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException</span></span>](./esentgivenlogfilehasbadsignatureexception-class.md)  
            [<span data-ttu-id="548d7-145">Microsoft. ISAM. ESENT. Interop. EsentGivenLogFileIsNotContiguousException</span><span class="sxs-lookup"><span data-stu-id="548d7-145">Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException</span></span>](./esentgivenlogfileisnotcontiguousexception-class.md)  
            [<span data-ttu-id="548d7-146">Microsoft. ISAM. ESENT. Interop. EsentInvalidCreateDbVersionException</span><span class="sxs-lookup"><span data-stu-id="548d7-146">Microsoft.Isam.Esent.Interop.EsentInvalidCreateDbVersionException</span></span>](./esentinvalidcreatedbversionexception-class.md)  
            [<span data-ttu-id="548d7-147">Microsoft. ISAM. ESENT. Interop. EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="548d7-147">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>](./esentinvaliddatabaseversionexception-class.md)  
            [<span data-ttu-id="548d7-148">Microsoft. ISAM. ESENT. Interop. EsentLogGenerationMismatchException</span><span class="sxs-lookup"><span data-stu-id="548d7-148">Microsoft.Isam.Esent.Interop.EsentLogGenerationMismatchException</span></span>](./esentloggenerationmismatchexception-class.md)  
            [<span data-ttu-id="548d7-149">Microsoft. ISAM. ESENT. Interop. EsentMissingCurrentLogFilesException</span><span class="sxs-lookup"><span data-stu-id="548d7-149">Microsoft.Isam.Esent.Interop.EsentMissingCurrentLogFilesException</span></span>](./esentmissingcurrentlogfilesexception-class.md)  
            [<span data-ttu-id="548d7-150">Microsoft. ISAM. ESENT. Interop. EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="548d7-150">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>](./esentmissingfiletobackupexception-class.md)  
            [<span data-ttu-id="548d7-151">Microsoft. ISAM. ESENT. Interop. EsentMissingRestoreLogFilesException</span><span class="sxs-lookup"><span data-stu-id="548d7-151">Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException</span></span>](./esentmissingrestorelogfilesexception-class.md)  
            [<span data-ttu-id="548d7-152">Microsoft. ISAM. ESENT. Interop. EsentPageSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="548d7-152">Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException</span></span>](./esentpagesizemismatchexception-class.md)  
            [<span data-ttu-id="548d7-153">Microsoft. ISAM. ESENT. Interop. EsentRequiredLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="548d7-153">Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException</span></span>](./esentrequiredlogfilesmissingexception-class.md)  
            [<span data-ttu-id="548d7-154">Microsoft. ISAM. ESENT. Interop. EsentStartingRestoreLogTooHighException</span><span class="sxs-lookup"><span data-stu-id="548d7-154">Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException</span></span>](./esentstartingrestorelogtoohighexception-class.md)