---
description: O codec JPEG XR nativo está disponível por meio do WIC (Windows Imaging Component). O formato JPEG XR, ao qual o codec dá suporte, foi projetado para fotografia digital profissional e consumidor.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Visão geral do codec JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d39608535f9be09821d8db3615641a84fd95a6
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444457"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="ad60e-104">Visão geral do codec JPEG XR</span><span class="sxs-lookup"><span data-stu-id="ad60e-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="ad60e-105">O codec JPEG XR nativo está disponível por meio do WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="ad60e-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="ad60e-106">O formato JPEG XR, ao qual o codec dá suporte, foi projetado para fotografia digital profissional e consumidor.</span><span class="sxs-lookup"><span data-stu-id="ad60e-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="ad60e-107">O formato JPEG XR pode atingir até duas vezes a eficiência de compactação do formato JPEG original, com artefatos de compactação menos perceptíveis.</span><span class="sxs-lookup"><span data-stu-id="ad60e-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="ad60e-108">Os recursos do JPEG XR incluem:</span><span class="sxs-lookup"><span data-stu-id="ad60e-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="ad60e-109">Suporte para imagens monocromáticas, RGB, CMYK e n canais</span><span class="sxs-lookup"><span data-stu-id="ad60e-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="ad60e-110">Formatos inteiros de 8, 16 e 32 bits</span><span class="sxs-lookup"><span data-stu-id="ad60e-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="ad60e-111">Alto intervalo dinâmico, formatos largos de jogos, usando valores de cor de ponto fixo ou de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="ad60e-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="ad60e-112">Decodificação progressiva</span><span class="sxs-lookup"><span data-stu-id="ad60e-112">Progressive decoding</span></span>
-   <span data-ttu-id="ad60e-113">Codificação com perda ou sem perda usando o mesmo algoritmo de compactação</span><span class="sxs-lookup"><span data-stu-id="ad60e-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="ad60e-114">Suporte para decodificação de regiões de interesse em imagens grandes</span><span class="sxs-lookup"><span data-stu-id="ad60e-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="ad60e-115">O formato JPEG XR é definido nos seguintes documentos padrão:</span><span class="sxs-lookup"><span data-stu-id="ad60e-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="ad60e-116">ITU-T T.832: Tecnologia da informação – sistema de codificação de imagem *XR JPEG – Especificação de codificação de imagem*</span><span class="sxs-lookup"><span data-stu-id="ad60e-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="ad60e-117">ISO/IEC 29199-2:2010: Tecnologia da informação – Sistema de codificação de imagem *XR JPEG — Parte 2: Especificação* de codificação de imagem</span><span class="sxs-lookup"><span data-stu-id="ad60e-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="ad60e-118">O padrão JPEG XR é baseado em grande parte no [formato hd photo,](hdphoto-format-overview.md) mas há algumas diferenças entre os dois formatos.</span><span class="sxs-lookup"><span data-stu-id="ad60e-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="ad60e-119">No Windows 8, o codec do HD Photo foi atualizado para dar suporte ao JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="ad60e-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="ad60e-120">O codificador agora sempre exibe um fluxo de bits em conformidade com JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="ad60e-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="ad60e-121">O decodificador pode decodificar imagens JPEG XR e HD Photo.</span><span class="sxs-lookup"><span data-stu-id="ad60e-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="ad60e-122">Melhorias substanciais de desempenho em relação ao codec do HD Photo foram feitas ao codec JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="ad60e-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="ad60e-123">Por exemplo, a decodificação de imagem de sub-resolução, como a geração de miniaturas, foi aprimorada, bem como a decodificação de imagem de baixa resolução.</span><span class="sxs-lookup"><span data-stu-id="ad60e-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="ad60e-124">É recomendável usar o formato JPEG XR em vez do formato hd photo.</span><span class="sxs-lookup"><span data-stu-id="ad60e-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="ad60e-125">Informações do Codec</span><span class="sxs-lookup"><span data-stu-id="ad60e-125">Codec Information</span></span>



|      <span data-ttu-id="ad60e-126">Componente</span><span class="sxs-lookup"><span data-stu-id="ad60e-126">Component</span></span>      |    <span data-ttu-id="ad60e-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-127">Description</span></span>                                                          |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ad60e-128">Extensão de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="ad60e-128">File name extension</span></span> | <span data-ttu-id="ad60e-129">"jxr" e "wdp"</span><span class="sxs-lookup"><span data-stu-id="ad60e-129">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="ad60e-130">GUID do contêiner</span><span class="sxs-lookup"><span data-stu-id="ad60e-130">Container GUID</span></span>      | <span data-ttu-id="ad60e-131">**Contêiner \_ GUIDFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="ad60e-131">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="ad60e-132">GUID do decodificador</span><span class="sxs-lookup"><span data-stu-id="ad60e-132">Decoder GUID</span></span>        | <span data-ttu-id="ad60e-133">**CLSID \_ WICWmpDecoder**</span><span class="sxs-lookup"><span data-stu-id="ad60e-133">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="ad60e-134">GUID do codificador</span><span class="sxs-lookup"><span data-stu-id="ad60e-134">Encoder GUID</span></span>        | <span data-ttu-id="ad60e-135">**CLSID \_ WICWmpEncoder**</span><span class="sxs-lookup"><span data-stu-id="ad60e-135">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="ad60e-136">Suporte ao perfil</span><span class="sxs-lookup"><span data-stu-id="ad60e-136">Profile Support</span></span>     | <span data-ttu-id="ad60e-137">O codificador e o decodificador são suportados até o Perfil Principal e até o nível 128.</span><span class="sxs-lookup"><span data-stu-id="ad60e-137">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="ad60e-138">Recursos do Codec</span><span class="sxs-lookup"><span data-stu-id="ad60e-138">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="ad60e-139">Alto Alcance Dinâmico</span><span class="sxs-lookup"><span data-stu-id="ad60e-139">High Dynamic Range</span></span>

<span data-ttu-id="ad60e-140">JPEG XR dá suporte a imagens de intervalo alto dinâmico, usando cores de ponto flutuante ou de ponto fixo.</span><span class="sxs-lookup"><span data-stu-id="ad60e-140">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="ad60e-141">Nesses formatos de cor, o intervalo numérico de um pixel é maior que o intervalo visível, portanto, você pode ajustar as cores acima ou abaixo do intervalo visível durante os estágios intermediários de processamento.</span><span class="sxs-lookup"><span data-stu-id="ad60e-141">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="ad60e-142">Ponto fixo: em uma representação de ponto fixo, 0 representa preto e 1,0 representa a saturação máxima.</span><span class="sxs-lookup"><span data-stu-id="ad60e-142">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="ad60e-143">O codec JPEG XR dá suporte a formatos de ponto fixo de 16 bits e 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ad60e-143">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="ad60e-144">Para 16 bits, 1,0 = 0x2000h, que fornece 13 bits para o intervalo visível \[ 0...1 \] .</span><span class="sxs-lookup"><span data-stu-id="ad60e-144">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="ad60e-145">O intervalo total é de -4,0 a +3,999 e é mapeado linearmente.</span><span class="sxs-lookup"><span data-stu-id="ad60e-145">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="ad60e-146">Para 32 bits, 1,0 = 0x01000000h, o intervalo visível é de 24 bits e o intervalo total é de -128 a +127,999.</span><span class="sxs-lookup"><span data-stu-id="ad60e-146">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="ad60e-147">Ponto flutuante: em uma representação de ponto flutuante, 0 representa preto e 1,0 representa a saturação máxima.</span><span class="sxs-lookup"><span data-stu-id="ad60e-147">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="ad60e-148">O codec JPEG XR dá suporte a formatos de ponto flutuante de 16 bits e 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ad60e-148">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="ad60e-149">Blocos</span><span class="sxs-lookup"><span data-stu-id="ad60e-149">Tiles</span></span>

<span data-ttu-id="ad60e-150">Um quadro pode ser particionado em sub-regiões retangulares chamadas *blocos*.</span><span class="sxs-lookup"><span data-stu-id="ad60e-150">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="ad60e-151">Um bloco é uma área de uma imagem que contém matrizes retangulares de macroblocks.</span><span class="sxs-lookup"><span data-stu-id="ad60e-151">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="ad60e-152">Os blocos permitem que as regiões da imagem sejam decodificadas sem processar a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="ad60e-152">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="ad60e-153">Durante a codificação, selecione o número de blocos definindo as propriedades **HorizontalTileSlices** e **VerticalTileSlices.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-153">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="ad60e-154">O tamanho mínimo do × 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="ad60e-154">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="ad60e-155">O codificador ajusta o número de blocos para manter essa restrição.</span><span class="sxs-lookup"><span data-stu-id="ad60e-155">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="ad60e-156">Há sobrecarga de armazenamento e processamento associada a cada bloco, portanto, você deve considerar o número de blocos necessários para cenários específicos.</span><span class="sxs-lookup"><span data-stu-id="ad60e-156">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="ad60e-157">Saída de fluxo de imagem</span><span class="sxs-lookup"><span data-stu-id="ad60e-157">Image Stream Output</span></span>

<span data-ttu-id="ad60e-158">O padrão JPEG-XR define duas partes de um arquivo JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="ad60e-158">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="ad60e-159">O fluxo de bits da imagem, definido no corpo do padrão.</span><span class="sxs-lookup"><span data-stu-id="ad60e-159">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="ad60e-160">O contêiner de imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-160">The image container.</span></span> <span data-ttu-id="ad60e-161">O arquivo contém metadados exif e XMP e é definido no Anexo A do padrão.</span><span class="sxs-lookup"><span data-stu-id="ad60e-161">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="ad60e-162">É possível e permitido pelo padrão inserir o fluxo de imagem dentro de outro tipo de contêiner de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad60e-162">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="ad60e-163">O codificador dá suporte a um modo somente de fluxo, que transmite o fluxo de bits de imagem bruto sem contêiner de imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-163">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="ad60e-164">Um aplicativo pode armazenar o fluxo de bits em algum outro formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="ad60e-164">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="ad60e-165">Para habilitar o modo somente fluxo, de definir a **propriedade StreamOnly.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-165">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="ad60e-166">Configurações de qualidade da imagem</span><span class="sxs-lookup"><span data-stu-id="ad60e-166">Image Quality Settings</span></span>

<span data-ttu-id="ad60e-167">Várias propriedades de codec controlam a qualidade da imagem de saída do codificador.</span><span class="sxs-lookup"><span data-stu-id="ad60e-167">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="ad60e-168">[ImageQuality](#imagequality) é uma propriedade comum entre codecs WIC.</span><span class="sxs-lookup"><span data-stu-id="ad60e-168">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="ad60e-169">Especifica a qualidade da imagem como um único valor de ponto flutuante de 0,0 a 1,0,</span><span class="sxs-lookup"><span data-stu-id="ad60e-169">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="ad60e-170">As [propriedades Quality,](#image-quality-settings) [Overlap](#overlap)e [Subsampling](#subsampling) dão mais controle sobre as configurações de qualidade.</span><span class="sxs-lookup"><span data-stu-id="ad60e-170">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="ad60e-171">Para usar as [propriedades Quality](#image-quality-settings), [Overlap](#overlap)e [Subsampling,](#subsampling) de definir a propriedade [UseCodecOptions](#usecodecoptions) como **VARIANT \_ TRUE.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-171">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="ad60e-172">Se [UseCodecOptions](#usecodecoptions) for **VARIANT \_ FALSE (VARIANT** **\_ FALSE** é o padrão), o codificador usará a [propriedade ImageQuality.](#imagequality)</span><span class="sxs-lookup"><span data-stu-id="ad60e-172">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="ad60e-173">O codificador mapeia o valor de ImageQuality [para Qualidade,](#image-quality-settings) [Sobreposição](#overlap)e [Submampling por](#subsampling) meio de uma tabela de lookup.</span><span class="sxs-lookup"><span data-stu-id="ad60e-173">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="ad60e-174">O codificador não dá suporte à **propriedade CompressionQuality.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-174">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="ad60e-175">Compressed Domain Transcode</span><span class="sxs-lookup"><span data-stu-id="ad60e-175">Compressed Domain Transcode</span></span>

<span data-ttu-id="ad60e-176">O codec JPEG XR pode executar determinadas transformações de imagem sem realmente decodificar os dados compactados e recodificá-los.</span><span class="sxs-lookup"><span data-stu-id="ad60e-176">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="ad60e-177">As operações de domínio compactadas são muito eficientes e evitam qualquer perda de qualidade adicional que seja típica quando você decodifica e codifica uma imagem compactada com perda.</span><span class="sxs-lookup"><span data-stu-id="ad60e-177">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="ad60e-178">Há suporte para as seguintes operações de domínio compactado:</span><span class="sxs-lookup"><span data-stu-id="ad60e-178">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="ad60e-179">Recorte uma região da imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-179">Crop a region of the image.</span></span>
-   <span data-ttu-id="ad60e-180">Girar ou inverter a imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-180">Rotate or flip the image.</span></span>
-   <span data-ttu-id="ad60e-181">Descarte dados de frequência para criar um arquivo de imagem menor.</span><span class="sxs-lookup"><span data-stu-id="ad60e-181">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="ad60e-182">Reorganize a imagem entre ordem espacial e de frequência.</span><span class="sxs-lookup"><span data-stu-id="ad60e-182">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="ad60e-183">O codificador JPEG XR usa a transcodificação de domínio compactado, se possível, quando a imagem de origem é uma imagem JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="ad60e-183">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="ad60e-184">Quando o codificador executa uma operação de domínio compactada, ele ignora as seguintes propriedades de codec: [AlphaQuality,](#alphaquality) [ImageQuality,](#imagequality) [InterleavedAlpha,](#interleavedalpha) [Lossless](#lossless)[Overlap](#overlap)e [Quality](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="ad60e-184">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="ad60e-185">Se as [propriedades HorizontalTileSlices](/windows) [e VerticalTileSlices](/windows) estão presentes, você deve defini-las como zero.</span><span class="sxs-lookup"><span data-stu-id="ad60e-185">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="ad60e-186">Não é possível alterar o tamanho do peça de uma imagem como parte de um transcódigo de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-186">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="ad60e-187">A lista a seguir descreve como executar as transformações de imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-187">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="ad60e-188">Para recortar a imagem, de definido a região desejada no [**parâmetro WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) do **método WriteSource.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-188">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="ad60e-189">Para girar ou inverter a imagem, de definir a [propriedade BitmapTransform.](#bitmaptransform)</span><span class="sxs-lookup"><span data-stu-id="ad60e-189">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="ad60e-190">Para descartar dados de frequência na imagem, de definir a [propriedade ImageDataDiscard.](#imagedatadiscard)</span><span class="sxs-lookup"><span data-stu-id="ad60e-190">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="ad60e-191">Para descartar dados de frequência no canal alfa, de definir a [propriedade AlphaDataDiscard.](#alphadatadiscard)</span><span class="sxs-lookup"><span data-stu-id="ad60e-191">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="ad60e-192">Descartar dados de frequência reduz o tamanho do arquivo codificado e pode reduzir a resolução.</span><span class="sxs-lookup"><span data-stu-id="ad60e-192">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="ad60e-193">Para alterar a organização da imagem entre a frequência e a ordenação espacial, de definir a [propriedade FrequencyOrdering.](/windows)</span><span class="sxs-lookup"><span data-stu-id="ad60e-193">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="ad60e-194">Para desabilitar o transcodificador de domínio compactado e forçar o codificador a codificar novamente a imagem, de definir [UseCodecOptions](#usecodecoptions) como **VARIANT \_ TRUE** e definir [CompressedDomainTranscode](#compresseddomaintranscode) como **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-194">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="ad60e-195">Opções do codificador</span><span class="sxs-lookup"><span data-stu-id="ad60e-195">Encoder Options</span></span>

<span data-ttu-id="ad60e-196">Para definir propriedades de codificação, use a interface [**IPropertyBag2.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad60e-196">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="ad60e-197">Para obter mais informações, consulte Visão [geral de codificação.](-wic-creating-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="ad60e-197">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="ad60e-198">A lista a seguir especifica as opções do codificador.</span><span class="sxs-lookup"><span data-stu-id="ad60e-198">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="ad60e-199">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="ad60e-199">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="ad60e-200">AlfaQuality</span><span class="sxs-lookup"><span data-stu-id="ad60e-200">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="ad60e-201">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="ad60e-201">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="ad60e-202">Compresseddomaintranscode</span><span class="sxs-lookup"><span data-stu-id="ad60e-202">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="ad60e-203">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="ad60e-203">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="ad60e-204">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="ad60e-204">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="ad60e-205">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="ad60e-205">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="ad60e-206">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="ad60e-206">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="ad60e-207">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="ad60e-207">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="ad60e-208">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="ad60e-208">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="ad60e-209">Lossless</span><span class="sxs-lookup"><span data-stu-id="ad60e-209">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="ad60e-210">Sobreposição</span><span class="sxs-lookup"><span data-stu-id="ad60e-210">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="ad60e-211">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="ad60e-211">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="ad60e-212">Qualidade</span><span class="sxs-lookup"><span data-stu-id="ad60e-212">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="ad60e-213">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="ad60e-213">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="ad60e-214">Subamostragem</span><span class="sxs-lookup"><span data-stu-id="ad60e-214">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="ad60e-215">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="ad60e-215">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="ad60e-216">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="ad60e-216">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="ad60e-217">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="ad60e-217">AlphaDataDiscard</span></span>

<span data-ttu-id="ad60e-218">Define a quantidade de dados de frequência alfa a ser descartada durante um transcódigo de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-218">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="ad60e-219">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-219">Data type</span></span> | <span data-ttu-id="ad60e-220">Vartype</span><span class="sxs-lookup"><span data-stu-id="ad60e-220">VARTYPE</span></span>     | <span data-ttu-id="ad60e-221">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-221">Range</span></span> | <span data-ttu-id="ad60e-222">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-222">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="ad60e-223">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="ad60e-223">**UCHAR**</span></span> | <span data-ttu-id="ad60e-224">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="ad60e-224">**VT\_UI1**</span></span> | <span data-ttu-id="ad60e-225">0–4</span><span class="sxs-lookup"><span data-stu-id="ad60e-225">0–4</span></span>   | <span data-ttu-id="ad60e-226">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ad60e-226">None</span></span>    |



 

<span data-ttu-id="ad60e-227">Essa propriedade se aplica somente se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **VARIANT \_ TRUE** e a imagem contiver um canal alfa planar ou um canal alfa intercalado; caso contrário, ela será ignorada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-227">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="ad60e-228">Para imagens que contêm um canal alfa planar, os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="ad60e-228">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="ad60e-229">Valor</span><span class="sxs-lookup"><span data-stu-id="ad60e-229">Value</span></span> | <span data-ttu-id="ad60e-230">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-230">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad60e-231">0</span><span class="sxs-lookup"><span data-stu-id="ad60e-231">0</span></span>     | <span data-ttu-id="ad60e-232">Nenhum dado de frequência de imagem é descartado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-232">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ad60e-233">1</span><span class="sxs-lookup"><span data-stu-id="ad60e-233">1</span></span>     | <span data-ttu-id="ad60e-234">Os flexbits são descartados.</span><span class="sxs-lookup"><span data-stu-id="ad60e-234">The flexbits are discarded.</span></span> <span data-ttu-id="ad60e-235">Isso reduz arbitrariamente a qualidade do canal alfa planar para a imagem transcodificada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-235">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="ad60e-236">, sem uma alteração na resolução efetiva.</span><span class="sxs-lookup"><span data-stu-id="ad60e-236">, without a change in the effective resolution.</span></span> <span data-ttu-id="ad60e-237">A redução exata no tamanho e na qualidade do arquivo depende de vários fatores e não pode ser especificada exatamente.</span><span class="sxs-lookup"><span data-stu-id="ad60e-237">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="ad60e-238">2</span><span class="sxs-lookup"><span data-stu-id="ad60e-238">2</span></span>     | <span data-ttu-id="ad60e-239">A faixa de dados de alta frequência de passagem é descartada, incluindo os flexbits.</span><span class="sxs-lookup"><span data-stu-id="ad60e-239">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="ad60e-240">Isso reduz efetivamente a resolução do canal alfa planar em um fator de 4 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="ad60e-240">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="ad60e-241">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada bloco 4x4 de pixels de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-241">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="ad60e-242">Normalmente, você deve definir esse valor somente quando a [propriedade ImageDataDiscard](#imagedatadiscard) tiver o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="ad60e-242">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="ad60e-243">3</span><span class="sxs-lookup"><span data-stu-id="ad60e-243">3</span></span>     | <span data-ttu-id="ad60e-244">As faixas de dados de alta passagem e baixa frequência são descartadas, incluindo os flexbits.</span><span class="sxs-lookup"><span data-stu-id="ad60e-244">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="ad60e-245">Isso reduz a resolução do canal alfa planar por um fator de 16 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="ad60e-245">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="ad60e-246">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada macroblock 16x16 de pixels de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-246">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="ad60e-247">Normalmente, você deve definir esse valor somente quando a [propriedade ImageDataDiscard](#imagedatadiscard) tiver o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="ad60e-247">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="ad60e-248">4</span><span class="sxs-lookup"><span data-stu-id="ad60e-248">4</span></span>     | <span data-ttu-id="ad60e-249">O canal alfa é completamente descartado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-249">The alpha channel is completely discarded.</span></span> <span data-ttu-id="ad60e-250">O formato de pixel da imagem transcodificada é alterado para refletir a remoção do canal alfa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-250">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="ad60e-251">Para imagens que contêm um canal alfa intercalado, o valor a seguir é válido.</span><span class="sxs-lookup"><span data-stu-id="ad60e-251">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="ad60e-252">Valor</span><span class="sxs-lookup"><span data-stu-id="ad60e-252">Value</span></span> | <span data-ttu-id="ad60e-253">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-253">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad60e-254">4</span><span class="sxs-lookup"><span data-stu-id="ad60e-254">4</span></span>     | <span data-ttu-id="ad60e-255">O canal alfa é completamente descartado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-255">The alpha channel is completely discarded.</span></span> <span data-ttu-id="ad60e-256">O formato de pixel da imagem transcodificada é alterado para refletir a remoção do canal alfa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-256">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="ad60e-257">Para alfa intercalado, a menos que essa propriedade seja definida como 4, o canal alfa é processado da mesma forma que os dados da imagem, de acordo com o valor da [propriedade ImageDataDiscard.](#imagedatadiscard)</span><span class="sxs-lookup"><span data-stu-id="ad60e-257">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="ad60e-258">AlfaQuality</span><span class="sxs-lookup"><span data-stu-id="ad60e-258">AlphaQuality</span></span>

<span data-ttu-id="ad60e-259">Define a qualidade da compactação para a imagem de canal alfa planar.</span><span class="sxs-lookup"><span data-stu-id="ad60e-259">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="ad60e-260">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-260">Data type</span></span> | <span data-ttu-id="ad60e-261">Vartype</span><span class="sxs-lookup"><span data-stu-id="ad60e-261">VARTYPE</span></span>     | <span data-ttu-id="ad60e-262">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-262">Range</span></span> | <span data-ttu-id="ad60e-263">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-263">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="ad60e-264">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="ad60e-264">**UCHAR**</span></span> | <span data-ttu-id="ad60e-265">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="ad60e-265">**VT\_UI1**</span></span> | <span data-ttu-id="ad60e-266">1–255</span><span class="sxs-lookup"><span data-stu-id="ad60e-266">1–255</span></span> | <span data-ttu-id="ad60e-267">1</span><span class="sxs-lookup"><span data-stu-id="ad60e-267">1</span></span>       |



 

<span data-ttu-id="ad60e-268">Essa propriedade se aplica quando a imagem tem um canal alfa e a [propriedade InterleavedAlpha](#interleavedalpha) é **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-268">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="ad60e-269">O valor 1 indica o modo sem perda.</span><span class="sxs-lookup"><span data-stu-id="ad60e-269">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="ad60e-270">O aumento de valores resulta em taxas de compactação mais altas e menor qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-270">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="ad60e-271">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="ad60e-271">BitmapTransform</span></span>

<span data-ttu-id="ad60e-272">Especifica se a imagem é girada ou invertida quando decodificada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-272">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="ad60e-273">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-273">Data type</span></span> | <span data-ttu-id="ad60e-274">Vartype</span><span class="sxs-lookup"><span data-stu-id="ad60e-274">VARTYPE</span></span>     | <span data-ttu-id="ad60e-275">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-275">Range</span></span>                                                                     | <span data-ttu-id="ad60e-276">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-276">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="ad60e-277">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="ad60e-277">**UCHAR**</span></span> | <span data-ttu-id="ad60e-278">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="ad60e-278">**VT\_UI1**</span></span> | [<span data-ttu-id="ad60e-279">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="ad60e-279">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="ad60e-280">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="ad60e-280">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="ad60e-281">Compresseddomaintranscode</span><span class="sxs-lookup"><span data-stu-id="ad60e-281">CompressedDomainTranscode</span></span>

<span data-ttu-id="ad60e-282">Habilita ou desabilita a transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-282">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="ad60e-283">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-283">Data type</span></span>         | <span data-ttu-id="ad60e-284">Vartype</span><span class="sxs-lookup"><span data-stu-id="ad60e-284">VARTYPE</span></span>      | <span data-ttu-id="ad60e-285">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-285">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="ad60e-286">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="ad60e-286">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-287">**BOOL da VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-287">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-288">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad60e-288">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="ad60e-289">Para desabilitar operações de domínio compactadas, de definir essa propriedade como **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ad60e-289">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="ad60e-290">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="ad60e-290">FrequencyOrder</span></span>

<span data-ttu-id="ad60e-291">Habilita a codificação na ordem de frequência.</span><span class="sxs-lookup"><span data-stu-id="ad60e-291">Enables encoding in frequency order.</span></span> <span data-ttu-id="ad60e-292">Implementações de dispositivo de codificadores JPEG XR podem organizar um arquivo em ordem espacial para reduzir a memória necessária durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="ad60e-292">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="ad60e-293">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-293">Data type</span></span>         | <span data-ttu-id="ad60e-294">Vartype</span><span class="sxs-lookup"><span data-stu-id="ad60e-294">VARTYPE</span></span>      | <span data-ttu-id="ad60e-295">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-295">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="ad60e-296">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="ad60e-296">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-297">**BOOL da VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-297">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-298">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="ad60e-298">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="ad60e-299">**VARIANT \_ TRUE:** ordem de frequência.</span><span class="sxs-lookup"><span data-stu-id="ad60e-299">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="ad60e-300">Os dados de menor frequência aparecem primeiro no arquivo e o conteúdo da imagem é agrupado por sua frequência em vez de sua orientação espacial.</span><span class="sxs-lookup"><span data-stu-id="ad60e-300">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="ad60e-301">Organizar um arquivo por ordem de frequência fornece o melhor desempenho para qualquer decodificação baseada em frequência.</span><span class="sxs-lookup"><span data-stu-id="ad60e-301">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="ad60e-302">**Variante \_ FALSE**: ordem espacial.</span><span class="sxs-lookup"><span data-stu-id="ad60e-302">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="ad60e-303">A ordem espacial reduz a memória necessária durante a codificação</span><span class="sxs-lookup"><span data-stu-id="ad60e-303">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="ad60e-304">A ordem de frequência é recomendada, a menos que você tenha motivos específicos de desempenho ou de aplicativo para usar a ordem espacial.</span><span class="sxs-lookup"><span data-stu-id="ad60e-304">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="ad60e-305">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="ad60e-305">HorizontalTileSlices</span></span>

<span data-ttu-id="ad60e-306">Define o número de blocos horizontais.</span><span class="sxs-lookup"><span data-stu-id="ad60e-306">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="ad60e-307">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-307">Data type</span></span>  | <span data-ttu-id="ad60e-308">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-308">VARTYPE</span></span>     | <span data-ttu-id="ad60e-309">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-309">Range</span></span>  | <span data-ttu-id="ad60e-310">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-310">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="ad60e-311">**NUM**</span><span class="sxs-lookup"><span data-stu-id="ad60e-311">**USHORT**</span></span> | <span data-ttu-id="ad60e-312">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="ad60e-312">**VT\_UI2**</span></span> | <span data-ttu-id="ad60e-313">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="ad60e-313">0–4095</span></span> | <span data-ttu-id="ad60e-314">(largura da imagem – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="ad60e-314">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="ad60e-315">O valor é o número de subdivisões horizontais; ou seja, o número de blocos horizontais – 1.</span><span class="sxs-lookup"><span data-stu-id="ad60e-315">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="ad60e-316">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="ad60e-316">IgnoreOverlap</span></span>

<span data-ttu-id="ad60e-317">Especifica como o codificador trata os limites de bloco durante uma transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-317">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="ad60e-318">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-318">Data type</span></span>         | <span data-ttu-id="ad60e-319">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-319">VARTYPE</span></span>      | <span data-ttu-id="ad60e-320">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-320">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="ad60e-321">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-321">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-322">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-322">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-323">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="ad60e-323">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="ad60e-324">Essa propriedade será aplicada somente se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true** e uma transcodificação de sub-região de exatamente um ou mais blocos for executada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-324">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="ad60e-325">A operação padrão para uma transcodificação de região é expandir a região solicitada para incluir os pixels adjacentes que são necessários para sobrepor a decodificação das bordas da região.</span><span class="sxs-lookup"><span data-stu-id="ad60e-325">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="ad60e-326">Se essa propriedade for definida como **Variant \_ true**, o codec ignorará os pixels adjacentes e apenas o bloco ou blocos selecionados serão extraídos.</span><span class="sxs-lookup"><span data-stu-id="ad60e-326">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="ad60e-327">Se a imagem de origem não for um lado ou se a região solicitada incluir blocos parciais, esse parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-327">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="ad60e-328">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="ad60e-328">ImageDataDiscard</span></span>

<span data-ttu-id="ad60e-329">Define a quantidade de dados de frequência de imagem a serem descartados durante uma transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-329">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="ad60e-330">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-330">Data type</span></span> | <span data-ttu-id="ad60e-331">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-331">VARTYPE</span></span>     | <span data-ttu-id="ad60e-332">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-332">Range</span></span> | <span data-ttu-id="ad60e-333">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-333">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="ad60e-334">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="ad60e-334">**UCHAR**</span></span> | <span data-ttu-id="ad60e-335">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="ad60e-335">**VT\_UI1**</span></span> | <span data-ttu-id="ad60e-336">0 a 3</span><span class="sxs-lookup"><span data-stu-id="ad60e-336">0–3</span></span>   | <span data-ttu-id="ad60e-337">0</span><span class="sxs-lookup"><span data-stu-id="ad60e-337">0</span></span>       |



 

<span data-ttu-id="ad60e-338">Essa propriedade só se aplicará se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true**; caso contrário, será ignorada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-338">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="ad60e-339">Valor</span><span class="sxs-lookup"><span data-stu-id="ad60e-339">Value</span></span> | <span data-ttu-id="ad60e-340">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-340">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad60e-341">0</span><span class="sxs-lookup"><span data-stu-id="ad60e-341">0</span></span>     | <span data-ttu-id="ad60e-342">Nenhum dado de frequência de imagem é Descartado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-342">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ad60e-343">1</span><span class="sxs-lookup"><span data-stu-id="ad60e-343">1</span></span>     | <span data-ttu-id="ad60e-344">Os FlexBits são descartados.</span><span class="sxs-lookup"><span data-stu-id="ad60e-344">The flexbits are discarded.</span></span> <span data-ttu-id="ad60e-345">Isso reduz arbitrariamente a qualidade da imagem transcodificada sem alterar a resolução efetiva da imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-345">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="ad60e-346">A redução exata no tamanho do arquivo e na qualidade depende de vários fatores e não pode ser especificada com exatidão.</span><span class="sxs-lookup"><span data-stu-id="ad60e-346">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="ad60e-347">Esse valor retorna um erro especificado para um canal alfa intercalado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-347">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="ad60e-348">2</span><span class="sxs-lookup"><span data-stu-id="ad60e-348">2</span></span>     | <span data-ttu-id="ad60e-349">A banda de dados de frequência de passagem alta é descartada, incluindo o FlexBits.</span><span class="sxs-lookup"><span data-stu-id="ad60e-349">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="ad60e-350">Isso reduz a resolução da imagem transcodificada por um fator de 4 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="ad60e-350">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="ad60e-351">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada bloco de pixels 4x4.</span><span class="sxs-lookup"><span data-stu-id="ad60e-351">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="ad60e-352">Portanto, a imagem transcodificada deve ser downsampledda adequadamente sempre que for decodificada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-352">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="ad60e-353">3</span><span class="sxs-lookup"><span data-stu-id="ad60e-353">3</span></span>     | <span data-ttu-id="ad60e-354">As faixas de dados de frequência de passagem alta e baixa são descartadas, incluindo o FlexBits.</span><span class="sxs-lookup"><span data-stu-id="ad60e-354">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="ad60e-355">Isso reduz a resolução da imagem transcodificada por um fator de 16 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="ad60e-355">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="ad60e-356">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada 16x16 macrobloco de pixels.</span><span class="sxs-lookup"><span data-stu-id="ad60e-356">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="ad60e-357">Portanto, a imagem transcodificada deve ser downsampledda adequadamente sempre que for decodificada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-357">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="ad60e-358">Se a imagem contiver um canal alfa intercalado, o valor de [ImageDataDiscard](#imagedatadiscard) será aplicado ao canal alfa, a menos que a propriedade [AlphaDataDiscard](#alphadatadiscard) esteja definida como 4; nesse caso, o canal alfa será Descartado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-358">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="ad60e-359">Para o planar alfa, os dados de frequência descartados são controlados pela propriedade [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="ad60e-359">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="ad60e-360">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="ad60e-360">ImageQuality</span></span>

<span data-ttu-id="ad60e-361">Define a qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-361">Sets the image quality.</span></span>



| <span data-ttu-id="ad60e-362">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-362">Data type</span></span> | <span data-ttu-id="ad60e-363">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-363">VARTYPE</span></span>    | <span data-ttu-id="ad60e-364">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-364">Range</span></span> | <span data-ttu-id="ad60e-365">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-365">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="ad60e-366">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="ad60e-366">**FLOAT**</span></span> | <span data-ttu-id="ad60e-367">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="ad60e-367">**VT\_R4**</span></span> | <span data-ttu-id="ad60e-368">0 a 1,0</span><span class="sxs-lookup"><span data-stu-id="ad60e-368">0–1.0</span></span> | <span data-ttu-id="ad60e-369">0,9</span><span class="sxs-lookup"><span data-stu-id="ad60e-369">0.9</span></span>     |



 

<span data-ttu-id="ad60e-370">O nível 1,0 oferece uma compactação matematicamente sem perdas.</span><span class="sxs-lookup"><span data-stu-id="ad60e-370">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="ad60e-371">O nível 0,0 é a configuração de qualidade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-371">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="ad60e-372">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="ad60e-372">InterleavedAlpha</span></span>

<span data-ttu-id="ad60e-373">Especifica se deve codificar alfa ou planar intercalado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-373">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="ad60e-374">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-374">Data type</span></span>         | <span data-ttu-id="ad60e-375">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-375">VARTYPE</span></span>      | <span data-ttu-id="ad60e-376">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-376">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="ad60e-377">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-377">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-378">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-378">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-379">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="ad60e-379">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="ad60e-380">**Variante \_ TRUE**: Alpha intercalado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-380">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="ad60e-381">As informações do canal alfa são codificadas como um canal intercalado adicional, sem correlação com os canais de conteúdo da imagem.</span><span class="sxs-lookup"><span data-stu-id="ad60e-381">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="ad60e-382">Esse modo é útil para decodificar alfa simultaneamente com a imagem quando a imagem é transmitida.</span><span class="sxs-lookup"><span data-stu-id="ad60e-382">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="ad60e-383">VARIANTE \_ false: planar alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="ad60e-383">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="ad60e-384">Um canal alfanumérico planar é codificado como uma imagem separada.</span><span class="sxs-lookup"><span data-stu-id="ad60e-384">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="ad60e-385">Os dados da imagem e o canal alfa são decodificados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="ad60e-385">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="ad60e-386">Opcionalmente, você pode definir o nível de qualidade do canal alfa definindo a propriedade [AlphaQuality](#alphaquality) .</span><span class="sxs-lookup"><span data-stu-id="ad60e-386">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="ad60e-387">Há suporte para alfa intercalado apenas para determinados formatos de pixel RGB.</span><span class="sxs-lookup"><span data-stu-id="ad60e-387">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="ad60e-388">O planar alfanumérico tem suporte para qualquer formato de imagem que define um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-388">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="ad60e-389">Lossless</span><span class="sxs-lookup"><span data-stu-id="ad60e-389">Lossless</span></span>

<span data-ttu-id="ad60e-390">Habilita a compactação de perdas.</span><span class="sxs-lookup"><span data-stu-id="ad60e-390">Enables losses compression.</span></span>



| <span data-ttu-id="ad60e-391">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-391">Data type</span></span>         | <span data-ttu-id="ad60e-392">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-392">VARTYPE</span></span>      | <span data-ttu-id="ad60e-393">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-393">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="ad60e-394">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-394">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-395">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-395">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-396">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="ad60e-396">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="ad60e-397">Se o valor for **Variant \_ true**, o codificador usará a compactação sem perdas.</span><span class="sxs-lookup"><span data-stu-id="ad60e-397">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="ad60e-398">Quando definido como **Variant \_ true**, essa propriedade substitui a propriedade [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="ad60e-398">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="ad60e-399">Post</span><span class="sxs-lookup"><span data-stu-id="ad60e-399">Overlap</span></span>

<span data-ttu-id="ad60e-400">Define o nível de filtragem de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="ad60e-400">Sets the level of overlap filtering.</span></span> <span data-ttu-id="ad60e-401">Com a filtragem de sobreposição, os coeficientes de transformação são aplicados entre limites de bloco e macrobloco.</span><span class="sxs-lookup"><span data-stu-id="ad60e-401">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="ad60e-402">Isso pode reduzir os artefatos de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ad60e-402">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="ad60e-403">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-403">Data type</span></span> | <span data-ttu-id="ad60e-404">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-404">VARTYPE</span></span>     | <span data-ttu-id="ad60e-405">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-405">Range</span></span> | <span data-ttu-id="ad60e-406">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-406">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="ad60e-407">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="ad60e-407">**UCHAR**</span></span> | <span data-ttu-id="ad60e-408">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="ad60e-408">**VT\_UI1**</span></span> | <span data-ttu-id="ad60e-409">0 a 4</span><span class="sxs-lookup"><span data-stu-id="ad60e-409">0–4</span></span>   | <span data-ttu-id="ad60e-410">1</span><span class="sxs-lookup"><span data-stu-id="ad60e-410">1</span></span>       |



 



| <span data-ttu-id="ad60e-411">Valor</span><span class="sxs-lookup"><span data-stu-id="ad60e-411">Value</span></span> | <span data-ttu-id="ad60e-412">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-412">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="ad60e-413">0</span><span class="sxs-lookup"><span data-stu-id="ad60e-413">0</span></span>     | <span data-ttu-id="ad60e-414">Sem sobreposição.</span><span class="sxs-lookup"><span data-stu-id="ad60e-414">No overlap.</span></span>                                   |
| <span data-ttu-id="ad60e-415">1</span><span class="sxs-lookup"><span data-stu-id="ad60e-415">1</span></span>     | <span data-ttu-id="ad60e-416">Um nível de sobreposição, divisão suave.</span><span class="sxs-lookup"><span data-stu-id="ad60e-416">One level of overlap, soft tiling.</span></span> <span data-ttu-id="ad60e-417">(Padrão.)</span><span class="sxs-lookup"><span data-stu-id="ad60e-417">(Default.)</span></span> |
| <span data-ttu-id="ad60e-418">2</span><span class="sxs-lookup"><span data-stu-id="ad60e-418">2</span></span>     | <span data-ttu-id="ad60e-419">Dois níveis de sobreposição, divisão suave.</span><span class="sxs-lookup"><span data-stu-id="ad60e-419">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="ad60e-420">3</span><span class="sxs-lookup"><span data-stu-id="ad60e-420">3</span></span>     | <span data-ttu-id="ad60e-421">Um nível de sobreposição, divisão fixa</span><span class="sxs-lookup"><span data-stu-id="ad60e-421">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="ad60e-422">4</span><span class="sxs-lookup"><span data-stu-id="ad60e-422">4</span></span>     | <span data-ttu-id="ad60e-423">Dois níveis de sobreposição, divisão fixa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-423">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="ad60e-424">Definições:</span><span class="sxs-lookup"><span data-stu-id="ad60e-424">Definitions:</span></span>

-   <span data-ttu-id="ad60e-425">Um nível de sobreposição: os valores codificados dos blocos 4x4 são modificados com base em blocos vizinhos.</span><span class="sxs-lookup"><span data-stu-id="ad60e-425">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="ad60e-426">Dois níveis de sobreposição: o primeiro nível de sobreposição é aplicado.</span><span class="sxs-lookup"><span data-stu-id="ad60e-426">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="ad60e-427">Além disso, os valores codificados de 16x16 macroblocos são modificados com base no macroblocos vizinho.</span><span class="sxs-lookup"><span data-stu-id="ad60e-427">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="ad60e-428">Divisão suave: a filtragem de sobreposição é aplicada entre limites de bloco.</span><span class="sxs-lookup"><span data-stu-id="ad60e-428">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="ad60e-429">Divisão fixa: a filtragem de sobreposição não é aplicada entre limites de bloco.</span><span class="sxs-lookup"><span data-stu-id="ad60e-429">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="ad60e-430">Blocos físicos podem introduzir alguns artefatos visuais ao longo dos limites de bloco.</span><span class="sxs-lookup"><span data-stu-id="ad60e-430">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="ad60e-431">Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="ad60e-431">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="ad60e-432">Progressivmode</span><span class="sxs-lookup"><span data-stu-id="ad60e-432">ProgressiveMode</span></span>

<span data-ttu-id="ad60e-433">Habilita ou desabilita a codificação progressiva.</span><span class="sxs-lookup"><span data-stu-id="ad60e-433">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="ad60e-434">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-434">Data type</span></span>         | <span data-ttu-id="ad60e-435">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-435">VARTYPE</span></span>      | <span data-ttu-id="ad60e-436">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-436">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="ad60e-437">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-437">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-438">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-438">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-439">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="ad60e-439">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="ad60e-440">Valor</span><span class="sxs-lookup"><span data-stu-id="ad60e-440">Value</span></span>              | <span data-ttu-id="ad60e-441">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-441">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="ad60e-442">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="ad60e-442">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="ad60e-443">Modo sequencial (padrão).</span><span class="sxs-lookup"><span data-stu-id="ad60e-443">Sequential mode (default).</span></span> |
| <span data-ttu-id="ad60e-444">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="ad60e-444">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="ad60e-445">Modo progressivo.</span><span class="sxs-lookup"><span data-stu-id="ad60e-445">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="ad60e-446">Qualidade</span><span class="sxs-lookup"><span data-stu-id="ad60e-446">Quality</span></span>

<span data-ttu-id="ad60e-447">Define a qualidade da compactação.</span><span class="sxs-lookup"><span data-stu-id="ad60e-447">Sets the compression quality.</span></span>



| <span data-ttu-id="ad60e-448">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-448">Data type</span></span> | <span data-ttu-id="ad60e-449">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-449">VARTYPE</span></span>     | <span data-ttu-id="ad60e-450">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-450">Range</span></span> | <span data-ttu-id="ad60e-451">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-451">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="ad60e-452">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="ad60e-452">**UCHAR**</span></span> | <span data-ttu-id="ad60e-453">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="ad60e-453">**VT\_UI1**</span></span> | <span data-ttu-id="ad60e-454">1 a 255</span><span class="sxs-lookup"><span data-stu-id="ad60e-454">1–255</span></span> | <span data-ttu-id="ad60e-455">1</span><span class="sxs-lookup"><span data-stu-id="ad60e-455">1</span></span>       |



 

<span data-ttu-id="ad60e-456">O valor 1 indica o modo sem perdas.</span><span class="sxs-lookup"><span data-stu-id="ad60e-456">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="ad60e-457">Os valores crescentes resultam em taxas de compactação mais altas e qualidade de imagem inferior.</span><span class="sxs-lookup"><span data-stu-id="ad60e-457">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="ad60e-458">Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="ad60e-458">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="ad60e-459">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="ad60e-459">StreamOnly</span></span>

<span data-ttu-id="ad60e-460">Habilita ou desabilita o modo somente fluxo.</span><span class="sxs-lookup"><span data-stu-id="ad60e-460">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="ad60e-461">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-461">Data type</span></span>         | <span data-ttu-id="ad60e-462">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-462">VARTYPE</span></span>      | <span data-ttu-id="ad60e-463">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-463">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="ad60e-464">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-464">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-465">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-465">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-466">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="ad60e-466">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="ad60e-467">Valor</span><span class="sxs-lookup"><span data-stu-id="ad60e-467">Value</span></span>              | <span data-ttu-id="ad60e-468">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-468">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ad60e-469">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="ad60e-469">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="ad60e-470">O codificador gera o fluxo de imagem bruta sem metadados.</span><span class="sxs-lookup"><span data-stu-id="ad60e-470">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="ad60e-471">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="ad60e-471">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="ad60e-472">O codificador gera o formato de contêiner (fluxo de imagem mais metadados).</span><span class="sxs-lookup"><span data-stu-id="ad60e-472">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="ad60e-473">Subamostragens</span><span class="sxs-lookup"><span data-stu-id="ad60e-473">Subsampling</span></span>

<span data-ttu-id="ad60e-474">Define a subamostra de croma.</span><span class="sxs-lookup"><span data-stu-id="ad60e-474">Sets the chroma subsampling.</span></span> <span data-ttu-id="ad60e-475">Essa propriedade só se aplica a imagens RGB.</span><span class="sxs-lookup"><span data-stu-id="ad60e-475">This property applies only to RGB images.</span></span>



| <span data-ttu-id="ad60e-476">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-476">Data type</span></span> | <span data-ttu-id="ad60e-477">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-477">VARTYPE</span></span>     | <span data-ttu-id="ad60e-478">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-478">Range</span></span> | <span data-ttu-id="ad60e-479">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-479">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="ad60e-480">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="ad60e-480">**UCHAR**</span></span> | <span data-ttu-id="ad60e-481">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="ad60e-481">**VT\_UI1**</span></span> | <span data-ttu-id="ad60e-482">0 a 3</span><span class="sxs-lookup"><span data-stu-id="ad60e-482">0–3</span></span>   | <span data-ttu-id="ad60e-483">3 se [ImageQuality](#imagequality) > 0,8; caso contrário, 1</span><span class="sxs-lookup"><span data-stu-id="ad60e-483">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad60e-484">Valor</span><span class="sxs-lookup"><span data-stu-id="ad60e-484">Value</span></span></th>
<th><span data-ttu-id="ad60e-485">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad60e-485">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ad60e-486">3</span><span class="sxs-lookup"><span data-stu-id="ad60e-486">3</span></span></td>
<td><span data-ttu-id="ad60e-487">codificação 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="ad60e-487">4:4:4 encoding.</span></span> <span data-ttu-id="ad60e-488">Preserva a resolução de croma completa.</span><span class="sxs-lookup"><span data-stu-id="ad60e-488">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad60e-489">2</span><span class="sxs-lookup"><span data-stu-id="ad60e-489">2</span></span></td>
<td><span data-ttu-id="ad60e-490">codificação 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="ad60e-490">4:2:2 encoding.</span></span> <span data-ttu-id="ad60e-491">A resolução de croma é 1/2 de resolução de luminância.</span><span class="sxs-lookup"><span data-stu-id="ad60e-491">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad60e-492">1</span><span class="sxs-lookup"><span data-stu-id="ad60e-492">1</span></span></td>
<td><span data-ttu-id="ad60e-493">codificação 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="ad60e-493">4:2:0 encoding.</span></span> <span data-ttu-id="ad60e-494">A resolução de croma é 1/4 de resolução de luminância.</span><span class="sxs-lookup"><span data-stu-id="ad60e-494">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad60e-495">0</span><span class="sxs-lookup"><span data-stu-id="ad60e-495">0</span></span></td>
<td><span data-ttu-id="ad60e-496">codificação 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="ad60e-496">4:0:0 encoding.</span></span> <span data-ttu-id="ad60e-497">Descarta todos os valores de croma e preserva apenas a luminância.</span><span class="sxs-lookup"><span data-stu-id="ad60e-497">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ad60e-498">Esse modo não é recomendado, pois o codec usa uma definição ligeiramente modificada de luminância para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="ad60e-498">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="ad60e-499">Em vez disso, é melhor converter a imagem em monocromático antes da codificação.</span><span class="sxs-lookup"><span data-stu-id="ad60e-499">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ad60e-500">4:2:2 e 4:2:0 preservam os detalhes de luminância às custas dos detalhes da cor.</span><span class="sxs-lookup"><span data-stu-id="ad60e-500">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="ad60e-501">Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="ad60e-501">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="ad60e-502">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="ad60e-502">UseCodecOptions</span></span>

<span data-ttu-id="ad60e-503">Especifica se as propriedades de [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostragem](#subsampling) devem ser usadas em vez da propriedade [ImageQuality](#imagequality) genérica.</span><span class="sxs-lookup"><span data-stu-id="ad60e-503">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="ad60e-504">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-504">Data type</span></span>         | <span data-ttu-id="ad60e-505">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-505">VARTYPE</span></span>      | <span data-ttu-id="ad60e-506">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-506">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="ad60e-507">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-507">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="ad60e-508">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="ad60e-508">**VT\_BOOL**</span></span> | <span data-ttu-id="ad60e-509">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="ad60e-509">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="ad60e-510">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="ad60e-510">VerticalTileSlices</span></span>

<span data-ttu-id="ad60e-511">Define o número de blocos horizontais.</span><span class="sxs-lookup"><span data-stu-id="ad60e-511">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="ad60e-512">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ad60e-512">Data type</span></span>  | <span data-ttu-id="ad60e-513">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad60e-513">VARTYPE</span></span>     | <span data-ttu-id="ad60e-514">Intervalo</span><span class="sxs-lookup"><span data-stu-id="ad60e-514">Range</span></span>  | <span data-ttu-id="ad60e-515">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad60e-515">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="ad60e-516">**NUM**</span><span class="sxs-lookup"><span data-stu-id="ad60e-516">**USHORT**</span></span> | <span data-ttu-id="ad60e-517">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="ad60e-517">**VT\_UI2**</span></span> | <span data-ttu-id="ad60e-518">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="ad60e-518">0–4095</span></span> | <span data-ttu-id="ad60e-519">(altura da imagem – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="ad60e-519">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="ad60e-520">O valor é o número de subdivisões verticais; ou seja, o número de blocos verticais – 1.</span><span class="sxs-lookup"><span data-stu-id="ad60e-520">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="ad60e-521">Formatos de cor com suporte</span><span class="sxs-lookup"><span data-stu-id="ad60e-521">Supported Color Formats</span></span>

<span data-ttu-id="ad60e-522">Para obter mais informações sobre esses formatos, consulte [formatos de pixel nativos](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="ad60e-522">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="ad60e-523">**Formatos de inteiros RGB**</span><span class="sxs-lookup"><span data-stu-id="ad60e-523">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="ad60e-524">\_WICPIXELFORMAT24BPPRGB GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-524">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="ad60e-525">\_WICPIXELFORMAT24BPPBGR GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-525">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="ad60e-526">\_WICPIXELFORMAT32BPPBGR GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-526">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="ad60e-527">\_WICPIXELFORMAT48BPPRGB GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-527">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="ad60e-528">\_WICPIXELFORMAT32BPPBGRA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-528">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="ad60e-529">\_WICPIXELFORMAT64BPPRGBA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-529">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="ad60e-530">\_WICPIXELFORMAT32BPPPBGRA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-530">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="ad60e-531">\_WICPIXELFORMAT64BPPPRGBA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-531">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="ad60e-532">**Formatos RGB de ponto fixo**</span><span class="sxs-lookup"><span data-stu-id="ad60e-532">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="ad60e-533">\_WICPIXELFORMAT48BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-533">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="ad60e-534">\_WICPIXELFORMAT64BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-534">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="ad60e-535">\_WICPIXELFORMAT96BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-535">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="ad60e-536">\_WICPIXELFORMAT128BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-536">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="ad60e-537">\_WICPIXELFORMAT128BPPRGBAFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-537">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="ad60e-538">**Formatos RGB de ponto flutuante**</span><span class="sxs-lookup"><span data-stu-id="ad60e-538">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="ad60e-539">\_WICPIXELFORMAT48BPPRGBHALF GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-539">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="ad60e-540">\_WICPIXELFORMAT64BPPRGBHALF GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-540">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="ad60e-541">\_WICPIXELFORMAT128BPPRGBFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-541">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="ad60e-542">\_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-542">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="ad60e-543">\_WICPIXELFORMAT64BPPRGBAHALF GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-543">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="ad60e-544">\_WICPIXELFORMAT128BPPRGBAFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-544">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="ad60e-545">\_WICPIXELFORMAT128BPPPRGBAFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-545">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="ad60e-546">**Formatos em escala de cinza**</span><span class="sxs-lookup"><span data-stu-id="ad60e-546">**Grayscale formats**</span></span>
    -   <span data-ttu-id="ad60e-547">\_WICPIXELFORMAT8BPPGRAY GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-547">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="ad60e-548">\_WICPIXELFORMAT16BPPGRAY GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-548">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="ad60e-549">\_WICPIXELFORMAT16BPPGRAYFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-549">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="ad60e-550">\_WICPIXELFORMAT16BPPGRAYHALF GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-550">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="ad60e-551">\_WICPIXELFORMAT32BPPGRAYFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-551">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="ad60e-552">\_WICPIXELFORMAT32BPPGRAYFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-552">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="ad60e-553">**Formatos empacotados**</span><span class="sxs-lookup"><span data-stu-id="ad60e-553">**Packed formats**</span></span>
    -   <span data-ttu-id="ad60e-554">\_WICPIXELFORMAT16BPPBGR555 GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-554">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="ad60e-555">\_WICPIXELFORMAT16BPPBGR565 GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-555">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="ad60e-556">\_WICPIXELFORMAT32BPPBGR101010 GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-556">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="ad60e-557">\_WICPIXELFORMAT32BPPRGBE GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-557">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="ad60e-558">**Formatos CMYK**</span><span class="sxs-lookup"><span data-stu-id="ad60e-558">**CMYK formats**</span></span>
    -   <span data-ttu-id="ad60e-559">\_WICPIXELFORMAT40BPPCMYKALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-559">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="ad60e-560">\_WICPIXELFORMAT64BPPCMYK GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-560">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="ad60e-561">\_WICPIXELFORMAT80BPPCMYKALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-561">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="ad60e-562">**Formatos de N canais**</span><span class="sxs-lookup"><span data-stu-id="ad60e-562">**N-channel formats**</span></span>
    -   <span data-ttu-id="ad60e-563">\_WICPIXELFORMAT32BPP4CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-563">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="ad60e-564">\_WICPIXELFORMAT40BPP5CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-564">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="ad60e-565">\_WICPIXELFORMAT48BPP6CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-565">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="ad60e-566">\_WICPIXELFORMAT56BPP7CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-566">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="ad60e-567">\_WICPIXELFORMAT64BPP8CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-567">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="ad60e-568">\_WICPIXELFORMAT32BPP3CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-568">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-569">\_WICPIXELFORMAT40BPP4CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-569">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-570">\_WICPIXELFORMAT48BPP5CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-570">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-571">\_WICPIXELFORMAT56BPP6CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-571">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-572">\_WICPIXELFORMAT64BPP7CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-572">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-573">\_WICPIXELFORMAT72BPP8CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-573">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-574">\_WICPIXELFORMAT48BPP3CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-574">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="ad60e-575">\_WICPIXELFORMAT64BPP4CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-575">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="ad60e-576">\_WICPIXELFORMAT80BPP5CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-576">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="ad60e-577">\_WICPIXELFORMAT96BPP6CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-577">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="ad60e-578">\_WICPIXELFORMAT128BPP8CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-578">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="ad60e-579">\_WICPIXELFORMAT64BPP3CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-579">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-580">\_WICPIXELFORMAT80BPP4CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-580">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-581">\_WICPIXELFORMAT96BPP5CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-581">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-582">\_WICPIXELFORMAT112BPP6CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-582">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-583">\_WICPIXELFORMAT128BPP7CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-583">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="ad60e-584">\_WICPIXELFORMAT144BPP8CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="ad60e-584">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
