---
title: Funções (STG)
description: As funções são rotinas ou sub-rotinas que retornam um valor ou valores específicos. As funções de armazenamento estruturado são descritas nas seções a seguir.
ms.assetid: 5fbb05ae-594d-4fa5-97d2-a2371e94c054
keywords:
- Strctd de armazenamento estruturado STG, referência, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f49c091b5ba9619b649e620da7b436ebac4ccb
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105754930"
---
# <a name="structured-storage-functions"></a><span data-ttu-id="4818a-105">Funções de armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="4818a-105">Structured Storage functions</span></span>

<span data-ttu-id="4818a-106">As funções são rotinas ou sub-rotinas que retornam um valor ou valores específicos.</span><span class="sxs-lookup"><span data-stu-id="4818a-106">Functions are routines or subroutines that return a specific value or values.</span></span> <span data-ttu-id="4818a-107">As funções de armazenamento estruturado são descritas nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="4818a-107">Structured Storage functions are described in the following sections:</span></span>

-   [<span data-ttu-id="4818a-108">**CreateILockBytesOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="4818a-108">**CreateILockBytesOnHGlobal**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal)
-   [<span data-ttu-id="4818a-109">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="4818a-109">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
-   [<span data-ttu-id="4818a-110">**FmtIdToPropStgName**</span><span class="sxs-lookup"><span data-stu-id="4818a-110">**FmtIdToPropStgName**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
-   [<span data-ttu-id="4818a-111">**FreePropVariantArray**</span><span class="sxs-lookup"><span data-stu-id="4818a-111">**FreePropVariantArray**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [<span data-ttu-id="4818a-112">**GetConvertStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-112">**GetConvertStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-getconvertstg)
-   [<span data-ttu-id="4818a-113">**GetHGlobalFromILockBytes**</span><span class="sxs-lookup"><span data-stu-id="4818a-113">**GetHGlobalFromILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes)
-   [<span data-ttu-id="4818a-114">**GetHGlobalFromStream**</span><span class="sxs-lookup"><span data-stu-id="4818a-114">**GetHGlobalFromStream**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream)
-   [<span data-ttu-id="4818a-115">**OleConvertIStorageToOLESTREAM**</span><span class="sxs-lookup"><span data-stu-id="4818a-115">**OleConvertIStorageToOLESTREAM**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestream)
-   [<span data-ttu-id="4818a-116">**OleConvertIStorageToOLESTREAMEx**</span><span class="sxs-lookup"><span data-stu-id="4818a-116">**OleConvertIStorageToOLESTREAMEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestreamex)
-   [<span data-ttu-id="4818a-117">**OleConvertOLESTREAMToIStorage**</span><span class="sxs-lookup"><span data-stu-id="4818a-117">**OleConvertOLESTREAMToIStorage**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorage)
-   [<span data-ttu-id="4818a-118">**OleConvertOLESTREAMToIStorageEx**</span><span class="sxs-lookup"><span data-stu-id="4818a-118">**OleConvertOLESTREAMToIStorageEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorageex)
-   [<span data-ttu-id="4818a-119">**PropStgNameToFmtId**</span><span class="sxs-lookup"><span data-stu-id="4818a-119">**PropStgNameToFmtId**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
-   [<span data-ttu-id="4818a-120">**PropVariantClear**</span><span class="sxs-lookup"><span data-stu-id="4818a-120">**PropVariantClear**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [<span data-ttu-id="4818a-121">**PropVariantCopy**</span><span class="sxs-lookup"><span data-stu-id="4818a-121">**PropVariantCopy**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)
-   [<span data-ttu-id="4818a-122">**PropVariantInit**</span><span class="sxs-lookup"><span data-stu-id="4818a-122">**PropVariantInit**</span></span>](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [<span data-ttu-id="4818a-123">**ReadClassStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-123">**ReadClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)
-   [<span data-ttu-id="4818a-124">**ReadClassStm**</span><span class="sxs-lookup"><span data-stu-id="4818a-124">**ReadClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstm)
-   [<span data-ttu-id="4818a-125">**ReadFmtUserTypeStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-125">**ReadFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)
-   [<span data-ttu-id="4818a-126">**StgConvertPropertyToVariant**</span><span class="sxs-lookup"><span data-stu-id="4818a-126">**StgConvertPropertyToVariant**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertpropertytovariant)
-   [<span data-ttu-id="4818a-127">**SetConvertStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-127">**SetConvertStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-setconvertstg)
-   [<span data-ttu-id="4818a-128">**StgConvertVariantToProperty**</span><span class="sxs-lookup"><span data-stu-id="4818a-128">**StgConvertVariantToProperty**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertvarianttoproperty)
-   [<span data-ttu-id="4818a-129">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="4818a-129">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
-   [<span data-ttu-id="4818a-130">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="4818a-130">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
-   [<span data-ttu-id="4818a-131">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-131">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
-   [<span data-ttu-id="4818a-132">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-132">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
-   [<span data-ttu-id="4818a-133">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="4818a-133">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
-   [<span data-ttu-id="4818a-134">**StgDeserializePropVariant**</span><span class="sxs-lookup"><span data-stu-id="4818a-134">**StgDeserializePropVariant**</span></span>](/windows/desktop/api/Propvarutil/nf-propvarutil-stgdeserializepropvariant)
-   [<span data-ttu-id="4818a-135">**StgGetIFillLockBytesOnFile**</span><span class="sxs-lookup"><span data-stu-id="4818a-135">**StgGetIFillLockBytesOnFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile)
-   [<span data-ttu-id="4818a-136">**StgGetIFillLockBytesOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="4818a-136">**StgGetIFillLockBytesOnILockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)
-   [<span data-ttu-id="4818a-137">**StgIsStorageFile**</span><span class="sxs-lookup"><span data-stu-id="4818a-137">**StgIsStorageFile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile)
-   [<span data-ttu-id="4818a-138">**StgIsStorageILockBytes**</span><span class="sxs-lookup"><span data-stu-id="4818a-138">**StgIsStorageILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstorageilockbytes)
-   [<span data-ttu-id="4818a-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span><span class="sxs-lookup"><span data-stu-id="4818a-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)
-   [<span data-ttu-id="4818a-140">**StgOpenLayoutDocfile**</span><span class="sxs-lookup"><span data-stu-id="4818a-140">**StgOpenLayoutDocfile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenlayoutdocfile)
-   [<span data-ttu-id="4818a-141">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-141">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
-   [<span data-ttu-id="4818a-142">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="4818a-142">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
-   [<span data-ttu-id="4818a-143">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="4818a-143">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
-   [<span data-ttu-id="4818a-144">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="4818a-144">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
-   [<span data-ttu-id="4818a-145">**StgPropertyLengthAsVariant**</span><span class="sxs-lookup"><span data-stu-id="4818a-145">**StgPropertyLengthAsVariant**</span></span>](/windows/desktop/api/Propapi/nf-propapi-stgpropertylengthasvariant)
-   [<span data-ttu-id="4818a-146">**StgSerializePropVariant**</span><span class="sxs-lookup"><span data-stu-id="4818a-146">**StgSerializePropVariant**</span></span>](/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant)
-   [<span data-ttu-id="4818a-147">**StgSetTimes**</span><span class="sxs-lookup"><span data-stu-id="4818a-147">**StgSetTimes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgsettimes)
-   [<span data-ttu-id="4818a-148">**WriteClassStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-148">**WriteClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)
-   [<span data-ttu-id="4818a-149">**WriteClassStm**</span><span class="sxs-lookup"><span data-stu-id="4818a-149">**WriteClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstm)
-   [<span data-ttu-id="4818a-150">**WriteFmtUserTypeStg**</span><span class="sxs-lookup"><span data-stu-id="4818a-150">**WriteFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg)

 

 
