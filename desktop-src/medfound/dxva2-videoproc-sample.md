---
description: Mostra como usar o processamento de vídeo DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Exemplo de DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296148"
---
# <a name="dxva2_videoproc-sample"></a><span data-ttu-id="a7bd4-103">Exemplo de VideoProc de DXVA2 \_</span><span class="sxs-lookup"><span data-stu-id="a7bd4-103">DXVA2\_VideoProc Sample</span></span>

<span data-ttu-id="a7bd4-104">Mostra como usar o [processamento de vídeo DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="a7bd4-104">Shows how to use [DXVA Video Processing](dxva-video-processing.md).</span></span>

<span data-ttu-id="a7bd4-105">Este exemplo gera por meio de programação um vídeo com um fluxo primário e um subfluxo.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-105">This sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="a7bd4-106">O fluxo primário exibe as barras de cores SMPTE e o Subfluxo é um retângulo semitransparente.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-106">The primary stream displays SMPTE color bars, and the substream is a semi-transparent rectangle.</span></span> <span data-ttu-id="a7bd4-107">O vídeo é então processado e exibido usando um processador de vídeo DXVA.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-107">The video is then processed and displayed using a DXVA video processor.</span></span> <span data-ttu-id="a7bd4-108">O usuário pode alterar os valores alfa planar, retângulos de origem e de destino, ajustes de cor e espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-108">The user can change the planar alpha values, source and destination rectangles, color adjustments, and color space.</span></span>

![captura de tela do \- exemplo de videoproc de dxva2](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="a7bd4-110">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="a7bd4-110">APIs Demonstrated</span></span>

<span data-ttu-id="a7bd4-111">Este exemplo demonstra as seguintes interfaces de DXVA:</span><span class="sxs-lookup"><span data-stu-id="a7bd4-111">This sample demonstrates the following DXVA interfaces:</span></span>

-   [<span data-ttu-id="a7bd4-112">**IDirectXVideoProcessorService**</span><span class="sxs-lookup"><span data-stu-id="a7bd4-112">**IDirectXVideoProcessorService**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [<span data-ttu-id="a7bd4-113">**IDirectXVideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="a7bd4-113">**IDirectXVideoProcessor**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a><span data-ttu-id="a7bd4-114">Uso</span><span class="sxs-lookup"><span data-stu-id="a7bd4-114">Usage</span></span>

<span data-ttu-id="a7bd4-115">O exemplo de VideoProc de DXVA2 \_ cria um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-115">The DXVA2\_VideoProc sample builds a Windows application.</span></span>

<span data-ttu-id="a7bd4-116">Opções de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="a7bd4-116">Command line options:</span></span>



| <span data-ttu-id="a7bd4-117">Opção</span><span class="sxs-lookup"><span data-stu-id="a7bd4-117">Option</span></span> | <span data-ttu-id="a7bd4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7bd4-118">Description</span></span>                                                                          |
|--------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7bd4-119">-hh</span><span class="sxs-lookup"><span data-stu-id="a7bd4-119">-hh</span></span>    | <span data-ttu-id="a7bd4-120">Força o aplicativo a usar um dispositivo Direct3D de hardware e um dispositivo de hardware DXVA.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-120">Forces the application to use a hardware Direct3D device and a hardware DXVA device.</span></span> |
| <span data-ttu-id="a7bd4-121">-HS</span><span class="sxs-lookup"><span data-stu-id="a7bd4-121">-hs</span></span>    | <span data-ttu-id="a7bd4-122">Força o aplicativo a usar um dispositivo Direct3D de hardware e um dispositivo de DXVA de software.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-122">Forces the application to use a hardware Direct3D device and a software DXVA device.</span></span> |
| <span data-ttu-id="a7bd4-123">-ss</span><span class="sxs-lookup"><span data-stu-id="a7bd4-123">-ss</span></span>    | <span data-ttu-id="a7bd4-124">Força o aplicativo a usar um dispositivo Direct3D de software e um dispositivo de DXVA de software.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-124">Forces the application to use a software Direct3D device and a software DXVA device.</span></span> |



 

<span data-ttu-id="a7bd4-125">Comandos de teclado:</span><span class="sxs-lookup"><span data-stu-id="a7bd4-125">Keyboard commands:</span></span>



| <span data-ttu-id="a7bd4-126">Chave</span><span class="sxs-lookup"><span data-stu-id="a7bd4-126">Key</span></span>       | <span data-ttu-id="a7bd4-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7bd4-127">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="a7bd4-128">ALT+ENTER</span><span class="sxs-lookup"><span data-stu-id="a7bd4-128">ALT+ENTER</span></span> | <span data-ttu-id="a7bd4-129">Alternar entre o modo de janela e o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-129">Switch between windowed mode and full-screen mode.</span></span>      |
| <span data-ttu-id="a7bd4-130">F1 – F8</span><span class="sxs-lookup"><span data-stu-id="a7bd4-130">F1–F8</span></span>     | <span data-ttu-id="a7bd4-131">Insira um dos modos mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-131">Enter one of the modes shown in the following table.</span></span>    |
| <span data-ttu-id="a7bd4-132">END</span><span class="sxs-lookup"><span data-stu-id="a7bd4-132">END</span></span>       | <span data-ttu-id="a7bd4-133">Habilitar ou desabilitar o registro em log de depuração de quadros descartados.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-133">Enable or disable debugging logging for dropped frames.</span></span> |
| <span data-ttu-id="a7bd4-134">HOME</span><span class="sxs-lookup"><span data-stu-id="a7bd4-134">HOME</span></span>      | <span data-ttu-id="a7bd4-135">Redefina um parâmetro para seu valor inicial.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-135">Reset a parameter to its initial value.</span></span>                 |



 

<span data-ttu-id="a7bd4-136">Cada uma das teclas de função F1 a F8 alterna para um modo no qual as teclas de seta podem ser usadas para ajustar um determinado parâmetro de renderização.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-136">Each of the function keys F1 through F8 switches to a mode in which the arrow keys can be used to adjust a particular rendering parameter.</span></span> <span data-ttu-id="a7bd4-137">Além disso, a cor do Subfluxo é alterada.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-137">In addition, the color of the substream changes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7bd4-138">Chave</span><span class="sxs-lookup"><span data-stu-id="a7bd4-138">Key</span></span></th>
<th><span data-ttu-id="a7bd4-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7bd4-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7bd4-140">F1</span><span class="sxs-lookup"><span data-stu-id="a7bd4-140">F1</span></span></td>
<td><span data-ttu-id="a7bd4-141">Ajuste os valores Alfa.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-141">Adjust the alpha values.</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-142">UP: aumentar o planar de ambos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-142">UP: Increase the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="a7bd4-143">Para baixo: diminua a alfa do planar de ambos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-143">DOWN: Decrease the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="a7bd4-144">RIGHT: aumentar o pixel alfa do Subfluxo.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-144">RIGHT: Increase the pixel alpha of the substream.</span></span></li>
<li><span data-ttu-id="a7bd4-145">ESQUERDA: diminuir o pixel alfa do Subfluxo.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-145">LEFT: Decrease the pixel alpha of the substream.</span></span></li>
</ul>
<span data-ttu-id="a7bd4-146">Cor do Subfluxo: branco</span><span class="sxs-lookup"><span data-stu-id="a7bd4-146">Substream color: White</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd4-147">F2</span><span class="sxs-lookup"><span data-stu-id="a7bd4-147">F2</span></span></td>
<td><span data-ttu-id="a7bd4-148">Ajuste a área de origem do fluxo primário (zoom).</span><span class="sxs-lookup"><span data-stu-id="a7bd4-148">Adjust the primary stream's source area (zoom).</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-149">UP: aumentar verticalmente (ampliar).</span><span class="sxs-lookup"><span data-stu-id="a7bd4-149">UP: Increase vertically (zoom in).</span></span></li>
<li><span data-ttu-id="a7bd4-150">Para baixo: diminuir verticalmente (reduzir).</span><span class="sxs-lookup"><span data-stu-id="a7bd4-150">DOWN: Decrease vertically (zoom out).</span></span></li>
<li><span data-ttu-id="a7bd4-151">DIREITA: aumentar horizontalmente (ampliar).</span><span class="sxs-lookup"><span data-stu-id="a7bd4-151">RIGHT: Increase horizontally (zoom in).</span></span></li>
<li><span data-ttu-id="a7bd4-152">ESQUERDA: diminuir horizontalmente (reduzir).</span><span class="sxs-lookup"><span data-stu-id="a7bd4-152">LEFT: Decrease horizontally (zoom out).</span></span></li>
</ul>
<span data-ttu-id="a7bd4-153">Cor do Subfluxo: vermelho</span><span class="sxs-lookup"><span data-stu-id="a7bd4-153">Substream color: Red</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd4-154">F3</span><span class="sxs-lookup"><span data-stu-id="a7bd4-154">F3</span></span></td>
<td><span data-ttu-id="a7bd4-155">Mova a área de origem do fluxo primário.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-155">Move the primary stream's source area.</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-156">UP: mover para cima.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-156">UP: Move up.</span></span></li>
<li><span data-ttu-id="a7bd4-157">Para baixo: mover para baixo.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-157">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="a7bd4-158">DIREITA: mover para a direita.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-158">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="a7bd4-159">ESQUERDA: mover para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-159">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="a7bd4-160">Cor do Subfluxo: amarelo</span><span class="sxs-lookup"><span data-stu-id="a7bd4-160">Substream color: Yellow</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd4-161">F4</span><span class="sxs-lookup"><span data-stu-id="a7bd4-161">F4</span></span></td>
<td><span data-ttu-id="a7bd4-162">Ajuste a área de destino do fluxo principal.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-162">Adjust the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-163">UP: aumentar verticalmente.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-163">UP: Increase vertically.</span></span></li>
<li><span data-ttu-id="a7bd4-164">Para baixo: diminuir verticalmente.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-164">DOWN: Decrease vertically.</span></span></li>
<li><span data-ttu-id="a7bd4-165">DIREITA: aumentar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-165">RIGHT: Increase horizontally.</span></span></li>
<li><span data-ttu-id="a7bd4-166">ESQUERDA: diminuir horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-166">LEFT: Decrease horizontally.</span></span></li>
</ul>
<span data-ttu-id="a7bd4-167">Cor do Subfluxo: verde</span><span class="sxs-lookup"><span data-stu-id="a7bd4-167">Substream color: Green</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd4-168">F5</span><span class="sxs-lookup"><span data-stu-id="a7bd4-168">F5</span></span></td>
<td><span data-ttu-id="a7bd4-169">Mova a área de destino do fluxo primário.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-169">Move the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-170">UP: mover para cima.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-170">UP: Move up.</span></span></li>
<li><span data-ttu-id="a7bd4-171">Para baixo: mover para baixo.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-171">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="a7bd4-172">DIREITA: mover para a direita.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-172">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="a7bd4-173">ESQUERDA: mover para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-173">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="a7bd4-174">Cor do Subfluxo: ciano</span><span class="sxs-lookup"><span data-stu-id="a7bd4-174">Substream color: Cyan</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd4-175">F6</span><span class="sxs-lookup"><span data-stu-id="a7bd4-175">F6</span></span></td>
<td><span data-ttu-id="a7bd4-176">Alterar a cor do plano de fundo ou o espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-176">Change background color or color space.</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-177">Para cima, para baixo: Percorra os espaços de cores.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-177">UP, DOWN: Cycle through color spaces.</span></span></li>
<li><span data-ttu-id="a7bd4-178">DIREITA, esquerda: percorrer as cores do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-178">RIGHT, LEFT: Cycle through background colors.</span></span></li>
</ul>
<span data-ttu-id="a7bd4-179">Cor do Subfluxo: azul</span><span class="sxs-lookup"><span data-stu-id="a7bd4-179">Substream color: Blue</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7bd4-180">F7</span><span class="sxs-lookup"><span data-stu-id="a7bd4-180">F7</span></span></td>
<td><span data-ttu-id="a7bd4-181">Ajustar o brilho e o contraste.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-181">Adjust brightness and contrast.</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-182">UP: aumentar o brilho.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-182">UP: Increase brightness.</span></span></li>
<li><span data-ttu-id="a7bd4-183">Para baixo: diminuir o brilho.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-183">DOWN: Decrease brightness.</span></span></li>
<li><span data-ttu-id="a7bd4-184">DIREITA: aumentar contraste.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-184">RIGHT: Increase contrast.</span></span></li>
<li><span data-ttu-id="a7bd4-185">ESQUERDA: diminuir contraste.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-185">LEFT: Decrease contrast.</span></span></li>
</ul>
<span data-ttu-id="a7bd4-186">Cor do Subfluxo: magenta</span><span class="sxs-lookup"><span data-stu-id="a7bd4-186">Substream color: Magenta</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7bd4-187">F8</span><span class="sxs-lookup"><span data-stu-id="a7bd4-187">F8</span></span></td>
<td><span data-ttu-id="a7bd4-188">Ajuste o matiz e a saturação.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-188">Adjust hue and saturation.</span></span><br/>
<ul>
<li><span data-ttu-id="a7bd4-189">UP: aumentar o matiz.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-189">UP: Increase hue.</span></span></li>
<li><span data-ttu-id="a7bd4-190">Para baixo: diminuir o matiz.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-190">DOWN: Decrease hue.</span></span></li>
<li><span data-ttu-id="a7bd4-191">DIREITA: aumentar a saturação.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-191">RIGHT: Increase saturation.</span></span></li>
<li><span data-ttu-id="a7bd4-192">ESQUERDA: diminuir a saturação.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-192">LEFT: Decrease saturation.</span></span></li>
</ul>
<span data-ttu-id="a7bd4-193">Cor do Subfluxo: preto</span><span class="sxs-lookup"><span data-stu-id="a7bd4-193">Substream color: Black</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a7bd4-194">Em cada modo, pressionar a tecla HOME redefine os parâmetros para esse modo para seus valores iniciais.</span><span class="sxs-lookup"><span data-stu-id="a7bd4-194">In each mode, pressing the HOME key resets the parameters for that mode to their initial values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7bd4-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7bd4-195">Requirements</span></span>



| <span data-ttu-id="a7bd4-196">Produto</span><span class="sxs-lookup"><span data-stu-id="a7bd4-196">Product</span></span>                                                        | <span data-ttu-id="a7bd4-197">Versão</span><span class="sxs-lookup"><span data-stu-id="a7bd4-197">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="a7bd4-198">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="a7bd4-198">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="a7bd4-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7bd4-199">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="a7bd4-200">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a7bd4-200">Downloading the Sample</span></span>

<span data-ttu-id="a7bd4-201">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span><span class="sxs-lookup"><span data-stu-id="a7bd4-201">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7bd4-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7bd4-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7bd4-203">Aceleração de vídeo do DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="a7bd4-203">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="a7bd4-204">Processamento de vídeo de DXVA</span><span class="sxs-lookup"><span data-stu-id="a7bd4-204">DXVA Video Processing</span></span>](dxva-video-processing.md)
</dt> <dt>

[<span data-ttu-id="a7bd4-205">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7bd4-205">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




