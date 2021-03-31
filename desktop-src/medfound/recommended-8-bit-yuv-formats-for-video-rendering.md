---
description: Formatos de YUV de 8 bits recomendados para renderização de vídeo
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formatos de YUV de 8 bits recomendados para renderização de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647747"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a><span data-ttu-id="a5470-103">Formatos de YUV de 8 bits recomendados para renderização de vídeo</span><span class="sxs-lookup"><span data-stu-id="a5470-103">Recommended 8-Bit YUV Formats for Video Rendering</span></span>

<span data-ttu-id="a5470-104">Carlos Sullivan e Stephen Estrop</span><span class="sxs-lookup"><span data-stu-id="a5470-104">Gary Sullivan and Stephen Estrop</span></span>

<span data-ttu-id="a5470-105">Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="a5470-105">Microsoft Corporation</span></span>

<span data-ttu-id="a5470-106">Abril de 2002, atualizado em novembro de 2008</span><span class="sxs-lookup"><span data-stu-id="a5470-106">April 2002, updated November 2008</span></span>

<span data-ttu-id="a5470-107">Este tópico descreve os formatos de cores YUV de 8 bits que são recomendados para a renderização de vídeo no sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="a5470-107">This topic describes the 8-bit YUV color formats that are recommended for video rendering in the Windows operating system.</span></span> <span data-ttu-id="a5470-108">Este artigo apresenta técnicas para converter entre os formatos YUV e RGB, além de fornecer técnicas para formatos YUV de upamostragem.</span><span class="sxs-lookup"><span data-stu-id="a5470-108">This article presents techniques for converting between YUV and RGB formats, and also provides techniques for upsampling YUV formats.</span></span> <span data-ttu-id="a5470-109">Este artigo destina-se a qualquer pessoa que trabalhe com decodificação ou renderização de vídeo YUV no Windows.</span><span class="sxs-lookup"><span data-stu-id="a5470-109">This article is intended for anyone working with YUV video decoding or rendering in Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="a5470-110">Introdução</span><span class="sxs-lookup"><span data-stu-id="a5470-110">Introduction</span></span>

<span data-ttu-id="a5470-111">Vários formatos YUV são definidos em todo o setor de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5470-111">Numerous YUV formats are defined throughout the video industry.</span></span> <span data-ttu-id="a5470-112">Este artigo identifica os formatos YUV de 8 bits recomendados para a renderização de vídeo no Windows.</span><span class="sxs-lookup"><span data-stu-id="a5470-112">This article identifies the 8-bit YUV formats that are recommended for video rendering in Windows.</span></span> <span data-ttu-id="a5470-113">Os fornecedores de decodificadores e os fornecedores de exibição são incentivados a dar suporte aos formatos descritos neste artigo.</span><span class="sxs-lookup"><span data-stu-id="a5470-113">Decoder vendors and display vendors are encouraged to support the formats described in this article.</span></span> <span data-ttu-id="a5470-114">Este artigo não aborda outros usos da cor YUV, como ainda fotografia.</span><span class="sxs-lookup"><span data-stu-id="a5470-114">This article does not address other uses of YUV color, such as still photography.</span></span>

<span data-ttu-id="a5470-115">Os formatos descritos neste artigo usam 8 bits por local de pixel para codificar o canal Y (também chamado de canal Luma) e usam 8 bits por amostra para codificar cada exemplo de croma U ou V.</span><span class="sxs-lookup"><span data-stu-id="a5470-115">The formats described in this article all use 8 bits per pixel location to encode the Y channel (also called the luma channel), and use 8 bits per sample to encode each U or V chroma sample.</span></span> <span data-ttu-id="a5470-116">No entanto, a maioria dos formatos YUV usa menos de 24 bits por pixel em média, pois eles contêm menos amostras de você e V que de Y. Este artigo não aborda os formatos YUV com canais Y de 10 ou mais.</span><span class="sxs-lookup"><span data-stu-id="a5470-116">However, most YUV formats use fewer than 24 bits per pixel on average, because they contain fewer samples of U and V than of Y. This article does not cover YUV formats with 10-bit or higher Y channels.</span></span>

> [!Note]  
> <span data-ttu-id="a5470-117">Para os fins deste artigo, o termo U é equivalente a CB e o termo V é equivalente a CR.</span><span class="sxs-lookup"><span data-stu-id="a5470-117">For the purposes of this article, the term U is equivalent to Cb, and the term V is equivalent to Cr.</span></span>

 

<span data-ttu-id="a5470-118">Este artigo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a5470-118">This article covers the following topics:</span></span>

-   <span data-ttu-id="a5470-119">[Amostragem de YUV](#yuv-sampling).</span><span class="sxs-lookup"><span data-stu-id="a5470-119">[YUV Sampling](#yuv-sampling).</span></span> <span data-ttu-id="a5470-120">Descreve as técnicas de amostragem de YUV mais comuns.</span><span class="sxs-lookup"><span data-stu-id="a5470-120">Describes the most common YUV sampling techniques.</span></span>
-   <span data-ttu-id="a5470-121">[Definições de superfície](#surface-definitions).</span><span class="sxs-lookup"><span data-stu-id="a5470-121">[Surface Definitions](#surface-definitions).</span></span> <span data-ttu-id="a5470-122">Descreve os formatos YUV recomendados.</span><span class="sxs-lookup"><span data-stu-id="a5470-122">Describes the recommended YUV formats.</span></span>
-   <span data-ttu-id="a5470-123">O [espaço de cores e as conversões de taxa de amostragem croma](#color-space-and-chroma-sampling-rate-conversions).</span><span class="sxs-lookup"><span data-stu-id="a5470-123">[Color Space and Chroma Sampling Rate Conversions](#color-space-and-chroma-sampling-rate-conversions).</span></span> <span data-ttu-id="a5470-124">Fornece algumas diretrizes para converter entre os formatos YUV e RGB e para converter entre diferentes formatos YUV.</span><span class="sxs-lookup"><span data-stu-id="a5470-124">Provides some guidelines for converting between YUV and RGB formats and for converting between different YUV formats.</span></span>
-   <span data-ttu-id="a5470-125">[Identificação dos formatos YUV no Media Foundation](#identifying-yuv-formats-in-media-foundation).</span><span class="sxs-lookup"><span data-stu-id="a5470-125">[Identifying YUV Formats in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span></span> <span data-ttu-id="a5470-126">Explica como descrever tipos de formato YUV no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a5470-126">Explains how to describe YUV format types in Media Foundation.</span></span>

## <a name="yuv-sampling"></a><span data-ttu-id="a5470-127">Amostragem de YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-127">YUV Sampling</span></span>

<span data-ttu-id="a5470-128">Os canais croma podem ter uma taxa de amostragem menor do que o canal do Luma, sem perda dramática de qualidade de perceptiva.</span><span class="sxs-lookup"><span data-stu-id="a5470-128">Chroma channels can have a lower sampling rate than the luma channel, without any dramatic loss of perceptual quality.</span></span> <span data-ttu-id="a5470-129">Uma notação chamada de notação "A:B: C" é usada para descrever a frequência com que você e V são amostrados em relação a Y:</span><span class="sxs-lookup"><span data-stu-id="a5470-129">A notation called the "A:B:C" notation is used to describe how often U and V are sampled relative to Y:</span></span>

-   <span data-ttu-id="a5470-130">4:4:4 significa nenhuma diminuição dos canais de croma.</span><span class="sxs-lookup"><span data-stu-id="a5470-130">4:4:4 means no downsampling of the chroma channels.</span></span>
-   <span data-ttu-id="a5470-131">4:2:2 significa redução horizontal de 2:1, sem redução vertical.</span><span class="sxs-lookup"><span data-stu-id="a5470-131">4:2:2 means 2:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="a5470-132">Cada linha de exame contém quatro exemplos de Y para cada dois exemplos de U ou V.</span><span class="sxs-lookup"><span data-stu-id="a5470-132">Every scan line contains four Y samples for every two U or V samples.</span></span>
-   <span data-ttu-id="a5470-133">4:2:0 significa redução horizontal de 2:1, com resolução vertical de 2:1.</span><span class="sxs-lookup"><span data-stu-id="a5470-133">4:2:0 means 2:1 horizontal downsampling, with 2:1 vertical downsampling.</span></span>
-   <span data-ttu-id="a5470-134">4:1:1 significa redução horizontal de 4:1, sem redução vertical.</span><span class="sxs-lookup"><span data-stu-id="a5470-134">4:1:1 means 4:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="a5470-135">Cada linha de exame contém quatro exemplos de Y para cada exemplo de você e de V.</span><span class="sxs-lookup"><span data-stu-id="a5470-135">Every scan line contains four Y samples for each U and V sample.</span></span> <span data-ttu-id="a5470-136">4:1:1 a amostragem é menos comum do que outros formatos e não é discutida detalhadamente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="a5470-136">4:1:1 sampling is less common than other formats, and is not discussed in detail in this article.</span></span>

<span data-ttu-id="a5470-137">Os diagramas a seguir mostram como o croma é amostrado para cada uma das taxas de redução da resolução.</span><span class="sxs-lookup"><span data-stu-id="a5470-137">The following diagrams shows how chroma is sampled for each of the downsampling rates.</span></span> <span data-ttu-id="a5470-138">Os exemplos de Luma são representados por uma cruz e os exemplos de croma são representados por um círculo.</span><span class="sxs-lookup"><span data-stu-id="a5470-138">Luma samples are represented by a cross, and chroma samples are represented by a circle.</span></span>

![Figura 1.](images/yuv-sampling-grids.png)

<span data-ttu-id="a5470-141">A forma dominante de 4:2:2 amostragem é definida no ITU-R recomendação BT. 601.</span><span class="sxs-lookup"><span data-stu-id="a5470-141">The dominant form of 4:2:2 sampling is defined in ITU-R Recommendation BT.601.</span></span> <span data-ttu-id="a5470-142">Há duas variantes comuns de 4:2:0 amostragem.</span><span class="sxs-lookup"><span data-stu-id="a5470-142">There are two common variants of 4:2:0 sampling.</span></span> <span data-ttu-id="a5470-143">Um deles é usado no vídeo MPEG-2 e o outro é usado em MPEG-1 e em recomendações ITU-T H. 261 e H. 263.</span><span class="sxs-lookup"><span data-stu-id="a5470-143">One of these is used in MPEG-2 video, and the other is used in MPEG-1 and in ITU-T Recommendations H.261 and H.263.</span></span>

<span data-ttu-id="a5470-144">Em comparação com o esquema MPEG-1, é mais simples converter entre o esquema MPEG-2 e as grades de amostragem definidas para os formatos 4:2:2 e 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="a5470-144">Compared with the MPEG-1 scheme, it is simpler to convert between the MPEG-2 scheme and the sampling grids defined for 4:2:2 and 4:4:4 formats.</span></span> <span data-ttu-id="a5470-145">Por esse motivo, o esquema MPEG-2 é preferencial no Windows e deve ser considerado a interpretação padrão dos formatos 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="a5470-145">For this reason, the MPEG-2 scheme is preferred in Windows, and should be considered the default interpretation of 4:2:0 formats.</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="a5470-146">Definições de superfície</span><span class="sxs-lookup"><span data-stu-id="a5470-146">Surface Definitions</span></span>

<span data-ttu-id="a5470-147">Esta seção descreve os formatos YUV de 8 bits recomendados para a renderização de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5470-147">This section describes the 8-bit YUV formats that are recommended for video rendering.</span></span> <span data-ttu-id="a5470-148">Eles se enquadram em várias categorias:</span><span class="sxs-lookup"><span data-stu-id="a5470-148">These fall into several categories:</span></span>

-   [<span data-ttu-id="a5470-149">4:4:4 formatos, 32 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-149">4:4:4 Formats, 32 Bits per Pixel</span></span>](#444-formats-32-bits-per-pixel)
-   [<span data-ttu-id="a5470-150">4:2:2 formatos, 16 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-150">4:2:2 Formats, 16 Bits per Pixel</span></span>](#422-formats-16-bits-per-pixel)
-   [<span data-ttu-id="a5470-151">4:2:0 formatos, 16 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-151">4:2:0 Formats, 16 Bits per Pixel</span></span>](#420-formats-16-bits-per-pixel)
-   [<span data-ttu-id="a5470-152">4:2:0 formatos, 12 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-152">4:2:0 Formats, 12 Bits per Pixel</span></span>](#420-formats-12-bits-per-pixel)

<span data-ttu-id="a5470-153">Primeiro, você deve estar ciente dos seguintes conceitos para entender o que segue:</span><span class="sxs-lookup"><span data-stu-id="a5470-153">First, you should be aware of the following concepts in order to understand what follows:</span></span>

-   <span data-ttu-id="a5470-154">*Origem da superfície*.</span><span class="sxs-lookup"><span data-stu-id="a5470-154">*Surface origin*.</span></span> <span data-ttu-id="a5470-155">Para os formatos YUV descritos neste artigo, a origem (0, 0) é sempre o canto superior esquerdo da superfície.</span><span class="sxs-lookup"><span data-stu-id="a5470-155">For the YUV formats described in this article, the origin (0,0) is always the top left corner of the surface.</span></span>
-   <span data-ttu-id="a5470-156">*Stride*.</span><span class="sxs-lookup"><span data-stu-id="a5470-156">*Stride*.</span></span> <span data-ttu-id="a5470-157">O stride de uma superfície, às vezes chamada de pitch, é a largura da superfície em bytes.</span><span class="sxs-lookup"><span data-stu-id="a5470-157">The stride of a surface, sometimes called the pitch, is the width of the surface in bytes.</span></span> <span data-ttu-id="a5470-158">Dada uma origem da superfície no canto superior esquerdo, o stride é sempre positivo.</span><span class="sxs-lookup"><span data-stu-id="a5470-158">Given a surface origin at the top left corner, the stride is always positive.</span></span>
-   <span data-ttu-id="a5470-159">*Alinhamento*.</span><span class="sxs-lookup"><span data-stu-id="a5470-159">*Alignment*.</span></span> <span data-ttu-id="a5470-160">O alinhamento de uma superfície é a critério do driver de vídeo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="a5470-160">The alignment of a surface is at the discretion of the graphics display driver.</span></span> <span data-ttu-id="a5470-161">A superfície sempre deve ser alinhada em DWORD; ou seja, as linhas individuais dentro da superfície têm a garantia de serem originadas em um limite de 32 bits (DWORD).</span><span class="sxs-lookup"><span data-stu-id="a5470-161">The surface must always be DWORD aligned; that is, individual lines within the surface are guaranteed to originate on a 32-bit (DWORD) boundary.</span></span> <span data-ttu-id="a5470-162">No entanto, o alinhamento pode ser maior que 32 bits, dependendo das necessidades do hardware.</span><span class="sxs-lookup"><span data-stu-id="a5470-162">The alignment can be larger than 32 bits, however, depending on the needs of the hardware.</span></span>
-   <span data-ttu-id="a5470-163">Formato embalado versus formato planar.</span><span class="sxs-lookup"><span data-stu-id="a5470-163">Packed format versus planar format.</span></span> <span data-ttu-id="a5470-164">Os formatos YUV são divididos em formatos *compactados* e formatos de *planar* .</span><span class="sxs-lookup"><span data-stu-id="a5470-164">YUV formats are divided into *packed* formats and *planar* formats.</span></span> <span data-ttu-id="a5470-165">Em um formato empacotado, os componentes Y, U e V são armazenados em uma única matriz.</span><span class="sxs-lookup"><span data-stu-id="a5470-165">In a packed format, the Y, U, and V components are stored in a single array.</span></span> <span data-ttu-id="a5470-166">Os pixels são organizados em grupos de macropixels, cujo layout depende do formato.</span><span class="sxs-lookup"><span data-stu-id="a5470-166">Pixels are organized into groups of macropixels, whose layout depends on the format.</span></span> <span data-ttu-id="a5470-167">Em um formato planar, os componentes Y, U e V são armazenados como três planos separados.</span><span class="sxs-lookup"><span data-stu-id="a5470-167">In a planar format, the Y, U, and V components are stored as three separate planes.</span></span>

<span data-ttu-id="a5470-168">Cada um dos formatos YUV descritos neste artigo tem um código FOURCC atribuído.</span><span class="sxs-lookup"><span data-stu-id="a5470-168">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="a5470-169">Um código FOURCC é um inteiro sem sinal de 32 bits que é criado pela concatenação de quatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="a5470-169">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

-   <span data-ttu-id="a5470-170">4:4:4 (32 bpp)</span><span class="sxs-lookup"><span data-stu-id="a5470-170">4:4:4 (32 bpp)</span></span>
    -   [<span data-ttu-id="a5470-171">AYUV</span><span class="sxs-lookup"><span data-stu-id="a5470-171">AYUV</span></span>](#ayuv)
-   <span data-ttu-id="a5470-172">4:2:2 (16 BPP)</span><span class="sxs-lookup"><span data-stu-id="a5470-172">4:2:2 (16 bpp)</span></span>
    -   [<span data-ttu-id="a5470-173">YUY2</span><span class="sxs-lookup"><span data-stu-id="a5470-173">YUY2</span></span>](#yuy2)
    -   [<span data-ttu-id="a5470-174">UYVY</span><span class="sxs-lookup"><span data-stu-id="a5470-174">UYVY</span></span>](#uyvy)
-   <span data-ttu-id="a5470-175">4:2:0 (16 BPP)</span><span class="sxs-lookup"><span data-stu-id="a5470-175">4:2:0 (16 bpp)</span></span>
    -   [<span data-ttu-id="a5470-176">IMC1</span><span class="sxs-lookup"><span data-stu-id="a5470-176">IMC1</span></span>](#imc1)
    -   [<span data-ttu-id="a5470-177">IMC3</span><span class="sxs-lookup"><span data-stu-id="a5470-177">IMC3</span></span>](#imc3)
-   <span data-ttu-id="a5470-178">4:2:0 (12 BPP)</span><span class="sxs-lookup"><span data-stu-id="a5470-178">4:2:0 (12 bpp)</span></span>
    -   [<span data-ttu-id="a5470-179">IMC2</span><span class="sxs-lookup"><span data-stu-id="a5470-179">IMC2</span></span>](#imc2)
    -   [<span data-ttu-id="a5470-180">IMC4</span><span class="sxs-lookup"><span data-stu-id="a5470-180">IMC4</span></span>](#imc4)
    -   [<span data-ttu-id="a5470-181">YV12</span><span class="sxs-lookup"><span data-stu-id="a5470-181">YV12</span></span>](#yv12)
    -   [<span data-ttu-id="a5470-182">NV12</span><span class="sxs-lookup"><span data-stu-id="a5470-182">NV12</span></span>](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a><span data-ttu-id="a5470-183">4:4:4 formatos, 32 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-183">4:4:4 Formats, 32 Bits per Pixel</span></span>

### <a name="ayuv"></a><span data-ttu-id="a5470-184">AYUV</span><span class="sxs-lookup"><span data-stu-id="a5470-184">AYUV</span></span>

<span data-ttu-id="a5470-185">Um único formato 4:4:4 é recomendado, com o código FOURCC AYUV.</span><span class="sxs-lookup"><span data-stu-id="a5470-185">A single 4:4:4 format is recommended, with the FOURCC code AYUV.</span></span> <span data-ttu-id="a5470-186">Esse é um formato empacotado, em que cada pixel é codificado como quatro bytes consecutivos, organizados na sequência mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5470-186">This is a packed format, where each pixel is encoded as four consecutive bytes, arranged in the sequence shown in the following illustration.</span></span>

![Figura 2.](images/yuvformats01.gif)

<span data-ttu-id="a5470-189">Os bytes marcados como um contêm valores para alfa.</span><span class="sxs-lookup"><span data-stu-id="a5470-189">The bytes marked A contain values for alpha.</span></span>

## <a name="422-formats-16-bits-per-pixel"></a><span data-ttu-id="a5470-190">4:2:2 formatos, 16 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-190">4:2:2 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="a5470-191">São recomendados dois formatos 4:2:2, com os seguintes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="a5470-191">Two 4:2:2 formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="a5470-192">YUY2</span><span class="sxs-lookup"><span data-stu-id="a5470-192">YUY2</span></span>
-   <span data-ttu-id="a5470-193">UYVY</span><span class="sxs-lookup"><span data-stu-id="a5470-193">UYVY</span></span>

<span data-ttu-id="a5470-194">Ambos são formatos compactados, em que cada macropixel é dois pixels codificados como quatro bytes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="a5470-194">Both are packed formats, where each macropixel is two pixels encoded as four consecutive bytes.</span></span> <span data-ttu-id="a5470-195">Isso resulta em redução horizontal do Croma por um fator de dois.</span><span class="sxs-lookup"><span data-stu-id="a5470-195">This results in horizontal downsampling of the chroma by a factor of two.</span></span>

### <a name="yuy2"></a><span data-ttu-id="a5470-196">YUY2</span><span class="sxs-lookup"><span data-stu-id="a5470-196">YUY2</span></span>

<span data-ttu-id="a5470-197">No formato YUY2, os dados podem ser tratados como uma matriz de valores de **caracteres** não assinados, onde o primeiro byte contém o primeiro exemplo y, o segundo byte contém o primeiro exemplo U (CB), o terceiro byte contém o segundo exemplo de y e o quarto byte contém o primeiro exemplo V (CR), como mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5470-197">In YUY2 format, the data can be treated as an array of unsigned **char** values, where the first byte contains the first Y sample, the second byte contains the first U (Cb) sample, the third byte contains the second Y sample, and the fourth byte contains the first V (Cr) sample, as shown in the following diagram.</span></span>

![Figura 3.](images/yuvformats02.gif)

<span data-ttu-id="a5470-200">Se a imagem for endereçada como uma matriz de valores de **palavras** little-endian, a primeira **palavra** conterá a primeira amostra Y do bits menos significativo (LSBs) e o primeiro exemplo U (CB) nos bits mais significativos (MSBs).</span><span class="sxs-lookup"><span data-stu-id="a5470-200">If the image is addressed as an array of little-endian **WORD** values, the first **WORD** contains the first Y sample in the least significant bits (LSBs) and the first U (Cb) sample in the most significant bits (MSBs).</span></span> <span data-ttu-id="a5470-201">A segunda **palavra** contém o segundo exemplo de Y no LSBs e o primeiro exemplo de V (CR) no MSBs.</span><span class="sxs-lookup"><span data-stu-id="a5470-201">The second **WORD** contains the second Y sample in the LSBs and the first V (Cr) sample in the MSBs.</span></span>

<span data-ttu-id="a5470-202">YUY2 é o formato de pixel preferido de 4:2:2 para aceleração de vídeo do Microsoft DirectX (DirectX VA).</span><span class="sxs-lookup"><span data-stu-id="a5470-202">YUY2 is the preferred 4:2:2 pixel format for Microsoft DirectX Video Acceleration (DirectX VA).</span></span> <span data-ttu-id="a5470-203">Espera-se que seja um requisito de termo intermediário para o DirectX VA Accelerators com suporte para vídeo 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="a5470-203">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:2 video.</span></span>

### <a name="uyvy"></a><span data-ttu-id="a5470-204">UYVY</span><span class="sxs-lookup"><span data-stu-id="a5470-204">UYVY</span></span>

<span data-ttu-id="a5470-205">Esse formato é o mesmo que o formato YUY2, exceto que a ordem de bytes é invertida, ou seja, os bytes croma e Luma são invertidos (Figura 4).</span><span class="sxs-lookup"><span data-stu-id="a5470-205">This format is the same as the YUY2 format except the byte order is reversed—that is, the chroma and luma bytes are flipped (Figure 4).</span></span> <span data-ttu-id="a5470-206">Se a imagem for endereçada como uma matriz de dois valores de **palavra** little-endian, a primeira **palavra** conterá U no LSBs e y0 no MSBs, e a segunda **palavra** conterá V no LSBs e Y1 no MSBs.</span><span class="sxs-lookup"><span data-stu-id="a5470-206">If the image is addressed as an array of two little-endian **WORD** values, the first **WORD** contains U in the LSBs and Y0 in the MSBs, and the second **WORD** contains V in the LSBs and Y1 in the MSBs.</span></span>

![Figura 4.](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a><span data-ttu-id="a5470-209">4:2:0 formatos, 16 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-209">4:2:0 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="a5470-210">Dois formatos de 4:2:0 16 bits por pixel (BPP) são recomendados, com os seguintes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="a5470-210">Two 4:2:0 16-bits per pixel (bpp) formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="a5470-211">IMC1</span><span class="sxs-lookup"><span data-stu-id="a5470-211">IMC1</span></span>
-   <span data-ttu-id="a5470-212">IMC3</span><span class="sxs-lookup"><span data-stu-id="a5470-212">IMC3</span></span>

<span data-ttu-id="a5470-213">Ambos os formatos YUV são formatos de planar.</span><span class="sxs-lookup"><span data-stu-id="a5470-213">Both of these YUV formats are planar formats.</span></span> <span data-ttu-id="a5470-214">Os canais croma são subamostrados por um fator de dois nas dimensões horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="a5470-214">The chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc1"></a><span data-ttu-id="a5470-215">IMC1</span><span class="sxs-lookup"><span data-stu-id="a5470-215">IMC1</span></span>

<span data-ttu-id="a5470-216">Todos os exemplos de Y aparecem primeiro na memória como uma matriz de valores de **caracteres** não assinados.</span><span class="sxs-lookup"><span data-stu-id="a5470-216">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="a5470-217">Isso é seguido de todos os exemplos de V (CR) e, em seguida, de todos os exemplos de U (CB).</span><span class="sxs-lookup"><span data-stu-id="a5470-217">This is followed by all of the V (Cr) samples, and then all of the U (Cb) samples.</span></span> <span data-ttu-id="a5470-218">Os planos V e U têm o mesmo Stride que o plano Y, resultando em áreas não usadas de memória, como mostra a Figura 5.</span><span class="sxs-lookup"><span data-stu-id="a5470-218">The V and U planes have the same stride as the Y plane, resulting in unused areas of memory, as shown in Figure 5.</span></span> <span data-ttu-id="a5470-219">Os planos de você e V devem começar nos limites de memória que são um múltiplo de 16 linhas.</span><span class="sxs-lookup"><span data-stu-id="a5470-219">The U and V planes must start on memory boundaries that are a multiple of 16 lines.</span></span> <span data-ttu-id="a5470-220">A Figura 5 mostra a origem de você e V para um quadro de vídeo 352 x 240.</span><span class="sxs-lookup"><span data-stu-id="a5470-220">Figure 5 shows the origin of U and V for a 352 x 240 video frame.</span></span> <span data-ttu-id="a5470-221">O endereço inicial dos planos você e V são calculados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5470-221">The starting address of the U and V planes are calculated as follows:</span></span>

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

<span data-ttu-id="a5470-222">em que *pY* é um ponteiro de byte para o início da matriz de memória, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5470-222">where *pY* is a byte pointer to the start of the memory array, as shown in the following diagram.</span></span>

![Figura 5.](images/yuvformats04.gif)

### <a name="imc3"></a><span data-ttu-id="a5470-225">IMC3</span><span class="sxs-lookup"><span data-stu-id="a5470-225">IMC3</span></span>

<span data-ttu-id="a5470-226">Esse formato é idêntico a IMC1, exceto que os planos de você e V são trocados, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5470-226">This format is identical to IMC1, except the U and V planes are swapped, as shown in the following diagram.</span></span>

![Figura 6.](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a><span data-ttu-id="a5470-229">4:2:0 formatos, 12 bits por pixel</span><span class="sxs-lookup"><span data-stu-id="a5470-229">4:2:0 Formats, 12 Bits per Pixel</span></span>

<span data-ttu-id="a5470-230">São recomendados quatro formatos 4:2:0 12-BPP, com os seguintes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="a5470-230">Four 4:2:0 12-bpp formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="a5470-231">IMC2</span><span class="sxs-lookup"><span data-stu-id="a5470-231">IMC2</span></span>
-   <span data-ttu-id="a5470-232">IMC4</span><span class="sxs-lookup"><span data-stu-id="a5470-232">IMC4</span></span>
-   <span data-ttu-id="a5470-233">YV12</span><span class="sxs-lookup"><span data-stu-id="a5470-233">YV12</span></span>
-   <span data-ttu-id="a5470-234">NV12</span><span class="sxs-lookup"><span data-stu-id="a5470-234">NV12</span></span>

<span data-ttu-id="a5470-235">Em todos esses formatos, os canais croma são subamostrados por um fator de dois nas dimensões horizontal e vertical.</span><span class="sxs-lookup"><span data-stu-id="a5470-235">In all of these formats, the chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc2"></a><span data-ttu-id="a5470-236">IMC2</span><span class="sxs-lookup"><span data-stu-id="a5470-236">IMC2</span></span>

<span data-ttu-id="a5470-237">Esse formato é o mesmo que IMC1, exceto pelas seguintes diferenças: as linhas V (CR) e U (CB) são intercaladas em limites de meia distância.</span><span class="sxs-lookup"><span data-stu-id="a5470-237">This format is the same as IMC1 except for the following difference: The V (Cr) and U (Cb) lines are interleaved at half-stride boundaries.</span></span> <span data-ttu-id="a5470-238">Em outras palavras, cada linha de avanço na área croma começa com uma linha de exemplos de V, seguida por uma linha de exemplos de U que começa no próximo limite de meio-Stride (Figura 7).</span><span class="sxs-lookup"><span data-stu-id="a5470-238">In other words, each full-stride line in the chroma area starts with a line of V samples, followed by a line of U samples that begins at the next half-stride boundary (Figure 7).</span></span> <span data-ttu-id="a5470-239">Esse layout faz uso mais eficiente do espaço de endereço do que IMC1.</span><span class="sxs-lookup"><span data-stu-id="a5470-239">This layout makes more efficient use of address space than IMC1.</span></span> <span data-ttu-id="a5470-240">Ele corta o espaço de endereço croma pela metade e, portanto, o espaço de endereço total em 25%.</span><span class="sxs-lookup"><span data-stu-id="a5470-240">It cuts the chroma address space in half, and thus the total address space by 25 percent.</span></span> <span data-ttu-id="a5470-241">Entre os formatos 4:2:0, IMC2 é o segundo formato preferencial, após NV12.</span><span class="sxs-lookup"><span data-stu-id="a5470-241">Among 4:2:0 formats, IMC2 is the second-most preferred format, after NV12.</span></span> <span data-ttu-id="a5470-242">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="a5470-242">The following image illustrates this process.</span></span>

![Figura 7.](images/yuvformats07.gif)

### <a name="imc4"></a><span data-ttu-id="a5470-245">IMC4</span><span class="sxs-lookup"><span data-stu-id="a5470-245">IMC4</span></span>

<span data-ttu-id="a5470-246">Esse formato é idêntico a IMC2, exceto que as linhas U (CB) e V (CR) são trocadas, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5470-246">This format is identical to IMC2, except the U (Cb) and V (Cr) lines are swapped, as shown in the following illustration.</span></span>

![Figura 8.](images/yuvformats06.gif)

### <a name="yv12"></a><span data-ttu-id="a5470-249">YV12</span><span class="sxs-lookup"><span data-stu-id="a5470-249">YV12</span></span>

<span data-ttu-id="a5470-250">Todos os exemplos de Y aparecem primeiro na memória como uma matriz de valores de **caracteres** não assinados.</span><span class="sxs-lookup"><span data-stu-id="a5470-250">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="a5470-251">Essa matriz é seguida imediatamente por todos os exemplos de V (CR).</span><span class="sxs-lookup"><span data-stu-id="a5470-251">This array is followed immediately by all of the V (Cr) samples.</span></span> <span data-ttu-id="a5470-252">O stride do plano V é metade do Stride do plano Y; e o plano V contém metade do número de linhas que o plano Y.</span><span class="sxs-lookup"><span data-stu-id="a5470-252">The stride of the V plane is half the stride of the Y plane; and the V plane contains half as many lines as the Y plane.</span></span> <span data-ttu-id="a5470-253">O plano V é seguido imediatamente por todos os exemplos de U (CB), com o mesmo Stride e número de linhas que o plano V, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5470-253">The V plane is followed immediately by all of the U (Cb) samples, with the same stride and number of lines as the V plane, as shown in the following illustration.</span></span>

![Figura 9.](images/yuvformats08.gif)

### <a name="nv12"></a><span data-ttu-id="a5470-256">NV12</span><span class="sxs-lookup"><span data-stu-id="a5470-256">NV12</span></span>

<span data-ttu-id="a5470-257">Todos os exemplos de Y aparecem primeiro na memória como uma matriz de valores de **caracteres** não assinados com um número par de linhas.</span><span class="sxs-lookup"><span data-stu-id="a5470-257">All of the Y samples appear first in memory as an array of unsigned **char** values with an even number of lines.</span></span> <span data-ttu-id="a5470-258">O plano Y é seguido imediatamente por uma matriz de valores de **caracteres** não assinados que contém exemplos de U (CB) e V (CR) empacotados.</span><span class="sxs-lookup"><span data-stu-id="a5470-258">The Y plane is followed immediately by an array of unsigned **char** values that contains packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="a5470-259">Quando a matriz de U-V combinada é endereçada como uma matriz de valores de **palavra** little-endian, o LSBs contém os valores U e MSBs contém os valores de V.</span><span class="sxs-lookup"><span data-stu-id="a5470-259">When the combined U-V array is addressed as an array of little-endian **WORD** values, the LSBs contain the U values, and the MSBs contain the V values.</span></span> <span data-ttu-id="a5470-260">NV12 é o formato de pixel preferencial de 4:2:0 para DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="a5470-260">NV12 is the preferred 4:2:0 pixel format for DirectX VA.</span></span> <span data-ttu-id="a5470-261">Espera-se que seja um requisito de termo intermediário para o DirectX VA Accelerators com suporte para vídeo 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="a5470-261">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:0 video.</span></span> <span data-ttu-id="a5470-262">A ilustração a seguir mostra o plano Y e a matriz que contém exemplos de você e V compactados.</span><span class="sxs-lookup"><span data-stu-id="a5470-262">The following illustration shows the Y plane and the array that contains packed U and V samples.</span></span>

![Figura 10.](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a><span data-ttu-id="a5470-265">Conversões de taxa de amostragem de croma e de espaço de cor</span><span class="sxs-lookup"><span data-stu-id="a5470-265">Color Space and Chroma Sampling Rate Conversions</span></span>

<span data-ttu-id="a5470-266">Esta seção fornece diretrizes para a conversão entre YUV e RGB e para a conversão entre alguns formatos YUV diferentes.</span><span class="sxs-lookup"><span data-stu-id="a5470-266">This section provides guidelines for converting between YUV and RGB, and for converting between some different YUV formats.</span></span> <span data-ttu-id="a5470-267">Consideramos dois esquemas de codificação RGB nesta seção: *computador de 8 bits RGB*, também conhecido como sRGB ou "Full-Scale" RGB, e *Studio Video RGB*, ou "RGB com sala de cabeça e Toe-Room".</span><span class="sxs-lookup"><span data-stu-id="a5470-267">We consider two RGB encoding schemes in this section: *8-bit computer RGB*, also known as sRGB or "full-scale" RGB, and *studio video RGB*, or "RGB with head-room and toe-room."</span></span> <span data-ttu-id="a5470-268">Eles são definidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5470-268">These are defined as follows:</span></span>

-   <span data-ttu-id="a5470-269">O computador RGB usa 8 bits para cada amostra de vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="a5470-269">Computer RGB uses 8 bits for each sample of red, green, and blue.</span></span> <span data-ttu-id="a5470-270">O preto é representado por R = G = B = 0 e o branco é representado por R = G = B = 255.</span><span class="sxs-lookup"><span data-stu-id="a5470-270">Black is represented by R = G = B = 0, and white is represented by R = G = B = 255.</span></span>
-   <span data-ttu-id="a5470-271">O vídeo RGB do estúdio usa um número de bits N para cada amostra de vermelho, verde e azul, em que N é 8 ou mais.</span><span class="sxs-lookup"><span data-stu-id="a5470-271">Studio video RGB uses some number of bits N for each sample of red, green, and blue, where N is 8 or more.</span></span> <span data-ttu-id="a5470-272">O vídeo RGB do estúdio usa um fator de dimensionamento diferente do computador RGB e tem um deslocamento.</span><span class="sxs-lookup"><span data-stu-id="a5470-272">Studio video RGB uses a different scaling factor than computer RGB, and it has an offset.</span></span> <span data-ttu-id="a5470-273">O preto é representado por R = G = B = 16 \* 2 ^ (n-8) e o branco é representado por r = g = b = 235 \* 2 ^ (n-8).</span><span class="sxs-lookup"><span data-stu-id="a5470-273">Black is represented by R = G = B = 16\*2^(N-8), and white is represented by R = G = B = 235\*2^(N-8).</span></span> <span data-ttu-id="a5470-274">No entanto, os valores reais podem ficar fora desse intervalo.</span><span class="sxs-lookup"><span data-stu-id="a5470-274">However, actual values may fall outside this range.</span></span>

<span data-ttu-id="a5470-275">O Studio Video RGB é a definição de RGB preferida para vídeo no Windows, enquanto o computador RGB é a definição de RGB preferida para aplicativos que não são de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5470-275">Studio video RGB is the preferred RGB definition for video in Windows, while computer RGB is the preferred RGB definition for non-video applications.</span></span> <span data-ttu-id="a5470-276">Em qualquer forma de RGB, as coordenadas de desvio são conforme especificado em ITU-R BT. 709 para a definição dos primários de cor RGB.</span><span class="sxs-lookup"><span data-stu-id="a5470-276">In either form of RGB, the chromaticity coordinates are as specified in ITU-R BT.709 for the definition of the RGB color primaries.</span></span> <span data-ttu-id="a5470-277">As coordenadas (x, y) de R, G e B são (0,64, 0,33), (0,30, 0,60) e (0,15, 0, 6), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a5470-277">The (x,y) coordinates of R, G, and B are (0.64, 0.33), (0.30, 0.60), and (0.15, 0.06), respectively.</span></span> <span data-ttu-id="a5470-278">O branco de referência é D65 com coordenadas (0,3127, 0,3290).</span><span class="sxs-lookup"><span data-stu-id="a5470-278">Reference white is D65 with coordinates (0.3127, 0.3290).</span></span> <span data-ttu-id="a5470-279">O gama nominal é 1/0.45 (aproximadamente 2,2), com gama preciso definido em detalhes em ITU-R BT. 709.</span><span class="sxs-lookup"><span data-stu-id="a5470-279">Nominal gamma is 1/0.45 (approximately 2.2), with precise gamma defined in detail in ITU-R BT.709.</span></span>

<span data-ttu-id="a5470-280">**Conversão entre RGB e 4:4:4 YUV**</span><span class="sxs-lookup"><span data-stu-id="a5470-280">**Conversion between RGB and 4:4:4 YUV**</span></span>

<span data-ttu-id="a5470-281">Primeiro descrevemos a conversão entre RGB e 4:4:4 YUV.</span><span class="sxs-lookup"><span data-stu-id="a5470-281">We first describe conversion between RGB and 4:4:4 YUV.</span></span> <span data-ttu-id="a5470-282">Para converter 4:2:0 ou 4:2:2 YUV em RGB, é recomendável converter os dados YUV para 4:4:4 YUV e, em seguida, converter de 4:4:4 YUV para RGB.</span><span class="sxs-lookup"><span data-stu-id="a5470-282">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="a5470-283">O formato AYUV, que é um formato 4:4:4, usa 8 bits cada para os exemplos Y, U e V.</span><span class="sxs-lookup"><span data-stu-id="a5470-283">The AYUV format, which is a 4:4:4 format, uses 8 bits each for the Y, U, and V samples.</span></span> <span data-ttu-id="a5470-284">O YUV também pode ser definido usando mais de 8 bits por amostra para alguns aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a5470-284">YUV can also be defined using more than 8 bits per sample for some applications.</span></span>

<span data-ttu-id="a5470-285">Duas conversões de YUV dominantes de RGB foram definidas para vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="a5470-285">Two dominant YUV conversions from RGB have been defined for digital video.</span></span> <span data-ttu-id="a5470-286">Ambos se baseiam na especificação conhecida como ITU-R recomendação BT. 709.</span><span class="sxs-lookup"><span data-stu-id="a5470-286">Both are based on the specification known as ITU-R Recommendation BT.709.</span></span> <span data-ttu-id="a5470-287">A primeira conversão é o formulário YUV mais antigo definido para o uso de 50-Hz em BT. 709.</span><span class="sxs-lookup"><span data-stu-id="a5470-287">The first conversion is the older YUV form defined for 50-Hz use in BT.709.</span></span> <span data-ttu-id="a5470-288">É o mesmo que a relação especificada no ITU-R recomendação BT. 601, também conhecida por seu nome mais antigo, CCIR 601.</span><span class="sxs-lookup"><span data-stu-id="a5470-288">It is the same as the relation specified in ITU-R Recommendation BT.601, also known by its older name, CCIR 601.</span></span> <span data-ttu-id="a5470-289">Ele deve ser considerado o formato YUV preferencial para resolução de TV de definição padrão (720 x 576) e vídeo de resolução inferior.</span><span class="sxs-lookup"><span data-stu-id="a5470-289">It should be considered the preferred YUV format for standard-definition TV resolution (720 x 576) and lower-resolution video.</span></span> <span data-ttu-id="a5470-290">Ele é caracterizado pelos valores de duas constantes *Kr* e *KB*:</span><span class="sxs-lookup"><span data-stu-id="a5470-290">It is characterized by the values of two constants *Kr* and *Kb*:</span></span>

``` syntax
Kr = 0.299
Kb = 0.114
```

<span data-ttu-id="a5470-291">A segunda conversão é o formulário YUV mais recente definido para o uso de 60-Hz em BT. 709 e deve ser considerado o formato preferencial para resoluções de vídeo acima de SDTV.</span><span class="sxs-lookup"><span data-stu-id="a5470-291">The second conversion is the newer YUV form defined for 60-Hz use in BT.709, and should be considered the preferred format for video resolutions above SDTV.</span></span> <span data-ttu-id="a5470-292">Ele é caracterizado por valores diferentes para essas duas constantes:</span><span class="sxs-lookup"><span data-stu-id="a5470-292">It is characterized by different values for these two constants:</span></span>

``` syntax
Kr = 0.2126
Kb = 0.0722
```

<span data-ttu-id="a5470-293">A conversão de RGB em YUV é definida começando com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a5470-293">Conversion from RGB to YUV is defined by starting with the following:</span></span>

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

<span data-ttu-id="a5470-294">Os valores YUV são obtidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5470-294">The YUV values are then obtained as follows:</span></span>

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

<span data-ttu-id="a5470-295">onde</span><span class="sxs-lookup"><span data-stu-id="a5470-295">where</span></span>

-   <span data-ttu-id="a5470-296">M é o número de bits por exemplo de YUV (M >= 8).</span><span class="sxs-lookup"><span data-stu-id="a5470-296">M is the number of bits per YUV sample (M >= 8).</span></span>
-   <span data-ttu-id="a5470-297">Z é a variável de nível preto.</span><span class="sxs-lookup"><span data-stu-id="a5470-297">Z is the black-level variable.</span></span> <span data-ttu-id="a5470-298">Para o computador RGB, Z é igual a 0.</span><span class="sxs-lookup"><span data-stu-id="a5470-298">For computer RGB, Z equals 0.</span></span> <span data-ttu-id="a5470-299">Para vídeo RGB do estúdio, Z é igual \* a 16 2 ^ (n-8), em que N é o número de bits por amostra RGB (N >= 8).</span><span class="sxs-lookup"><span data-stu-id="a5470-299">For studio video RGB, Z equals 16\*2^(N-8), where N is the number of bits per RGB sample (N >= 8).</span></span>
-   <span data-ttu-id="a5470-300">S é a variável de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a5470-300">S is the scaling variable.</span></span> <span data-ttu-id="a5470-301">Para o computador RGB, S é igual a 255.</span><span class="sxs-lookup"><span data-stu-id="a5470-301">For computer RGB, S equals 255.</span></span> <span data-ttu-id="a5470-302">Para vídeo RGB do estúdio, S é igual a 219 \* 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="a5470-302">For studio video RGB, S equals 219\*2^(N-8).</span></span>

<span data-ttu-id="a5470-303">A função Floor (x) retorna o maior inteiro menor ou igual a x.</span><span class="sxs-lookup"><span data-stu-id="a5470-303">The function floor(x) returns the largest integer less than or equal to x.</span></span> <span data-ttu-id="a5470-304">A função clip3 (x, y, z) é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5470-304">The function clip3(x, y, z) is defined as follows:</span></span>

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> <span data-ttu-id="a5470-305">clip3 deve ser implementado como uma função em vez de uma macro de pré-processador; caso contrário, várias avaliações dos argumentos ocorrerão.</span><span class="sxs-lookup"><span data-stu-id="a5470-305">clip3 should be implemented as a function rather than a preprocessor macro; otherwise multiple evaluations of the arguments will occur.</span></span>

 

<span data-ttu-id="a5470-306">A amostra Y representa o brilho, e as amostras você e V representam os desvios de cor para azul e vermelho, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a5470-306">The Y sample represents brightness, and the U and V samples represent the color deviations toward blue and red, respectively.</span></span> <span data-ttu-id="a5470-307">O intervalo nominal para Y é 16 \* 2 ^ (m-8) a 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="a5470-307">The nominal range for Y is 16\*2^(M-8) to 235\*2^(M-8).</span></span> <span data-ttu-id="a5470-308">O preto é representado como 16 \* 2 ^ (m-8) e o branco é representado como 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="a5470-308">Black is represented as 16\*2^(M-8), and white is represented as 235\*2^(M-8).</span></span> <span data-ttu-id="a5470-309">O intervalo nominal para você e V é 16 \* 2 ^ (m-8) a 240 \* 2 ^ (m-8), com o valor 128 \* 2 ^ (m-8) representando croma neutro.</span><span class="sxs-lookup"><span data-stu-id="a5470-309">The nominal range for U and V are 16\*2^(M-8) to 240\*2^(M-8), with the value 128\*2^(M-8) representing neutral chroma.</span></span> <span data-ttu-id="a5470-310">No entanto, os valores reais podem ficar fora desses intervalos.</span><span class="sxs-lookup"><span data-stu-id="a5470-310">However, actual values may fall outside these ranges.</span></span>

<span data-ttu-id="a5470-311">Para dados de entrada na forma de vídeo RGB do estúdio, a operação de clipe é necessária para manter os valores de você e V dentro do intervalo de 0 a (2 ^ M)-1.</span><span class="sxs-lookup"><span data-stu-id="a5470-311">For input data in the form of studio video RGB, the clip operation is necessary to keep the U and V values within the range 0 to (2^M)-1.</span></span> <span data-ttu-id="a5470-312">Se a entrada for o computador RGB, a operação de clipe não será necessária, pois a fórmula de conversão não poderá produzir valores fora desse intervalo.</span><span class="sxs-lookup"><span data-stu-id="a5470-312">If the input is computer RGB, the clip operation is not required, because the conversion formula cannot produce values outside of this range.</span></span>

<span data-ttu-id="a5470-313">Essas são as fórmulas exatas sem aproximação.</span><span class="sxs-lookup"><span data-stu-id="a5470-313">These are the exact formulas without approximation.</span></span> <span data-ttu-id="a5470-314">Tudo o que se segue neste documento é derivado dessas fórmulas.</span><span class="sxs-lookup"><span data-stu-id="a5470-314">Everything that follows in this document is derived from these formulas.</span></span> <span data-ttu-id="a5470-315">Esta seção descreve as seguintes conversões:</span><span class="sxs-lookup"><span data-stu-id="a5470-315">This section describes the following conversions:</span></span>

-   [<span data-ttu-id="a5470-316">Convertendo RGB888 em YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="a5470-316">Converting RGB888 to YUV 4:4:4</span></span>](#converting-rgb888-to-yuv-444)
-   [<span data-ttu-id="a5470-317">Convertendo YUV de 8 bits em RGB888</span><span class="sxs-lookup"><span data-stu-id="a5470-317">Converting 8-bit YUV to RGB888</span></span>](#converting-8-bit-yuv-to-rgb888)
-   [<span data-ttu-id="a5470-318">Convertendo 4:2:0 YUV para 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-318">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>](#converting-420-yuv-to-422-yuv)
-   [<span data-ttu-id="a5470-319">Convertendo 4:2:2 YUV para 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-319">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>](#converting-422-yuv-to-444-yuv)
-   [<span data-ttu-id="a5470-320">Convertendo 4:2:0 YUV para 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-320">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a><span data-ttu-id="a5470-321">Convertendo RGB888 em YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="a5470-321">Converting RGB888 to YUV 4:4:4</span></span>

<span data-ttu-id="a5470-322">No caso da entrada RGB do computador e da saída YUV do BT de 8 bits. 601, acreditamos que as fórmulas fornecidas na seção anterior podem ser razoavelmente aproximadas pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="a5470-322">In the case of computer RGB input and 8-bit BT.601 YUV output, we believe that the formulas given in the previous section can be reasonably approximated by the following:</span></span>

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

<span data-ttu-id="a5470-323">Essas fórmulas produzem resultados de 8 bits usando coeficientes que não exigem mais de 8 bits de precisão (não assinado).</span><span class="sxs-lookup"><span data-stu-id="a5470-323">These formulas produce 8-bit results using coefficients that require no more than 8 bits of (unsigned) precision.</span></span> <span data-ttu-id="a5470-324">Os resultados intermediários precisarão de até 16 bits de precisão.</span><span class="sxs-lookup"><span data-stu-id="a5470-324">Intermediate results will require up to 16 bits of precision.</span></span>

## <a name="converting-8-bit-yuv-to-rgb888"></a><span data-ttu-id="a5470-325">Convertendo YUV de 8 bits em RGB888</span><span class="sxs-lookup"><span data-stu-id="a5470-325">Converting 8-bit YUV to RGB888</span></span>

<span data-ttu-id="a5470-326">Das fórmulas RGB para YUV originais, uma pode derivar as seguintes relações para BT. 601.</span><span class="sxs-lookup"><span data-stu-id="a5470-326">From the original RGB-to-YUV formulas, one can derive the following relationships for BT.601.</span></span>

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

<span data-ttu-id="a5470-327">Portanto, dada:</span><span class="sxs-lookup"><span data-stu-id="a5470-327">Therefore, given:</span></span>

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

<span data-ttu-id="a5470-328">as fórmulas para converter YUV em RGB podem ser derivadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5470-328">the formulas to convert YUV to RGB can be derived as follows:</span></span>

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

<span data-ttu-id="a5470-329">onde `clip()` denota o recorte para um intervalo de \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="a5470-329">where `clip()` denotes clipping to a range of \[0..255\].</span></span> <span data-ttu-id="a5470-330">Acreditamos que essas fórmulas podem ser razoavelmente aproximadas pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="a5470-330">We believe these formulas can be reasonably approximated by the following:</span></span>

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

<span data-ttu-id="a5470-331">Essas fórmulas usam alguns coeficientes que exigem mais de 8 bits de precisão para produzir cada resultado de 8 bits, e os resultados intermediários precisarão de mais de 16 bits de precisão.</span><span class="sxs-lookup"><span data-stu-id="a5470-331">These formulas use some coefficients that require more than 8 bits of precision to produce each 8-bit result, and intermediate results will require more than 16 bits of precision.</span></span>

<span data-ttu-id="a5470-332">Para converter 4:2:0 ou 4:2:2 YUV em RGB, é recomendável converter os dados YUV para 4:4:4 YUV e, em seguida, converter de 4:4:4 YUV para RGB.</span><span class="sxs-lookup"><span data-stu-id="a5470-332">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="a5470-333">As seções a seguir apresentam alguns métodos para converter os formatos 4:2:0 e 4:2:2 para 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="a5470-333">The sections that follow present some methods for converting 4:2:0 and 4:2:2 formats to 4:4:4.</span></span>

## <a name="converting-420-yuv-to-422-yuv"></a><span data-ttu-id="a5470-334">Convertendo 4:2:0 YUV para 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-334">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>

<span data-ttu-id="a5470-335">Converter 4:2:0 YUV para 4:2:2 YUV requer conversão vertical por um fator de dois.</span><span class="sxs-lookup"><span data-stu-id="a5470-335">Converting 4:2:0 YUV to 4:2:2 YUV requires vertical upconversion by a factor of two.</span></span> <span data-ttu-id="a5470-336">Esta seção descreve um método de exemplo para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="a5470-336">This section describes an example method for performing the upconversion.</span></span> <span data-ttu-id="a5470-337">O método pressupõe que as imagens de vídeo são varredura progressiva.</span><span class="sxs-lookup"><span data-stu-id="a5470-337">The method assumes that the video pictures are progressive scan.</span></span>

> [!Note]  
> <span data-ttu-id="a5470-338">O processo de conversão de verificação entrelaçada 4:2:0 a 4:2:2 apresenta problemas de atípicos e é difícil de implementar.</span><span class="sxs-lookup"><span data-stu-id="a5470-338">The 4:2:0 to 4:2:2 interlaced scan conversion process presents atypical problems and is difficult to implement.</span></span> <span data-ttu-id="a5470-339">Este artigo não aborda o problema de conversão de verificação entrelaçada de 4:2:0 para 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="a5470-339">This article does not address the issue of converting interlaced scan from 4:2:0 to 4:2:2.</span></span>

 

<span data-ttu-id="a5470-340">Deixe que cada linha vertical de exemplos de croma de entrada seja uma matriz `Cin[]` que varia de 0 a N-1.</span><span class="sxs-lookup"><span data-stu-id="a5470-340">Let each vertical line of input chroma samples be an array `Cin[]` that ranges from 0 to N - 1.</span></span> <span data-ttu-id="a5470-341">A linha vertical correspondente na imagem de saída será uma matriz `Cout[]` que varia de 0 a 2n-1.</span><span class="sxs-lookup"><span data-stu-id="a5470-341">The corresponding vertical line on the output image will be an array `Cout[]` that ranges from 0 to 2N - 1.</span></span> <span data-ttu-id="a5470-342">Para converter cada linha vertical, execute o seguinte processo:</span><span class="sxs-lookup"><span data-stu-id="a5470-342">To convert each vertical line, perform the following process:</span></span>

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

<span data-ttu-id="a5470-343">em que clip () denota recorte para um intervalo de \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="a5470-343">where clip() denotes clipping to a range of \[0..255\].</span></span>

> [!Note]  
> <span data-ttu-id="a5470-344">As equações para lidar com as bordas podem ser matematicamente simplificadas.</span><span class="sxs-lookup"><span data-stu-id="a5470-344">The equations for handling the edges can be mathematically simplified.</span></span> <span data-ttu-id="a5470-345">Eles são mostrados neste formulário para ilustrar o efeito de fixação MSS nas bordas da imagem.</span><span class="sxs-lookup"><span data-stu-id="a5470-345">They are shown in this form to illustrate the clamping effect at the edges of the picture.</span></span>

 

<span data-ttu-id="a5470-346">Na verdade, esse método calcula cada valor ausente interpolando a curva sobre os quatro pixels adjacentes, ponderados em direção aos valores dos dois pixels mais próximos (Figura 11).</span><span class="sxs-lookup"><span data-stu-id="a5470-346">In effect, this method calculates each missing value by interpolating the curve over the four adjacent pixels, weighted toward the values of the two nearest pixels (Figure 11).</span></span> <span data-ttu-id="a5470-347">O método de interpolação específico usado neste exemplo gera amostras ausentes em posições de meio-inteiro usando um método conhecido chamado Catmull-Rom interpolação, também conhecido como interpolação de convolução cúbica.</span><span class="sxs-lookup"><span data-stu-id="a5470-347">The specific interpolation method used in this example generates missing samples at half-integer positions using a well-known method called Catmull-Rom interpolation, also known as cubic convolution interpolation.</span></span>

![Figura 11.](images/yuvformats14.gif)

<span data-ttu-id="a5470-350">Em termos de processamento de sinal, a coconversão vertical deve, idealmente, incluir uma compensação de mudança de fase para considerar o deslocamento vertical de meia pixel (em relação à grade de amostragem de 4:2:2 de saída) entre os locais das linhas de exemplo 4:2:0 e o local de cada outra linha de exemplo 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="a5470-350">In signal processing terms, the vertical upconversion should ideally include a phase shift compensation to account for the half-pixel vertical offset (relative to the output 4:2:2 sampling grid) between the locations of the 4:2:0 sample lines and the location of every other 4:2:2 sample line.</span></span> <span data-ttu-id="a5470-351">No entanto, a introdução desse deslocamento aumentaria a quantidade de processamento necessário para gerar os exemplos e tornaria impossível reconstruir os exemplos originais do 4:2:0 da imagem de 4:2:2 de amostra.</span><span class="sxs-lookup"><span data-stu-id="a5470-351">However, introducing this offset would increase the amount of processing required to generate the samples, and make it impossible to reconstruct the original 4:2:0 samples from the upsampled 4:2:2 image.</span></span> <span data-ttu-id="a5470-352">Isso também tornaria impossível decodificar o vídeo diretamente em superfícies de 4:2:2 e, em seguida, usar essas superfícies como imagens de referência para decodificar imagens subsequentes no fluxo.</span><span class="sxs-lookup"><span data-stu-id="a5470-352">It would also make it impossible to decode video directly into 4:2:2 surfaces and then use those surfaces as reference pictures for decoding subsequent pictures in the stream.</span></span> <span data-ttu-id="a5470-353">Portanto, o método fornecido aqui não leva em conta o alinhamento vertical preciso dos exemplos.</span><span class="sxs-lookup"><span data-stu-id="a5470-353">Therefore, the method provided here does not take into account the precise vertical alignment of the samples.</span></span> <span data-ttu-id="a5470-354">Fazer isso provavelmente não é visualmente prejudicial às resoluções de imagem razoavelmente altas.</span><span class="sxs-lookup"><span data-stu-id="a5470-354">Doing so is probably not visually harmful at reasonably high picture resolutions.</span></span>

<span data-ttu-id="a5470-355">Se você começar com o vídeo 4:2:0 que usa a grade de amostragem definida no vídeo H. 261, H. 263 ou MPEG-1, a fase da saída 4:2:2 exemplos de croma também será deslocada por um deslocamento horizontal de meio-pixel em relação ao espaçamento na grade de amostragem de Luma (um deslocamento trimestral em relação ao espaçamento da grade de amostragem 4:2:2 croma).</span><span class="sxs-lookup"><span data-stu-id="a5470-355">If you start with 4:2:0 video that uses the sampling grid defined in H.261, H.263, or MPEG-1 video, the phase of the output 4:2:2 chroma samples will also be shifted by a half-pixel horizontal offset relative to the spacing on the luma sampling grid (a quarter-pixel offset relative to the spacing of the 4:2:2 chroma sampling grid).</span></span> <span data-ttu-id="a5470-356">No entanto, a forma MPEG-2 do vídeo 4:2:0 provavelmente é mais comumente usada em PCs e não sofre com esse problema.</span><span class="sxs-lookup"><span data-stu-id="a5470-356">However, the MPEG-2 form of 4:2:0 video is probably more commonly used on PCs and does not suffer from this problem.</span></span> <span data-ttu-id="a5470-357">Além disso, a distinção provavelmente não é visualmente prejudicial às resoluções de imagem razoavelmente altas.</span><span class="sxs-lookup"><span data-stu-id="a5470-357">Moreover, the distinction is probably not visually harmful at reasonably high picture resolutions.</span></span> <span data-ttu-id="a5470-358">Tentar corrigir esse problema criaria o mesmo tipo de problema discutido para o deslocamento de fase vertical.</span><span class="sxs-lookup"><span data-stu-id="a5470-358">Trying to correct for this problem would create the same sort of problems discussed for the vertical phase offset.</span></span>

## <a name="converting-422-yuv-to-444-yuv"></a><span data-ttu-id="a5470-359">Convertendo 4:2:2 YUV para 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-359">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="a5470-360">Converter 4:2:2 YUV para 4:4:4 YUV exige conversão horizontal por um fator de dois.</span><span class="sxs-lookup"><span data-stu-id="a5470-360">Converting 4:2:2 YUV to 4:4:4 YUV requires horizontal upconversion by a factor of two.</span></span> <span data-ttu-id="a5470-361">O método descrito anteriormente para upconverter vertical também pode ser aplicado à upconversão horizontal.</span><span class="sxs-lookup"><span data-stu-id="a5470-361">The method described previously for vertical upconversion can also be applied to horizontal upconversion.</span></span> <span data-ttu-id="a5470-362">Para o vídeo MPEG-2 e ITU-R BT. 601, esse método produzirá exemplos com o alinhamento de fase correto.</span><span class="sxs-lookup"><span data-stu-id="a5470-362">For MPEG-2 and ITU-R BT.601 video, this method will produce samples with the correct phase alignment.</span></span>

## <a name="converting-420-yuv-to-444-yuv"></a><span data-ttu-id="a5470-363">Convertendo 4:2:0 YUV para 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-363">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="a5470-364">Para converter 4:2:0 YUV para 4:4:4 YUV, você pode simplesmente seguir os dois métodos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a5470-364">To convert 4:2:0 YUV to 4:4:4 YUV, you can simply follow the two methods described previously.</span></span> <span data-ttu-id="a5470-365">Converta a imagem 4:2:0 em 4:2:2 e converta a imagem 4:2:2 em 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="a5470-365">Convert the 4:2:0 image to 4:2:2, and then convert the 4:2:2 image to 4:4:4.</span></span> <span data-ttu-id="a5470-366">Você também pode alternar a ordem dos dois processos de upconversão, uma vez que a ordem da operação não importa muito para a qualidade visual do resultado.</span><span class="sxs-lookup"><span data-stu-id="a5470-366">You can also switch the order of the two upconversion processes, as the order of operation does not really matter to the visual quality of the result.</span></span>

## <a name="other-yuv-formats"></a><span data-ttu-id="a5470-367">Outros formatos YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-367">Other YUV Formats</span></span>

<span data-ttu-id="a5470-368">Alguns outros formatos YUV menos comuns incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a5470-368">Some other, less common YUV formats include the following:</span></span>

-   <span data-ttu-id="a5470-369">AI44 é um formato YUV palettized com 8 bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="a5470-369">AI44 is a palettized YUV format with 8 bits per sample.</span></span> <span data-ttu-id="a5470-370">Cada exemplo contém um índice nos quatro bits mais significativos (MSBs) e um valor alfa nos quatro bits menos significativos (LSBs).</span><span class="sxs-lookup"><span data-stu-id="a5470-370">Each sample contains an index in the 4 most significant bits (MSBs) and an alpha value in the 4 least significant bits (LSBs).</span></span> <span data-ttu-id="a5470-371">O índice refere-se a uma matriz de entradas de paleta YUV, que devem ser definidas no tipo de mídia para o formato.</span><span class="sxs-lookup"><span data-stu-id="a5470-371">The index refers to an array of YUV palette entries, which must be defined in the media type for the format.</span></span> <span data-ttu-id="a5470-372">Esse formato é usado principalmente para imagens de subimagem.</span><span class="sxs-lookup"><span data-stu-id="a5470-372">This format is primarily used for subpicture images.</span></span>
-   <span data-ttu-id="a5470-373">NV11 é um formato planar de 4:1:1 com 12 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="a5470-373">NV11 is a 4:1:1 planar format with 12 bits per pixel.</span></span> <span data-ttu-id="a5470-374">Os exemplos Y aparecem primeiro na memória.</span><span class="sxs-lookup"><span data-stu-id="a5470-374">The Y samples appear first in memory.</span></span> <span data-ttu-id="a5470-375">O plano Y é seguido por uma matriz de exemplos de U (CB) e V (CR) empacotados.</span><span class="sxs-lookup"><span data-stu-id="a5470-375">The Y plane is followed by an array of packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="a5470-376">Quando a matriz de U-V combinada é endereçada como uma matriz de valores de **palavras** little-endian, os exemplos de u estão contidos no LSBs de cada **palavra** e os exemplos de V estão contidos no MSBs.</span><span class="sxs-lookup"><span data-stu-id="a5470-376">When the combined U-V array is addressed as an array of little-endian **WORD** values, the U samples are contained in the LSBs of each **WORD**, and the V samples are contained in the MSBs.</span></span> <span data-ttu-id="a5470-377">(Esse layout de memória é semelhante a NV12, embora a amostragem de croma seja diferente.)</span><span class="sxs-lookup"><span data-stu-id="a5470-377">(This memory layout is similar to NV12 although the chroma sampling is different.)</span></span>
-   <span data-ttu-id="a5470-378">Y41P é um formato empacotado 4:1:1, com você e V amostrados a cada quarto pixel horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="a5470-378">Y41P is a 4:1:1 packed format, with U and V sampled every fourth pixel horizontally.</span></span> <span data-ttu-id="a5470-379">Cada macropixel contém 8 pixels em três bytes, com o seguinte layout de byte: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span><span class="sxs-lookup"><span data-stu-id="a5470-379">Each macropixel contains 8 pixels in three bytes, with the following byte layout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span></span>
-   <span data-ttu-id="a5470-380">Y41T é idêntico a Y41P, exceto que o bit menos significativo de cada amostra Y especifica a chave croma (0 = Transparent, 1 = opaco).</span><span class="sxs-lookup"><span data-stu-id="a5470-380">Y41T is identical to Y41P, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="a5470-381">Y42T é idêntico a UYVY, exceto que o bit menos significativo de cada amostra Y especifica a chave croma (0 = Transparent, 1 = opaco).</span><span class="sxs-lookup"><span data-stu-id="a5470-381">Y42T is identical to UYVY, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="a5470-382">YVYU é equivalente a YUYV, exceto que as amostras você e V são trocadas.</span><span class="sxs-lookup"><span data-stu-id="a5470-382">YVYU is equivalent to YUYV except the U and V samples are swapped.</span></span>

## <a name="identifying-yuv-formats-in-media-foundation"></a><span data-ttu-id="a5470-383">Identificando formatos YUV no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5470-383">Identifying YUV Formats in Media Foundation</span></span>

<span data-ttu-id="a5470-384">Cada um dos formatos YUV descritos neste artigo tem um código FOURCC atribuído.</span><span class="sxs-lookup"><span data-stu-id="a5470-384">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="a5470-385">Um código FOURCC é um inteiro sem sinal de 32 bits que é criado pela concatenação de quatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="a5470-385">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

<span data-ttu-id="a5470-386">Há várias macros C/C++ que facilitam a declaração de valores FOURCC no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="a5470-386">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="a5470-387">Por exemplo, a macro **MAKEFOURCC** é declarada em mmsystem. h e a macro **FCC** é declarada em Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="a5470-387">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="a5470-388">Use-os da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5470-388">Use them as follows:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

<span data-ttu-id="a5470-389">Você também pode declarar um código FOURCC diretamente como um literal de cadeia de caracteres simplesmente revertendo a ordem dos caracteres.</span><span class="sxs-lookup"><span data-stu-id="a5470-389">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="a5470-390">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a5470-390">For example:</span></span>

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

<span data-ttu-id="a5470-391">A reversão do pedido é necessária porque o sistema operacional Windows usa uma arquitetura little-endian.</span><span class="sxs-lookup"><span data-stu-id="a5470-391">Reversing the order is necessary because the Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="a5470-392">' Y ' = 0x59, ' U ' = 0x55 e ' 2 ' = 0x32, portanto, ' 2YUY ' é 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="a5470-392">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

<span data-ttu-id="a5470-393">Em Media Foundation, os formatos são identificados por um GUID de tipo principal e um GUID de subtipo.</span><span class="sxs-lookup"><span data-stu-id="a5470-393">In Media Foundation, formats are identified by a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="a5470-394">O tipo principal para formatos de vídeo do computador é sempre MFMediaType \_ vídeo.</span><span class="sxs-lookup"><span data-stu-id="a5470-394">The major type for computer video formats is always MFMediaType\_Video .</span></span> <span data-ttu-id="a5470-395">O subtipo pode ser construído mapeando o código FOURCC para um GUID, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a5470-395">The subtype can be constructed by mapping the FOURCC code to a GUID, as follows:</span></span>

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="a5470-396">em que `XXXXXXXX` é o código FOURCC.</span><span class="sxs-lookup"><span data-stu-id="a5470-396">where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="a5470-397">Portanto, o GUID de subtipo para YUY2 é:</span><span class="sxs-lookup"><span data-stu-id="a5470-397">Thus, the subtype GUID for YUY2 is:</span></span>

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="a5470-398">As constantes para os GUIDs de formato YUV mais comuns são definidas no arquivo de cabeçalho mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="a5470-398">Constants for the most common YUV format GUIDs are defined in the header file mfapi.h.</span></span> <span data-ttu-id="a5470-399">Para obter uma lista dessas constantes, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a5470-399">For a list of these constants, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5470-400">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5470-400">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5470-401">Sobre o vídeo YUV</span><span class="sxs-lookup"><span data-stu-id="a5470-401">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="a5470-402">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="a5470-402">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



