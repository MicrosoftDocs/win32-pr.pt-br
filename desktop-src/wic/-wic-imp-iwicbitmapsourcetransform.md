---
description: Implementando IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementando IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297086"
---
# <a name="implementing-iwicbitmapsourcetransform"></a><span data-ttu-id="3e312-103">Implementando IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="3e312-103">Implementing IWICBitmapSourceTransform</span></span>

## <a name="iwicbitmapsourcetransform"></a><span data-ttu-id="3e312-104">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="3e312-104">IWICBitmapSourceTransform</span></span>

<span data-ttu-id="3e312-105">Embora opcional, é altamente recomendável que cada decodificador Implemente essa interface em sua classe de decodificação de nível de quadro, pois pode fornecer grandes benefícios de desempenho.</span><span class="sxs-lookup"><span data-stu-id="3e312-105">Though optional, we highly recommend that every decoder implement this interface on your frame-level decoding class, because it can provide major performance benefits.</span></span> <span data-ttu-id="3e312-106">Quando um aplicativo solicita uma região específica de interesse, tamanho, orientação ou formato de pixel, em vez de apenas decodificar a imagem inteira em resolução completa e, em seguida, aplicar as transformações solicitadas, o Windows Imaging Component (WIC) chama [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para essa interface no objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="3e312-106">When an application requests a specific region of interest, size, orientation, or pixel format, instead of just decoding the whole image at full resolution and then applying the requested transforms, Windows Imaging Component (WIC) calls [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for this interface on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span> <span data-ttu-id="3e312-107">Se o decodificador de quadro oferecer suporte a ele, o WIC chamará o método ou métodos apropriados para determinar se o decodificador de quadro pode executar a transformação solicitada ou determinar o tamanho ou o formato de pixel mais próximo que o decodificador pode fornecer para o solicitado.</span><span class="sxs-lookup"><span data-stu-id="3e312-107">If the frame decoder supports it, WIC calls the appropriate method or methods to determine whether the frame decoder can perform the requested transform or determine the closest size or pixel format the decoder can provide to the one requested.</span></span> <span data-ttu-id="3e312-108">Se o decodificador puder executar a transformação ou transformações solicitadas, o WIC invocará [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) com os parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="3e312-108">If the decoder can perform the requested transform or transforms, WIC invokes [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the appropriate parameters.</span></span> <span data-ttu-id="3e312-109">Se o decodificador puder executar algumas, mas não todas as transformações solicitadas, o WIC solicitará que o decodificador execute os que ele pode e use os objetos de transformação do WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) para executar as transformações restantes que não puderam ser executadas pelo decodificador de quadro no resultado da chamada **CopyPixels** .</span><span class="sxs-lookup"><span data-stu-id="3e312-109">If the decoder can perform some, but not all of the requested transforms, WIC asks the decoder to perform those that it can, and uses the WIC transform objects ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) to perform the remaining transforms that could not be performed by the frame decoder on the result of the **CopyPixels** call.</span></span> <span data-ttu-id="3e312-110">Se o decodificador não oferecer suporte a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), o WIC deverá usar os objetos de transformação para executar todas as transformações.</span><span class="sxs-lookup"><span data-stu-id="3e312-110">If the decoder doesn’t support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), then WIC must use the transform objects to perform all of the transforms.</span></span> <span data-ttu-id="3e312-111">Normalmente, é muito mais eficiente para o decodificador executar transformações durante o processo de decodificação do que decodificar a imagem inteira e, em seguida, executar as transformações.</span><span class="sxs-lookup"><span data-stu-id="3e312-111">It’s usually much more efficient for the decoder to perform transforms during the decoding process than it is to decode the entire image and then perform the transforms.</span></span> <span data-ttu-id="3e312-112">Isso é especialmente verdadeiro para operações como dimensionar para um tamanho muito menor ou conversões de formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="3e312-112">This is especially true for operations such as scaling to a much smaller size or pixel format conversions.</span></span>


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [<span data-ttu-id="3e312-113">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="3e312-113">DoesSupportTransform</span></span>](#doessupporttransform)
-   [<span data-ttu-id="3e312-114">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="3e312-114">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="3e312-115">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="3e312-115">GetClosestSize</span></span>](#getclosestsize)
-   [<span data-ttu-id="3e312-116">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="3e312-116">GetClosestPixelFormat</span></span>](#getclosestpixelformat)

### <a name="doessupporttransform"></a><span data-ttu-id="3e312-117">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="3e312-117">DoesSupportTransform</span></span>

<span data-ttu-id="3e312-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) pergunta se o decodificador dá suporte à operação de rotação ou inversão solicitada.</span><span class="sxs-lookup"><span data-stu-id="3e312-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) asks whether the decoder supports the requested rotation or flipping operation.</span></span> <span data-ttu-id="3e312-119">Os [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) que podem ser solicitados são:</span><span class="sxs-lookup"><span data-stu-id="3e312-119">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) that may be requested are:</span></span>


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a><span data-ttu-id="3e312-120">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="3e312-120">CopyPixels</span></span>

<span data-ttu-id="3e312-121">O [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) executa o trabalho real de decodificação dos bits de imagem, como o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) na interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , mas o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) em [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) é muito mais poderoso e pode melhorar significativamente o desempenho do processamento de imagens.</span><span class="sxs-lookup"><span data-stu-id="3e312-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) performs the actual work of decoding the image bits, such as the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, but the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method on [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is much more powerful, and can improve image processing performance significantly.</span></span>

<span data-ttu-id="3e312-122">Quando várias operações de transformação são solicitadas, o resultado depende da ordem em que as operações são executadas.</span><span class="sxs-lookup"><span data-stu-id="3e312-122">When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.</span></span> <span data-ttu-id="3e312-123">Para garantir a previsibilidade e a consistência entre codecs, é importante que todos os codecs executem essas operações na mesma ordem.</span><span class="sxs-lookup"><span data-stu-id="3e312-123">To ensure predictability and consistency across codecs, it’s important that all codecs perform these operations in the same order.</span></span> <span data-ttu-id="3e312-124">Essa é a ordem canônica para executar essas operações.</span><span class="sxs-lookup"><span data-stu-id="3e312-124">This is the canonical order for performing these operations.</span></span>

1.  <span data-ttu-id="3e312-125">Escala</span><span class="sxs-lookup"><span data-stu-id="3e312-125">Scale</span></span>
2.  <span data-ttu-id="3e312-126">Crop</span><span class="sxs-lookup"><span data-stu-id="3e312-126">Crop</span></span>
3.  <span data-ttu-id="3e312-127">Rotate</span><span class="sxs-lookup"><span data-stu-id="3e312-127">Rotate</span></span>

<span data-ttu-id="3e312-128">A conversão de formato de pixel pode ser executada a qualquer momento, porque ela não tem nenhum efeito nas outras transformações.</span><span class="sxs-lookup"><span data-stu-id="3e312-128">Pixel format conversion can be performed at any time, because it has no effect on the other transforms.</span></span>

<span data-ttu-id="3e312-129">O primeiro parâmetro, *prcSrc*, é usado para especificar a região de interesse para recortar a imagem.</span><span class="sxs-lookup"><span data-stu-id="3e312-129">The first parameter, *prcSrc*, is used to specify the region of interest for clipping the image.</span></span> <span data-ttu-id="3e312-130">Como o dimensionamento é executado antes do recorte por convenção, se a imagem for dimensionada e recortada, a região de interesse deverá ser determinada depois que a imagem for dimensionada.</span><span class="sxs-lookup"><span data-stu-id="3e312-130">Because scaling is performed before clipping by convention, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.</span></span>

<span data-ttu-id="3e312-131">O segundo e o terceiro parâmetros indicam o tamanho para o qual dimensionar a imagem.</span><span class="sxs-lookup"><span data-stu-id="3e312-131">The second and third parameters indicate the size to which to scale the image.</span></span>

<span data-ttu-id="3e312-132">O parâmetro *pguidDstFormat* indica o formato de pixel solicitado para a imagem decodificada.</span><span class="sxs-lookup"><span data-stu-id="3e312-132">The *pguidDstFormat* parameter indicates the requested pixel format for the decoded image.</span></span> <span data-ttu-id="3e312-133">Como o WIC já chamou [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), ele deve ser um formato de pixel que o decodificador indicou que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="3e312-133">Because WIC has already called [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), this should be a pixel format that the decoder has indicated that it supports.</span></span>

<span data-ttu-id="3e312-134">O parâmetro *dstTransform* indica o ângulo de rotação solicitado e se deve virar a imagem verticalmente, horizontalmente ou ambas.</span><span class="sxs-lookup"><span data-stu-id="3e312-134">The *dstTransform* parameter indicates the requested rotation angle, and whether to flip the image vertically, horizontally, or both.</span></span> <span data-ttu-id="3e312-135">Novamente, como o WIC já terá chamado [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), a transformação solicitada deve ser aquela que o decodificador já indicou que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="3e312-135">Again, because WIC will have already called [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), the requested transform should be one that the decoder has already indicated that it supports.</span></span> <span data-ttu-id="3e312-136">Lembre-se de que a rotação sempre deve ser executada após o dimensionamento e o recorte.</span><span class="sxs-lookup"><span data-stu-id="3e312-136">Remember that rotation should always be performed after scaling and clipping.</span></span>

### <a name="getclosestsize"></a><span data-ttu-id="3e312-137">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="3e312-137">GetClosestSize</span></span>

<span data-ttu-id="3e312-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) usa dois parâmetros de entrada/saída.</span><span class="sxs-lookup"><span data-stu-id="3e312-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) takes two in/out parameters.</span></span> <span data-ttu-id="3e312-139">O chamador usa os parâmetros *puiWidth* e *puiHeight* para especificar o tamanho no qual o chamador prefere a imagem a ser decodificada.</span><span class="sxs-lookup"><span data-stu-id="3e312-139">The caller uses the *puiWidth* and *puiHeight* parameters to specify the size at which that the caller prefers the image to be decoded.</span></span> <span data-ttu-id="3e312-140">No entanto, um decodificador pode decodificar uma imagem apenas para um tamanho que seja um múltiplo de seu tamanho de DCT, e diferentes formatos de imagem podem ter tamanhos de DCT diferentes.</span><span class="sxs-lookup"><span data-stu-id="3e312-140">However, a decoder can decode an image only to a size that’s a multiple of its DCT size, and different image formats can have different DCT sizes.</span></span> <span data-ttu-id="3e312-141">O decodificador deve determinar, com base em seu próprio tamanho de DCT, o mais próximo que pode chegar ao tamanho solicitado e definir o *puiWidth* e *puiHeight* para essas dimensões no retorno.</span><span class="sxs-lookup"><span data-stu-id="3e312-141">The decoder should determine, based on its own DCT size, the closest it can come to the requested size, and set the *puiWidth* and *puiHeight* to those dimensions on return.</span></span> <span data-ttu-id="3e312-142">Se um tamanho maior for solicitado, mas o codec não der suporte ao upsizing, o original deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="3e312-142">If a larger size is requested, but the codec doesn’t support upscaling, the original should be returned.</span></span>

### <a name="getclosestpixelformat"></a><span data-ttu-id="3e312-143">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="3e312-143">GetClosestPixelFormat</span></span>

<span data-ttu-id="3e312-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) é usado para determinar o formato de pixel mais próximo ao formato de pixel solicitado que o decodificador pode fornecer sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="3e312-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) is used to determine the closest pixel format to the requested pixel format that the decoder can provide without loss of data.</span></span> <span data-ttu-id="3e312-145">É sempre preferível converter para um formato de pixel mais largo do que um mais estreito, mesmo que ele aumente o tamanho da imagem, pois ela sempre poderá ser reconverteda para um formato mais restritivo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="3e312-145">It’s always preferable to convert to a wider pixel format than a narrower one, even though it will increase the size of the image, because it can always be reconverted to a more restrictive format if necessary.</span></span> <span data-ttu-id="3e312-146">No entanto, depois que os dados forem perdidos, eles não poderão ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="3e312-146">However, after the data is lost, it can’t be recovered.</span></span>

## <a name="continued-reading"></a><span data-ttu-id="3e312-147">Leitura continuada</span><span class="sxs-lookup"><span data-stu-id="3e312-147">Continued Reading</span></span>

<span data-ttu-id="3e312-148">Para saber mais sobre como criar um codec habilitado para WIC, consulte [implementando IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span><span class="sxs-lookup"><span data-stu-id="3e312-148">To learn more about how to create a WIC-enabled codec, see [Implementing IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e312-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e312-149">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3e312-150">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3e312-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e312-151">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="3e312-151">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[<span data-ttu-id="3e312-152">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="3e312-152">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="3e312-153">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="3e312-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e312-154">Implementando o IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="3e312-154">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="3e312-155">Implementando IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="3e312-155">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="3e312-156">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="3e312-156">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="3e312-157">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="3e312-157">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
