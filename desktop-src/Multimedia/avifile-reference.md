---
title: Referência de AVIFile
description: Referência de AVIFile
ms.assetid: 73532d83-89c2-4911-8558-ce110e9f0f95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0291d0ac5864a9b370e79a98fa061770d05bca03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006071"
---
# <a name="avifile-reference"></a><span data-ttu-id="7c337-103">Referência de AVIFile</span><span class="sxs-lookup"><span data-stu-id="7c337-103">AVIFile Reference</span></span>

<span data-ttu-id="7c337-104">Esta seção descreve as funções, as estruturas e as macros para aplicativos que usam os serviços AVIFiles.</span><span class="sxs-lookup"><span data-stu-id="7c337-104">This section describes the functions, structures, and macros for applications using the AVIFile services.</span></span> <span data-ttu-id="7c337-105">Esses elementos são agrupados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7c337-105">These elements are grouped as follows:</span></span>

## <a name="avifile-library-operations"></a><span data-ttu-id="7c337-106">Operações de biblioteca AVIFile</span><span class="sxs-lookup"><span data-stu-id="7c337-106">AVIFile Library Operations</span></span>

-   [<span data-ttu-id="7c337-107">**AVIFileInit**</span><span class="sxs-lookup"><span data-stu-id="7c337-107">**AVIFileInit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinit)
-   [<span data-ttu-id="7c337-108">**AVIFileExit**</span><span class="sxs-lookup"><span data-stu-id="7c337-108">**AVIFileExit**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileexit)

## <a name="opening-and-closing-avi-files"></a><span data-ttu-id="7c337-109">Abrindo e fechando arquivos AVI</span><span class="sxs-lookup"><span data-stu-id="7c337-109">Opening and Closing AVI Files</span></span>

-   [<span data-ttu-id="7c337-110">**AVIFileOpen**</span><span class="sxs-lookup"><span data-stu-id="7c337-110">**AVIFileOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileopen)
-   [<span data-ttu-id="7c337-111">**AVIFileAddRef**</span><span class="sxs-lookup"><span data-stu-id="7c337-111">**AVIFileAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileaddref)
-   [<span data-ttu-id="7c337-112">**AVIFileRelease**</span><span class="sxs-lookup"><span data-stu-id="7c337-112">**AVIFileRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilerelease)
-   [<span data-ttu-id="7c337-113">**GetOpenFileNamePreview**</span><span class="sxs-lookup"><span data-stu-id="7c337-113">**GetOpenFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

## <a name="reading-from-a-file"></a><span data-ttu-id="7c337-114">Lendo de um arquivo</span><span class="sxs-lookup"><span data-stu-id="7c337-114">Reading from a File</span></span>

-   [<span data-ttu-id="7c337-115">**AVIFileInfo**</span><span class="sxs-lookup"><span data-stu-id="7c337-115">**AVIFileInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifileinfo)
-   [<span data-ttu-id="7c337-116">**AVIFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="7c337-116">**AVIFILEINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa)
-   [<span data-ttu-id="7c337-117">**AVIFileReadData**</span><span class="sxs-lookup"><span data-stu-id="7c337-117">**AVIFileReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata)

## <a name="writing-to-a-file"></a><span data-ttu-id="7c337-118">Gravando em um arquivo</span><span class="sxs-lookup"><span data-stu-id="7c337-118">Writing to a File</span></span>

-   [<span data-ttu-id="7c337-119">**AVIFileWriteData**</span><span class="sxs-lookup"><span data-stu-id="7c337-119">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)

## <a name="using-the-clipboard"></a><span data-ttu-id="7c337-120">Usando a área de transferência</span><span class="sxs-lookup"><span data-stu-id="7c337-120">Using the Clipboard</span></span>

-   [<span data-ttu-id="7c337-121">**AVIPutFileOnClipboard**</span><span class="sxs-lookup"><span data-stu-id="7c337-121">**AVIPutFileOnClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard)
-   [<span data-ttu-id="7c337-122">**AVIGetFromClipboard**</span><span class="sxs-lookup"><span data-stu-id="7c337-122">**AVIGetFromClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)
-   [<span data-ttu-id="7c337-123">**AVIClearClipboard**</span><span class="sxs-lookup"><span data-stu-id="7c337-123">**AVIClearClipboard**</span></span>](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard)

## <a name="opening-and-closing-streams"></a><span data-ttu-id="7c337-124">Abrindo e fechando fluxos</span><span class="sxs-lookup"><span data-stu-id="7c337-124">Opening and Closing Streams</span></span>

-   [<span data-ttu-id="7c337-125">**AVIFileGetStream**</span><span class="sxs-lookup"><span data-stu-id="7c337-125">**AVIFileGetStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream)
-   [<span data-ttu-id="7c337-126">**AVIStreamOpenFromFile**</span><span class="sxs-lookup"><span data-stu-id="7c337-126">**AVIStreamOpenFromFile**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea)
-   [<span data-ttu-id="7c337-127">**AVIStreamAddRef**</span><span class="sxs-lookup"><span data-stu-id="7c337-127">**AVIStreamAddRef**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref)
-   [<span data-ttu-id="7c337-128">**AVIStreamRelease**</span><span class="sxs-lookup"><span data-stu-id="7c337-128">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="reading-stream-information"></a><span data-ttu-id="7c337-129">Lendo informações de fluxo</span><span class="sxs-lookup"><span data-stu-id="7c337-129">Reading Stream Information</span></span>

-   [<span data-ttu-id="7c337-130">**AVISTREAMINFO**</span><span class="sxs-lookup"><span data-stu-id="7c337-130">**AVISTREAMINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)
-   [<span data-ttu-id="7c337-131">**AVIStreamReadData**</span><span class="sxs-lookup"><span data-stu-id="7c337-131">**AVIStreamReadData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata)
-   [<span data-ttu-id="7c337-132">**AVIStreamDataSize**</span><span class="sxs-lookup"><span data-stu-id="7c337-132">**AVIStreamDataSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize)
-   [<span data-ttu-id="7c337-133">**AVIStreamReadFormat**</span><span class="sxs-lookup"><span data-stu-id="7c337-133">**AVIStreamReadFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat)
-   [<span data-ttu-id="7c337-134">**AVIStreamFormatSize**</span><span class="sxs-lookup"><span data-stu-id="7c337-134">**AVIStreamFormatSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize)
-   [<span data-ttu-id="7c337-135">**AVIStreamRead**</span><span class="sxs-lookup"><span data-stu-id="7c337-135">**AVIStreamRead**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamread)
-   [<span data-ttu-id="7c337-136">**AVIStreamSampleSize**</span><span class="sxs-lookup"><span data-stu-id="7c337-136">**AVIStreamSampleSize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize)
-   [<span data-ttu-id="7c337-137">**AVIStreamBeginStreaming**</span><span class="sxs-lookup"><span data-stu-id="7c337-137">**AVIStreamBeginStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming)
-   [<span data-ttu-id="7c337-138">**AVIStreamEndStreaming**</span><span class="sxs-lookup"><span data-stu-id="7c337-138">**AVIStreamEndStreaming**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming)

## <a name="decompressing-video-data-in-a-stream"></a><span data-ttu-id="7c337-139">Descompactando dados de vídeo em um fluxo</span><span class="sxs-lookup"><span data-stu-id="7c337-139">Decompressing Video Data in a Stream</span></span>

-   [<span data-ttu-id="7c337-140">**AVIStreamGetFrameOpen**</span><span class="sxs-lookup"><span data-stu-id="7c337-140">**AVIStreamGetFrameOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen)
-   [<span data-ttu-id="7c337-141">**AVIStreamGetFrame**</span><span class="sxs-lookup"><span data-stu-id="7c337-141">**AVIStreamGetFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe)
-   [<span data-ttu-id="7c337-142">**AVIStreamGetFrameClose**</span><span class="sxs-lookup"><span data-stu-id="7c337-142">**AVIStreamGetFrameClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose)

## <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="7c337-143">Criando um arquivo de fluxos existentes</span><span class="sxs-lookup"><span data-stu-id="7c337-143">Creating a File from Existing Streams</span></span>

-   [<span data-ttu-id="7c337-144">**AVISave**</span><span class="sxs-lookup"><span data-stu-id="7c337-144">**AVISave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisavea)
-   [<span data-ttu-id="7c337-145">**AVISaveV**</span><span class="sxs-lookup"><span data-stu-id="7c337-145">**AVISaveV**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveva)
-   [<span data-ttu-id="7c337-146">**AVISaveOptions**</span><span class="sxs-lookup"><span data-stu-id="7c337-146">**AVISaveOptions**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions)
-   [<span data-ttu-id="7c337-147">**GetSaveFileNamePreview**</span><span class="sxs-lookup"><span data-stu-id="7c337-147">**GetSaveFileNamePreview**</span></span>](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa)
-   [<span data-ttu-id="7c337-148">**AVIMakeFileFromStreams**</span><span class="sxs-lookup"><span data-stu-id="7c337-148">**AVIMakeFileFromStreams**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams)

## <a name="writing-individual-streams"></a><span data-ttu-id="7c337-149">Gravando fluxos individuais</span><span class="sxs-lookup"><span data-stu-id="7c337-149">Writing Individual Streams</span></span>

-   [<span data-ttu-id="7c337-150">**AVIFileCreateStream**</span><span class="sxs-lookup"><span data-stu-id="7c337-150">**AVIFileCreateStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream)
-   [<span data-ttu-id="7c337-151">**AVIStreamSetFormat**</span><span class="sxs-lookup"><span data-stu-id="7c337-151">**AVIStreamSetFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat)
-   [<span data-ttu-id="7c337-152">**AVIStreamWrite**</span><span class="sxs-lookup"><span data-stu-id="7c337-152">**AVIStreamWrite**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite)
-   [<span data-ttu-id="7c337-153">**AVIFileWriteData**</span><span class="sxs-lookup"><span data-stu-id="7c337-153">**AVIFileWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata)
-   [<span data-ttu-id="7c337-154">**AVIStreamWriteData**</span><span class="sxs-lookup"><span data-stu-id="7c337-154">**AVIStreamWriteData**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata)
-   [<span data-ttu-id="7c337-155">**AVIStreamRelease**</span><span class="sxs-lookup"><span data-stu-id="7c337-155">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="finding-the-starting-position-in-a-stream"></a><span data-ttu-id="7c337-156">Localizando a posição inicial em um fluxo</span><span class="sxs-lookup"><span data-stu-id="7c337-156">Finding the Starting Position in a Stream</span></span>

-   [<span data-ttu-id="7c337-157">**AVIStreamStart**</span><span class="sxs-lookup"><span data-stu-id="7c337-157">**AVIStreamStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstart)
-   [<span data-ttu-id="7c337-158">**AVIStreamStartTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-158">**AVIStreamStartTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime)
-   [<span data-ttu-id="7c337-159">**AVIStreamLength**</span><span class="sxs-lookup"><span data-stu-id="7c337-159">**AVIStreamLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlength)
-   [<span data-ttu-id="7c337-160">**AVIStreamLengthTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-160">**AVIStreamLengthTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime)
-   [<span data-ttu-id="7c337-161">**AVIStreamFindSample**</span><span class="sxs-lookup"><span data-stu-id="7c337-161">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="7c337-162">**AVIStreamEnd**</span><span class="sxs-lookup"><span data-stu-id="7c337-162">**AVIStreamEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamend)
-   [<span data-ttu-id="7c337-163">**AVIStreamEndTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-163">**AVIStreamEndTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime)

## <a name="finding-sample-and-key-frames"></a><span data-ttu-id="7c337-164">Localizando amostras e quadros-chave</span><span class="sxs-lookup"><span data-stu-id="7c337-164">Finding Sample and Key Frames</span></span>

-   [<span data-ttu-id="7c337-165">**AVIStreamFindSample**</span><span class="sxs-lookup"><span data-stu-id="7c337-165">**AVIStreamFindSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample)
-   [<span data-ttu-id="7c337-166">**AVIStreamIsKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="7c337-166">**AVIStreamIsKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)
-   [<span data-ttu-id="7c337-167">**AVIStreamNearestKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="7c337-167">**AVIStreamNearestKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)
-   [<span data-ttu-id="7c337-168">**AVIStreamNearestKeyFrameTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-168">**AVIStreamNearestKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime)
-   [<span data-ttu-id="7c337-169">**AVIStreamNearestSample**</span><span class="sxs-lookup"><span data-stu-id="7c337-169">**AVIStreamNearestSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)
-   [<span data-ttu-id="7c337-170">**AVIStreamNearestSampleTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-170">**AVIStreamNearestSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)
-   [<span data-ttu-id="7c337-171">**AVIStreamNextKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="7c337-171">**AVIStreamNextKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)
-   [<span data-ttu-id="7c337-172">**AVIStreamNextKeyFrameTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-172">**AVIStreamNextKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)
-   [<span data-ttu-id="7c337-173">**AVIStreamNextSample**</span><span class="sxs-lookup"><span data-stu-id="7c337-173">**AVIStreamNextSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)
-   [<span data-ttu-id="7c337-174">**AVIStreamNextSampleTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-174">**AVIStreamNextSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)
-   [<span data-ttu-id="7c337-175">**AVIStreamPrevKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="7c337-175">**AVIStreamPrevKeyFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)
-   [<span data-ttu-id="7c337-176">**AVIStreamPrevKeyFrameTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-176">**AVIStreamPrevKeyFrameTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)
-   [<span data-ttu-id="7c337-177">**AVIStreamPrevSample**</span><span class="sxs-lookup"><span data-stu-id="7c337-177">**AVIStreamPrevSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)
-   [<span data-ttu-id="7c337-178">**AVIStreamPrevSampleTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-178">**AVIStreamPrevSampleTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)
-   [<span data-ttu-id="7c337-179">**AVIStreamSampleToSample**</span><span class="sxs-lookup"><span data-stu-id="7c337-179">**AVIStreamSampleToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)

## <a name="switching-between-samples-and-time"></a><span data-ttu-id="7c337-180">Alternando entre exemplos e hora</span><span class="sxs-lookup"><span data-stu-id="7c337-180">Switching Between Samples and Time</span></span>

-   [<span data-ttu-id="7c337-181">**AVIStreamSampleToTime**</span><span class="sxs-lookup"><span data-stu-id="7c337-181">**AVIStreamSampleToTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime)
-   [<span data-ttu-id="7c337-182">**AVIStreamTimeToSample**</span><span class="sxs-lookup"><span data-stu-id="7c337-182">**AVIStreamTimeToSample**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample)

## <a name="creating-temporary-streams"></a><span data-ttu-id="7c337-183">Criando fluxos temporários</span><span class="sxs-lookup"><span data-stu-id="7c337-183">Creating Temporary Streams</span></span>

-   [<span data-ttu-id="7c337-184">**AVIStreamCreate**</span><span class="sxs-lookup"><span data-stu-id="7c337-184">**AVIStreamCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate)
-   [<span data-ttu-id="7c337-185">**AVIMakeCompressedStream**</span><span class="sxs-lookup"><span data-stu-id="7c337-185">**AVIMakeCompressedStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream)
-   [<span data-ttu-id="7c337-186">**AVIStreamRelease**</span><span class="sxs-lookup"><span data-stu-id="7c337-186">**AVIStreamRelease**</span></span>](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease)

## <a name="editing-avi-streams"></a><span data-ttu-id="7c337-187">Editando fluxos AVI</span><span class="sxs-lookup"><span data-stu-id="7c337-187">Editing AVI Streams</span></span>

-   [<span data-ttu-id="7c337-188">**CreateEditableStream**</span><span class="sxs-lookup"><span data-stu-id="7c337-188">**CreateEditableStream**</span></span>](/windows/desktop/api/Vfw/nf-vfw-createeditablestream)
-   [<span data-ttu-id="7c337-189">**EditStreamCut**</span><span class="sxs-lookup"><span data-stu-id="7c337-189">**EditStreamCut**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcut)
-   [<span data-ttu-id="7c337-190">**EditStreamCopy**</span><span class="sxs-lookup"><span data-stu-id="7c337-190">**EditStreamCopy**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy)
-   [<span data-ttu-id="7c337-191">**EditStreamPaste**</span><span class="sxs-lookup"><span data-stu-id="7c337-191">**EditStreamPaste**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreampaste)
-   [<span data-ttu-id="7c337-192">**EditStreamClone**</span><span class="sxs-lookup"><span data-stu-id="7c337-192">**EditStreamClone**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamclone)
-   [<span data-ttu-id="7c337-193">**EditStreamSetInfo**</span><span class="sxs-lookup"><span data-stu-id="7c337-193">**EditStreamSetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa)
-   [<span data-ttu-id="7c337-194">**EditStreamSetName**</span><span class="sxs-lookup"><span data-stu-id="7c337-194">**EditStreamSetName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea)

## <a name="related-topics"></a><span data-ttu-id="7c337-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c337-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c337-196">Funções e macros do AVIFile</span><span class="sxs-lookup"><span data-stu-id="7c337-196">AVIFile Functions and Macros</span></span>](avifile-functions-and-macros.md)
</dt> </dl>

 

 




