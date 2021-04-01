---
description: Este tópico descreve dois conceitos relacionados, a taxa de proporção de imagem e a taxa de proporção de pixel.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Taxa de proporção da imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164897"
---
# <a name="picture-aspect-ratio"></a><span data-ttu-id="a7e64-103">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="a7e64-103">Picture Aspect Ratio</span></span>

<span data-ttu-id="a7e64-104">Este tópico descreve dois conceitos relacionados, a taxa de proporção de imagem e a taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="a7e64-104">This topic describes two related concepts, picture aspect ratio and pixel aspect ratio.</span></span> <span data-ttu-id="a7e64-105">Em seguida, ele descreve como esses conceitos são expressos em Microsoft Media Foundation usando tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a7e64-105">It then describes how these concepts are expressed in Microsoft Media Foundation using media types.</span></span>

-   [<span data-ttu-id="a7e64-106">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="a7e64-106">Picture Aspect Ratio</span></span>](#picture-aspect-ratio)
    -   [<span data-ttu-id="a7e64-107">Formato Letterbox</span><span class="sxs-lookup"><span data-stu-id="a7e64-107">Letterboxing</span></span>](#letterboxing)
    -   [<span data-ttu-id="a7e64-108">Panorâmica e verificação</span><span class="sxs-lookup"><span data-stu-id="a7e64-108">Pan-and-Scan</span></span>](#pan-and-scan)
-   [<span data-ttu-id="a7e64-109">Taxa de proporção de pixel</span><span class="sxs-lookup"><span data-stu-id="a7e64-109">Pixel Aspect Ratio</span></span>](#pixel-aspect-ratio)
-   [<span data-ttu-id="a7e64-110">Trabalhando com taxas de proporção</span><span class="sxs-lookup"><span data-stu-id="a7e64-110">Working with Aspect Ratios</span></span>](#working-with-aspect-ratios)
-   [<span data-ttu-id="a7e64-111">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="a7e64-111">Code Examples</span></span>](#code-examples)
    -   [<span data-ttu-id="a7e64-112">Localizando a área de exibição</span><span class="sxs-lookup"><span data-stu-id="a7e64-112">Finding the Display Area</span></span>](#finding-the-display-area)
    -   [<span data-ttu-id="a7e64-113">Convertendo taxas de proporção de pixel</span><span class="sxs-lookup"><span data-stu-id="a7e64-113">Converting Between Pixel Aspect Ratios</span></span>](#converting-between-pixel-aspect-ratios)
    -   [<span data-ttu-id="a7e64-114">Calculando a área Letterbox</span><span class="sxs-lookup"><span data-stu-id="a7e64-114">Calculating the Letterbox Area</span></span>](#calculating-the-letterbox-area)
-   [<span data-ttu-id="a7e64-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7e64-115">Related topics</span></span>](#related-topics)

## <a name="picture-aspect-ratio"></a><span data-ttu-id="a7e64-116">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="a7e64-116">Picture Aspect Ratio</span></span>

<span data-ttu-id="a7e64-117">A *taxa de proporção da imagem* define a forma da imagem de vídeo exibida.</span><span class="sxs-lookup"><span data-stu-id="a7e64-117">*Picture aspect ratio* defines the shape of the displayed video image.</span></span> <span data-ttu-id="a7e64-118">A taxa de proporção da imagem é X:Yda, em que X:Y é a proporção da largura da imagem até a altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="a7e64-118">Picture aspect ratio is notated X:Y, where X:Y is the ratio of picture width to picture height.</span></span> <span data-ttu-id="a7e64-119">A maioria dos padrões de vídeo usa a taxa de proporção de imagem 4:3 ou 16:9.</span><span class="sxs-lookup"><span data-stu-id="a7e64-119">Most video standards use either 4:3 or 16:9 picture aspect ratio.</span></span> <span data-ttu-id="a7e64-120">A taxa de proporção de 16:9 é geralmente chamada de *widescreen*.</span><span class="sxs-lookup"><span data-stu-id="a7e64-120">The 16:9 aspect ratio is commonly called *widescreen*.</span></span> <span data-ttu-id="a7e64-121">O filme cinema geralmente usa uma taxa de proporção de 1:85:1 ou 1:66:1.</span><span class="sxs-lookup"><span data-stu-id="a7e64-121">Cinema film often uses a 1:85:1 or 1:66:1 aspect ratio.</span></span> <span data-ttu-id="a7e64-122">A taxa de proporção da imagem também é chamada de *exibição de taxa de proporção* (dar).</span><span class="sxs-lookup"><span data-stu-id="a7e64-122">Picture aspect ratio is also called *display aspect ratio* (DAR).</span></span>

![diagrama mostrando as taxas de proporção 4:3 e 16:9](images/aspect-ratio01.png)

<span data-ttu-id="a7e64-124">Às vezes, a imagem de vídeo não tem a mesma forma que a área de exibição.</span><span class="sxs-lookup"><span data-stu-id="a7e64-124">Sometimes the video image does not have the same shape as the display area.</span></span> <span data-ttu-id="a7e64-125">Por exemplo, um vídeo 4:3 pode ser mostrado em uma televisão widescreen (16 × 9).</span><span class="sxs-lookup"><span data-stu-id="a7e64-125">For example, a 4:3 video might be shown on a widescreen (16×9) television.</span></span> <span data-ttu-id="a7e64-126">No vídeo do computador, o vídeo pode ser mostrado dentro de uma janela que tem um tamanho arbitrário.</span><span class="sxs-lookup"><span data-stu-id="a7e64-126">In computer video, the video might be shown inside a window that has an arbitrary size.</span></span> <span data-ttu-id="a7e64-127">Nesse caso, há três maneiras pelas quais a imagem pode ser ajustada na área de exibição:</span><span class="sxs-lookup"><span data-stu-id="a7e64-127">In that case, there are three ways the image can be made to fit within the display area:</span></span>

-   <span data-ttu-id="a7e64-128">Alongar a imagem ao longo de um eixo para se ajustar à área de exibição.</span><span class="sxs-lookup"><span data-stu-id="a7e64-128">Stretch the image along one axis to fit the display area.</span></span>
-   <span data-ttu-id="a7e64-129">Dimensione a imagem para ajustá-la à área de exibição, mantendo a taxa de proporção da imagem original.</span><span class="sxs-lookup"><span data-stu-id="a7e64-129">Scale the image to fit the display area, while maintaining the original picture aspect ratio.</span></span>
-   <span data-ttu-id="a7e64-130">Cortar a imagem.</span><span class="sxs-lookup"><span data-stu-id="a7e64-130">Crop the image.</span></span>

<span data-ttu-id="a7e64-131">Esticar a imagem para se ajustar à área de exibição está quase sempre errado, pois não preserva a taxa de proporção da imagem correta.</span><span class="sxs-lookup"><span data-stu-id="a7e64-131">Stretching the image to fit the display area is almost always wrong, because it does not preserve the correct picture aspect ratio.</span></span>

### <a name="letterboxing"></a><span data-ttu-id="a7e64-132">Formato Letterbox</span><span class="sxs-lookup"><span data-stu-id="a7e64-132">Letterboxing</span></span>

<span data-ttu-id="a7e64-133">O processo de dimensionamento de uma imagem widescreen para se ajustar a uma exibição de 4:3 é chamado de *formato Letterbox*, mostrado no próximo diagrama.</span><span class="sxs-lookup"><span data-stu-id="a7e64-133">The process of scaling a widescreen image to fit a 4:3 display is called *letterboxing*, shown in the next diagram.</span></span> <span data-ttu-id="a7e64-134">As áreas rectanglular resultantes na parte superior e inferior da imagem normalmente são preenchidas com preto, embora outras cores possam ser usadas.</span><span class="sxs-lookup"><span data-stu-id="a7e64-134">The resulting rectanglular areas at the top and bottom of the image are typically filled with black, although other colors can be used.</span></span>

![diagrama mostrando a maneira correta de Letterbox](images/aspect-ratio02.png)

<span data-ttu-id="a7e64-136">O caso inverso, dimensionando uma imagem 4:3 para se ajustar a uma tela widescreen, às vezes é chamado de *pillarboxing*.</span><span class="sxs-lookup"><span data-stu-id="a7e64-136">The reverse case, scaling a 4:3 image to fit a widescreen display, is sometimes called *pillarboxing*.</span></span> <span data-ttu-id="a7e64-137">No entanto, o termo *Letterbox* também é usado em um sentido geral, para significar o dimensionamento de uma imagem de vídeo para se ajustar a qualquer área de exibição específica.</span><span class="sxs-lookup"><span data-stu-id="a7e64-137">However, the term *letterbox* is also used in a general sense, to mean scaling a video image to fit any given display area.</span></span>

![diagrama mostrando pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a><span data-ttu-id="a7e64-139">Panorâmica e verificação</span><span class="sxs-lookup"><span data-stu-id="a7e64-139">Pan-and-Scan</span></span>

<span data-ttu-id="a7e64-140">A panorâmica e a verificação é uma técnica na qual uma imagem em tela larga é cortada em uma área retangular de 4 × 3, para exibição em um dispositivo de vídeo 4:3.</span><span class="sxs-lookup"><span data-stu-id="a7e64-140">Pan-and-scan is a technique whereby a widescreen image is cropped to a 4×3 rectangular area, for display on a 4:3 display device.</span></span> <span data-ttu-id="a7e64-141">A imagem resultante preenche toda a tela, sem a necessidade de áreas Letterbox pretas, mas partes da imagem original são cortadas fora da imagem.</span><span class="sxs-lookup"><span data-stu-id="a7e64-141">The resulting image fills the entire display, without requiring black letterbox areas, but portions of the original image are cropped out of the picture.</span></span> <span data-ttu-id="a7e64-142">A área cortada pode passar de um quadro para um quadro, como a área de deslocamentos de juros.</span><span class="sxs-lookup"><span data-stu-id="a7e64-142">The area that is cropped can move from frame to frame, as the area of interest shifts.</span></span> <span data-ttu-id="a7e64-143">O termo "panorâmica" em *panorâmica e digitalização* refere-se ao efeito de panorâmica que é causado pela movimentação da área de panorâmica e exame.</span><span class="sxs-lookup"><span data-stu-id="a7e64-143">The term "pan" in *pan-and-scan* refers to the panning effect that is caused by moving the pan-and-scan area.</span></span>

![diagrama mostrando a panorâmica e a verificação](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a><span data-ttu-id="a7e64-145">Taxa de proporção de pixel</span><span class="sxs-lookup"><span data-stu-id="a7e64-145">Pixel Aspect Ratio</span></span>

<span data-ttu-id="a7e64-146">*Taxa de proporção de pixel* (par) mede a forma de um pixel.</span><span class="sxs-lookup"><span data-stu-id="a7e64-146">*Pixel aspect ratio* (PAR) measures the shape of a pixel.</span></span>

<span data-ttu-id="a7e64-147">Quando uma imagem digital é capturada, a imagem é amostrada vertical e horizontalmente, resultando em uma matriz retangular de amostras quantificadas, chamadas de *pixels* ou *pixels*.</span><span class="sxs-lookup"><span data-stu-id="a7e64-147">When a digital image is captured, the image is sampled both vertically and horizontally, resulting in a rectangular array of quantized samples, called *pixels* or *pels*.</span></span> <span data-ttu-id="a7e64-148">A forma da grade de amostragem determina a forma dos pixels na imagem digitalizada.</span><span class="sxs-lookup"><span data-stu-id="a7e64-148">The shape of the sampling grid determines the shape of the pixels in the digitized image.</span></span>

<span data-ttu-id="a7e64-149">Aqui está um exemplo que usa números pequenos para manter a matemática simples.</span><span class="sxs-lookup"><span data-stu-id="a7e64-149">Here is an example that uses small numbers to keep the math simple.</span></span> <span data-ttu-id="a7e64-150">Suponha que a imagem original seja quadrada (ou seja, a taxa de proporção da imagem é 1:1); e suponha que a grade de amostragem contenha 12 elementos, organizados em uma grade 4 × 3.</span><span class="sxs-lookup"><span data-stu-id="a7e64-150">Suppose that the original image is square (that is, the picture aspect ratio is 1:1); and suppose the sampling grid contains 12 elements, arranged in a 4×3 grid.</span></span> <span data-ttu-id="a7e64-151">A forma de cada pixel resultante será mais alta do que a largura.</span><span class="sxs-lookup"><span data-stu-id="a7e64-151">The shape of each resulting pixel will be taller than it is wide.</span></span> <span data-ttu-id="a7e64-152">Especificamente, a forma de cada pixel será 3 × 4.</span><span class="sxs-lookup"><span data-stu-id="a7e64-152">Specifically, the shape of each pixel will be 3×4.</span></span> <span data-ttu-id="a7e64-153">Os pixels que não são quadrados são chamados *de pixels não quadrados*.</span><span class="sxs-lookup"><span data-stu-id="a7e64-153">Pixels that are not square are called *non-square pixels*.</span></span>

![diagrama mostrando uma grade de amostragem não quadrada](images/aspect-ratio05.png)

<span data-ttu-id="a7e64-155">A taxa de proporção de pixel também se aplica ao dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a7e64-155">Pixel aspect ratio also applies to the display device.</span></span> <span data-ttu-id="a7e64-156">A forma física do dispositivo de vídeo e a resolução de pixels físicos (horizontalmente) determinam o PAR do dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a7e64-156">The physical shape of the display device and the physical pixel resolution (across and down) determine the PAR of the display device.</span></span> <span data-ttu-id="a7e64-157">Os monitores de computador geralmente usam pixels quadrados.</span><span class="sxs-lookup"><span data-stu-id="a7e64-157">Computer monitors generally use square pixels.</span></span> <span data-ttu-id="a7e64-158">Se a imagem PAR e o PAR de exibição não coincidirem, a imagem deverá ser dimensionada em uma dimensão, vertical ou horizontalmente, para ser exibida corretamente.</span><span class="sxs-lookup"><span data-stu-id="a7e64-158">If the image PAR and the display PAR do not match, the image must be scaled in one dimension, either vertically or horizontally, in order to display correctly.</span></span> <span data-ttu-id="a7e64-159">A fórmula a seguir relaciona o PAR, a taxa de proporção de exibição (DAR) e o tamanho da imagem em pixels:</span><span class="sxs-lookup"><span data-stu-id="a7e64-159">The following formula relates PAR, display aspect ratio (DAR), and image size in pixels:</span></span>

<span data-ttu-id="a7e64-160">*Dar* = (*largura da imagem em pixels*,  /  *altura da imagem em pixels*) × *par*</span><span class="sxs-lookup"><span data-stu-id="a7e64-160">*DAR* = (*image width in pixels* / *image height in pixels*) × *PAR*</span></span>

<span data-ttu-id="a7e64-161">Observe que a largura da imagem e a altura da imagem nessa fórmula referem-se à imagem na memória, não à imagem exibida.</span><span class="sxs-lookup"><span data-stu-id="a7e64-161">Note that image width and image height in this formula refer to the image in memory, not the displayed image.</span></span>

<span data-ttu-id="a7e64-162">Aqui está um exemplo do mundo real: o vídeo analógico da NTSC-M contém 480 linhas de digitalização na área de imagem ativa.</span><span class="sxs-lookup"><span data-stu-id="a7e64-162">Here is a real-world example: NTSC-M analog video contains 480 scan lines in the active image area.</span></span> <span data-ttu-id="a7e64-163">ITU-R rec. BT. 601 especifica uma taxa de amostragem horizontal de 704 pixels visíveis por linha, produzindo uma imagem digital com 704 x 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="a7e64-163">ITU-R Rec. BT.601 specifies a horizontal sampling rate of 704 visible pixels per line, yielding a digital image with 704 x 480 pixels.</span></span> <span data-ttu-id="a7e64-164">A taxa de proporção de imagem pretendida é 4:3, produzindo um PAR de 10:11.</span><span class="sxs-lookup"><span data-stu-id="a7e64-164">The intended picture aspect ratio is 4:3, yielding a PAR of 10:11.</span></span>

-   <span data-ttu-id="a7e64-165">DAR: 4:3</span><span class="sxs-lookup"><span data-stu-id="a7e64-165">DAR: 4:3</span></span>
-   <span data-ttu-id="a7e64-166">Largura em pixels: 704</span><span class="sxs-lookup"><span data-stu-id="a7e64-166">Width in pixels: 704</span></span>
-   <span data-ttu-id="a7e64-167">Altura em pixels: 480</span><span class="sxs-lookup"><span data-stu-id="a7e64-167">Height in pixels: 480</span></span>
-   <span data-ttu-id="a7e64-168">PAR: 10/11</span><span class="sxs-lookup"><span data-stu-id="a7e64-168">PAR: 10/11</span></span>

<span data-ttu-id="a7e64-169">4/3 = (704/420) x (10/11)</span><span class="sxs-lookup"><span data-stu-id="a7e64-169">4/3 = (704/420) x (10/11)</span></span>

<span data-ttu-id="a7e64-170">Para exibir essa imagem corretamente em um dispositivo de vídeo com pixels quadrados, você deve dimensionar a largura em 10/11 ou a altura em 11/10.</span><span class="sxs-lookup"><span data-stu-id="a7e64-170">To display this image correctly on a display device with square pixels, you must scale either the width by 10/11 or the height by 11/10.</span></span>

## <a name="working-with-aspect-ratios"></a><span data-ttu-id="a7e64-171">Trabalhando com taxas de proporção</span><span class="sxs-lookup"><span data-stu-id="a7e64-171">Working with Aspect Ratios</span></span>

<span data-ttu-id="a7e64-172">A forma correta de um quadro de vídeo é definida pela *taxa de proporção de pixel* (par) e pela *área de exibição*.</span><span class="sxs-lookup"><span data-stu-id="a7e64-172">The correct shape of a video frame is defined by the *pixel aspect ratio* (PAR) and the *display area*.</span></span>

-   <span data-ttu-id="a7e64-173">O PAR define a forma dos pixels em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="a7e64-173">The PAR defines the shape of the pixels in an image.</span></span> <span data-ttu-id="a7e64-174">Pixels quadrados têm uma taxa de proporção de 1:1.</span><span class="sxs-lookup"><span data-stu-id="a7e64-174">Square pixels have an aspect ratio of 1:1.</span></span> <span data-ttu-id="a7e64-175">Qualquer outra taxa de proporção descreve um pixel não quadrado.</span><span class="sxs-lookup"><span data-stu-id="a7e64-175">Any other aspect ratio describes a non-square pixel.</span></span> <span data-ttu-id="a7e64-176">Por exemplo, a televisão NTSC usa um PAR de 10:11.</span><span class="sxs-lookup"><span data-stu-id="a7e64-176">For example, NTSC television uses a 10:11 PAR.</span></span> <span data-ttu-id="a7e64-177">Supondo que você esteja apresentando o vídeo em um monitor de computador, a exibição terá pixels quadrados (1:1 PAR).</span><span class="sxs-lookup"><span data-stu-id="a7e64-177">Assuming that you are presenting the video on a computer monitor, the display will have square pixels (1:1 PAR).</span></span> <span data-ttu-id="a7e64-178">O PAR do conteúdo de origem é fornecido no atributo [**de \_ \_ taxa de \_ proporção \_ MF MT pixel**](mf-mt-pixel-aspect-ratio-attribute.md) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a7e64-178">The PAR of the source content is given in the [**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute on the media type.</span></span>
-   <span data-ttu-id="a7e64-179">A área de exibição é a região da imagem de vídeo que deve ser mostrada.</span><span class="sxs-lookup"><span data-stu-id="a7e64-179">The display area is the region of the video image that is intended to be shown.</span></span> <span data-ttu-id="a7e64-180">Há duas áreas de exibição relevantes que podem ser especificadas no tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="a7e64-180">There are two relevant display areas that might be specified in the media type:</span></span>
    -   <span data-ttu-id="a7e64-181">Abertura de panorâmica e digitalização.</span><span class="sxs-lookup"><span data-stu-id="a7e64-181">Pan-and-scan aperture.</span></span> <span data-ttu-id="a7e64-182">A abertura de panorâmica e digitalização é uma região de 4 × 3 de vídeo que deve ser exibida no modo de panorâmica/digitalização.</span><span class="sxs-lookup"><span data-stu-id="a7e64-182">The pan-and-scan aperture is a 4×3 region of video that should be displayed in pan/scan mode.</span></span> <span data-ttu-id="a7e64-183">Ele é usado para mostrar o conteúdo de tela larga em uma exibição de 4 × 3 sem formato letterbox.</span><span class="sxs-lookup"><span data-stu-id="a7e64-183">It is used to show wide-screen content on a 4×3 display without letterboxing.</span></span> <span data-ttu-id="a7e64-184">A abertura de Pan-and-scan é fornecida no atributo [**MF \_ MT Pan de \_ \_ \_ abertura da varredura**](mf-mt-pan-scan-aperture-attribute.md) e deve ser usada somente quando o atributo de verificação de Pan do [**MF \_ MT \_ \_ \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md) for **true**.</span><span class="sxs-lookup"><span data-stu-id="a7e64-184">The pan-and-scan aperture is given in the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute and should be used only when the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute is **TRUE**.</span></span>
    -   <span data-ttu-id="a7e64-185">Exibir abertura.</span><span class="sxs-lookup"><span data-stu-id="a7e64-185">Display aperture.</span></span> <span data-ttu-id="a7e64-186">Essa abertura é definida em alguns padrões de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a7e64-186">This aperture is defined in some video standards.</span></span> <span data-ttu-id="a7e64-187">Qualquer coisa fora da abertura de exibição é a região de sobrevarredura e não deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="a7e64-187">Anything outside of the display aperture is the overscan region and should not be displayed.</span></span> <span data-ttu-id="a7e64-188">Por exemplo, a televisão NTSC tem 720 × 480 pixels com uma abertura de exibição de 704 × 480.</span><span class="sxs-lookup"><span data-stu-id="a7e64-188">For example, NTSC television is 720×480 pixels with a display aperture of 704×480.</span></span> <span data-ttu-id="a7e64-189">A abertura de exibição é fornecida no atributo de [**\_ \_ \_ \_ abertura de exibição mínima de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e64-189">The display aperture is given in the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span> <span data-ttu-id="a7e64-190">Se estiver presente, ele deverá ser usado quando o modo Pan-and-scan for **false**.</span><span class="sxs-lookup"><span data-stu-id="a7e64-190">If present, it should be used when pan-and-scan mode is **FALSE**.</span></span>

<span data-ttu-id="a7e64-191">Se o modo Pan-and-can for **false** e nenhuma abertura de exibição for definida, o quadro de vídeo inteiro deverá ser exibido.</span><span class="sxs-lookup"><span data-stu-id="a7e64-191">If pan-and-can mode is **FALSE** and no display aperture is defined, the entire video frame should be displayed.</span></span> <span data-ttu-id="a7e64-192">Na verdade, esse é o caso para a maioria dos conteúdos de vídeo além do vídeo de televisão e DVD.</span><span class="sxs-lookup"><span data-stu-id="a7e64-192">In fact, this is the case for most video content other than television and DVD video.</span></span> <span data-ttu-id="a7e64-193">A taxa de proporção de toda a imagem é calculada como (altura da área de exibição da *largura da área de exibição*  /  ) × *par*.</span><span class="sxs-lookup"><span data-stu-id="a7e64-193">The aspect ratio of the entire picture is calculated as (*display area width* / *display area height*) × *PAR*.</span></span>

## <a name="code-examples"></a><span data-ttu-id="a7e64-194">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="a7e64-194">Code Examples</span></span>

### <a name="finding-the-display-area"></a><span data-ttu-id="a7e64-195">Localizando a área de exibição</span><span class="sxs-lookup"><span data-stu-id="a7e64-195">Finding the Display Area</span></span>

<span data-ttu-id="a7e64-196">O código a seguir mostra como obter a área de exibição do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a7e64-196">The following code shows how to get the display area from the media type.</span></span>


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a><span data-ttu-id="a7e64-197">Convertendo taxas de proporção de pixel</span><span class="sxs-lookup"><span data-stu-id="a7e64-197">Converting Between Pixel Aspect Ratios</span></span>

<span data-ttu-id="a7e64-198">O código a seguir mostra como converter um retângulo de uma taxa de proporção de pixel (PAR) para outro, preservando a taxa de proporção da imagem.</span><span class="sxs-lookup"><span data-stu-id="a7e64-198">The following code shows how to convert a rectangle from one pixel aspect ratio (PAR) to another, while preserving the picture aspect ratio.</span></span>


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a><span data-ttu-id="a7e64-199">Calculando a área Letterbox</span><span class="sxs-lookup"><span data-stu-id="a7e64-199">Calculating the Letterbox Area</span></span>

<span data-ttu-id="a7e64-200">O código a seguir calcula a área Letterbox, dado um retângulo de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="a7e64-200">The following code calculates the letterbox area, given a source and destination rectangle.</span></span> <span data-ttu-id="a7e64-201">Supõe-se que os dois retângulos têm o mesmo PAR.</span><span class="sxs-lookup"><span data-stu-id="a7e64-201">It is assumed that both rectangles have the same PAR.</span></span>


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a><span data-ttu-id="a7e64-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7e64-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7e64-203">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="a7e64-203">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="a7e64-204">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="a7e64-204">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="a7e64-205">**\_abertura de \_ \_ exibição mínima \_ de MF MT**</span><span class="sxs-lookup"><span data-stu-id="a7e64-205">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="a7e64-206">**\_abertura de \_ digitalização de Pan MT \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="a7e64-206">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="a7e64-207">**\_exame de Pan MT do MF \_ \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="a7e64-207">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[<span data-ttu-id="a7e64-208">**taxa de proporção de pixel do MF \_ MT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7e64-208">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



