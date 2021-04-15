---
description: 'Saiba mais sobre: classe EsentObsoleteException'
title: Classe EsentObsoleteException
TOCTitle: EsentObsoleteException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObsoleteException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9d9597c3022d18ba0c6d476710f1c43430babc2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104506322"
---
# <a name="esentobsoleteexception-class"></a><span data-ttu-id="a9b8b-103">Classe EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-103">EsentObsoleteException class</span></span>

<span data-ttu-id="a9b8b-104">Classe base para exceções obsoletas.</span><span class="sxs-lookup"><span data-stu-id="a9b8b-104">Base class for Obsolete exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a9b8b-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="a9b8b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a9b8b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a9b8b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a9b8b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a9b8b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a9b8b-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a9b8b-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a9b8b-110">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="a9b8b-111">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            

<span data-ttu-id="a9b8b-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a9b8b-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a9b8b-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a9b8b-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b8b-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9b8b-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentObsoleteException _
    Inherits EsentApiException
'Usage
Dim instance As EsentObsoleteException
```

``` csharp
[SerializableAttribute]
public abstract class EsentObsoleteException : EsentApiException
```

## <a name="thread-safety"></a><span data-ttu-id="a9b8b-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="a9b8b-115">Thread safety</span></span>

<span data-ttu-id="a9b8b-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a9b8b-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a9b8b-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="a9b8b-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9b8b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9b8b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a9b8b-119">Referência</span><span class="sxs-lookup"><span data-stu-id="a9b8b-119">Reference</span></span>

[<span data-ttu-id="a9b8b-120">Membros do EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-120">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="a9b8b-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a9b8b-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="a9b8b-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="a9b8b-122">Derived types</span></span>

[<span data-ttu-id="a9b8b-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="a9b8b-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a9b8b-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a9b8b-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a9b8b-125">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a9b8b-126">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a9b8b-127">Microsoft. ISAM. ESENT. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-127">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          <span data-ttu-id="a9b8b-128">Microsoft. ISAM. ESENT. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-128">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>  
            [<span data-ttu-id="a9b8b-129">Microsoft. ISAM. ESENT. Interop. EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-129">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>](./esentaccessdeniedexception-class.md)  
            [<span data-ttu-id="a9b8b-130">Microsoft. ISAM. ESENT. Interop. EsentBadBackupDatabaseSizeException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-130">Microsoft.Isam.Esent.Interop.EsentBadBackupDatabaseSizeException</span></span>](./esentbadbackupdatabasesizeexception-class.md)  
            [<span data-ttu-id="a9b8b-131">Microsoft. ISAM. ESENT. Interop. EsentBadBookmarkException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-131">Microsoft.Isam.Esent.Interop.EsentBadBookmarkException</span></span>](./esentbadbookmarkexception-class.md)  
            [<span data-ttu-id="a9b8b-132">Microsoft. ISAM. ESENT. Interop. EsentBadDbSignatureException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-132">Microsoft.Isam.Esent.Interop.EsentBadDbSignatureException</span></span>](./esentbaddbsignatureexception-class.md)  
            [<span data-ttu-id="a9b8b-133">Microsoft. ISAM. ESENT. Interop. EsentBadPatchPageException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-133">Microsoft.Isam.Esent.Interop.EsentBadPatchPageException</span></span>](./esentbadpatchpageexception-class.md)  
            [<span data-ttu-id="a9b8b-134">Microsoft. ISAM. ESENT. Interop. EsentBadSLVSignatureException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-134">Microsoft.Isam.Esent.Interop.EsentBadSLVSignatureException</span></span>](./esentbadslvsignatureexception-class.md)  
            [<span data-ttu-id="a9b8b-135">Microsoft. ISAM. ESENT. Interop. EsentCannotAddFixedVarColumnToDerivedTableException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-135">Microsoft.Isam.Esent.Interop.EsentCannotAddFixedVarColumnToDerivedTableException</span></span>](./esentcannotaddfixedvarcolumntoderivedtableexception-class.md)  
            [<span data-ttu-id="a9b8b-136">Microsoft. ISAM. ESENT. Interop. EsentCannotNestDistributedTransactionsException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-136">Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException</span></span>](./esentcannotnestdistributedtransactionsexception-class.md)  
            [<span data-ttu-id="a9b8b-137">Microsoft. ISAM. ESENT. Interop. EsentColumnIndexedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-137">Microsoft.Isam.Esent.Interop.EsentColumnIndexedException</span></span>](./esentcolumnindexedexception-class.md)  
            [<span data-ttu-id="a9b8b-138">Microsoft. ISAM. ESENT. Interop. EsentColumnInRelationshipException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-138">Microsoft.Isam.Esent.Interop.EsentColumnInRelationshipException</span></span>](./esentcolumninrelationshipexception-class.md)  
            [<span data-ttu-id="a9b8b-139">Microsoft. ISAM. ESENT. Interop. EsentColumnLongException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-139">Microsoft.Isam.Esent.Interop.EsentColumnLongException</span></span>](./esentcolumnlongexception-class.md)  
            [<span data-ttu-id="a9b8b-140">Microsoft. ISAM. ESENT. Interop. EsentContainerNotEmptyException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-140">Microsoft.Isam.Esent.Interop.EsentContainerNotEmptyException</span></span>](./esentcontainernotemptyexception-class.md)  
            [<span data-ttu-id="a9b8b-141">Microsoft. ISAM. ESENT. Interop. EsentCurrencyStackOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-141">Microsoft.Isam.Esent.Interop.EsentCurrencyStackOutOfMemoryException</span></span>](./esentcurrencystackoutofmemoryexception-class.md)  
            [<span data-ttu-id="a9b8b-142">Microsoft. ISAM. ESENT. Interop. EsentDatabase200FormatException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-142">Microsoft.Isam.Esent.Interop.EsentDatabase200FormatException</span></span>](./esentdatabase200formatexception-class.md)  
            [<span data-ttu-id="a9b8b-143">Microsoft. ISAM. ESENT. Interop. EsentDatabase400FormatException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-143">Microsoft.Isam.Esent.Interop.EsentDatabase400FormatException</span></span>](./esentdatabase400formatexception-class.md)  
            [<span data-ttu-id="a9b8b-144">Microsoft. ISAM. ESENT. Interop. EsentDatabase500FormatException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-144">Microsoft.Isam.Esent.Interop.EsentDatabase500FormatException</span></span>](./esentdatabase500formatexception-class.md)  
            [<span data-ttu-id="a9b8b-145">Microsoft. ISAM. ESENT. Interop. EsentDatabaseIdInUseException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-145">Microsoft.Isam.Esent.Interop.EsentDatabaseIdInUseException</span></span>](./esentdatabaseidinuseexception-class.md)  
            [<span data-ttu-id="a9b8b-146">Microsoft. ISAM. ESENT. Interop. EsentDatabasePatchFileMismatchException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-146">Microsoft.Isam.Esent.Interop.EsentDatabasePatchFileMismatchException</span></span>](./esentdatabasepatchfilemismatchexception-class.md)  
            [<span data-ttu-id="a9b8b-147">Microsoft. ISAM. ESENT. Interop. EsentDatabasesNotFromSameSnapshotException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-147">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>](./esentdatabasesnotfromsamesnapshotexception-class.md)  
            [<span data-ttu-id="a9b8b-148">Microsoft. ISAM. ESENT. Interop. EsentDatabaseStreamingFileMismatchException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-148">Microsoft.Isam.Esent.Interop.EsentDatabaseStreamingFileMismatchException</span></span>](./esentdatabasestreamingfilemismatchexception-class.md)  
            [<span data-ttu-id="a9b8b-149">Microsoft. ISAM. ESENT. Interop. EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-149">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>](./esentdatabaseunavailableexception-class.md)  
            [<span data-ttu-id="a9b8b-150">Microsoft. ISAM. ESENT. Interop. EsentDataHasChangedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-150">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>](./esentdatahaschangedexception-class.md)  
            [<span data-ttu-id="a9b8b-151">Microsoft. ISAM. ESENT. Interop. EsentDistributedTransactionAlreadyPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-151">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionAlreadyPreparedToCommitException</span></span>](./esentdistributedtransactionalreadypreparedtocommitexception-class.md)  
            [<span data-ttu-id="a9b8b-152">Microsoft. ISAM. ESENT. Interop. EsentDistributedTransactionNotYetPreparedToCommitException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-152">Microsoft.Isam.Esent.Interop.EsentDistributedTransactionNotYetPreparedToCommitException</span></span>](./esentdistributedtransactionnotyetpreparedtocommitexception-class.md)  
            [<span data-ttu-id="a9b8b-153">Microsoft. ISAM. ESENT. Interop. EsentDTCCallbackUnexpectedErrorException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-153">Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException</span></span>](./esentdtccallbackunexpectederrorexception-class.md)  
            [<span data-ttu-id="a9b8b-154">Microsoft. ISAM. ESENT. Interop. EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-154">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>](./esentdtcmissingcallbackexception-class.md)  
            [<span data-ttu-id="a9b8b-155">Microsoft. ISAM. ESENT. Interop. EsentDTCMissingCallbackOnRecoveryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-155">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException</span></span>](./esentdtcmissingcallbackonrecoveryexception-class.md)  
            [<span data-ttu-id="a9b8b-156">Microsoft. ISAM. ESENT. Interop. EsentFileCloseException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-156">Microsoft.Isam.Esent.Interop.EsentFileCloseException</span></span>](./esentfilecloseexception-class.md)  
            [<span data-ttu-id="a9b8b-157">Microsoft. ISAM. ESENT. Interop. EsentFileIOAbortException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-157">Microsoft.Isam.Esent.Interop.EsentFileIOAbortException</span></span>](./esentfileioabortexception-class.md)  
            [<span data-ttu-id="a9b8b-158">Microsoft. ISAM. ESENT. Interop. EsentFileIOFailException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-158">Microsoft.Isam.Esent.Interop.EsentFileIOFailException</span></span>](./esentfileiofailexception-class.md)  
            [<span data-ttu-id="a9b8b-159">Microsoft. ISAM. ESENT. Interop. EsentFileIORetryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-159">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>](./esentfileioretryexception-class.md)  
            [<span data-ttu-id="a9b8b-160">Microsoft. ISAM. ESENT. Interop. EsentFileIOSparseException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-160">Microsoft.Isam.Esent.Interop.EsentFileIOSparseException</span></span>](./esentfileiosparseexception-class.md)  
            [<span data-ttu-id="a9b8b-161">Microsoft. ISAM. ESENT. Interop. EsentIndexCantBuildException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-161">Microsoft.Isam.Esent.Interop.EsentIndexCantBuildException</span></span>](./esentindexcantbuildexception-class.md)  
            [<span data-ttu-id="a9b8b-162">Microsoft. ISAM. ESENT. Interop. EsentIndexTuplesTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-162">Microsoft.Isam.Esent.Interop.EsentIndexTuplesTooManyColumnsException</span></span>](./esentindextuplestoomanycolumnsexception-class.md)  
            [<span data-ttu-id="a9b8b-163">Microsoft. ISAM. ESENT. Interop. EsentInvalidCountryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-163">Microsoft.Isam.Esent.Interop.EsentInvalidCountryException</span></span>](./esentinvalidcountryexception-class.md)  
            [<span data-ttu-id="a9b8b-164">Microsoft. ISAM. ESENT. Interop. EsentInvalidFilenameException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-164">Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException</span></span>](./esentinvalidfilenameexception-class.md)  
            [<span data-ttu-id="a9b8b-165">Microsoft. ISAM. ESENT. Interop. EsentInvalidLogDirectoryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-165">Microsoft.Isam.Esent.Interop.EsentInvalidLogDirectoryException</span></span>](./esentinvalidlogdirectoryexception-class.md)  
            [<span data-ttu-id="a9b8b-166">Microsoft. ISAM. ESENT. Interop. EsentInvalidLoggedOperationException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-166">Microsoft.Isam.Esent.Interop.EsentInvalidLoggedOperationException</span></span>](./esentinvalidloggedoperationexception-class.md)  
            [<span data-ttu-id="a9b8b-167">Microsoft. ISAM. ESENT. Interop. EsentInvalidObjectException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-167">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>](./esentinvalidobjectexception-class.md)  
            [<span data-ttu-id="a9b8b-168">Microsoft. ISAM. ESENT. Interop. EsentInvalidOnSortException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-168">Microsoft.Isam.Esent.Interop.EsentInvalidOnSortException</span></span>](./esentinvalidonsortexception-class.md)  
            [<span data-ttu-id="a9b8b-169">Microsoft. ISAM. ESENT. Interop. EsentInvalidSystemPathException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-169">Microsoft.Isam.Esent.Interop.EsentInvalidSystemPathException</span></span>](./esentinvalidsystempathexception-class.md)  
            [<span data-ttu-id="a9b8b-170">Microsoft. ISAM. ESENT. Interop. EsentKeyBoundaryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-170">Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException</span></span>](./esentkeyboundaryexception-class.md)  
            [<span data-ttu-id="a9b8b-171">Microsoft. ISAM. ESENT. Interop. EsentKeyTooBigException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-171">Microsoft.Isam.Esent.Interop.EsentKeyTooBigException</span></span>](./esentkeytoobigexception-class.md)  
            [<span data-ttu-id="a9b8b-172">Microsoft. ISAM. ESENT. Interop. EsentLanguageNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-172">Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException</span></span>](./esentlanguagenotsupportedexception-class.md)  
            [<span data-ttu-id="a9b8b-173">Microsoft. ISAM. ESENT. Interop. EsentLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-173">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>](./esentlinknotsupportedexception-class.md)  
            [<span data-ttu-id="a9b8b-174">Microsoft. ISAM. ESENT. Interop. EsentLogBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-174">Microsoft.Isam.Esent.Interop.EsentLogBufferTooSmallException</span></span>](./esentlogbuffertoosmallexception-class.md)  
            [<span data-ttu-id="a9b8b-175">Microsoft. ISAM. ESENT. Interop. EsentMissingPatchPageException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-175">Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException</span></span>](./esentmissingpatchpageexception-class.md)  
            [<span data-ttu-id="a9b8b-176">Microsoft. ISAM. ESENT. Interop. EsentMustCommitDistributedTransactionToLevel0Exception</span><span class="sxs-lookup"><span data-stu-id="a9b8b-176">Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception</span></span>](./esentmustcommitdistributedtransactiontolevel0exception-class.md)  
            [<span data-ttu-id="a9b8b-177">Microsoft. ISAM. ESENT. Interop. EsentMustDisableLoggingForDbUpgradeException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-177">Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException</span></span>](./esentmustdisableloggingfordbupgradeexception-class.md)  
            [<span data-ttu-id="a9b8b-178">Microsoft. ISAM. ESENT. Interop. EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-178">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>](./esentnotindistributedtransactionexception-class.md)  
            [<span data-ttu-id="a9b8b-179">Microsoft. ISAM. ESENT. Interop. EsentObjectDuplicateException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-179">Microsoft.Isam.Esent.Interop.EsentObjectDuplicateException</span></span>](./esentobjectduplicateexception-class.md)  
            [<span data-ttu-id="a9b8b-180">Microsoft. ISAM. ESENT. Interop. EsentPageBoundaryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-180">Microsoft.Isam.Esent.Interop.EsentPageBoundaryException</span></span>](./esentpageboundaryexception-class.md)  
            [<span data-ttu-id="a9b8b-181">Microsoft. ISAM. ESENT. Interop. EsentPatchFileMissingException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-181">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>](./esentpatchfilemissingexception-class.md)  
            [<span data-ttu-id="a9b8b-182">Microsoft. ISAM. ESENT. Interop. EsentRfsFailureException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-182">Microsoft.Isam.Esent.Interop.EsentRfsFailureException</span></span>](./esentrfsfailureexception-class.md)  
            [<span data-ttu-id="a9b8b-183">Microsoft. ISAM. ESENT. Interop. EsentRfsNotArmedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-183">Microsoft.Isam.Esent.Interop.EsentRfsNotArmedException</span></span>](./esentrfsnotarmedexception-class.md)  
            [<span data-ttu-id="a9b8b-184">Microsoft. ISAM. ESENT. Interop. EsentRollbackRequiredException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-184">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>](./esentrollbackrequiredexception-class.md)  
            [<span data-ttu-id="a9b8b-185">Microsoft. ISAM. ESENT. Interop. EsentSLVBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-185">Microsoft.Isam.Esent.Interop.EsentSLVBufferTooSmallException</span></span>](./esentslvbuffertoosmallexception-class.md)  
            [<span data-ttu-id="a9b8b-186">Microsoft. ISAM. ESENT. Interop. EsentSLVColumnCannotDeleteException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-186">Microsoft.Isam.Esent.Interop.EsentSLVColumnCannotDeleteException</span></span>](./esentslvcolumncannotdeleteexception-class.md)  
            [<span data-ttu-id="a9b8b-187">Microsoft. ISAM. ESENT. Interop. EsentSLVColumnDefaultValueNotAllowedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-187">Microsoft.Isam.Esent.Interop.EsentSLVColumnDefaultValueNotAllowedException</span></span>](./esentslvcolumndefaultvaluenotallowedexception-class.md)  
            [<span data-ttu-id="a9b8b-188">Microsoft. ISAM. ESENT. Interop. EsentSLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-188">Microsoft.Isam.Esent.Interop.EsentSLVCorruptedException</span></span>](./esentslvcorruptedexception-class.md)  
            [<span data-ttu-id="a9b8b-189">Microsoft. ISAM. ESENT. Interop. EsentSLVDatabaseMissingException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-189">Microsoft.Isam.Esent.Interop.EsentSLVDatabaseMissingException</span></span>](./esentslvdatabasemissingexception-class.md)  
            [<span data-ttu-id="a9b8b-190">Microsoft. ISAM. ESENT. Interop. EsentSLVEAListCorruptException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-190">Microsoft.Isam.Esent.Interop.EsentSLVEAListCorruptException</span></span>](./esentslvealistcorruptexception-class.md)  
            [<span data-ttu-id="a9b8b-191">Microsoft. ISAM. ESENT. Interop. EsentSLVEAListTooBigException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-191">Microsoft.Isam.Esent.Interop.EsentSLVEAListTooBigException</span></span>](./esentslvealisttoobigexception-class.md)  
            [<span data-ttu-id="a9b8b-192">Microsoft. ISAM. ESENT. Interop. EsentSLVEAListZeroAllocationException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-192">Microsoft.Isam.Esent.Interop.EsentSLVEAListZeroAllocationException</span></span>](./esentslvealistzeroallocationexception-class.md)  
            [<span data-ttu-id="a9b8b-193">Microsoft. ISAM. ESENT. Interop. EsentSLVFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-193">Microsoft.Isam.Esent.Interop.EsentSLVFileAccessDeniedException</span></span>](./esentslvfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="a9b8b-194">Microsoft. ISAM. ESENT. Interop. EsentSLVFileInUseException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-194">Microsoft.Isam.Esent.Interop.EsentSLVFileInUseException</span></span>](./esentslvfileinuseexception-class.md)  
            [<span data-ttu-id="a9b8b-195">Microsoft. ISAM. ESENT. Interop. EsentSLVFileInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-195">Microsoft.Isam.Esent.Interop.EsentSLVFileInvalidPathException</span></span>](./esentslvfileinvalidpathexception-class.md)  
            [<span data-ttu-id="a9b8b-196">Microsoft. ISAM. ESENT. Interop. EsentSLVFileIOException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-196">Microsoft.Isam.Esent.Interop.EsentSLVFileIOException</span></span>](./esentslvfileioexception-class.md)  
            [<span data-ttu-id="a9b8b-197">Microsoft. ISAM. ESENT. Interop. EsentSLVFileNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-197">Microsoft.Isam.Esent.Interop.EsentSLVFileNotFoundException</span></span>](./esentslvfilenotfoundexception-class.md)  
            [<span data-ttu-id="a9b8b-198">Microsoft. ISAM. ESENT. Interop. EsentSLVFileStaleException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-198">Microsoft.Isam.Esent.Interop.EsentSLVFileStaleException</span></span>](./esentslvfilestaleexception-class.md)  
            [<span data-ttu-id="a9b8b-199">Microsoft. ISAM. ESENT. Interop. EsentSLVFileUnknownException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-199">Microsoft.Isam.Esent.Interop.EsentSLVFileUnknownException</span></span>](./esentslvfileunknownexception-class.md)  
            [<span data-ttu-id="a9b8b-200">Microsoft. ISAM. ESENT. Interop. EsentSLVHeaderBadChecksumException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-200">Microsoft.Isam.Esent.Interop.EsentSLVHeaderBadChecksumException</span></span>](./esentslvheaderbadchecksumexception-class.md)  
            [<span data-ttu-id="a9b8b-201">Microsoft. ISAM. ESENT. Interop. EsentSLVHeaderCorruptedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-201">Microsoft.Isam.Esent.Interop.EsentSLVHeaderCorruptedException</span></span>](./esentslvheadercorruptedexception-class.md)  
            [<span data-ttu-id="a9b8b-202">Microsoft. ISAM. ESENT. Interop. EsentSLVInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-202">Microsoft.Isam.Esent.Interop.EsentSLVInvalidPathException</span></span>](./esentslvinvalidpathexception-class.md)  
            [<span data-ttu-id="a9b8b-203">Microsoft. ISAM. ESENT. Interop. EsentSLVOwnerMapAlreadyExistsException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-203">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapAlreadyExistsException</span></span>](./esentslvownermapalreadyexistsexception-class.md)  
            [<span data-ttu-id="a9b8b-204">Microsoft. ISAM. ESENT. Interop. EsentSLVOwnerMapCorruptedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-204">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapCorruptedException</span></span>](./esentslvownermapcorruptedexception-class.md)  
            [<span data-ttu-id="a9b8b-205">Microsoft. ISAM. ESENT. Interop. EsentSLVOwnerMapPageNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-205">Microsoft.Isam.Esent.Interop.EsentSLVOwnerMapPageNotFoundException</span></span>](./esentslvownermappagenotfoundexception-class.md)  
            [<span data-ttu-id="a9b8b-206">Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotCommittedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-206">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotCommittedException</span></span>](./esentslvpagesnotcommittedexception-class.md)  
            [<span data-ttu-id="a9b8b-207">Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-207">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotDeletedException</span></span>](./esentslvpagesnotdeletedexception-class.md)  
            [<span data-ttu-id="a9b8b-208">Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotFreeException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-208">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotFreeException</span></span>](./esentslvpagesnotfreeexception-class.md)  
            [<span data-ttu-id="a9b8b-209">Microsoft. ISAM. ESENT. Interop. EsentSLVPagesNotReservedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-209">Microsoft.Isam.Esent.Interop.EsentSLVPagesNotReservedException</span></span>](./esentslvpagesnotreservedexception-class.md)  
            [<span data-ttu-id="a9b8b-210">Microsoft. ISAM. ESENT. Interop. EsentSLVProviderNotLoadedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-210">Microsoft.Isam.Esent.Interop.EsentSLVProviderNotLoadedException</span></span>](./esentslvprovidernotloadedexception-class.md)  
            [<span data-ttu-id="a9b8b-211">Microsoft. ISAM. ESENT. Interop. EsentSLVProviderVersionMismatchException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-211">Microsoft.Isam.Esent.Interop.EsentSLVProviderVersionMismatchException</span></span>](./esentslvproviderversionmismatchexception-class.md)  
            [<span data-ttu-id="a9b8b-212">Microsoft. ISAM. ESENT. Interop. EsentSLVReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-212">Microsoft.Isam.Esent.Interop.EsentSLVReadVerifyFailureException</span></span>](./esentslvreadverifyfailureexception-class.md)  
            [<span data-ttu-id="a9b8b-213">Microsoft. ISAM. ESENT. Interop. EsentSLVRootNotSpecifiedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-213">Microsoft.Isam.Esent.Interop.EsentSLVRootNotSpecifiedException</span></span>](./esentslvrootnotspecifiedexception-class.md)  
            [<span data-ttu-id="a9b8b-214">Microsoft. ISAM. ESENT. Interop. EsentSLVRootPathInvalidException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-214">Microsoft.Isam.Esent.Interop.EsentSLVRootPathInvalidException</span></span>](./esentslvrootpathinvalidexception-class.md)  
            [<span data-ttu-id="a9b8b-215">Microsoft. ISAM. ESENT. Interop. EsentSLVRootStillOpenException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-215">Microsoft.Isam.Esent.Interop.EsentSLVRootStillOpenException</span></span>](./esentslvrootstillopenexception-class.md)  
            [<span data-ttu-id="a9b8b-216">Microsoft. ISAM. ESENT. Interop. EsentSLVSpaceCorruptedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-216">Microsoft.Isam.Esent.Interop.EsentSLVSpaceCorruptedException</span></span>](./esentslvspacecorruptedexception-class.md)  
            [<span data-ttu-id="a9b8b-217">Microsoft. ISAM. ESENT. Interop. EsentSLVSpaceWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-217">Microsoft.Isam.Esent.Interop.EsentSLVSpaceWriteConflictException</span></span>](./esentslvspacewriteconflictexception-class.md)  
            [<span data-ttu-id="a9b8b-218">Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileAlreadyExistsException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-218">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileAlreadyExistsException</span></span>](./esentslvstreamingfilealreadyexistsexception-class.md)  
            [<span data-ttu-id="a9b8b-219">Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileFullException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-219">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileFullException</span></span>](./esentslvstreamingfilefullexception-class.md)  
            [<span data-ttu-id="a9b8b-220">Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileInUseException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-220">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileInUseException</span></span>](./esentslvstreamingfileinuseexception-class.md)  
            [<span data-ttu-id="a9b8b-221">Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileMissingException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-221">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileMissingException</span></span>](./esentslvstreamingfilemissingexception-class.md)  
            [<span data-ttu-id="a9b8b-222">Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileNotCreatedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-222">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileNotCreatedException</span></span>](./esentslvstreamingfilenotcreatedexception-class.md)  
            [<span data-ttu-id="a9b8b-223">Microsoft. ISAM. ESENT. Interop. EsentSLVStreamingFileReadOnlyException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-223">Microsoft.Isam.Esent.Interop.EsentSLVStreamingFileReadOnlyException</span></span>](./esentslvstreamingfilereadonlyexception-class.md)  
            [<span data-ttu-id="a9b8b-224">Microsoft. ISAM. ESENT. Interop. EsentSoftRecoveryOnSnapshotException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-224">Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException</span></span>](./esentsoftrecoveryonsnapshotexception-class.md)  
            [<span data-ttu-id="a9b8b-225">Microsoft. ISAM. ESENT. Interop. EsentSPAvailExtCacheOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-225">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfMemoryException</span></span>](./esentspavailextcacheoutofmemoryexception-class.md)  
            [<span data-ttu-id="a9b8b-226">Microsoft. ISAM. ESENT. Interop. EsentSPAvailExtCacheOutOfSyncException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-226">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCacheOutOfSyncException</span></span>](./esentspavailextcacheoutofsyncexception-class.md)  
            [<span data-ttu-id="a9b8b-227">Microsoft. ISAM. ESENT. Interop. EsentSQLLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-227">Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException</span></span>](./esentsqllinknotsupportedexception-class.md)  
            [<span data-ttu-id="a9b8b-228">Microsoft. ISAM. ESENT. Interop. EsentStreamingDataNotLoggedException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-228">Microsoft.Isam.Esent.Interop.EsentStreamingDataNotLoggedException</span></span>](./esentstreamingdatanotloggedexception-class.md)  
            [<span data-ttu-id="a9b8b-229">Microsoft. ISAM. ESENT. Interop. EsentTaggedNotNULLException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-229">Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException</span></span>](./esenttaggednotnullexception-class.md)  
            [<span data-ttu-id="a9b8b-230">Microsoft. ISAM. ESENT. Interop. EsentTempFileOpenErrorException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-230">Microsoft.Isam.Esent.Interop.EsentTempFileOpenErrorException</span></span>](./esenttempfileopenerrorexception-class.md)  
            [<span data-ttu-id="a9b8b-231">Microsoft. ISAM. ESENT. Interop. EsentTooManyOpenDatabasesException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-231">Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException</span></span>](./esenttoomanyopendatabasesexception-class.md)  
            [<span data-ttu-id="a9b8b-232">Microsoft. ISAM. ESENT. Interop. EsentTooManySplitsException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-232">Microsoft.Isam.Esent.Interop.EsentTooManySplitsException</span></span>](./esenttoomanysplitsexception-class.md)  
            [<span data-ttu-id="a9b8b-233">Microsoft. ISAM. ESENT. Interop. EsentUnicodeTranslationBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="a9b8b-233">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationBufferTooSmallException</span></span>](./esentunicodetranslationbuffertoosmallexception-class.md)