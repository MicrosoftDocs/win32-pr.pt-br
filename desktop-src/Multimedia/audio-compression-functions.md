---
title: Funções de compactação de áudio
description: Funções de compactação de áudio
ms.assetid: da207a50-9c67-4cf3-920b-5878637060db
keywords:
- áudio de multimídia, funções do ACM
- áudio, funções do ACM
- Gerenciador de compactação de áudio (ACM), funções
- ACM (Gerenciador de compactação de áudio), funções
- Referência do ACM, funções
- referência para ACM, funções
- Funções do ACM
- compactação de áudio, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a495e52e404d04955a2c330729ef82cccb726554
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293933"
---
# <a name="audio-compression-functions"></a><span data-ttu-id="f0bb0-111">Funções de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="f0bb0-111">Audio Compression Functions</span></span>

<span data-ttu-id="f0bb0-112">As funções a seguir são usadas com a compactação de áudio.</span><span class="sxs-lookup"><span data-stu-id="f0bb0-112">The following functions are used with audio compression.</span></span>

-   [<span data-ttu-id="f0bb0-113">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-113">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="f0bb0-114">**acmDriverClose**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-114">**acmDriverClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [<span data-ttu-id="f0bb0-115">**acmDriverDetails**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-115">**acmDriverDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverdetails)
-   [<span data-ttu-id="f0bb0-116">**acmDriverEnum**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-116">**acmDriverEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [<span data-ttu-id="f0bb0-117">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-117">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="f0bb0-118">**acmDriverID**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-118">**acmDriverID**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [<span data-ttu-id="f0bb0-119">**acmDriverMessage**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-119">**acmDriverMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [<span data-ttu-id="f0bb0-120">**acmDriverOpen**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-120">**acmDriverOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [<span data-ttu-id="f0bb0-121">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-121">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="f0bb0-122">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-122">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [<span data-ttu-id="f0bb0-123">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-123">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)
-   [<span data-ttu-id="f0bb0-124">**acmFilterChoose**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-124">**acmFilterChoose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose)
-   [<span data-ttu-id="f0bb0-125">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-125">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="f0bb0-126">**acmFilterDetails**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-126">**acmFilterDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails)
-   [<span data-ttu-id="f0bb0-127">**acmFilterEnum**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-127">**acmFilterEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [<span data-ttu-id="f0bb0-128">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-128">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="f0bb0-129">**acmFilterTagDetails**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-129">**acmFilterTagDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails)
-   [<span data-ttu-id="f0bb0-130">**acmFilterTagEnum**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-130">**acmFilterTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [<span data-ttu-id="f0bb0-131">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-131">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="f0bb0-132">**acmFormatChoose**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-132">**acmFormatChoose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)
-   [<span data-ttu-id="f0bb0-133">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-133">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [<span data-ttu-id="f0bb0-134">**acmFormatDetails**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-134">**acmFormatDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatdetails)
-   [<span data-ttu-id="f0bb0-135">**acmFormatEnum**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-135">**acmFormatEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [<span data-ttu-id="f0bb0-136">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-136">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="f0bb0-137">**acmFormatSuggest**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-137">**acmFormatSuggest**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [<span data-ttu-id="f0bb0-138">**acmFormatTagDetails**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-138">**acmFormatTagDetails**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagdetails)
-   [<span data-ttu-id="f0bb0-139">**acmFormatTagEnum**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-139">**acmFormatTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [<span data-ttu-id="f0bb0-140">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-140">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   [<span data-ttu-id="f0bb0-141">**acmGetVersion**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-141">**acmGetVersion**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [<span data-ttu-id="f0bb0-142">**acmMetrics**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-142">**acmMetrics**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)
-   [<span data-ttu-id="f0bb0-143">**acmStreamClose**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-143">**acmStreamClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [<span data-ttu-id="f0bb0-144">**acmStreamConvert**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-144">**acmStreamConvert**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   <span data-ttu-id="f0bb0-145">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0bb0-145">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>
-   [<span data-ttu-id="f0bb0-146">**acmStreamMessage**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-146">**acmStreamMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [<span data-ttu-id="f0bb0-147">**acmStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-147">**acmStreamOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [<span data-ttu-id="f0bb0-148">**acmStreamPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-148">**acmStreamPrepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [<span data-ttu-id="f0bb0-149">**acmStreamReset**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-149">**acmStreamReset**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [<span data-ttu-id="f0bb0-150">**acmStreamSize**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-150">**acmStreamSize**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [<span data-ttu-id="f0bb0-151">**acmStreamUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="f0bb0-151">**acmStreamUnprepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="related-topics"></a><span data-ttu-id="f0bb0-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0bb0-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0bb0-153">Referência do Gerenciador de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="f0bb0-153">Audio Compression Manager Reference</span></span>](audio-compression-manager-reference.md)
</dt> </dl>

 

 