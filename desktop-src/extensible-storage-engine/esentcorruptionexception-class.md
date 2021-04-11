---
description: 'Saiba mais sobre: classe EsentCorruptionException'
title: Classe EsentCorruptionException
TOCTitle: EsentCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a6914c2bf133a1050e3e3800e5c113c6cac1a11f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172427"
---
# <a name="esentcorruptionexception-class"></a><span data-ttu-id="654ae-103">Classe EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="654ae-103">EsentCorruptionException class</span></span>

<span data-ttu-id="654ae-104">Classe base para exceções de corrupção.</span><span class="sxs-lookup"><span data-stu-id="654ae-104">Base class for Corruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="654ae-105">Hierarquia de herança</span><span class="sxs-lookup"><span data-stu-id="654ae-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="654ae-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="654ae-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="654ae-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="654ae-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="654ae-108">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="654ae-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="654ae-109">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="654ae-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="654ae-110">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="654ae-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="654ae-111">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="654ae-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            

<span data-ttu-id="654ae-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="654ae-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="654ae-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="654ae-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="654ae-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="654ae-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentCorruptionException _
    Inherits EsentDataException
'Usage
Dim instance As EsentCorruptionException
```

``` csharp
[SerializableAttribute]
public abstract class EsentCorruptionException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="654ae-115">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="654ae-115">Thread safety</span></span>

<span data-ttu-id="654ae-116">Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="654ae-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="654ae-117">Não há garantia de que qualquer membro de instância seja seguro para threads.</span><span class="sxs-lookup"><span data-stu-id="654ae-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="654ae-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="654ae-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="654ae-119">Referência</span><span class="sxs-lookup"><span data-stu-id="654ae-119">Reference</span></span>

[<span data-ttu-id="654ae-120">Membros do EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="654ae-120">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="654ae-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="654ae-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="654ae-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="654ae-122">Derived types</span></span>

[<span data-ttu-id="654ae-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="654ae-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="654ae-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="654ae-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="654ae-125">Microsoft. ISAM. ESENT. EsentException</span><span class="sxs-lookup"><span data-stu-id="654ae-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="654ae-126">Microsoft. ISAM. ESENT. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="654ae-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="654ae-127">Microsoft. ISAM. ESENT. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="654ae-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="654ae-128">Microsoft. ISAM. ESENT. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="654ae-128">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>  
            [<span data-ttu-id="654ae-129">Microsoft. ISAM. ESENT. Interop. EsentBadEmptyPageException</span><span class="sxs-lookup"><span data-stu-id="654ae-129">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>](./esentbademptypageexception-class.md)  
            [<span data-ttu-id="654ae-130">Microsoft. ISAM. ESENT. Interop. EsentBadPageLinkException</span><span class="sxs-lookup"><span data-stu-id="654ae-130">Microsoft.Isam.Esent.Interop.EsentBadPageLinkException</span></span>](./esentbadpagelinkexception-class.md)  
            [<span data-ttu-id="654ae-131">Microsoft. ISAM. ESENT. Interop. EsentBadParentPageLinkException</span><span class="sxs-lookup"><span data-stu-id="654ae-131">Microsoft.Isam.Esent.Interop.EsentBadParentPageLinkException</span></span>](./esentbadparentpagelinkexception-class.md)  
            [<span data-ttu-id="654ae-132">Microsoft. ISAM. ESENT. Interop. EsentCatalogCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-132">Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException</span></span>](./esentcatalogcorruptedexception-class.md)  
            [<span data-ttu-id="654ae-133">Microsoft. ISAM. ESENT. Interop. EsentCheckpointCorruptException</span><span class="sxs-lookup"><span data-stu-id="654ae-133">Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException</span></span>](./esentcheckpointcorruptexception-class.md)  
            [<span data-ttu-id="654ae-134">Microsoft. ISAM. ESENT. Interop. EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="654ae-134">Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException</span></span>](./esentcommittedlogfilecorruptexception-class.md)  
            [<span data-ttu-id="654ae-135">Microsoft. ISAM. ESENT. Interop. EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="654ae-135">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>](./esentcommittedlogfilesmissingexception-class.md)  
            [<span data-ttu-id="654ae-136">Microsoft. ISAM. ESENT. Interop. EsentDatabaseBufferDependenciesCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-136">Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException</span></span>](./esentdatabasebufferdependenciescorruptedexception-class.md)  
            [<span data-ttu-id="654ae-137">Microsoft. ISAM. ESENT. Interop. EsentDatabaseCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-137">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException</span></span>](./esentdatabasecorruptedexception-class.md)  
            [<span data-ttu-id="654ae-138">Microsoft. ISAM. ESENT. Interop. EsentDbTimeCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-138">Microsoft.Isam.Esent.Interop.EsentDbTimeCorruptedException</span></span>](./esentdbtimecorruptedexception-class.md)  
            [<span data-ttu-id="654ae-139">Microsoft. ISAM. ESENT. Interop. EsentDecompressionFailedException</span><span class="sxs-lookup"><span data-stu-id="654ae-139">Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException</span></span>](./esentdecompressionfailedexception-class.md)  
            [<span data-ttu-id="654ae-140">Microsoft. ISAM. ESENT. Interop. EsentDerivedColumnCorruptionException</span><span class="sxs-lookup"><span data-stu-id="654ae-140">Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException</span></span>](./esentderivedcolumncorruptionexception-class.md)  
            [<span data-ttu-id="654ae-141">Microsoft. ISAM. ESENT. Interop. EsentDiskReadVerificationFailureException</span><span class="sxs-lookup"><span data-stu-id="654ae-141">Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException</span></span>](./esentdiskreadverificationfailureexception-class.md)  
            [<span data-ttu-id="654ae-142">Microsoft. ISAM. ESENT. Interop. EsentFileIOBeyondEOFException</span><span class="sxs-lookup"><span data-stu-id="654ae-142">Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException</span></span>](./esentfileiobeyondeofexception-class.md)  
            [<span data-ttu-id="654ae-143">Microsoft. ISAM. ESENT. Interop. EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="654ae-143">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>](./esentfilesystemcorruptionexception-class.md)  
            [<span data-ttu-id="654ae-144">Microsoft. ISAM. ESENT. Interop. EsentIndexBuildCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-144">Microsoft.Isam.Esent.Interop.EsentIndexBuildCorruptedException</span></span>](./esentindexbuildcorruptedexception-class.md)  
            [<span data-ttu-id="654ae-145">Microsoft. ISAM. ESENT. Interop. EsentInvalidLogSequenceException</span><span class="sxs-lookup"><span data-stu-id="654ae-145">Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException</span></span>](./esentinvalidlogsequenceexception-class.md)  
            [<span data-ttu-id="654ae-146">Microsoft. ISAM. ESENT. Interop. EsentLogCorruptDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="654ae-146">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRecoveryException</span></span>](./esentlogcorruptduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="654ae-147">Microsoft. ISAM. ESENT. Interop. EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="654ae-147">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>](./esentlogcorruptduringhardrestoreexception-class.md)  
            [<span data-ttu-id="654ae-148">Microsoft. ISAM. ESENT. Interop. EsentLogCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-148">Microsoft.Isam.Esent.Interop.EsentLogCorruptedException</span></span>](./esentlogcorruptedexception-class.md)  
            [<span data-ttu-id="654ae-149">Microsoft. ISAM. ESENT. Interop. EsentLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="654ae-149">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>](./esentlogfilecorruptexception-class.md)  
            [<span data-ttu-id="654ae-150">Microsoft. ISAM. ESENT. Interop. EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="654ae-150">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>](./esentlogreadverifyfailureexception-class.md)  
            [<span data-ttu-id="654ae-151">Microsoft. ISAM. ESENT. Interop. EsentLogTornWriteDuringHardRecoveryException</span><span class="sxs-lookup"><span data-stu-id="654ae-151">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRecoveryException</span></span>](./esentlogtornwriteduringhardrecoveryexception-class.md)  
            [<span data-ttu-id="654ae-152">Microsoft. ISAM. ESENT. Interop. EsentLogTornWriteDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="654ae-152">Microsoft.Isam.Esent.Interop.EsentLogTornWriteDuringHardRestoreException</span></span>](./esentlogtornwriteduringhardrestoreexception-class.md)  
            [<span data-ttu-id="654ae-153">Microsoft. ISAM. ESENT. Interop. EsentLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-153">Microsoft.Isam.Esent.Interop.EsentLVCorruptedException</span></span>](./esentlvcorruptedexception-class.md)  
            [<span data-ttu-id="654ae-154">Microsoft. ISAM. ESENT. Interop. EsentMissingLogFileException</span><span class="sxs-lookup"><span data-stu-id="654ae-154">Microsoft.Isam.Esent.Interop.EsentMissingLogFileException</span></span>](./esentmissinglogfileexception-class.md)  
            [<span data-ttu-id="654ae-155">Microsoft. ISAM. ESENT. Interop. EsentMissingPreviousLogFileException</span><span class="sxs-lookup"><span data-stu-id="654ae-155">Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException</span></span>](./esentmissingpreviouslogfileexception-class.md)  
            [<span data-ttu-id="654ae-156">Microsoft. ISAM. ESENT. Interop. EsentPageNotInitializedException</span><span class="sxs-lookup"><span data-stu-id="654ae-156">Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException</span></span>](./esentpagenotinitializedexception-class.md)  
            [<span data-ttu-id="654ae-157">Microsoft. ISAM. ESENT. Interop. EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-157">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>](./esentprimaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="654ae-158">Microsoft. ISAM. ESENT. Interop. EsentReadLostFlushVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="654ae-158">Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException</span></span>](./esentreadlostflushverifyfailureexception-class.md)  
            [<span data-ttu-id="654ae-159">Microsoft. ISAM. ESENT. Interop. EsentReadPgnoVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="654ae-159">Microsoft.Isam.Esent.Interop.EsentReadPgnoVerifyFailureException</span></span>](./esentreadpgnoverifyfailureexception-class.md)  
            [<span data-ttu-id="654ae-160">Microsoft. ISAM. ESENT. Interop. EsentReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="654ae-160">Microsoft.Isam.Esent.Interop.EsentReadVerifyFailureException</span></span>](./esentreadverifyfailureexception-class.md)  
            [<span data-ttu-id="654ae-161">Microsoft. ISAM. ESENT. Interop. EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="654ae-161">Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException</span></span>](./esentrecordformatconversionfailedexception-class.md)  
            [<span data-ttu-id="654ae-162">Microsoft. ISAM. ESENT. Interop. EsentRecoveryVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="654ae-162">Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException</span></span>](./esentrecoveryverifyfailureexception-class.md)  
            [<span data-ttu-id="654ae-163">Microsoft. ISAM. ESENT. Interop. EsentRedoAbruptEndedException</span><span class="sxs-lookup"><span data-stu-id="654ae-163">Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException</span></span>](./esentredoabruptendedexception-class.md)  
            [<span data-ttu-id="654ae-164">Microsoft. ISAM. ESENT. Interop. EsentSecondaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-164">Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException</span></span>](./esentsecondaryindexcorruptedexception-class.md)  
            [<span data-ttu-id="654ae-165">Microsoft. ISAM. ESENT. Interop. EsentSPAvailExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-165">Microsoft.Isam.Esent.Interop.EsentSPAvailExtCorruptedException</span></span>](./esentspavailextcorruptedexception-class.md)  
            [<span data-ttu-id="654ae-166">Microsoft. ISAM. ESENT. Interop. EsentSPOwnExtCorruptedException</span><span class="sxs-lookup"><span data-stu-id="654ae-166">Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException</span></span>](./esentspownextcorruptedexception-class.md)