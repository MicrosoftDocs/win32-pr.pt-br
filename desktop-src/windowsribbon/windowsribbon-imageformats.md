---
title: Especificando recursos de imagem da faixa de uma
description: Como um sistema de apresentação de comando avançado, o Windows Ribbon Framework foi projetado para dar suporte extensivo a recursos de imagem em toda a interface do usuário (IU) da faixa de faixas. Todos os recursos de imagem são declarados na marcação da faixa de lista ou consultados de um aplicativo host da faixa de Ribbon.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Faixa de, recursos de imagem do Windows
- Faixa de das, recursos de imagem
- Faixa de, transparência do Windows
- Faixa de, transparência
- Faixa de, profundidade de cor do Windows
- Faixa de, profundidade de cor
- Faixa de medida do Windows, contraste
- Faixa de faixas, contraste
- recursos de imagem no Windows Ribbon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454266"
---
# <a name="specifying-ribbon-image-resources"></a><span data-ttu-id="e4bd1-113">Especificando recursos de imagem da faixa de uma</span><span class="sxs-lookup"><span data-stu-id="e4bd1-113">Specifying Ribbon Image Resources</span></span>

<span data-ttu-id="e4bd1-114">Como um sistema de apresentação de comando avançado, o Windows Ribbon Framework foi projetado para dar suporte extensivo a recursos de imagem em toda a interface do usuário (IU) da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-114">As a rich command presentation system, the Windows Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="e4bd1-115">Todos os recursos de imagem são declarados na [marcação da faixa](windowsribbon-schema.md) de lista ou consultados de um aplicativo host da faixa de Ribbon.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-115">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="e4bd1-116">Para o Windows 8 e posterior, a estrutura da faixa de opções dá suporte aos seguintes formatos de gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Portable Network Graphics) com transparência.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-116">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="e4bd1-117">Para o Windows 7 e versões anteriores, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado no Windows.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-117">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="e4bd1-118">Um erro de compilação pode ocorrer se um formato de imagem sem suporte for fornecido para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-118">A compilation error may occur if an unsupported image format is supplied to the framework.</span></span>

 

## <a name="image-sizes"></a><span data-ttu-id="e4bd1-119">Tamanhos de imagem</span><span class="sxs-lookup"><span data-stu-id="e4bd1-119">Image Sizes</span></span>

<span data-ttu-id="e4bd1-120">Para fornecer maior flexibilidade para layouts de controle da faixa de opção ao redimensionar uma janela de aplicativo, a estrutura da faixa de faixas aceita e renderiza imagens em um dos dois tamanhos: grande ou pequena.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-120">To provide greater flexibility for Ribbon control layouts when resizing an application window, the Ribbon framework accepts and renders images in one of two sizes: large or small.</span></span>

<span data-ttu-id="e4bd1-121">As imagens a seguir ilustram um aplicativo de faixa de opções que dá suporte a vários tamanhos de faixa de opção por meio de layouts de controle flexíveis e a substituição de imagens grandes com imagens pequenas, quando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-121">The following images illustrate a Ribbon application that supports multiple Ribbon sizes through flexible control layouts and the replacement of large images with small images where available.</span></span>

<span data-ttu-id="e4bd1-122">A captura de tela a seguir mostra a faixa de opções com imagens grandes para os controles de zoom.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-122">The following screen shot shows the Ribbon with large images for the Zoom controls.</span></span>

![captura de tela mostrando uma faixa de faixas que usa imagens grandes para os controles de zoom.](images/overviews/imageresources-largeimage.png)

<span data-ttu-id="e4bd1-124">A captura de tela a seguir mostra a mesma faixa de opções redimensionada com imagens pequenas para os controles de zoom</span><span class="sxs-lookup"><span data-stu-id="e4bd1-124">The following screen shot shows the same Ribbon resized with small images for the Zoom controls</span></span>

![captura de tela mostrando uma faixa de faixas que usa imagens pequenas para os controles de zoom.](images/overviews/imageresources-smallimage.png)

<span data-ttu-id="e4bd1-126">A captura de tela a seguir mostra a faixa de opções no estado oculto.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-126">The following screen shot shows the ribbon in hidden state.</span></span> <span data-ttu-id="e4bd1-127">A faixa de opção fica oculta quando todos os layouts de controle potenciais foram esgotados e a faixa de faixas não pode ser renderizada com um espaço de trabalho de aplicativo utilizável.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-127">The ribbon is hidden when all potential control layouts have been exhausted and the ribbon cannot be rendered with a usable application workspace.</span></span>

![captura de tela mostrando uma faixa de faixas recolhida.](images/overviews/imageresources-noimage.png)

<span data-ttu-id="e4bd1-129">Para qualquer imagem, o tamanho exato do pixel depende da resolução de vídeo ou pontos por polegada (DPI) do monitor que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-129">For any image, the exact pixel size is dependent on the display resolution, or dots per inch (dpi), of the monitor being used.</span></span> <span data-ttu-id="e4bd1-130">Às 96 dpi, as imagens grandes são de 32 a 16 pixels de tamanho e as imagens pequenas têm um tamanho de 16x16 pixels.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-130">At 96 dpi, large images are 32x32 pixels in size and small images are 16x16 pixels in size.</span></span> <span data-ttu-id="e4bd1-131">Os tamanhos de imagem aumentam de maneira linear em relação ao DPI, conforme ilustrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-131">The image sizes increase in a linear fashion relative to dpi as illustrated in the following table.</span></span>



| <span data-ttu-id="e4bd1-132">EXIBI</span><span class="sxs-lookup"><span data-stu-id="e4bd1-132">DPI</span></span>     | <span data-ttu-id="e4bd1-133">Imagem pequena</span><span class="sxs-lookup"><span data-stu-id="e4bd1-133">Small Image</span></span>  | <span data-ttu-id="e4bd1-134">Imagem grande</span><span class="sxs-lookup"><span data-stu-id="e4bd1-134">Large Image</span></span>  |
|---------|--------------|--------------|
| <span data-ttu-id="e4bd1-135">96 dpi</span><span class="sxs-lookup"><span data-stu-id="e4bd1-135">96 dpi</span></span>  | <span data-ttu-id="e4bd1-136">16x16 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-136">16x16 pixels</span></span> | <span data-ttu-id="e4bd1-137">32x32 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-137">32x32 pixels</span></span> |
| <span data-ttu-id="e4bd1-138">120 dpi</span><span class="sxs-lookup"><span data-stu-id="e4bd1-138">120 dpi</span></span> | <span data-ttu-id="e4bd1-139">20x20 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-139">20x20 pixels</span></span> | <span data-ttu-id="e4bd1-140">40x40 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-140">40x40 pixels</span></span> |
| <span data-ttu-id="e4bd1-141">144 dpi</span><span class="sxs-lookup"><span data-stu-id="e4bd1-141">144 dpi</span></span> | <span data-ttu-id="e4bd1-142">24x24 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-142">24x24 pixels</span></span> | <span data-ttu-id="e4bd1-143">48x48 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-143">48x48 pixels</span></span> |
| <span data-ttu-id="e4bd1-144">192 DPI</span><span class="sxs-lookup"><span data-stu-id="e4bd1-144">192 dpi</span></span> | <span data-ttu-id="e4bd1-145">32x32 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-145">32x32 pixels</span></span> | <span data-ttu-id="e4bd1-146">64 x 64 pixels</span><span class="sxs-lookup"><span data-stu-id="e4bd1-146">64x64 pixels</span></span> |



 

<span data-ttu-id="e4bd1-147">A estrutura da faixa de faixas dimensiona os recursos de imagem conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-147">The Ribbon framework scales image resources as required.</span></span> <span data-ttu-id="e4bd1-148">No entanto, como o redimensionamento pode gerar artefatos indesejáveis e degradação de imagem, é altamente recomendável que o aplicativo forneça um pequeno conjunto de recursos de imagem que abrangem várias configurações de DPI usadas com frequência.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-148">However, because resizing may yield undesirable artifacts and image degradation, it is highly recommended that the application provide a small set of image resources that span various commonly used dpi settings.</span></span> <span data-ttu-id="e4bd1-149">Se uma correspondência exata não for encontrada, a imagem mais próxima será dimensionada ou reduzida verticalmente.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-149">If an exact match is not found, the nearest image will be scaled up or down.</span></span>

<span data-ttu-id="e4bd1-150">Para facilitar isso, os recursos de imagem podem ser declarados na marcação da faixa de faixas usando um conjunto de elementos [**Image**](windowsribbon-element-image.md) para cada elemento [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="e4bd1-150">To facilitate this, image resources can be declared in Ribbon markup by using a set of [**Image**](windowsribbon-element-image.md) elements for each [**Command**](windowsribbon-element-command.md) element.</span></span> <span data-ttu-id="e4bd1-151">Em tempo de execução, a estrutura seleciona a imagem a ser exibida com base no atributo *MinDPI* de cada elemento **Image** .</span><span class="sxs-lookup"><span data-stu-id="e4bd1-151">At run time, the framework selects the image to display based on the *MinDPI* attribute of each **Image** element.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e4bd1-152">Quando uma coleção de recursos de imagem que são projetados para dar suporte a configurações de dpi de tela específicas é fornecida à estrutura da faixa de opções por meio de um conjunto de elementos [**Image**](windowsribbon-element-image.md) , a estrutura usa a **imagem** com um valor de atributo *MinDPI* que corresponde à configuração de dpi de tela atual.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-152">When a collection of image resources that are designed to support specific screen dpi settings is supplied to the Ribbon framework through a set of [**Image**](windowsribbon-element-image.md) elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>
>
> <span data-ttu-id="e4bd1-153">Se nenhum elemento [**Image**](windowsribbon-element-image.md) for declarado com um valor *MinDPI* que corresponda à configuração de dpi de tela atual, a estrutura selecionará a **imagem** que tem o valor de *MinDPI* mais próximo menor que a configuração de dpi de tela atual e dimensionará o recurso de imagem para cima.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-153">If no [**Image**](windowsribbon-element-image.md) element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="e4bd1-154">Caso contrário, se nenhum elemento **Image** for declarado com um valor de atributo *MinDPI* menor que a configuração de dpi de tela atual, a estrutura escolherá o valor de *MinDPI* mais próximo maior que a configuração de dpi de tela atual e dimensionará o recurso de imagem para baixo.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-154">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

 

<span data-ttu-id="e4bd1-155">O exemplo a seguir ilustra como declarar um conjunto de imagens para acomodar vários tamanhos de faixa de opções e configurações do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-155">The following example illustrates how to declare a set of images to accommodate various Ribbon sizes and system settings.</span></span>


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



<span data-ttu-id="e4bd1-156">Se as imagens declaradas na marcação forem invalidadas em tempo de execução por qualquer motivo, o aplicativo host será consultado em busca de novas imagens.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-156">If images declared in markup are invalidated at run time for any reason, the host application is queried for new images.</span></span> <span data-ttu-id="e4bd1-157">Quando essas imagens são geradas e carregadas programaticamente, o aplicativo deve tentar retornar imagens que são dimensionadas de acordo com os tamanhos de ícone do sistema padrão determinados pela [ \_ métrica do sistema SM CXICON](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span><span class="sxs-lookup"><span data-stu-id="e4bd1-157">When these images are generated and loaded programmatically, the application should attempt to return images that are sized according to the default system icon sizes determined by the [SM\_CXICON system metric](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span></span>

> [!Note]  
> <span data-ttu-id="e4bd1-158">Imagens grandes têm um tamanho de SM \_ CXICON por SM \_ CXICON e imagens pequenas têm um tamanho de SM \_ CXICON/2 por SM \_ CXICON/2.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-158">Large images have a size of SM\_CXICON by SM\_CXICON and small images have a size of SM\_CXICON/2 by SM\_CXICON/2.</span></span>

 

## <a name="color-depth-transparency-and-contrast"></a><span data-ttu-id="e4bd1-159">Intensidade de cor, transparência e contraste</span><span class="sxs-lookup"><span data-stu-id="e4bd1-159">Color Depth, Transparency, and Contrast</span></span>

<span data-ttu-id="e4bd1-160">Espera-se que as imagens regulares estejam no formato de pixel ARGB de 32 bits por pixel (BPP) e dimensionadas para o tamanho do ícone do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-160">Regular images are expected to be in 32 bits per pixel (BPP) ARGB pixel format and scaled to the default system icon size.</span></span> <span data-ttu-id="e4bd1-161">Esse formato dá suporte à transparência e à suavização (usando 8 bits por canal).</span><span class="sxs-lookup"><span data-stu-id="e4bd1-161">This format supports both transparency and antialiasing (using 8 bits per channel).</span></span>

> [!WARNING]
> <span data-ttu-id="e4bd1-162">Muitas ferramentas de edição de imagens não preservam o canal alfa de 8 bits de ordem mais alta ao carregar ou salvar imagens de 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-162">Many image editing tools do not preserve the highest order 8-bit alpha channel when loading or saving 32 BPP images.</span></span>

 

<span data-ttu-id="e4bd1-163">Para que uma imagem seja exibida corretamente no modo de alto contraste, ela deve estar em um formato de pixel em palete 4 BPP.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-163">For an image to display correctly in high-contrast mode, it must be in a 4 BPP palletized pixel format.</span></span> <span data-ttu-id="e4bd1-164">Quando a imagem é renderizada, a estrutura da faixa de faixas remapeia cores específicas com base no contexto de alto contraste da imagem.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-164">When the image is rendered, the Ribbon framework remaps specific colors based on the high-contrast context of the image.</span></span>

<span data-ttu-id="e4bd1-165">A tabela a seguir lista o comportamento de renderização de cores de alto contraste da estrutura.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-165">The following table lists the high-contrast color rendering behavior of the framework.</span></span>



<span data-ttu-id="e4bd1-166">Cor do pixel</span><span class="sxs-lookup"><span data-stu-id="e4bd1-166">Pixel color</span></span>

<span data-ttu-id="e4bd1-167">Valor RGB</span><span class="sxs-lookup"><span data-stu-id="e4bd1-167">RGB value</span></span>

<span data-ttu-id="e4bd1-168">Comportamento</span><span class="sxs-lookup"><span data-stu-id="e4bd1-168">Behavior</span></span>

<span data-ttu-id="e4bd1-169">Plano de fundo branco</span><span class="sxs-lookup"><span data-stu-id="e4bd1-169">White background</span></span>

<span data-ttu-id="e4bd1-170">Plano de fundo escuro</span><span class="sxs-lookup"><span data-stu-id="e4bd1-170">Dark Background</span></span>

<span data-ttu-id="e4bd1-171">MAGENTA</span><span class="sxs-lookup"><span data-stu-id="e4bd1-171">MAGENTA</span></span>

<span data-ttu-id="e4bd1-172">800080</span><span class="sxs-lookup"><span data-stu-id="e4bd1-172">800080</span></span>

<span data-ttu-id="e4bd1-173">Transparente</span><span class="sxs-lookup"><span data-stu-id="e4bd1-173">Transparent</span></span>

<span data-ttu-id="e4bd1-174">Transparente</span><span class="sxs-lookup"><span data-stu-id="e4bd1-174">Transparent</span></span>

<span data-ttu-id="e4bd1-175">Afasta</span><span class="sxs-lookup"><span data-stu-id="e4bd1-175">BLACK</span></span>

<span data-ttu-id="e4bd1-176">000000</span><span class="sxs-lookup"><span data-stu-id="e4bd1-176">000000</span></span>

<span data-ttu-id="e4bd1-177">WINDOWTEXT de cor \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-177">COLOR\_WINDOWTEXT</span></span>

<span data-ttu-id="e4bd1-178">Branco</span><span class="sxs-lookup"><span data-stu-id="e4bd1-178">WHITE</span></span>

<span data-ttu-id="e4bd1-179">Branco</span><span class="sxs-lookup"><span data-stu-id="e4bd1-179">WHITE</span></span>

<span data-ttu-id="e4bd1-180">FFFFFF</span><span class="sxs-lookup"><span data-stu-id="e4bd1-180">FFFFFF</span></span>

<span data-ttu-id="e4bd1-181">janela de cores \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-181">COLOR\_WINDOW</span></span>

<span data-ttu-id="e4bd1-182">Afasta</span><span class="sxs-lookup"><span data-stu-id="e4bd1-182">BLACK</span></span>

<span data-ttu-id="e4bd1-183">CINZA-ESCURO</span><span class="sxs-lookup"><span data-stu-id="e4bd1-183">DARK GRAY</span></span>

<span data-ttu-id="e4bd1-184">808080</span><span class="sxs-lookup"><span data-stu-id="e4bd1-184">808080</span></span>

<span data-ttu-id="e4bd1-185">3DSHADOW de cor \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-185">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="e4bd1-186">3DSHADOW de cor \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-186">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="e4bd1-187">TONALIDADE</span><span class="sxs-lookup"><span data-stu-id="e4bd1-187">GRAY</span></span>

<span data-ttu-id="e4bd1-188">C0C0C0</span><span class="sxs-lookup"><span data-stu-id="e4bd1-188">C0C0C0</span></span>

<span data-ttu-id="e4bd1-189">3DFACE de cor \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-189">COLOR\_3DFACE</span></span>

<span data-ttu-id="e4bd1-190">3DFACE de cor \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-190">COLOR\_3DFACE</span></span>

<span data-ttu-id="e4bd1-191">CINZA-CLARO</span><span class="sxs-lookup"><span data-stu-id="e4bd1-191">LIGHT GRAY</span></span>

<span data-ttu-id="e4bd1-192">DFDFDF</span><span class="sxs-lookup"><span data-stu-id="e4bd1-192">DFDFDF</span></span>

<span data-ttu-id="e4bd1-193">3DLIGHT de cor \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-193">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="e4bd1-194">3DLIGHT de cor \_</span><span class="sxs-lookup"><span data-stu-id="e4bd1-194">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="e4bd1-195">AZUL-ESCURO</span><span class="sxs-lookup"><span data-stu-id="e4bd1-195">DARK BLUE</span></span>

<span data-ttu-id="e4bd1-196">000080</span><span class="sxs-lookup"><span data-stu-id="e4bd1-196">000080</span></span>

<span data-ttu-id="e4bd1-197">N/D</span><span class="sxs-lookup"><span data-stu-id="e4bd1-197">n/a</span></span>

<span data-ttu-id="e4bd1-198">Branco</span><span class="sxs-lookup"><span data-stu-id="e4bd1-198">WHITE</span></span>



 

<span data-ttu-id="e4bd1-199">Para obter mais informações sobre os formatos de imagem com suporte na estrutura da faixa de opções, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e4bd1-199">For more information on the image formats supported by the Ribbon framework, see the following:</span></span>

-   <span data-ttu-id="e4bd1-200">[Estrutura BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) -descreve o formato de pixel ARGB de 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-200">[BITMAPINFOHEADER structure](/previous-versions//dd183376(v=vs.85)) - describes the 32 BPP ARGB pixel format.</span></span>
-   <span data-ttu-id="e4bd1-201">[Função CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) – descreve como criar uma imagem de formato de pixel ARGB de 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-201">[CreateDIBSection function](/windows/win32/api/wingdi/nf-wingdi-createdibsection) - describes how to create a 32 BPP ARGB pixel format image.</span></span>
-   <span data-ttu-id="e4bd1-202">[Função LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) – descreve como carregar uma imagem de formato de pixel ARGB de 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-202">[LoadImage function](/windows/win32/api/winuser/nf-winuser-loadimagea) - describes how to load a 32 BPP ARGB pixel format image.</span></span>

## <a name="accessibility"></a><span data-ttu-id="e4bd1-203">Acessibilidade</span><span class="sxs-lookup"><span data-stu-id="e4bd1-203">Accessibility</span></span>

<span data-ttu-id="e4bd1-204">Depender de recursos de imagem para fornecer informações, transmitir funcionalidade de controle e expor o estado do aplicativo, aumenta a necessidade de requisitos de acessibilidade durante o design e o desenvolvimento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-204">Relying on image resources to provide information, convey control functionality, and expose application state, increases the need for accessibility requirements during application design and development.</span></span>

<span data-ttu-id="e4bd1-205">Para suporte de alto contraste básico, a faixa de faixas permite que um conjunto separado de arquivos de imagem seja exibido quando um tema de alto contraste está ativo.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-205">For basic high contrast support, the Ribbon allows for a separate set of image files to be displayed when a high-contrast theme is active.</span></span> <span data-ttu-id="e4bd1-206">Essas imagens podem ser 32 BPP ou 4 BPP, com cores mapeadas para uma paleta especial em que as cores escuras e claras são invertidas dependendo das cores de primeiro e segundo plano do tema de alto contraste ativo.</span><span class="sxs-lookup"><span data-stu-id="e4bd1-206">These images can be 32 BPP or 4 BPP, with colors mapped to a special palette where dark and light colors are inverted depending on the foreground and background colors of the active high-contrast theme.</span></span>

<span data-ttu-id="e4bd1-207">O exemplo a seguir demonstra como os recursos de imagem de alto contraste são declarados na marcação da faixa de opções:</span><span class="sxs-lookup"><span data-stu-id="e4bd1-207">The following example demonstrates how high-contrast image resources are declared in Ribbon markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="e4bd1-208">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4bd1-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4bd1-209">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="e4bd1-209">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[<span data-ttu-id="e4bd1-210">\_SmallImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="e4bd1-210">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[<span data-ttu-id="e4bd1-211">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="e4bd1-211">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[<span data-ttu-id="e4bd1-212">\_LargeImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="e4bd1-212">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[<span data-ttu-id="e4bd1-213">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="e4bd1-213">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="e4bd1-214">\_SmallHighContrastImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="e4bd1-214">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[<span data-ttu-id="e4bd1-215">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="e4bd1-215">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="e4bd1-216">\_LargeHighContrastImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="e4bd1-216">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 