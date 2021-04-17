---
description: O codec JPEG XR nativo está disponível por meio do Windows Imaging Component (WIC). O formato JPEG XR, ao qual o codec dá suporte, foi projetado para fotografias digitais de consumidores e profissionais.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Visão geral do codec do JPEG XR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784664"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="e1ae3-104">Visão geral do codec do JPEG XR</span><span class="sxs-lookup"><span data-stu-id="e1ae3-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="e1ae3-105">O codec JPEG XR nativo está disponível por meio do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="e1ae3-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="e1ae3-106">O formato JPEG XR, ao qual o codec dá suporte, foi projetado para fotografias digitais de consumidores e profissionais.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="e1ae3-107">O formato JPEG XR pode atingir até duas vezes a eficiência da compactação do formato JPEG original, com artefatos de compactação menos perceptíveis.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="e1ae3-108">Os recursos do JPEG XR incluem:</span><span class="sxs-lookup"><span data-stu-id="e1ae3-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="e1ae3-109">Suporte para imagens monocromáticas, RGB, CMYK e n-Channel</span><span class="sxs-lookup"><span data-stu-id="e1ae3-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="e1ae3-110">formatos de inteiro de 8, 16 e 32 bits</span><span class="sxs-lookup"><span data-stu-id="e1ae3-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="e1ae3-111">Alto intervalo dinâmico, formatos de ampla gama, usando valores de cores de ponto fixo ou ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="e1ae3-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="e1ae3-112">Decodificação progressiva</span><span class="sxs-lookup"><span data-stu-id="e1ae3-112">Progressive decoding</span></span>
-   <span data-ttu-id="e1ae3-113">Codificação com perdas ou sem perdas usando o mesmo algoritmo de compactação</span><span class="sxs-lookup"><span data-stu-id="e1ae3-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="e1ae3-114">Suporte para decodificação de regiões de interesse em imagens grandes</span><span class="sxs-lookup"><span data-stu-id="e1ae3-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="e1ae3-115">O formato JPEG XR é definido nos seguintes documentos de padrões:</span><span class="sxs-lookup"><span data-stu-id="e1ae3-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="e1ae3-116">ITU-T T. 832: *tecnologia da informação – sistema de codificação de imagem JPEG XR – especificação de codificação de imagem*</span><span class="sxs-lookup"><span data-stu-id="e1ae3-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="e1ae3-117">ISO/IEC 29199-2:2010: *tecnologia da informação – sistema de codificação de imagem JPEG XR – parte 2: especificação de codificação de imagem*</span><span class="sxs-lookup"><span data-stu-id="e1ae3-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="e1ae3-118">O JPEG XR Standard é amplamente baseado no formato [HD Photo](hdphoto-format-overview.md) , mas há algumas diferenças entre os dois formatos.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="e1ae3-119">No Windows 8, o HD Photo codec foi atualizado para dar suporte a JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="e1ae3-120">O codificador agora sempre gera um fluxo de bits compatível com o JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="e1ae3-121">O decodificador pode decodificar imagens JPEG XR e HD Photo.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="e1ae3-122">Melhorias de desempenho substanciais, em relação ao codec HD Photo, foram feitas no codec JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="e1ae3-123">Por exemplo, a decodificação de imagem de subresolução, como geração de miniaturas, foi aprimorada, bem como decodificação de imagem de baixa resolução.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="e1ae3-124">É recomendável que você use o formato JPEG XR em vez do formato HD Photo.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="e1ae3-125">Informações do codec</span><span class="sxs-lookup"><span data-stu-id="e1ae3-125">Codec Information</span></span>



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e1ae3-126">Extensão de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-126">File name extension</span></span> | <span data-ttu-id="e1ae3-127">"jxr" e "WDP"</span><span class="sxs-lookup"><span data-stu-id="e1ae3-127">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="e1ae3-128">GUID do contêiner</span><span class="sxs-lookup"><span data-stu-id="e1ae3-128">Container GUID</span></span>      | <span data-ttu-id="e1ae3-129">**\_CONTAINERFORMATWMP GUID**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-129">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="e1ae3-130">GUID do decodificador</span><span class="sxs-lookup"><span data-stu-id="e1ae3-130">Decoder GUID</span></span>        | <span data-ttu-id="e1ae3-131">**\_WICWMPDECODER CLSID**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-131">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="e1ae3-132">GUID do codificador</span><span class="sxs-lookup"><span data-stu-id="e1ae3-132">Encoder GUID</span></span>        | <span data-ttu-id="e1ae3-133">**\_WICWMPENCODER CLSID**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-133">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="e1ae3-134">Suporte a perfil</span><span class="sxs-lookup"><span data-stu-id="e1ae3-134">Profile Support</span></span>     | <span data-ttu-id="e1ae3-135">O codificador e o decodificador suportam até o perfil principal e até o nível 128.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-135">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="e1ae3-136">Recursos do codec</span><span class="sxs-lookup"><span data-stu-id="e1ae3-136">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="e1ae3-137">Intervalo dinâmico alto</span><span class="sxs-lookup"><span data-stu-id="e1ae3-137">High Dynamic Range</span></span>

<span data-ttu-id="e1ae3-138">O JPEG XR dá suporte a imagens de intervalo alto-dinâmicas, usando cores de ponto ou de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-138">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="e1ae3-139">Nesses formatos de cor, o intervalo numérico de um pixel é maior do que o intervalo visível, de modo que você pode ajustar as cores acima ou abaixo do intervalo visível durante os estágios de processamento intermediário.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-139">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="e1ae3-140">Ponto fixo: em uma representação de ponto fixo, 0 representa preto e 1,0 representa a saturação máxima.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-140">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="e1ae3-141">O codec do JPEG XR dá suporte a formatos de ponto fixo de 16 bits e 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-141">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="e1ae3-142">Para 16 bits, 1,0 = 0x2000h, que fornece 13 bits para o intervalo visível \[ 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-142">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="e1ae3-143">O intervalo total é de – 4,0 a + 3,999 e é mapeado linearmente.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-143">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="e1ae3-144">Para 32 bits, 1,0 = 0x01000000h, o intervalo visível é de 24 bits e o intervalo total é de – 128 a + 127,999.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-144">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="e1ae3-145">Ponto flutuante: em uma representação de ponto flutuante, 0 representa preto e 1,0 representa a saturação máxima.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-145">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="e1ae3-146">O codec do JPEG XR dá suporte a formatos de ponto flutuante de 16 bits e 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-146">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="e1ae3-147">Blocos</span><span class="sxs-lookup"><span data-stu-id="e1ae3-147">Tiles</span></span>

<span data-ttu-id="e1ae3-148">Um quadro pode ser particionado em subregiãos retangulares chamadas *blocos*.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-148">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="e1ae3-149">Um bloco é uma área de uma imagem que contém matrizes retangulares de macroblocos.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-149">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="e1ae3-150">Os blocos permitem que regiões da imagem sejam decodificadas sem processar a imagem inteira.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-150">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="e1ae3-151">Durante a codificação, selecione o número de blocos definindo as propriedades **HorizontalTileSlices** e **VerticalTileSlices** .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-151">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="e1ae3-152">O tamanho mínimo do bloco é 16 × 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-152">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="e1ae3-153">O codificador ajusta o número de blocos para manter essa restrição.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-153">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="e1ae3-154">Há sobrecarga de armazenamento e processamento associada a cada bloco, portanto, você deve considerar o número de blocos necessários para cenários específicos.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-154">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="e1ae3-155">Saída de fluxo de imagem</span><span class="sxs-lookup"><span data-stu-id="e1ae3-155">Image Stream Output</span></span>

<span data-ttu-id="e1ae3-156">O padrão JPEG-XR define duas partes de um arquivo JPEG-XR:</span><span class="sxs-lookup"><span data-stu-id="e1ae3-156">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="e1ae3-157">O fluxo de bits de imagem, definido no corpo do padrão.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-157">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="e1ae3-158">O contêiner da imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-158">The image container.</span></span> <span data-ttu-id="e1ae3-159">O arquivo contém metadados EXIF e XMP e é definido no anexo A do padrão.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-159">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="e1ae3-160">Ele é possível e permitido pelo padrão, para inserir o fluxo de imagem dentro de outro tipo de contêiner de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-160">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="e1ae3-161">O codificador dá suporte a um modo somente de fluxo, que gera o fluxo de bits de imagem bruto sem contêiner de imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-161">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="e1ae3-162">Um aplicativo pode armazenar o fluxo de bits em algum outro formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-162">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="e1ae3-163">Para habilitar o modo somente fluxo, defina a propriedade **StreamOnly** .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-163">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="e1ae3-164">Configurações de qualidade da imagem</span><span class="sxs-lookup"><span data-stu-id="e1ae3-164">Image Quality Settings</span></span>

<span data-ttu-id="e1ae3-165">Várias propriedades de codec controlam a qualidade da imagem de saída do codificador.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-165">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="e1ae3-166">[ImageQuality](#imagequality) é uma propriedade comum entre os codecs do WIC.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-166">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="e1ae3-167">Ele especifica a qualidade da imagem como um único valor de ponto flutuante de 0,0 a 1,0,</span><span class="sxs-lookup"><span data-stu-id="e1ae3-167">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="e1ae3-168">As propriedades [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostragem](#subsampling) fornecem mais controle sobre as configurações de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-168">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="e1ae3-169">Para usar as propriedades [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostrar](#subsampling) , defina a propriedade [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-169">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="e1ae3-170">Se [UseCodecOptions](#usecodecoptions) for **Variant \_ false** (**Variant \_ false** é o padrão), o codificador usará a propriedade [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-170">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="e1ae3-171">O codificador mapeia o valor de ImageQuality para [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostrar](#subsampling) por meio de uma tabela de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-171">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="e1ae3-172">O codificador não oferece suporte à propriedade **CompressionQuality** .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-172">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="e1ae3-173">Transcodificação de domínio compactado</span><span class="sxs-lookup"><span data-stu-id="e1ae3-173">Compressed Domain Transcode</span></span>

<span data-ttu-id="e1ae3-174">O codec do JPEG XR pode executar determinadas transformações de imagem sem, na verdade, decodificar os dados compactados e codificá-los novamente.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-174">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="e1ae3-175">As operações de domínio compactadas são muito eficientes e evitam qualquer perda de qualidade adicional que seja típica quando você decodifica e codifica novamente uma imagem compactada com perdas.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-175">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="e1ae3-176">Há suporte para as seguintes operações de domínio compactado:</span><span class="sxs-lookup"><span data-stu-id="e1ae3-176">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="e1ae3-177">Corte uma região da imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-177">Crop a region of the image.</span></span>
-   <span data-ttu-id="e1ae3-178">Girar ou inverter a imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-178">Rotate or flip the image.</span></span>
-   <span data-ttu-id="e1ae3-179">Descartar dados de frequência para criar um arquivo de imagem menor.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-179">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="e1ae3-180">Reorganizar a imagem entre a ordem espacial e de frequência.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-180">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="e1ae3-181">O codificador do JPEG XR usa transcodificação de domínio compactado, se possível, quando a imagem de origem é uma imagem JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-181">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="e1ae3-182">Quando o codificador executa uma operação de domínio compactado, ele ignora as seguintes propriedades de codec: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha),[sobreposição](#overlap) [sem perdas](#lossless)e [qualidade](#image-quality-settings).</span><span class="sxs-lookup"><span data-stu-id="e1ae3-182">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="e1ae3-183">Se as propriedades [HorizontalTileSlices](/windows) e [VerticalTileSlices](/windows) estiverem presentes, você deverá defini-las como zero.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-183">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="e1ae3-184">Você não pode alterar o tamanho de bloco de uma imagem como parte de uma transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-184">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="e1ae3-185">A lista a seguir descreve como executar as transformações de imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-185">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="e1ae3-186">Para cortar a imagem, defina a região desejada no parâmetro [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) do método **WriteState** .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-186">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="e1ae3-187">Para girar ou inverter a imagem, defina a propriedade [BitmapTransform](#bitmaptransform) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-187">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="e1ae3-188">Para descartar dados de frequência na imagem, defina a propriedade [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-188">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="e1ae3-189">Para descartar dados de frequência no canal alfa, defina a propriedade [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-189">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="e1ae3-190">A descartação de dados de frequência reduz o tamanho do arquivo codificado e pode reduzir a resolução.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-190">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="e1ae3-191">Para alterar a organização da imagem entre frequência e ordenação espacial, defina a propriedade [FrequencyOrdering](/windows) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-191">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="e1ae3-192">Para desabilitar a transcodificação de domínio compactado e forçar o codificador a codificar novamente a imagem, defina [UseCodecOptions](#usecodecoptions) como **Variant \_ true** e defina [CompressedDomainTranscode](#compresseddomaintranscode) como **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-192">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="e1ae3-193">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="e1ae3-193">Encoder Options</span></span>

<span data-ttu-id="e1ae3-194">Para definir as propriedades de codificação, use a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-194">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="e1ae3-195">Para obter mais informações, consulte [visão geral da codificação](-wic-creating-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e1ae3-195">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="e1ae3-196">A lista a seguir especifica as opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-196">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="e1ae3-197">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="e1ae3-197">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="e1ae3-198">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="e1ae3-198">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="e1ae3-199">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="e1ae3-199">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="e1ae3-200">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="e1ae3-200">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="e1ae3-201">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="e1ae3-201">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="e1ae3-202">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="e1ae3-202">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="e1ae3-203">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="e1ae3-203">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="e1ae3-204">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="e1ae3-204">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="e1ae3-205">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="e1ae3-205">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="e1ae3-206">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="e1ae3-206">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="e1ae3-207">Lossless</span><span class="sxs-lookup"><span data-stu-id="e1ae3-207">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="e1ae3-208">Post</span><span class="sxs-lookup"><span data-stu-id="e1ae3-208">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="e1ae3-209">Progressivmode</span><span class="sxs-lookup"><span data-stu-id="e1ae3-209">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="e1ae3-210">Qualidade</span><span class="sxs-lookup"><span data-stu-id="e1ae3-210">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="e1ae3-211">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="e1ae3-211">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="e1ae3-212">Subamostragens</span><span class="sxs-lookup"><span data-stu-id="e1ae3-212">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="e1ae3-213">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="e1ae3-213">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="e1ae3-214">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="e1ae3-214">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="e1ae3-215">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="e1ae3-215">AlphaDataDiscard</span></span>

<span data-ttu-id="e1ae3-216">Define a quantidade de dados de frequência Alfa a serem descartados durante uma transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-216">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="e1ae3-217">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-217">Data type</span></span> | <span data-ttu-id="e1ae3-218">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-218">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-219">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-219">Range</span></span> | <span data-ttu-id="e1ae3-220">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-220">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="e1ae3-221">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-221">**UCHAR**</span></span> | <span data-ttu-id="e1ae3-222">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-222">**VT\_UI1**</span></span> | <span data-ttu-id="e1ae3-223">0 a 4</span><span class="sxs-lookup"><span data-stu-id="e1ae3-223">0–4</span></span>   | <span data-ttu-id="e1ae3-224">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e1ae3-224">None</span></span>    |



 

<span data-ttu-id="e1ae3-225">Essa propriedade só se aplicará se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true** e a imagem contiver um canal planar ou um canal alfa intercalado. caso contrário, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-225">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="e1ae3-226">Para imagens que contêm um canal do planar, os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-226">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="e1ae3-227">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae3-227">Value</span></span> | <span data-ttu-id="e1ae3-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae3-228">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ae3-229">0</span><span class="sxs-lookup"><span data-stu-id="e1ae3-229">0</span></span>     | <span data-ttu-id="e1ae3-230">Nenhum dado de frequência de imagem é Descartado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-230">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e1ae3-231">1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-231">1</span></span>     | <span data-ttu-id="e1ae3-232">Os FlexBits são descartados.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-232">The flexbits are discarded.</span></span> <span data-ttu-id="e1ae3-233">Isso reduz arbitrariamente a qualidade do canal do planar alfa para a imagem transcodificada.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-233">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="e1ae3-234">, sem uma alteração na resolução efetiva.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-234">, without a change in the effective resolution.</span></span> <span data-ttu-id="e1ae3-235">A redução exata no tamanho do arquivo e na qualidade depende de vários fatores e não pode ser especificada com exatidão.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-235">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="e1ae3-236">2</span><span class="sxs-lookup"><span data-stu-id="e1ae3-236">2</span></span>     | <span data-ttu-id="e1ae3-237">A banda de dados de frequência de passagem alta é descartada, incluindo o FlexBits.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-237">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="e1ae3-238">Isso reduz efetivamente a resolução do canal do planar alfa por um fator de 4 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-238">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="e1ae3-239">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada bloco 4x4 de pixels de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-239">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="e1ae3-240">Normalmente, você deve definir esse valor somente quando a propriedade [ImageDataDiscard](#imagedatadiscard) tiver o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-240">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="e1ae3-241">3</span><span class="sxs-lookup"><span data-stu-id="e1ae3-241">3</span></span>     | <span data-ttu-id="e1ae3-242">As faixas de dados de frequência de passagem alta e baixa são descartadas, incluindo o FlexBits.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-242">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="e1ae3-243">Esse ffectively reduz a resolução do canal do planar alfa por um fator de 16 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-243">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="e1ae3-244">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada 16x16 macrobloco de pixels de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-244">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="e1ae3-245">Normalmente, você deve definir esse valor somente quando a propriedade [ImageDataDiscard](#imagedatadiscard) tiver o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-245">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="e1ae3-246">4</span><span class="sxs-lookup"><span data-stu-id="e1ae3-246">4</span></span>     | <span data-ttu-id="e1ae3-247">O canal alfa é completamente Descartado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-247">The alpha channel is completely discarded.</span></span> <span data-ttu-id="e1ae3-248">O formato de pixel da imagem transcodificada é alterado para refletir a remoção do canal alfa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-248">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="e1ae3-249">Para imagens que contêm um canal alfa intercalado, o valor a seguir é válido.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-249">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="e1ae3-250">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae3-250">Value</span></span> | <span data-ttu-id="e1ae3-251">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae3-251">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ae3-252">4</span><span class="sxs-lookup"><span data-stu-id="e1ae3-252">4</span></span>     | <span data-ttu-id="e1ae3-253">O canal alfa é completamente Descartado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-253">The alpha channel is completely discarded.</span></span> <span data-ttu-id="e1ae3-254">O formato de pixel da imagem transcodificada é alterado para refletir a remoção do canal alfa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-254">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="e1ae3-255">Para alfa intercalado, a menos que essa propriedade seja definida como 4, o canal alfa é processado da mesma forma que os dados da imagem, de acordo com o valor da propriedade [ImageDataDiscard](#imagedatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-255">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="e1ae3-256">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="e1ae3-256">AlphaQuality</span></span>

<span data-ttu-id="e1ae3-257">Define a qualidade de compactação para a imagem do canal alfa do planar.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-257">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="e1ae3-258">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-258">Data type</span></span> | <span data-ttu-id="e1ae3-259">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-259">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-260">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-260">Range</span></span> | <span data-ttu-id="e1ae3-261">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-261">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="e1ae3-262">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-262">**UCHAR**</span></span> | <span data-ttu-id="e1ae3-263">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-263">**VT\_UI1**</span></span> | <span data-ttu-id="e1ae3-264">1 a 255</span><span class="sxs-lookup"><span data-stu-id="e1ae3-264">1–255</span></span> | <span data-ttu-id="e1ae3-265">1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-265">1</span></span>       |



 

<span data-ttu-id="e1ae3-266">Essa propriedade se aplica quando a imagem tem um canal alfa e a propriedade [InterleavedAlpha](#interleavedalpha) é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-266">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="e1ae3-267">O valor 1 indica o modo sem perdas.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-267">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="e1ae3-268">Os valores crescentes resultam em taxas de compactação mais altas e qualidade de imagem inferior.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-268">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="e1ae3-269">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="e1ae3-269">BitmapTransform</span></span>

<span data-ttu-id="e1ae3-270">Especifica se a imagem é girada ou invertida quando decodificada.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-270">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="e1ae3-271">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-271">Data type</span></span> | <span data-ttu-id="e1ae3-272">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-272">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-273">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-273">Range</span></span>                                                                     | <span data-ttu-id="e1ae3-274">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-274">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="e1ae3-275">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-275">**UCHAR**</span></span> | <span data-ttu-id="e1ae3-276">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-276">**VT\_UI1**</span></span> | [<span data-ttu-id="e1ae3-277">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-277">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="e1ae3-278">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-278">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="e1ae3-279">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="e1ae3-279">CompressedDomainTranscode</span></span>

<span data-ttu-id="e1ae3-280">Habilita ou desabilita a transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-280">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="e1ae3-281">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-281">Data type</span></span>         | <span data-ttu-id="e1ae3-282">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-282">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-283">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-283">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="e1ae3-284">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-284">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-285">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-285">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-286">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-286">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="e1ae3-287">Para desabilitar operações de domínio compactado, defina essa propriedade como **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-287">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="e1ae3-288">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="e1ae3-288">FrequencyOrder</span></span>

<span data-ttu-id="e1ae3-289">Habilita a codificação na ordem de frequência.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-289">Enables encoding in frequency order.</span></span> <span data-ttu-id="e1ae3-290">Implementações de dispositivo de codificadores JPEG XR podem organizar um arquivo em ordem espacial para reduzir a memória necessária durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-290">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="e1ae3-291">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-291">Data type</span></span>         | <span data-ttu-id="e1ae3-292">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-292">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-293">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-293">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="e1ae3-294">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-294">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-295">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-295">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-296">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-296">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="e1ae3-297">**Variante \_ TRUE**: ordem de frequência.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-297">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="e1ae3-298">Os dados de frequência mais baixos aparecem primeiro no arquivo, e o conteúdo da imagem é agrupado por sua frequência, em vez de sua orientação espacial.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-298">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="e1ae3-299">Organizar um arquivo por ordem de frequência fornece o melhor desempenho para qualquer decodificação baseada em frequência.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-299">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="e1ae3-300">**Variante \_ FALSE**: ordem espacial.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-300">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="e1ae3-301">A ordem espacial reduz a memória necessária durante a codificação</span><span class="sxs-lookup"><span data-stu-id="e1ae3-301">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="e1ae3-302">A ordem de frequência é recomendada, a menos que você tenha motivos específicos de desempenho ou de aplicativo para usar a ordem espacial.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-302">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="e1ae3-303">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="e1ae3-303">HorizontalTileSlices</span></span>

<span data-ttu-id="e1ae3-304">Define o número de blocos horizontais.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-304">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="e1ae3-305">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-305">Data type</span></span>  | <span data-ttu-id="e1ae3-306">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-306">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-307">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-307">Range</span></span>  | <span data-ttu-id="e1ae3-308">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-308">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="e1ae3-309">**NUM**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-309">**USHORT**</span></span> | <span data-ttu-id="e1ae3-310">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-310">**VT\_UI2**</span></span> | <span data-ttu-id="e1ae3-311">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="e1ae3-311">0–4095</span></span> | <span data-ttu-id="e1ae3-312">(largura da imagem – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="e1ae3-312">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="e1ae3-313">O valor é o número de subdivisões horizontais; ou seja, o número de blocos horizontais – 1.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-313">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="e1ae3-314">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="e1ae3-314">IgnoreOverlap</span></span>

<span data-ttu-id="e1ae3-315">Especifica como o codificador trata os limites de bloco durante uma transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-315">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="e1ae3-316">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-316">Data type</span></span>         | <span data-ttu-id="e1ae3-317">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-317">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-318">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-318">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="e1ae3-319">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-319">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-320">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-320">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-321">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-321">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="e1ae3-322">Essa propriedade será aplicada somente se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true** e uma transcodificação de sub-região de exatamente um ou mais blocos for executada.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-322">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="e1ae3-323">A operação padrão para uma transcodificação de região é expandir a região solicitada para incluir os pixels adjacentes que são necessários para sobrepor a decodificação das bordas da região.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-323">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="e1ae3-324">Se essa propriedade for definida como **Variant \_ true**, o codec ignorará os pixels adjacentes e apenas o bloco ou blocos selecionados serão extraídos.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-324">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="e1ae3-325">Se a imagem de origem não for um lado ou se a região solicitada incluir blocos parciais, esse parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-325">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="e1ae3-326">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="e1ae3-326">ImageDataDiscard</span></span>

<span data-ttu-id="e1ae3-327">Define a quantidade de dados de frequência de imagem a serem descartados durante uma transcodificação de domínio compactado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-327">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="e1ae3-328">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-328">Data type</span></span> | <span data-ttu-id="e1ae3-329">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-329">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-330">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-330">Range</span></span> | <span data-ttu-id="e1ae3-331">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-331">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="e1ae3-332">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-332">**UCHAR**</span></span> | <span data-ttu-id="e1ae3-333">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-333">**VT\_UI1**</span></span> | <span data-ttu-id="e1ae3-334">0 a 3</span><span class="sxs-lookup"><span data-stu-id="e1ae3-334">0–3</span></span>   | <span data-ttu-id="e1ae3-335">0</span><span class="sxs-lookup"><span data-stu-id="e1ae3-335">0</span></span>       |



 

<span data-ttu-id="e1ae3-336">Essa propriedade só se aplicará se a propriedade [CompressedDomainTranscode](#compresseddomaintranscode) estiver definida como **Variant \_ true**; caso contrário, será ignorada.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-336">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="e1ae3-337">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae3-337">Value</span></span> | <span data-ttu-id="e1ae3-338">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae3-338">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ae3-339">0</span><span class="sxs-lookup"><span data-stu-id="e1ae3-339">0</span></span>     | <span data-ttu-id="e1ae3-340">Nenhum dado de frequência de imagem é Descartado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-340">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e1ae3-341">1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-341">1</span></span>     | <span data-ttu-id="e1ae3-342">Os FlexBits são descartados.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-342">The flexbits are discarded.</span></span> <span data-ttu-id="e1ae3-343">Isso reduz arbitrariamente a qualidade da imagem transcodificada sem alterar a resolução efetiva da imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-343">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="e1ae3-344">A redução exata no tamanho do arquivo e na qualidade depende de vários fatores e não pode ser especificada com exatidão.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-344">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="e1ae3-345">Esse valor retorna um erro especificado para um canal alfa intercalado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-345">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="e1ae3-346">2</span><span class="sxs-lookup"><span data-stu-id="e1ae3-346">2</span></span>     | <span data-ttu-id="e1ae3-347">A banda de dados de frequência de passagem alta é descartada, incluindo o FlexBits.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-347">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="e1ae3-348">Isso reduz a resolução da imagem transcodificada por um fator de 4 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-348">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="e1ae3-349">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada bloco de pixels 4x4.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-349">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="e1ae3-350">Portanto, a imagem transcodificada deve ser downsampledda adequadamente sempre que for decodificada.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-350">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="e1ae3-351">3</span><span class="sxs-lookup"><span data-stu-id="e1ae3-351">3</span></span>     | <span data-ttu-id="e1ae3-352">As faixas de dados de frequência de passagem alta e baixa são descartadas, incluindo o FlexBits.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-352">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="e1ae3-353">Isso reduz a resolução da imagem transcodificada por um fator de 16 em ambas as dimensões.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-353">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="e1ae3-354">As dimensões reais da imagem transcodificada permanecem as mesmas, mas a imagem perde todos os detalhes em cada 16x16 macrobloco de pixels.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-354">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="e1ae3-355">Portanto, a imagem transcodificada deve ser downsampledda adequadamente sempre que for decodificada.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-355">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="e1ae3-356">Se a imagem contiver um canal alfa intercalado, o valor de [ImageDataDiscard](#imagedatadiscard) será aplicado ao canal alfa, a menos que a propriedade [AlphaDataDiscard](#alphadatadiscard) esteja definida como 4; nesse caso, o canal alfa será Descartado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-356">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="e1ae3-357">Para o planar alfa, os dados de frequência descartados são controlados pela propriedade [AlphaDataDiscard](#alphadatadiscard) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-357">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="e1ae3-358">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="e1ae3-358">ImageQuality</span></span>

<span data-ttu-id="e1ae3-359">Define a qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-359">Sets the image quality.</span></span>



| <span data-ttu-id="e1ae3-360">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-360">Data type</span></span> | <span data-ttu-id="e1ae3-361">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-361">VARTYPE</span></span>    | <span data-ttu-id="e1ae3-362">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-362">Range</span></span> | <span data-ttu-id="e1ae3-363">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-363">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="e1ae3-364">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-364">**FLOAT**</span></span> | <span data-ttu-id="e1ae3-365">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-365">**VT\_R4**</span></span> | <span data-ttu-id="e1ae3-366">0 a 1,0</span><span class="sxs-lookup"><span data-stu-id="e1ae3-366">0–1.0</span></span> | <span data-ttu-id="e1ae3-367">0,9</span><span class="sxs-lookup"><span data-stu-id="e1ae3-367">0.9</span></span>     |



 

<span data-ttu-id="e1ae3-368">O nível 1,0 oferece uma compactação matematicamente sem perdas.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-368">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="e1ae3-369">O nível 0,0 é a configuração de qualidade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-369">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="e1ae3-370">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="e1ae3-370">InterleavedAlpha</span></span>

<span data-ttu-id="e1ae3-371">Especifica se deve codificar alfa ou planar intercalado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-371">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="e1ae3-372">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-372">Data type</span></span>         | <span data-ttu-id="e1ae3-373">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-373">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-374">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-374">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="e1ae3-375">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-375">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-376">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-376">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-377">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-377">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="e1ae3-378">**Variante \_ TRUE**: Alpha intercalado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-378">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="e1ae3-379">As informações do canal alfa são codificadas como um canal intercalado adicional, sem correlação com os canais de conteúdo da imagem.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-379">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="e1ae3-380">Esse modo é útil para decodificar alfa simultaneamente com a imagem quando a imagem é transmitida.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-380">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="e1ae3-381">VARIANTE \_ false: planar alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-381">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="e1ae3-382">Um canal alfanumérico planar é codificado como uma imagem separada.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-382">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="e1ae3-383">Os dados da imagem e o canal alfa são decodificados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-383">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="e1ae3-384">Opcionalmente, você pode definir o nível de qualidade do canal alfa definindo a propriedade [AlphaQuality](#alphaquality) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-384">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="e1ae3-385">Há suporte para alfa intercalado apenas para determinados formatos de pixel RGB.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-385">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="e1ae3-386">O planar alfanumérico tem suporte para qualquer formato de imagem que define um canal alfa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-386">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="e1ae3-387">Lossless</span><span class="sxs-lookup"><span data-stu-id="e1ae3-387">Lossless</span></span>

<span data-ttu-id="e1ae3-388">Habilita a compactação de perdas.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-388">Enables losses compression.</span></span>



| <span data-ttu-id="e1ae3-389">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-389">Data type</span></span>         | <span data-ttu-id="e1ae3-390">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-390">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-391">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-391">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="e1ae3-392">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-392">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-393">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-393">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-394">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="e1ae3-394">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="e1ae3-395">Se o valor for **Variant \_ true**, o codificador usará a compactação sem perdas.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-395">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="e1ae3-396">Quando definido como **Variant \_ true**, essa propriedade substitui a propriedade [ImageQuality](#imagequality) .</span><span class="sxs-lookup"><span data-stu-id="e1ae3-396">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="e1ae3-397">Post</span><span class="sxs-lookup"><span data-stu-id="e1ae3-397">Overlap</span></span>

<span data-ttu-id="e1ae3-398">Define o nível de filtragem de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-398">Sets the level of overlap filtering.</span></span> <span data-ttu-id="e1ae3-399">Com a filtragem de sobreposição, os coeficientes de transformação são aplicados entre limites de bloco e macrobloco.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-399">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="e1ae3-400">Isso pode reduzir os artefatos de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-400">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="e1ae3-401">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-401">Data type</span></span> | <span data-ttu-id="e1ae3-402">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-402">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-403">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-403">Range</span></span> | <span data-ttu-id="e1ae3-404">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-404">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="e1ae3-405">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-405">**UCHAR**</span></span> | <span data-ttu-id="e1ae3-406">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-406">**VT\_UI1**</span></span> | <span data-ttu-id="e1ae3-407">0 a 4</span><span class="sxs-lookup"><span data-stu-id="e1ae3-407">0–4</span></span>   | <span data-ttu-id="e1ae3-408">1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-408">1</span></span>       |



 



| <span data-ttu-id="e1ae3-409">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae3-409">Value</span></span> | <span data-ttu-id="e1ae3-410">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae3-410">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="e1ae3-411">0</span><span class="sxs-lookup"><span data-stu-id="e1ae3-411">0</span></span>     | <span data-ttu-id="e1ae3-412">Sem sobreposição.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-412">No overlap.</span></span>                                   |
| <span data-ttu-id="e1ae3-413">1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-413">1</span></span>     | <span data-ttu-id="e1ae3-414">Um nível de sobreposição, divisão suave.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-414">One level of overlap, soft tiling.</span></span> <span data-ttu-id="e1ae3-415">(Padrão.)</span><span class="sxs-lookup"><span data-stu-id="e1ae3-415">(Default.)</span></span> |
| <span data-ttu-id="e1ae3-416">2</span><span class="sxs-lookup"><span data-stu-id="e1ae3-416">2</span></span>     | <span data-ttu-id="e1ae3-417">Dois níveis de sobreposição, divisão suave.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-417">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="e1ae3-418">3</span><span class="sxs-lookup"><span data-stu-id="e1ae3-418">3</span></span>     | <span data-ttu-id="e1ae3-419">Um nível de sobreposição, divisão fixa</span><span class="sxs-lookup"><span data-stu-id="e1ae3-419">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="e1ae3-420">4</span><span class="sxs-lookup"><span data-stu-id="e1ae3-420">4</span></span>     | <span data-ttu-id="e1ae3-421">Dois níveis de sobreposição, divisão fixa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-421">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="e1ae3-422">Definições:</span><span class="sxs-lookup"><span data-stu-id="e1ae3-422">Definitions:</span></span>

-   <span data-ttu-id="e1ae3-423">Um nível de sobreposição: os valores codificados dos blocos 4x4 são modificados com base em blocos vizinhos.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-423">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="e1ae3-424">Dois níveis de sobreposição: o primeiro nível de sobreposição é aplicado.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-424">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="e1ae3-425">Além disso, os valores codificados de 16x16 macroblocos são modificados com base no macroblocos vizinho.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-425">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="e1ae3-426">Divisão suave: a filtragem de sobreposição é aplicada entre limites de bloco.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-426">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="e1ae3-427">Divisão fixa: a filtragem de sobreposição não é aplicada entre limites de bloco.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-427">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="e1ae3-428">Blocos físicos podem introduzir alguns artefatos visuais ao longo dos limites de bloco.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-428">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="e1ae3-429">Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-429">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="e1ae3-430">Progressivmode</span><span class="sxs-lookup"><span data-stu-id="e1ae3-430">ProgressiveMode</span></span>

<span data-ttu-id="e1ae3-431">Habilita ou desabilita a codificação progressiva.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-431">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="e1ae3-432">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-432">Data type</span></span>         | <span data-ttu-id="e1ae3-433">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-433">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-434">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-434">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="e1ae3-435">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-435">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-436">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-436">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-437">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-437">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="e1ae3-438">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae3-438">Value</span></span>              | <span data-ttu-id="e1ae3-439">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae3-439">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="e1ae3-440">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-440">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="e1ae3-441">Modo sequencial (padrão).</span><span class="sxs-lookup"><span data-stu-id="e1ae3-441">Sequential mode (default).</span></span> |
| <span data-ttu-id="e1ae3-442">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-442">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="e1ae3-443">Modo progressivo.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-443">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="e1ae3-444">Qualidade</span><span class="sxs-lookup"><span data-stu-id="e1ae3-444">Quality</span></span>

<span data-ttu-id="e1ae3-445">Define a qualidade da compactação.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-445">Sets the compression quality.</span></span>



| <span data-ttu-id="e1ae3-446">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-446">Data type</span></span> | <span data-ttu-id="e1ae3-447">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-447">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-448">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-448">Range</span></span> | <span data-ttu-id="e1ae3-449">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-449">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="e1ae3-450">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-450">**UCHAR**</span></span> | <span data-ttu-id="e1ae3-451">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-451">**VT\_UI1**</span></span> | <span data-ttu-id="e1ae3-452">1 a 255</span><span class="sxs-lookup"><span data-stu-id="e1ae3-452">1–255</span></span> | <span data-ttu-id="e1ae3-453">1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-453">1</span></span>       |



 

<span data-ttu-id="e1ae3-454">O valor 1 indica o modo sem perdas.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-454">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="e1ae3-455">Os valores crescentes resultam em taxas de compactação mais altas e qualidade de imagem inferior.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-455">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="e1ae3-456">Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-456">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="e1ae3-457">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="e1ae3-457">StreamOnly</span></span>

<span data-ttu-id="e1ae3-458">Habilita ou desabilita o modo somente fluxo.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-458">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="e1ae3-459">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-459">Data type</span></span>         | <span data-ttu-id="e1ae3-460">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-460">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-461">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-461">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="e1ae3-462">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-462">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-463">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-463">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-464">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-464">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="e1ae3-465">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae3-465">Value</span></span>              | <span data-ttu-id="e1ae3-466">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae3-466">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="e1ae3-467">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-467">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="e1ae3-468">O codificador gera o fluxo de imagem bruta sem metadados.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-468">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="e1ae3-469">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-469">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="e1ae3-470">O codificador gera o formato de contêiner (fluxo de imagem mais metadados).</span><span class="sxs-lookup"><span data-stu-id="e1ae3-470">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="e1ae3-471">Subamostragens</span><span class="sxs-lookup"><span data-stu-id="e1ae3-471">Subsampling</span></span>

<span data-ttu-id="e1ae3-472">Define a subamostra de croma.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-472">Sets the chroma subsampling.</span></span> <span data-ttu-id="e1ae3-473">Essa propriedade só se aplica a imagens RGB.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-473">This property applies only to RGB images.</span></span>



| <span data-ttu-id="e1ae3-474">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-474">Data type</span></span> | <span data-ttu-id="e1ae3-475">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-475">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-476">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-476">Range</span></span> | <span data-ttu-id="e1ae3-477">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-477">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="e1ae3-478">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-478">**UCHAR**</span></span> | <span data-ttu-id="e1ae3-479">**\_UI1 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-479">**VT\_UI1**</span></span> | <span data-ttu-id="e1ae3-480">0 a 3</span><span class="sxs-lookup"><span data-stu-id="e1ae3-480">0–3</span></span>   | <span data-ttu-id="e1ae3-481">3 se [ImageQuality](#imagequality) > 0,8; caso contrário, 1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-481">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1ae3-482">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ae3-482">Value</span></span></th>
<th><span data-ttu-id="e1ae3-483">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ae3-483">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1ae3-484">3</span><span class="sxs-lookup"><span data-stu-id="e1ae3-484">3</span></span></td>
<td><span data-ttu-id="e1ae3-485">codificação 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-485">4:4:4 encoding.</span></span> <span data-ttu-id="e1ae3-486">Preserva a resolução de croma completa.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-486">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ae3-487">2</span><span class="sxs-lookup"><span data-stu-id="e1ae3-487">2</span></span></td>
<td><span data-ttu-id="e1ae3-488">codificação 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-488">4:2:2 encoding.</span></span> <span data-ttu-id="e1ae3-489">A resolução de croma é 1/2 de resolução de luminância.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-489">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1ae3-490">1</span><span class="sxs-lookup"><span data-stu-id="e1ae3-490">1</span></span></td>
<td><span data-ttu-id="e1ae3-491">codificação 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-491">4:2:0 encoding.</span></span> <span data-ttu-id="e1ae3-492">A resolução de croma é 1/4 de resolução de luminância.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-492">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1ae3-493">0</span><span class="sxs-lookup"><span data-stu-id="e1ae3-493">0</span></span></td>
<td><span data-ttu-id="e1ae3-494">codificação 4:0:0.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-494">4:0:0 encoding.</span></span> <span data-ttu-id="e1ae3-495">Descarta todos os valores de croma e preserva apenas a luminância.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-495">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e1ae3-496">Esse modo não é recomendado, pois o codec usa uma definição ligeiramente modificada de luminância para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-496">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="e1ae3-497">Em vez disso, é melhor converter a imagem em monocromático antes da codificação.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-497">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e1ae3-498">4:2:2 e 4:2:0 preservam os detalhes de luminância às custas dos detalhes da cor.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-498">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="e1ae3-499">Se você definir essa propriedade, defina também [UseCodecOptions](#usecodecoptions) como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-499">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="e1ae3-500">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="e1ae3-500">UseCodecOptions</span></span>

<span data-ttu-id="e1ae3-501">Especifica se as propriedades de [qualidade](#image-quality-settings), [sobreposição](#overlap)e [subamostragem](#subsampling) devem ser usadas em vez da propriedade [ImageQuality](#imagequality) genérica.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-501">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="e1ae3-502">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-502">Data type</span></span>         | <span data-ttu-id="e1ae3-503">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-503">VARTYPE</span></span>      | <span data-ttu-id="e1ae3-504">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-504">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="e1ae3-505">**BOOL de variante \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-505">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-506">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-506">**VT\_BOOL**</span></span> | <span data-ttu-id="e1ae3-507">**VARIANTE \_ falso**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-507">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="e1ae3-508">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="e1ae3-508">VerticalTileSlices</span></span>

<span data-ttu-id="e1ae3-509">Define o número de blocos horizontais.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-509">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="e1ae3-510">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1ae3-510">Data type</span></span>  | <span data-ttu-id="e1ae3-511">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e1ae3-511">VARTYPE</span></span>     | <span data-ttu-id="e1ae3-512">Intervalo</span><span class="sxs-lookup"><span data-stu-id="e1ae3-512">Range</span></span>  | <span data-ttu-id="e1ae3-513">Padrão</span><span class="sxs-lookup"><span data-stu-id="e1ae3-513">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="e1ae3-514">**NUM**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-514">**USHORT**</span></span> | <span data-ttu-id="e1ae3-515">**\_UI2 VT**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-515">**VT\_UI2**</span></span> | <span data-ttu-id="e1ae3-516">0 – 4095</span><span class="sxs-lookup"><span data-stu-id="e1ae3-516">0–4095</span></span> | <span data-ttu-id="e1ae3-517">(altura da imagem – 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="e1ae3-517">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="e1ae3-518">O valor é o número de subdivisões verticais; ou seja, o número de blocos verticais – 1.</span><span class="sxs-lookup"><span data-stu-id="e1ae3-518">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="e1ae3-519">Formatos de cor com suporte</span><span class="sxs-lookup"><span data-stu-id="e1ae3-519">Supported Color Formats</span></span>

<span data-ttu-id="e1ae3-520">Para obter mais informações sobre esses formatos, consulte [formatos de pixel nativos](-wic-codec-native-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="e1ae3-520">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="e1ae3-521">**Formatos de inteiros RGB**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-521">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="e1ae3-522">\_WICPIXELFORMAT24BPPRGB GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-522">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="e1ae3-523">\_WICPIXELFORMAT24BPPBGR GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-523">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="e1ae3-524">\_WICPIXELFORMAT32BPPBGR GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-524">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="e1ae3-525">\_WICPIXELFORMAT48BPPRGB GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-525">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="e1ae3-526">\_WICPIXELFORMAT32BPPBGRA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-526">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="e1ae3-527">\_WICPIXELFORMAT64BPPRGBA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-527">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="e1ae3-528">\_WICPIXELFORMAT32BPPPBGRA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-528">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="e1ae3-529">\_WICPIXELFORMAT64BPPPRGBA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-529">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="e1ae3-530">**Formatos RGB de ponto fixo**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-530">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="e1ae3-531">\_WICPIXELFORMAT48BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-531">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="e1ae3-532">\_WICPIXELFORMAT64BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-532">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="e1ae3-533">\_WICPIXELFORMAT96BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-533">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="e1ae3-534">\_WICPIXELFORMAT128BPPRGBFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-534">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="e1ae3-535">\_WICPIXELFORMAT128BPPRGBAFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-535">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="e1ae3-536">**Formatos RGB de ponto flutuante**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-536">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="e1ae3-537">\_WICPIXELFORMAT48BPPRGBHALF GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-537">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="e1ae3-538">\_WICPIXELFORMAT64BPPRGBHALF GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-538">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="e1ae3-539">\_WICPIXELFORMAT128BPPRGBFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-539">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="e1ae3-540">\_WICPIXELFORMAT64BPPRGBAFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-540">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="e1ae3-541">\_WICPIXELFORMAT64BPPRGBAHALF GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-541">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="e1ae3-542">\_WICPIXELFORMAT128BPPRGBAFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-542">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="e1ae3-543">\_WICPIXELFORMAT128BPPPRGBAFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-543">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="e1ae3-544">**Formatos em escala de cinza**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-544">**Grayscale formats**</span></span>
    -   <span data-ttu-id="e1ae3-545">\_WICPIXELFORMAT8BPPGRAY GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-545">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="e1ae3-546">\_WICPIXELFORMAT16BPPGRAY GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-546">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="e1ae3-547">\_WICPIXELFORMAT16BPPGRAYFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-547">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="e1ae3-548">\_WICPIXELFORMAT16BPPGRAYHALF GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-548">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="e1ae3-549">\_WICPIXELFORMAT32BPPGRAYFIXEDPOINT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-549">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="e1ae3-550">\_WICPIXELFORMAT32BPPGRAYFLOAT GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-550">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="e1ae3-551">**Formatos empacotados**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-551">**Packed formats**</span></span>
    -   <span data-ttu-id="e1ae3-552">\_WICPIXELFORMAT16BPPBGR555 GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-552">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="e1ae3-553">\_WICPIXELFORMAT16BPPBGR565 GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-553">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="e1ae3-554">\_WICPIXELFORMAT32BPPBGR101010 GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-554">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="e1ae3-555">\_WICPIXELFORMAT32BPPRGBE GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-555">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="e1ae3-556">**Formatos CMYK**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-556">**CMYK formats**</span></span>
    -   <span data-ttu-id="e1ae3-557">\_WICPIXELFORMAT40BPPCMYKALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-557">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="e1ae3-558">\_WICPIXELFORMAT64BPPCMYK GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-558">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="e1ae3-559">\_WICPIXELFORMAT80BPPCMYKALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-559">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="e1ae3-560">**Formatos de N canais**</span><span class="sxs-lookup"><span data-stu-id="e1ae3-560">**N-channel formats**</span></span>
    -   <span data-ttu-id="e1ae3-561">\_WICPIXELFORMAT32BPP4CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-561">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="e1ae3-562">\_WICPIXELFORMAT40BPP5CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-562">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="e1ae3-563">\_WICPIXELFORMAT48BPP6CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-563">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="e1ae3-564">\_WICPIXELFORMAT56BPP7CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-564">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="e1ae3-565">\_WICPIXELFORMAT64BPP8CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-565">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="e1ae3-566">\_WICPIXELFORMAT32BPP3CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-566">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-567">\_WICPIXELFORMAT40BPP4CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-567">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-568">\_WICPIXELFORMAT48BPP5CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-568">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-569">\_WICPIXELFORMAT56BPP6CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-569">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-570">\_WICPIXELFORMAT64BPP7CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-570">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-571">\_WICPIXELFORMAT72BPP8CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-571">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-572">\_WICPIXELFORMAT48BPP3CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-572">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="e1ae3-573">\_WICPIXELFORMAT64BPP4CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-573">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="e1ae3-574">\_WICPIXELFORMAT80BPP5CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-574">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="e1ae3-575">\_WICPIXELFORMAT96BPP6CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-575">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="e1ae3-576">\_WICPIXELFORMAT128BPP8CHANNELS GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-576">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="e1ae3-577">\_WICPIXELFORMAT64BPP3CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-577">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-578">\_WICPIXELFORMAT80BPP4CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-578">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-579">\_WICPIXELFORMAT96BPP5CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-579">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-580">\_WICPIXELFORMAT112BPP6CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-580">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-581">\_WICPIXELFORMAT128BPP7CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-581">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="e1ae3-582">\_WICPIXELFORMAT144BPP8CHANNELSALPHA GUID</span><span class="sxs-lookup"><span data-stu-id="e1ae3-582">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
