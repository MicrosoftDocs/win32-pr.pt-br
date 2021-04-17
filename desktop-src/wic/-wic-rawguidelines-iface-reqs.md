---
description: Requisitos do método de interface
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Requisitos do método de interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749521"
---
# <a name="interface-method-requirements"></a><span data-ttu-id="68ca5-103">Requisitos do método de interface</span><span class="sxs-lookup"><span data-stu-id="68ca5-103">Interface Method Requirements</span></span>

<span data-ttu-id="68ca5-104">Nem todo método em cada interface deve ter uma implementação.</span><span class="sxs-lookup"><span data-stu-id="68ca5-104">Not every method on every interface must have an implementation.</span></span> <span data-ttu-id="68ca5-105">Por exemplo, alguns codecs têm metadados globais, miniaturas ou contextos de cores, enquanto outros codecs os fornecem apenas em uma base por quadro.</span><span class="sxs-lookup"><span data-stu-id="68ca5-105">For example, some codecs have global metadata, thumbnails, or color contexts, whereas other codecs provide these only on a per-frame basis.</span></span> <span data-ttu-id="68ca5-106">Se os autores de codec fornecerem esses somente por quadro, eles precisarão implementar apenas [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) ou ColorContexts, ou implementar os métodos [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) ou [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) em vez de em [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="68ca5-106">If codec authors provide these only on a per-frame basis, they need only implement the [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) or ColorContexts, or implement the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) or [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) rather than on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="68ca5-107">Da mesma forma, alguns codecs não usam formatos indexados e, portanto, não são necessários para implementar os métodos [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) e [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="68ca5-107">Likewise, some codecs do not use indexed formats and so are not required to implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) and [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) methods.</span></span> <span data-ttu-id="68ca5-108">Portanto, esses métodos são opcionais e são deixados para a critério do criador do codec.</span><span class="sxs-lookup"><span data-stu-id="68ca5-108">These methods are therefore optional and are left to the discretion of the codec creator.</span></span> <span data-ttu-id="68ca5-109">A maioria dos outros métodos são necessários.</span><span class="sxs-lookup"><span data-stu-id="68ca5-109">Most other methods are required.</span></span>

<span data-ttu-id="68ca5-110">Para o Windows 7, [**obtenha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) e [**obter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) são necessários e devem ser implementados nas classes de nível de contêiner ou nas classes de nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="68ca5-110">For Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)/[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) and [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) are required and must be implemented on either the contain-level classes or on the frame-level classes.</span></span> <span data-ttu-id="68ca5-111">Se o formato do arquivo de imagem não der suporte a visualizações ou miniaturas em qualquer um desses locais, você deverá revisar o formato do arquivo de imagem para fornecer esse suporte.</span><span class="sxs-lookup"><span data-stu-id="68ca5-111">If your image file format doesn't support previews or thumbnails in either of these locations, then you should revise your image file format to provide such support.</span></span>

<span data-ttu-id="68ca5-112">Quando um método não é implementado, é importante retornar um erro apropriado para que o chamador possa determinar que o recurso solicitado não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="68ca5-112">When a method is not implemented, it is important to return an appropriate error so the caller can determine that the requested feature is not supported.</span></span> <span data-ttu-id="68ca5-113">Por exemplo, se os autores de codec não oferecerem suporte a miniaturas de nível de contêiner, eles deverão retornar [WINCODEC \_ Err \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) quando um aplicativo chamar [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)e, se eles não tiverem uma paleta, deverão retornar [WINCODEC \_ Err \_ PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="68ca5-113">For example, if codec authors do not support container-level thumbnails, they should return [WINCODEC\_ERR\_CODECNOTHUMBNAIL](-wic-codec-error-codes.md) when an application calls [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), and if they don't have a palette, they should return [WINCODEC\_ERR\_PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span></span> <span data-ttu-id="68ca5-114">Se não existir nenhum código de [ \_ erro WINCODEC](-wic-codec-error-codes.md) adequado, o codec deverá retornar E \_ NOTIMPL para métodos não implementados.</span><span class="sxs-lookup"><span data-stu-id="68ca5-114">If no suitable [WINCODEC\_ERR](-wic-codec-error-codes.md) code exists, then the codec should return E\_NOTIMPL for unimplemented methods.</span></span>

<span data-ttu-id="68ca5-115">As tabelas a seguir listam os métodos obrigatórios e opcionais para cada interface do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="68ca5-115">The following tables list the required and optional methods for each Windows Imaging Component (WIC) interfaces.</span></span>

[<span data-ttu-id="68ca5-116">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="68ca5-116">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



<span data-ttu-id="68ca5-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68ca5-117">Required</span></span>

[<span data-ttu-id="68ca5-118">**QueryCapability**</span><span class="sxs-lookup"><span data-stu-id="68ca5-118">**QueryCapability**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[<span data-ttu-id="68ca5-119">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="68ca5-119">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[<span data-ttu-id="68ca5-120">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="68ca5-120">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[<span data-ttu-id="68ca5-121">**GetDecoderInfo**</span><span class="sxs-lookup"><span data-stu-id="68ca5-121">**GetDecoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[<span data-ttu-id="68ca5-122">**GetFrameCount**</span><span class="sxs-lookup"><span data-stu-id="68ca5-122">**GetFrameCount**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[<span data-ttu-id="68ca5-123">**GetFrame**</span><span class="sxs-lookup"><span data-stu-id="68ca5-123">**GetFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

<span data-ttu-id="68ca5-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="68ca5-124">Optional</span></span>

<span data-ttu-id="68ca5-125">¹ [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)</span><span class="sxs-lookup"><span data-stu-id="68ca5-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span></span>

<span data-ttu-id="68ca5-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="68ca5-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span></span>

[<span data-ttu-id="68ca5-127">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="68ca5-127">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[<span data-ttu-id="68ca5-128">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="68ca5-128">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[<span data-ttu-id="68ca5-129">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="68ca5-129">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="68ca5-130">¹ necessário se o formato de arquivo de imagem oferecer suporte a visualizações em nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="68ca5-130">¹Required if your image file format supports container-level previews.</span></span> <span data-ttu-id="68ca5-131">Se esse não for o caso, você é altamente incentivado a revisar o formato de arquivo de imagem para dar suporte a isso.</span><span class="sxs-lookup"><span data-stu-id="68ca5-131">If this is not the case you are strongly encouraged to revise your image file format to support this.</span></span> <span data-ttu-id="68ca5-132">Se implementado aqui, um [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) correspondente será necessário na classe de codificação no nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="68ca5-132">If implemented here, then a corresponding [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is required on the container-level encode class.</span></span>

<span data-ttu-id="68ca5-133">² necessário aqui ou na classe de decodificação de nível de quadro, dependendo de onde o formato de arquivo de imagem armazena miniaturas.</span><span class="sxs-lookup"><span data-stu-id="68ca5-133">²Required either here, or on the frame-level decode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="68ca5-134">Se for implementado aqui, um [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) correspondente será necessário na classe de codificação no nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="68ca5-134">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) is required on the container-level encode class.</span></span>

[<span data-ttu-id="68ca5-135">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="68ca5-135">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



<span data-ttu-id="68ca5-136">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68ca5-136">Required</span></span>

[<span data-ttu-id="68ca5-137">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="68ca5-137">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[<span data-ttu-id="68ca5-138">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="68ca5-138">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[<span data-ttu-id="68ca5-139">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="68ca5-139">**GetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[<span data-ttu-id="68ca5-140">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="68ca5-140">**GetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[<span data-ttu-id="68ca5-141">**Resolution**</span><span class="sxs-lookup"><span data-stu-id="68ca5-141">**GetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[<span data-ttu-id="68ca5-142">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="68ca5-142">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

<span data-ttu-id="68ca5-143">Opcional</span><span class="sxs-lookup"><span data-stu-id="68ca5-143">Optional</span></span>

<span data-ttu-id="68ca5-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="68ca5-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span></span>

[<span data-ttu-id="68ca5-145">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="68ca5-145">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="68ca5-146">¹ precisou aqui ou na classe de decodificação de nível de contêiner, dependendo de onde o formato de arquivo de imagem armazena miniaturas.</span><span class="sxs-lookup"><span data-stu-id="68ca5-146">¹Required either here, or on the container-level decode class, depending on where you image file format stores thumbnails.</span></span> <span data-ttu-id="68ca5-147">Se for implementado aqui, um [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) correspondente será necessário na classe de codificador de nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="68ca5-147">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is required on the frame-level encoder class.</span></span>

[<span data-ttu-id="68ca5-148">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="68ca5-148">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="68ca5-149">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68ca5-149">Required</span></span>

[<span data-ttu-id="68ca5-150">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="68ca5-150">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[<span data-ttu-id="68ca5-151">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="68ca5-151">**GetCount**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[<span data-ttu-id="68ca5-152">**GetReaderByIndex**</span><span class="sxs-lookup"><span data-stu-id="68ca5-152">**GetReaderByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[<span data-ttu-id="68ca5-153">**GetEnumerator**</span><span class="sxs-lookup"><span data-stu-id="68ca5-153">**GetEnumerator**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[<span data-ttu-id="68ca5-154">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="68ca5-154">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



<span data-ttu-id="68ca5-155">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68ca5-155">Required</span></span>

[<span data-ttu-id="68ca5-156">**DoesSupportTransform**</span><span class="sxs-lookup"><span data-stu-id="68ca5-156">**DoesSupportTransform**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[<span data-ttu-id="68ca5-157">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="68ca5-157">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

<span data-ttu-id="68ca5-158">Opcional</span><span class="sxs-lookup"><span data-stu-id="68ca5-158">Optional</span></span>

[<span data-ttu-id="68ca5-159">**GetClosestSize**</span><span class="sxs-lookup"><span data-stu-id="68ca5-159">**GetClosestSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[<span data-ttu-id="68ca5-160">**GetClosestPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="68ca5-160">**GetClosestPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[<span data-ttu-id="68ca5-161">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="68ca5-161">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

<span data-ttu-id="68ca5-162">Consulte [suporte para IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), mais adiante neste documento.</span><span class="sxs-lookup"><span data-stu-id="68ca5-162">See [Support for IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), later in this document.</span></span>

[<span data-ttu-id="68ca5-163">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="68ca5-163">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



<span data-ttu-id="68ca5-164">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68ca5-164">Required</span></span>

[<span data-ttu-id="68ca5-165">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="68ca5-165">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="68ca5-166">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="68ca5-166">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[<span data-ttu-id="68ca5-167">**GetEncoderInfo**</span><span class="sxs-lookup"><span data-stu-id="68ca5-167">**GetEncoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[<span data-ttu-id="68ca5-168">**CreateNewFrame**</span><span class="sxs-lookup"><span data-stu-id="68ca5-168">**CreateNewFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[<span data-ttu-id="68ca5-169">**Compromisso**</span><span class="sxs-lookup"><span data-stu-id="68ca5-169">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="68ca5-170">Opcional</span><span class="sxs-lookup"><span data-stu-id="68ca5-170">Optional</span></span>

<span data-ttu-id="68ca5-171">¹ de [**Visualização**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)</span><span class="sxs-lookup"><span data-stu-id="68ca5-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span></span>

<span data-ttu-id="68ca5-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="68ca5-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span></span>

[<span data-ttu-id="68ca5-173">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="68ca5-173">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[<span data-ttu-id="68ca5-174">**GetMetadataQueryWriter**</span><span class="sxs-lookup"><span data-stu-id="68ca5-174">**GetMetadataQueryWriter**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[<span data-ttu-id="68ca5-175">**SetPalette**</span><span class="sxs-lookup"><span data-stu-id="68ca5-175">**SetPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

<span data-ttu-id="68ca5-176">¹ necessário se o formato de arquivo de imagem der suporte a visualizações em nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="68ca5-176">¹Required if your image file format supports frame-level previews.</span></span>

<span data-ttu-id="68ca5-177">² necessário aqui ou na classe de codificação no nível do quadro, dependendo de onde o formato do arquivo de imagem armazena miniaturas.</span><span class="sxs-lookup"><span data-stu-id="68ca5-177">²Required either here, or on the frame-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="68ca5-178">Se for implementado aqui, um [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) correspondente será necessário na classe de decodificação de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="68ca5-178">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) is required on the container-level decode class.</span></span>

[<span data-ttu-id="68ca5-179">**IWICBitmapFrameEncode**</span><span class="sxs-lookup"><span data-stu-id="68ca5-179">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



<span data-ttu-id="68ca5-180">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68ca5-180">Required</span></span>

[<span data-ttu-id="68ca5-181">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="68ca5-181">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="68ca5-182">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="68ca5-182">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="68ca5-183">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="68ca5-183">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="68ca5-184">**Size**</span><span class="sxs-lookup"><span data-stu-id="68ca5-184">**SetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[<span data-ttu-id="68ca5-185">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="68ca5-185">**SetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[<span data-ttu-id="68ca5-186">**Resolution**</span><span class="sxs-lookup"><span data-stu-id="68ca5-186">**SetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[<span data-ttu-id="68ca5-187">**WritePixels**</span><span class="sxs-lookup"><span data-stu-id="68ca5-187">**WritePixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[<span data-ttu-id="68ca5-188">**Gravação**</span><span class="sxs-lookup"><span data-stu-id="68ca5-188">**WriteSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[<span data-ttu-id="68ca5-189">**Compromisso**</span><span class="sxs-lookup"><span data-stu-id="68ca5-189">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="68ca5-190">Opcional</span><span class="sxs-lookup"><span data-stu-id="68ca5-190">Optional</span></span>

<span data-ttu-id="68ca5-191">¹ [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)</span><span class="sxs-lookup"><span data-stu-id="68ca5-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span></span>

[<span data-ttu-id="68ca5-192">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="68ca5-192">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

<span data-ttu-id="68ca5-193">¹ precisou aqui ou na classe de codificação no nível do contêiner, dependendo de onde o formato do arquivo de imagem armazena miniaturas.</span><span class="sxs-lookup"><span data-stu-id="68ca5-193">¹Required either here, or on the container-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="68ca5-194">Se for implementado aqui, um [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) correspondente será necessário na classe de decodificação no nível do quadro.</span><span class="sxs-lookup"><span data-stu-id="68ca5-194">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) is required on the frame-level decode class.</span></span>

[<span data-ttu-id="68ca5-195">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="68ca5-195">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="68ca5-196">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68ca5-196">Required</span></span>

[<span data-ttu-id="68ca5-197">**InitializeFromBlockReader**</span><span class="sxs-lookup"><span data-stu-id="68ca5-197">**InitializeFromBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[<span data-ttu-id="68ca5-198">**AddWriter**</span><span class="sxs-lookup"><span data-stu-id="68ca5-198">**AddWriter**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[<span data-ttu-id="68ca5-199">**GetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="68ca5-199">**GetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[<span data-ttu-id="68ca5-200">**SetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="68ca5-200">**SetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[<span data-ttu-id="68ca5-201">**RemoveWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="68ca5-201">**RemoveWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a><span data-ttu-id="68ca5-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68ca5-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="68ca5-203">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="68ca5-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68ca5-204">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="68ca5-204">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="68ca5-205">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="68ca5-205">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="68ca5-206">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="68ca5-206">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
