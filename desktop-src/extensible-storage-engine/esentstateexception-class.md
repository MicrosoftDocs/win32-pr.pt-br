---
description: 'Saiba mais sobre: classe EsentStateException'
title: Classe EsentStateException
TOCTitle: EsentStateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstateexception(v=EXCHG.10)
ms:contentKeyID: 55102986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5815c3b308874f69eab9dcc7b3803ee24f6831b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172425"
---
# <a name="esentstateexception-class"></a><span data-ttu-id="116ca-103">Classe EsentStateException</span><span class="sxs-lookup"><span data-stu-id="116ca-103">EsentStateException class</span></span>

<span data-ttu-id="116ca-104">Classe base para exceções de estado.</span><span class="sxs-lookup"><span data-stu-id="116ca-104">Base class for State exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="116ca-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="116ca-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="116ca-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="116ca-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="116ca-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="116ca-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="116ca-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="116ca-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="116ca-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="116ca-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="116ca-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="116ca-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="116ca-111">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="116ca-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            

<span data-ttu-id="116ca-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="116ca-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="116ca-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="116ca-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="116ca-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="116ca-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentStateException _
    Inherits EsentApiException
'Usage
Dim instance As EsentStateException
```

``` csharp
[SerializableAttribute]
public abstract class EsentStateException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="116ca-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="116ca-115">Thread safety</span></span>

<span data-ttu-id="116ca-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="116ca-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="116ca-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="116ca-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="116ca-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="116ca-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="116ca-119">Referência</span><span class="sxs-lookup"><span data-stu-id="116ca-119">Reference</span></span>

[<span data-ttu-id="116ca-120">Membros do EsentStateException</span><span class="sxs-lookup"><span data-stu-id="116ca-120">EsentStateException members</span></span>](./esentstateexception-members.md)

[<span data-ttu-id="116ca-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="116ca-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="116ca-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="116ca-122">Derived types</span></span>

[<span data-ttu-id="116ca-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="116ca-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="116ca-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="116ca-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="116ca-125">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="116ca-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="116ca-126">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="116ca-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="116ca-127">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="116ca-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="116ca-128">Microsoft. ISAM. ESENT. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="116ca-128">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>  
            [<span data-ttu-id="116ca-129">Microsoft. ISAM. ESENT. Interop. EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="116ca-129">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>](./esentbackupinprogressexception-class.md)  
            [<span data-ttu-id="116ca-130">Microsoft. ISAM. ESENT. Interop. EsentBackupNotAllowedYetException</span><span class="sxs-lookup"><span data-stu-id="116ca-130">Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException</span></span>](./esentbackupnotallowedyetexception-class.md)  
            [<span data-ttu-id="116ca-131">Microsoft. ISAM. ESENT. Interop. EsentBadItagSequenceException</span><span class="sxs-lookup"><span data-stu-id="116ca-131">Microsoft.Isam.Esent.Interop.EsentBadItagSequenceException</span></span>](./esentbaditagsequenceexception-class.md)  
            [<span data-ttu-id="116ca-132">Microsoft. ISAM. ESENT. Interop. EsentBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="116ca-132">Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException</span></span>](./esentbuffertoosmallexception-class.md)  
            [<span data-ttu-id="116ca-133">Microsoft. ISAM. ESENT. Interop. EsentCallbackFailedException</span><span class="sxs-lookup"><span data-stu-id="116ca-133">Microsoft.Isam.Esent.Interop.EsentCallbackFailedException</span></span>](./esentcallbackfailedexception-class.md)  
            [<span data-ttu-id="116ca-134">Microsoft. ISAM. ESENT. Interop. EsentDatabaseAlreadyUpgradedException</span><span class="sxs-lookup"><span data-stu-id="116ca-134">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>](./esentdatabasealreadyupgradedexception-class.md)  
            [<span data-ttu-id="116ca-135">Microsoft. ISAM. ESENT. Interop. EsentDatabaseFailedIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="116ca-135">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>](./esentdatabasefailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="116ca-136">Microsoft. ISAM. ESENT. Interop. EsentDatabaseIncompleteUpgradeException</span><span class="sxs-lookup"><span data-stu-id="116ca-136">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException</span></span>](./esentdatabaseincompleteupgradeexception-class.md)  
            [<span data-ttu-id="116ca-137">Microsoft. ISAM. ESENT. Interop. EsentDatabaseLeakInSpaceException</span><span class="sxs-lookup"><span data-stu-id="116ca-137">Microsoft.Isam.Esent.Interop.EsentDatabaseLeakInSpaceException</span></span>](./esentdatabaseleakinspaceexception-class.md)  
            [<span data-ttu-id="116ca-138">Microsoft. ISAM. ESENT. Interop. EsentDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="116ca-138">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>](./esentdirtyshutdownexception-class.md)  
            [<span data-ttu-id="116ca-139">Microsoft. ISAM. ESENT. Interop. EsentFileNotFoundException</span><span class="sxs-lookup"><span data-stu-id="116ca-139">Microsoft.Isam.Esent.Interop.EsentFileNotFoundException</span></span>](./esentfilenotfoundexception-class.md)  
            [<span data-ttu-id="116ca-140">Microsoft. ISAM. ESENT. Interop. EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="116ca-140">Microsoft.Isam.Esent.Interop.EsentIndexInUseException</span></span>](./esentindexinuseexception-class.md)  
            [<span data-ttu-id="116ca-141">Microsoft. ISAM. ESENT. Interop. EsentIndexNotFoundException</span><span class="sxs-lookup"><span data-stu-id="116ca-141">Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException</span></span>](./esentindexnotfoundexception-class.md)  
            [<span data-ttu-id="116ca-142">Microsoft. ISAM. ESENT. Interop. EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="116ca-142">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>](./esentinvalidbuffersizeexception-class.md)  
            [<span data-ttu-id="116ca-143">Microsoft. ISAM. ESENT. Interop. EsentInvalidLogDataSequenceException</span><span class="sxs-lookup"><span data-stu-id="116ca-143">Microsoft.Isam.Esent.Interop.EsentInvalidLogDataSequenceException</span></span>](./esentinvalidlogdatasequenceexception-class.md)  
            [<span data-ttu-id="116ca-144">Microsoft. ISAM. ESENT. Interop. EsentKeyDuplicateException</span><span class="sxs-lookup"><span data-stu-id="116ca-144">Microsoft.Isam.Esent.Interop.EsentKeyDuplicateException</span></span>](./esentkeyduplicateexception-class.md)  
            [<span data-ttu-id="116ca-145">Microsoft. ISAM. ESENT. Interop. EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="116ca-145">Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException</span></span>](./esentkeytruncatedexception-class.md)  
            [<span data-ttu-id="116ca-146">Microsoft. ISAM. ESENT. Interop. EsentLogFileSizeMismatchDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="116ca-146">Microsoft.Isam.Esent.Interop.EsentLogFileSizeMismatchDatabasesConsistentException</span></span>](./esentlogfilesizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="116ca-147">Microsoft. ISAM. ESENT. Interop. EsentLogSectorSizeMismatchDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="116ca-147">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchDatabasesConsistentException</span></span>](./esentlogsectorsizemismatchdatabasesconsistentexception-class.md)  
            [<span data-ttu-id="116ca-148">Microsoft. ISAM. ESENT. Interop. EsentLSNotSetException</span><span class="sxs-lookup"><span data-stu-id="116ca-148">Microsoft.Isam.Esent.Interop.EsentLSNotSetException</span></span>](./esentlsnotsetexception-class.md)  
            [<span data-ttu-id="116ca-149">Microsoft. ISAM. ESENT. Interop. EsentMissingFullBackupException</span><span class="sxs-lookup"><span data-stu-id="116ca-149">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>](./esentmissingfullbackupexception-class.md)  
            [<span data-ttu-id="116ca-150">Microsoft. ISAM. ESENT. Interop. EsentMultiValuedDuplicateAfterTruncationException</span><span class="sxs-lookup"><span data-stu-id="116ca-150">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateAfterTruncationException</span></span>](./esentmultivaluedduplicateaftertruncationexception-class.md)  
            [<span data-ttu-id="116ca-151">Microsoft. ISAM. ESENT. Interop. EsentMultiValuedDuplicateException</span><span class="sxs-lookup"><span data-stu-id="116ca-151">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>](./esentmultivaluedduplicateexception-class.md)  
            [<span data-ttu-id="116ca-152">Microsoft. ISAM. ESENT. Interop. EsentNoAttachmentsFailedIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="116ca-152">Microsoft.Isam.Esent.Interop.EsentNoAttachmentsFailedIncrementalReseedException</span></span>](./esentnoattachmentsfailedincrementalreseedexception-class.md)  
            [<span data-ttu-id="116ca-153">Microsoft. ISAM. ESENT. Interop. EsentNoBackupException</span><span class="sxs-lookup"><span data-stu-id="116ca-153">Microsoft.Isam.Esent.Interop.EsentNoBackupException</span></span>](./esentnobackupexception-class.md)  
            [<span data-ttu-id="116ca-154">Microsoft. ISAM. ESENT. Interop. EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="116ca-154">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>](./esentnocurrentrecordexception-class.md)  
            [<span data-ttu-id="116ca-155">Microsoft. ISAM. ESENT. Interop. EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="116ca-155">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>](./esentobjectnotfoundexception-class.md)  
            [<span data-ttu-id="116ca-156">Microsoft. ISAM. ESENT. Interop. EsentOSSnapshotNotAllowedException</span><span class="sxs-lookup"><span data-stu-id="116ca-156">Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException</span></span>](./esentossnapshotnotallowedexception-class.md)  
            [<span data-ttu-id="116ca-157">Microsoft. ISAM. ESENT. Interop. EsentRecordDeletedException</span><span class="sxs-lookup"><span data-stu-id="116ca-157">Microsoft.Isam.Esent.Interop.EsentRecordDeletedException</span></span>](./esentrecorddeletedexception-class.md)  
            [<span data-ttu-id="116ca-158">Microsoft. ISAM. ESENT. Interop. EsentRecordNotFoundException</span><span class="sxs-lookup"><span data-stu-id="116ca-158">Microsoft.Isam.Esent.Interop.EsentRecordNotFoundException</span></span>](./esentrecordnotfoundexception-class.md)  
            [<span data-ttu-id="116ca-159">Microsoft. ISAM. ESENT. Interop. EsentRecordTooBigException</span><span class="sxs-lookup"><span data-stu-id="116ca-159">Microsoft.Isam.Esent.Interop.EsentRecordTooBigException</span></span>](./esentrecordtoobigexception-class.md)  
            [<span data-ttu-id="116ca-160">Microsoft. ISAM. ESENT. Interop. EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="116ca-160">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-class.md)  
            [<span data-ttu-id="116ca-161">Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithErrorsException</span><span class="sxs-lookup"><span data-stu-id="116ca-161">Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException</span></span>](./esentrecoveredwitherrorsexception-class.md)  
            [<span data-ttu-id="116ca-162">Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithoutUndoDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="116ca-162">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException</span></span>](./esentrecoveredwithoutundodatabasesconsistentexception-class.md)  
            [<span data-ttu-id="116ca-163">Microsoft. ISAM. ESENT. Interop. EsentRecoveredWithoutUndoException</span><span class="sxs-lookup"><span data-stu-id="116ca-163">Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoException</span></span>](./esentrecoveredwithoutundoexception-class.md)  
            [<span data-ttu-id="116ca-164">Microsoft. ISAM. ESENT. Interop. EsentRestoreInProgressException</span><span class="sxs-lookup"><span data-stu-id="116ca-164">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>](./esentrestoreinprogressexception-class.md)  
            [<span data-ttu-id="116ca-165">Microsoft. ISAM. ESENT. Interop. EsentSeparatedLongValueException</span><span class="sxs-lookup"><span data-stu-id="116ca-165">Microsoft.Isam.Esent.Interop.EsentSeparatedLongValueException</span></span>](./esentseparatedlongvalueexception-class.md)  
            [<span data-ttu-id="116ca-166">Microsoft. ISAM. ESENT. Interop. EsentSurrogateBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="116ca-166">Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException</span></span>](./esentsurrogatebackupinprogressexception-class.md)  
            [<span data-ttu-id="116ca-167">Microsoft. ISAM. ESENT. Interop. EsentTableDuplicateException</span><span class="sxs-lookup"><span data-stu-id="116ca-167">Microsoft.Isam.Esent.Interop.EsentTableDuplicateException</span></span>](./esenttableduplicateexception-class.md)  
            [<span data-ttu-id="116ca-168">Microsoft. ISAM. ESENT. Interop. EsentTableInUseException</span><span class="sxs-lookup"><span data-stu-id="116ca-168">Microsoft.Isam.Esent.Interop.EsentTableInUseException</span></span>](./esenttableinuseexception-class.md)  
            [<span data-ttu-id="116ca-169">Microsoft. ISAM. ESENT. Interop. EsentTestInjectionNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="116ca-169">Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException</span></span>](./esenttestinjectionnotsupportedexception-class.md)  
            [<span data-ttu-id="116ca-170">Microsoft. ISAM. ESENT. Interop. EsentWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="116ca-170">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>](./esentwriteconflictexception-class.md)  
            [<span data-ttu-id="116ca-171">Microsoft. ISAM. ESENT. Interop. EsentWriteConflictPrimaryIndexException</span><span class="sxs-lookup"><span data-stu-id="116ca-171">Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException</span></span>](./esentwriteconflictprimaryindexexception-class.md)