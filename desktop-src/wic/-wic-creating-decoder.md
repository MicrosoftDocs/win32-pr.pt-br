---
description: O tópico apresenta o decodificador de bitmap, um componente de codec principal do Windows Imaging Component (WIC) usado para decodificar arquivos de imagem de um fluxo.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Visão geral da decodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297623"
---
# <a name="decoding-overview"></a><span data-ttu-id="6d12a-103">Visão geral da decodificação</span><span class="sxs-lookup"><span data-stu-id="6d12a-103">Decoding Overview</span></span>

<span data-ttu-id="6d12a-104">O tópico apresenta o decodificador de bitmap, um componente de codec principal do Windows Imaging Component (WIC) usado para decodificar arquivos de imagem de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="6d12a-104">The topic introduces the bitmap decoder, a core Windows Imaging Component (WIC) codec component used to decode image files from a stream.</span></span>

<span data-ttu-id="6d12a-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d12a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6d12a-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="6d12a-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="6d12a-107">Decodificadores de bitmap nativos</span><span class="sxs-lookup"><span data-stu-id="6d12a-107">Native Bitmap Decoders</span></span>](#native-bitmap-decoders)
-   [<span data-ttu-id="6d12a-108">Criando um decodificador de bitmap</span><span class="sxs-lookup"><span data-stu-id="6d12a-108">Creating a Bitmap Decoder</span></span>](#creating-a-bitmap-decoder)
-   [<span data-ttu-id="6d12a-109">Extensibilidade do decodificador</span><span class="sxs-lookup"><span data-stu-id="6d12a-109">Decoder Extensibility</span></span>](#decoder-extensibility)
-   [<span data-ttu-id="6d12a-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d12a-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="6d12a-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="6d12a-111">Introduction</span></span>

<span data-ttu-id="6d12a-112">Os decodificadores de bitmap podem ser exibidos como o contêiner externo de uma imagem digital e fornecem acesso a propriedades globais e quadros de imagem.</span><span class="sxs-lookup"><span data-stu-id="6d12a-112">Bitmap decoders can be viewed as the outer container of a digital image and provides access to global properties and image frames.</span></span> <span data-ttu-id="6d12a-113">Alguns formatos de imagem dão suporte a miniaturas globais, visualizações, contextos de cor ou metadados, enquanto outros fornecem essas propriedades somente no nível do quadro.</span><span class="sxs-lookup"><span data-stu-id="6d12a-113">Some image formats support global thumbnails, previews, color contexts, or metadata, while others provide these properties only at the frame level.</span></span> <span data-ttu-id="6d12a-114">No entanto, observe que muitos dos formatos de imagem padrão não dão suporte a essas propriedades globais.</span><span class="sxs-lookup"><span data-stu-id="6d12a-114">Note, however, many of the standard image formats do not support these global properties.</span></span> <span data-ttu-id="6d12a-115">Assim, muitas das implementações de codecs nativos fornecidas pelo WIC não dão suporte à maioria dessas propriedades globais.</span><span class="sxs-lookup"><span data-stu-id="6d12a-115">As such, many of the native codec implementations provided by WIC do not support the majority of these global properties.</span></span> <span data-ttu-id="6d12a-116">Consulte a tabela na seção decodificadores de bitmap nativos deste tópico para obter informações sobre o suporte a propriedades globais.</span><span class="sxs-lookup"><span data-stu-id="6d12a-116">See the table in the Native Bitmap Decoders section of this topic for information about global property support.</span></span>

<span data-ttu-id="6d12a-117">No WIC, os decodificadores de bitmap são representados pela interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e fornecem acesso a essas propriedades globais do bitmap e, mais importante, aos quadros que ele contém.</span><span class="sxs-lookup"><span data-stu-id="6d12a-117">In WIC, bitmap decoders are represented by the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and provides access to these global properties of the bitmap and, more importantly, the frames it contains.</span></span> <span data-ttu-id="6d12a-118">A interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) representa um quadro de bitmap individual e é discutida em detalhes na [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="6d12a-118">The [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface represents an individual bitmap frame and is discussed in detail in the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="native-bitmap-decoders"></a><span data-ttu-id="6d12a-119">Decodificadores de bitmap nativos</span><span class="sxs-lookup"><span data-stu-id="6d12a-119">Native Bitmap Decoders</span></span>

<span data-ttu-id="6d12a-120">O WIC fornece várias implementações nativas da interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para os formatos de imagem da Web padrão e o formato de foto HD de alto alcance dinâmico.</span><span class="sxs-lookup"><span data-stu-id="6d12a-120">WIC provides several native implementations of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface for the standard web image formats and the high dynamic range HD Photo format.</span></span> <span data-ttu-id="6d12a-121">A tabela a seguir lista os decodificadores nativos disponíveis, o nome do identificador de classe e o suporte para propriedades globais.</span><span class="sxs-lookup"><span data-stu-id="6d12a-121">The following table lists the available native decoders, class identifier name, and support for global properties.</span></span> <span data-ttu-id="6d12a-122">Embora um recurso possa não dar suporte a uma propriedade como miniaturas no nível global, o formato da imagem pode dar suporte a essas propriedades no nível de quadro individual.</span><span class="sxs-lookup"><span data-stu-id="6d12a-122">Though a feature may not support a property such as thumbnails at the global level, the image format may support such properties at the individual frame level.</span></span>



| <span data-ttu-id="6d12a-123">Formato de imagem</span><span class="sxs-lookup"><span data-stu-id="6d12a-123">Image Format</span></span> | <span data-ttu-id="6d12a-124">Nome do CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-124">CLSID Name</span></span>            | <span data-ttu-id="6d12a-125">Miniaturas</span><span class="sxs-lookup"><span data-stu-id="6d12a-125">Thumbnails</span></span> | <span data-ttu-id="6d12a-126">Visualizações</span><span class="sxs-lookup"><span data-stu-id="6d12a-126">Previews</span></span> | <span data-ttu-id="6d12a-127">Contextos de cor</span><span class="sxs-lookup"><span data-stu-id="6d12a-127">Color Contexts</span></span> | <span data-ttu-id="6d12a-128">Metadados</span><span class="sxs-lookup"><span data-stu-id="6d12a-128">Metadata</span></span> |
|--------------|-----------------------|------------|----------|----------------|----------|
| <span data-ttu-id="6d12a-129">BMP</span><span class="sxs-lookup"><span data-stu-id="6d12a-129">BMP</span></span>          | <span data-ttu-id="6d12a-130">\_WICBMPDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-130">CLSID\_WICBmpDecoder</span></span>  | <span data-ttu-id="6d12a-131">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-131">No</span></span>         | <span data-ttu-id="6d12a-132">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-132">No</span></span>       | <span data-ttu-id="6d12a-133">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-133">No</span></span>             | <span data-ttu-id="6d12a-134">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-134">No</span></span>       |
| <span data-ttu-id="6d12a-135">GIF</span><span class="sxs-lookup"><span data-stu-id="6d12a-135">GIF</span></span>          | <span data-ttu-id="6d12a-136">\_WICGIFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-136">CLSID\_WICGifDecoder</span></span>  | <span data-ttu-id="6d12a-137">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-137">No</span></span>         | <span data-ttu-id="6d12a-138">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-138">No</span></span>       | <span data-ttu-id="6d12a-139">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-139">No</span></span>             | <span data-ttu-id="6d12a-140">Sim</span><span class="sxs-lookup"><span data-stu-id="6d12a-140">Yes</span></span>      |
| <span data-ttu-id="6d12a-141">ICO</span><span class="sxs-lookup"><span data-stu-id="6d12a-141">ICO</span></span>          | <span data-ttu-id="6d12a-142">\_WICICODECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-142">CLSID\_WICIcoDecoder</span></span>  | <span data-ttu-id="6d12a-143">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-143">No</span></span>         | <span data-ttu-id="6d12a-144">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-144">No</span></span>       | <span data-ttu-id="6d12a-145">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-145">No</span></span>             | <span data-ttu-id="6d12a-146">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-146">No</span></span>       |
| <span data-ttu-id="6d12a-147">JPEG</span><span class="sxs-lookup"><span data-stu-id="6d12a-147">JPEG</span></span>         | <span data-ttu-id="6d12a-148">\_WICJPEGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-148">CLSID\_WICJpegDecoder</span></span> | <span data-ttu-id="6d12a-149">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-149">No</span></span>         | <span data-ttu-id="6d12a-150">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-150">No</span></span>       | <span data-ttu-id="6d12a-151">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-151">No</span></span>             | <span data-ttu-id="6d12a-152">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-152">No</span></span>       |
| <span data-ttu-id="6d12a-153">PNG</span><span class="sxs-lookup"><span data-stu-id="6d12a-153">PNG</span></span>          | <span data-ttu-id="6d12a-154">\_WICPNGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-154">CLSID\_WICPngDecoder</span></span>  | <span data-ttu-id="6d12a-155">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-155">No</span></span>         | <span data-ttu-id="6d12a-156">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-156">No</span></span>       | <span data-ttu-id="6d12a-157">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-157">No</span></span>             | <span data-ttu-id="6d12a-158">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-158">No</span></span>       |
| <span data-ttu-id="6d12a-159">TIFF</span><span class="sxs-lookup"><span data-stu-id="6d12a-159">TIFF</span></span>         | <span data-ttu-id="6d12a-160">\_WICTIFFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-160">CLSID\_WICTiffDecoder</span></span> | <span data-ttu-id="6d12a-161">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-161">No</span></span>         | <span data-ttu-id="6d12a-162">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-162">No</span></span>       | <span data-ttu-id="6d12a-163">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-163">No</span></span>             | <span data-ttu-id="6d12a-164">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-164">No</span></span>       |
| <span data-ttu-id="6d12a-165">Foto de HD</span><span class="sxs-lookup"><span data-stu-id="6d12a-165">HD Photo</span></span>     | <span data-ttu-id="6d12a-166">\_WICWMPDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="6d12a-166">CLSID\_WICWmpDecoder</span></span>  | <span data-ttu-id="6d12a-167">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-167">No</span></span>         | <span data-ttu-id="6d12a-168">Sim</span><span class="sxs-lookup"><span data-stu-id="6d12a-168">Yes</span></span>      | <span data-ttu-id="6d12a-169">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-169">No</span></span>             | <span data-ttu-id="6d12a-170">Não</span><span class="sxs-lookup"><span data-stu-id="6d12a-170">No</span></span>       |



 

## <a name="creating-a-bitmap-decoder"></a><span data-ttu-id="6d12a-171">Criando um decodificador de bitmap</span><span class="sxs-lookup"><span data-stu-id="6d12a-171">Creating a Bitmap Decoder</span></span>

<span data-ttu-id="6d12a-172">Para decodificar uma imagem usando o WIC, primeiro você precisa criar uma instância de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para o formato de imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="6d12a-172">To decode an image using WIC, you first need to create an instance of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) for the targeted image format.</span></span> <span data-ttu-id="6d12a-173">A instância do decodificador permite que você acesse as propriedades globais e os metadados, se houver suporte, bem como os quadros de imagem.</span><span class="sxs-lookup"><span data-stu-id="6d12a-173">The decoder instance enables you to access the global properties and metadata, if supported, as well as the image frames.</span></span> <span data-ttu-id="6d12a-174">O WIC Imaging Factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), fornece vários métodos para criar decodificadores de bitmap.</span><span class="sxs-lookup"><span data-stu-id="6d12a-174">The WIC imaging factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), provides several methods for creating bitmap decoders.</span></span> <span data-ttu-id="6d12a-175">Os métodos de fábrica a seguir são fornecidos para criar decodificadores de bitmap.</span><span class="sxs-lookup"><span data-stu-id="6d12a-175">The following factory methods are provided to create bitmap decoders.</span></span>

-   [<span data-ttu-id="6d12a-176">**CreateDecoder**</span><span class="sxs-lookup"><span data-stu-id="6d12a-176">**CreateDecoder**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [<span data-ttu-id="6d12a-177">**CreateDecoderFromFileHandle**</span><span class="sxs-lookup"><span data-stu-id="6d12a-177">**CreateDecoderFromFileHandle**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [<span data-ttu-id="6d12a-178">**CreateDecoderFromFilename**</span><span class="sxs-lookup"><span data-stu-id="6d12a-178">**CreateDecoderFromFilename**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [<span data-ttu-id="6d12a-179">**CreateDecoderFromStream**</span><span class="sxs-lookup"><span data-stu-id="6d12a-179">**CreateDecoderFromStream**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

<span data-ttu-id="6d12a-180">O código a seguir demonstra como criar um decodificador de bitmap usando um nome de arquivo de imagem e recuperar o primeiro quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="6d12a-180">The following code demonstrates the how to create a bitmap decoder using an image filename and retrieve the first frame of the image.</span></span>


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a><span data-ttu-id="6d12a-181">Extensibilidade do decodificador</span><span class="sxs-lookup"><span data-stu-id="6d12a-181">Decoder Extensibility</span></span>

<span data-ttu-id="6d12a-182">Um dos principais recursos do WIC é uma estrutura de extensibilidade que permite que os desenvolvedores de codecs desenvolvam seus próprios codecs de imagem e obtenham o mesmo suporte de plataforma que as implementações nativas de codecs de imagem.</span><span class="sxs-lookup"><span data-stu-id="6d12a-182">One of the core features of WIC is an extensibility framework that enables codec developers to develop their own image codecs and get the same platform support as the native implementations of image codecs.</span></span> <span data-ttu-id="6d12a-183">Um único conjunto consistente de interfaces é usado para todo o processamento de imagem, independentemente do formato da imagem.</span><span class="sxs-lookup"><span data-stu-id="6d12a-183">A single, consistent set of interfaces is used for all image processing, regardless of image format.</span></span> <span data-ttu-id="6d12a-184">Qualquer aplicativo que use o WIC Obtém o suporte automático para novos formatos de imagem assim que o codec é instalado.</span><span class="sxs-lookup"><span data-stu-id="6d12a-184">Any application using WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="6d12a-185">Para obter mais informações sobre o desenvolvimento de codecs, consulte os tópicos em [desenvolvimento de componentes](-wic-component-development.md).</span><span class="sxs-lookup"><span data-stu-id="6d12a-185">For more information on codec development, see the topics in [Component Development](-wic-component-development.md).</span></span> <span data-ttu-id="6d12a-186">Para obter mais informações sobre o desenvolvimento de decodificadores, consulte [implementando um Decodificador WIC-Enabled](-wic-implementingwicdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="6d12a-186">For more information on decoder development, see [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d12a-187">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d12a-187">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6d12a-188">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6d12a-188">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6d12a-189">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="6d12a-189">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="6d12a-190">Visão geral da codificação</span><span class="sxs-lookup"><span data-stu-id="6d12a-190">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

[<span data-ttu-id="6d12a-191">Desenvolvimento de componentes</span><span class="sxs-lookup"><span data-stu-id="6d12a-191">Component Development</span></span>](-wic-component-development.md)
</dt> </dl>

 

 



