---
title: Referência do Gerenciador de compactação de vídeo
description: Referência do Gerenciador de compactação de vídeo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video for Windows (VFW), Gerenciador de compactação de vídeo (VCM)
- VFW (vídeo para Windows), Gerenciador de compactação de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159505"
---
# <a name="video-compression-manager-reference"></a><span data-ttu-id="aefce-105">Referência do Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="aefce-105">Video Compression Manager Reference</span></span>

<span data-ttu-id="aefce-106">Esta seção descreve as funções, estruturas, mensagens e macros, associadas a VCM.</span><span class="sxs-lookup"><span data-stu-id="aefce-106">This section describes the functions, structures, messages, and macros, associated with VCM.</span></span> <span data-ttu-id="aefce-107">Esses elementos são agrupados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="aefce-107">These elements are grouped as follows.</span></span>

## <a name="compressor-installation-and-removal"></a><span data-ttu-id="aefce-108">Instalação e remoção do compactador</span><span class="sxs-lookup"><span data-stu-id="aefce-108">Compressor Installation and Removal</span></span>

-   [<span data-ttu-id="aefce-109">**ICInstall**</span><span class="sxs-lookup"><span data-stu-id="aefce-109">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="aefce-110">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="aefce-110">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="aefce-111">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="aefce-111">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="aefce-112">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="aefce-112">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="aefce-113">**ICRemove**</span><span class="sxs-lookup"><span data-stu-id="aefce-113">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="aefce-114">**ICOpenFunction**</span><span class="sxs-lookup"><span data-stu-id="aefce-114">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a><span data-ttu-id="aefce-115">Localizando e abrindo um compressor</span><span class="sxs-lookup"><span data-stu-id="aefce-115">Locating and Opening a Compressor</span></span>

-   [<span data-ttu-id="aefce-116">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="aefce-116">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="aefce-117">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="aefce-117">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="aefce-118">**ICDecompressOpen**</span><span class="sxs-lookup"><span data-stu-id="aefce-118">**ICDecompressOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [<span data-ttu-id="aefce-119">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="aefce-119">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="aefce-120">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="aefce-120">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="aefce-121">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="aefce-121">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a><span data-ttu-id="aefce-122">Selecionando compactadores</span><span class="sxs-lookup"><span data-stu-id="aefce-122">Selecting Compressors</span></span>

-   [<span data-ttu-id="aefce-123">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="aefce-123">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="aefce-124">**ICCompressorFree**</span><span class="sxs-lookup"><span data-stu-id="aefce-124">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="aefce-125">**COMPVARS**</span><span class="sxs-lookup"><span data-stu-id="aefce-125">**COMPVARS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a><span data-ttu-id="aefce-126">Configurando compactadores</span><span class="sxs-lookup"><span data-stu-id="aefce-126">Configuring Compressors</span></span>

-   [<span data-ttu-id="aefce-127">**\_Configurar ICM**</span><span class="sxs-lookup"><span data-stu-id="aefce-127">**ICM\_CONFIGURE**</span></span>](icm-configure.md)
-   [<span data-ttu-id="aefce-128">**ICM \_ GETstate**</span><span class="sxs-lookup"><span data-stu-id="aefce-128">**ICM\_GETSTATE**</span></span>](icm-getstate.md)
-   [<span data-ttu-id="aefce-129">**Autostate do ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-129">**ICM\_SETSTATE**</span></span>](icm-setstate.md)
-   [<span data-ttu-id="aefce-130">**ICSendMessage**</span><span class="sxs-lookup"><span data-stu-id="aefce-130">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a><span data-ttu-id="aefce-131">Informações de compressor</span><span class="sxs-lookup"><span data-stu-id="aefce-131">Compressor Information</span></span>

-   [<span data-ttu-id="aefce-132">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="aefce-132">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="aefce-133">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="aefce-133">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="aefce-134">**GETDEFAULTKEYFRAMERATE de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-134">**ICM\_GETDEFAULTKEYFRAMERATE**</span></span>](icm-getdefaultkeyframerate.md)
-   [<span data-ttu-id="aefce-135">**ICGetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="aefce-135">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="aefce-136">**GETDEFAULTQUALITY de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-136">**ICM\_GETDEFAULTQUALITY**</span></span>](icm-getdefaultquality.md)
-   [<span data-ttu-id="aefce-137">**sobre o ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-137">**ICM\_ABOUT**</span></span>](icm-about.md)

## <a name="single-image-compression"></a><span data-ttu-id="aefce-138">Compactação de imagem única</span><span class="sxs-lookup"><span data-stu-id="aefce-138">Single Image Compression</span></span>

-   [<span data-ttu-id="aefce-139">**ICImageCompress**</span><span class="sxs-lookup"><span data-stu-id="aefce-139">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a><span data-ttu-id="aefce-140">Compactação de sequência</span><span class="sxs-lookup"><span data-stu-id="aefce-140">Sequence Compression</span></span>

-   [<span data-ttu-id="aefce-141">**ICSeqCompressFrame**</span><span class="sxs-lookup"><span data-stu-id="aefce-141">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="aefce-142">**ICSeqCompressFrameStart**</span><span class="sxs-lookup"><span data-stu-id="aefce-142">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="aefce-143">**ICSeqCompressFrameEnd**</span><span class="sxs-lookup"><span data-stu-id="aefce-143">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a><span data-ttu-id="aefce-144">COMPVARS</span><span class="sxs-lookup"><span data-stu-id="aefce-144">COMPVARS</span></span>

-   [<span data-ttu-id="aefce-145">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="aefce-145">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a><span data-ttu-id="aefce-146">Compactação de dados de imagem</span><span class="sxs-lookup"><span data-stu-id="aefce-146">Image Data Compression</span></span>

-   [<span data-ttu-id="aefce-147">**ICCOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="aefce-147">**ICCOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [<span data-ttu-id="aefce-148">**\_formato de obtenção de compactação ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-148">**ICM\_COMPRESS\_GET\_FORMAT**</span></span>](icm-compress-get-format.md)
-   [<span data-ttu-id="aefce-149">**\_consulta de compactação ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-149">**ICM\_COMPRESS\_QUERY**</span></span>](icm-compress-query.md)
-   [<span data-ttu-id="aefce-150">**\_tamanho de obtenção de compactação ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-150">**ICM\_COMPRESS\_GET\_SIZE**</span></span>](icm-compress-get-size.md)
-   [<span data-ttu-id="aefce-151">**\_início de compactação de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-151">**ICM\_COMPRESS\_BEGIN**</span></span>](icm-compress-begin.md)
-   [<span data-ttu-id="aefce-152">**\_fim da compactação ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-152">**ICM\_COMPRESS\_END**</span></span>](icm-compress-end.md)

## <a name="compressor-monitoring"></a><span data-ttu-id="aefce-153">Monitoramento de compactador</span><span class="sxs-lookup"><span data-stu-id="aefce-153">Compressor Monitoring</span></span>

-   [<span data-ttu-id="aefce-154">**ICSETSTATUSPROC**</span><span class="sxs-lookup"><span data-stu-id="aefce-154">**ICSETSTATUSPROC**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a><span data-ttu-id="aefce-155">Descompactando imagens únicas</span><span class="sxs-lookup"><span data-stu-id="aefce-155">Decompressing Single Images</span></span>

-   [<span data-ttu-id="aefce-156">**ICImageDecompress**</span><span class="sxs-lookup"><span data-stu-id="aefce-156">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a><span data-ttu-id="aefce-157">Descompactando dados de imagem</span><span class="sxs-lookup"><span data-stu-id="aefce-157">Decompressing Image Data</span></span>

-   [<span data-ttu-id="aefce-158">**ICDECOMPRESSEX**</span><span class="sxs-lookup"><span data-stu-id="aefce-158">**ICDECOMPRESSEX**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [<span data-ttu-id="aefce-159">**ICDecompressExBegin**</span><span class="sxs-lookup"><span data-stu-id="aefce-159">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="aefce-160">**\_fim do DECOMPRESSEX de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-160">**ICM\_DECOMPRESSEX\_END**</span></span>](icm-decompressex-end.md)
-   [<span data-ttu-id="aefce-161">**\_formato de obtenção de DEScompactação de ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-161">**ICM\_DECOMPRESS\_GET\_FORMAT**</span></span>](icm-decompress-get-format.md)
-   [<span data-ttu-id="aefce-162">**\_ \_ extrair paleta descompactar \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-162">**ICM\_DECOMPRESS\_GET\_PALETTE**</span></span>](icm-decompress-get-palette.md)
-   [<span data-ttu-id="aefce-163">**ICDecompressExQuery**</span><span class="sxs-lookup"><span data-stu-id="aefce-163">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="aefce-164">**ICDECOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="aefce-164">**ICDECOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [<span data-ttu-id="aefce-165">**\_início de DEScompactação de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-165">**ICM\_DECOMPRESS\_BEGIN**</span></span>](icm-decompress-begin.md)
-   [<span data-ttu-id="aefce-166">**\_fim da DEScompactação de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-166">**ICM\_DECOMPRESS\_END**</span></span>](icm-decompress-end.md)
-   [<span data-ttu-id="aefce-167">**\_consulta de DEScompactação ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-167">**ICM\_DECOMPRESS\_QUERY**</span></span>](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a><span data-ttu-id="aefce-168">Usando recursos de Hardware-Drawing</span><span class="sxs-lookup"><span data-stu-id="aefce-168">Using Hardware-Drawing Capabilities</span></span>

-   [<span data-ttu-id="aefce-169">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="aefce-169">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="aefce-170">**ICDRAWBEGIN**</span><span class="sxs-lookup"><span data-stu-id="aefce-170">**ICDRAWBEGIN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [<span data-ttu-id="aefce-171">**\_final do desenho ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-171">**ICM\_DRAW\_END**</span></span>](icm-draw-end.md)
-   [<span data-ttu-id="aefce-172">**\_liberação de desenho ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-172">**ICM\_DRAW\_FLUSH**</span></span>](icm-draw-flush.md)
-   [<span data-ttu-id="aefce-173">**\_consulta de desenho ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-173">**ICM\_DRAW\_QUERY**</span></span>](icm-draw-query.md)
-   [<span data-ttu-id="aefce-174">**ICDrawSuggestFormat**</span><span class="sxs-lookup"><span data-stu-id="aefce-174">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="aefce-175">**\_início do desenho do ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-175">**ICM\_DRAW\_START**</span></span>](icm-draw-start.md)
-   [<span data-ttu-id="aefce-176">**\_parada de desenho de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-176">**ICM\_DRAW\_STOP**</span></span>](icm-draw-stop.md)
-   [<span data-ttu-id="aefce-177">**GETBUFFERSWANTED de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-177">**ICM\_GETBUFFERSWANTED**</span></span>](icm-getbufferswanted.md)
-   [<span data-ttu-id="aefce-178">**compreender o ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-178">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="aefce-179">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="aefce-179">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="aefce-180">**ICDRAW**</span><span class="sxs-lookup"><span data-stu-id="aefce-180">**ICDRAW**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [<span data-ttu-id="aefce-181">**\_extrair \_ getTime do ICM**</span><span class="sxs-lookup"><span data-stu-id="aefce-181">**ICM\_DRAW\_GETTIME**</span></span>](icm-draw-gettime.md)
-   [<span data-ttu-id="aefce-182">**ICM de \_ desenhar \_ setTime**</span><span class="sxs-lookup"><span data-stu-id="aefce-182">**ICM\_DRAW\_SETTIME**</span></span>](icm-draw-settime.md)
-   [<span data-ttu-id="aefce-183">**\_janela de desenho do ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-183">**ICM\_DRAW\_WINDOW**</span></span>](icm-draw-window.md)
-   [<span data-ttu-id="aefce-184">**compreender o ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-184">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="aefce-185">**\_CHANGEPALETTE desenhar de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-185">**ICM\_DRAW\_CHANGEPALETTE**</span></span>](icm-draw-changepalette.md)
-   [<span data-ttu-id="aefce-186">**\_RENDERBUFFER desenhar de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="aefce-186">**ICM\_DRAW\_RENDERBUFFER**</span></span>](icm-draw-renderbuffer.md)

## <a name="related-topics"></a><span data-ttu-id="aefce-187">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aefce-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aefce-188">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="aefce-188">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 




