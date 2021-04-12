---
description: Mixagem não quadrada
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Mixagem não quadrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500550"
---
# <a name="non-square-mixing"></a><span data-ttu-id="7bd6e-103">Mixagem não quadrada</span><span class="sxs-lookup"><span data-stu-id="7bd6e-103">Non-Square Mixing</span></span>

<span data-ttu-id="7bd6e-104">Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="7bd6e-105">Quando o VMR-9 combina dois ou mais fluxos, há dois pontos em que o dimensionamento pode ocorrer: quando o mixer compõe os fluxos de entrada e quando o alocador de dados renderiza a imagem composta.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-105">When the VMR-9 mixes two or more streams, there are two points where scaling can occur: When the mixer composites the input streams, and when the allocator-presenter renders the composited image.</span></span>

![operações de mixagem do VMR](images/vmr-nonsquare-mixing.png)

<span data-ttu-id="7bd6e-107">As versões anteriores do VMR-9 sempre compõevam os fluxos de entrada usando uma taxa de proporção de pixel (PAR) quadrado (1:1), mesmo quando havia apenas um fluxo de vídeo único.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-107">Previous versions of the VMR-9 always composited the input streams using a square (1:1) pixel aspect ratio (PAR), even when there was only a single video stream.</span></span> <span data-ttu-id="7bd6e-108">Se o fluxo de entrada tiver pixels não quadrados, isso causaria uma operação de dimensionamento desnecessária.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-108">If the input stream had non-square pixels, this caused an unnecessary scaling operation.</span></span> <span data-ttu-id="7bd6e-109">O dimensionamento deve ser evitado o máximo possível, é claro, porque ele degrada a qualidade final da imagem.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-109">Scaling should be avoided as much as possible, of course, because it degrades the final image quality.</span></span>

<span data-ttu-id="7bd6e-110">A partir do Windows XP Service Pack 2, o VMR-9 dá suporte a duas maneiras diferentes de evitar o problema de dimensionamento duplo:</span><span class="sxs-lookup"><span data-stu-id="7bd6e-110">Starting in Windows XP Service Pack 2, the VMR-9 supports two different ways to avoid the problem of double scaling:</span></span>

-   <span data-ttu-id="7bd6e-111">Implemente um apresentador de alocador personalizado e dê suporte à interface [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .</span><span class="sxs-lookup"><span data-stu-id="7bd6e-111">Implement a custom allocator-presenter and support the [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) interface.</span></span>
-   <span data-ttu-id="7bd6e-112">Use o modo de combinação não quadrado.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-112">Use non-square mixing mode.</span></span>

<span data-ttu-id="7bd6e-113">Esta seção descreve o modo de mistura não quadrada.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-113">This section describes non-square mixing mode.</span></span> <span data-ttu-id="7bd6e-114">Os aplicativos podem combinar as duas técnicas.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-114">Applications can combine both techniques.</span></span>

<span data-ttu-id="7bd6e-115">**Como funciona a mistura não quadrada**</span><span class="sxs-lookup"><span data-stu-id="7bd6e-115">**How Non-Square Mixing Works**</span></span>

<span data-ttu-id="7bd6e-116">No modo de mistura não-quadrada, o VMR-9 seleciona um fluxo de entrada para ser o tamanho e o PAR de destino.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-116">In non-square mixing mode, the VMR-9 selects one input stream to be the target size and PAR.</span></span> <span data-ttu-id="7bd6e-117">O mixer do VMR não dimensiona o vídeo do fluxo ou de quaisquer outros fluxos com o mesmo tamanho de imagem e PAR.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-117">The VMR's mixer does not scale the video from that stream or from any other streams with the same image size and PAR.</span></span> <span data-ttu-id="7bd6e-118">Fluxos com um tamanho ou taxa de proporção diferente são dimensionados para corresponder ao PAR de destino e letterboxed para se ajustarem ao tamanho final da imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-118">Streams with a different size or aspect ratio are scaled to match the target PAR and letterboxed to fit the final output image size.</span></span>

<span data-ttu-id="7bd6e-119">A escolha dos fluxos depende do modo de combinação atual:</span><span class="sxs-lookup"><span data-stu-id="7bd6e-119">The choice of streams depends on the current mixing mode:</span></span>

-   <span data-ttu-id="7bd6e-120">O modo de mixagem YUV é restrito a um fluxo de vídeo no pino 0.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-120">YUV mixing mode is restricted to one video stream on pin 0.</span></span> <span data-ttu-id="7bd6e-121">(Os outros Pins podem ter fluxos de subimagem ou legenda oculta.) Portanto, o VMR-9 sempre seleciona o pino 0 para o tamanho da imagem de destino e PAR.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-121">(The other pins may have subpicture or closed caption streams.) Therefore, the VMR-9 always selects pin 0 for the target image size and PAR.</span></span>
-   <span data-ttu-id="7bd6e-122">No modo de mixagem RGB, o VMR seleciona o fluxo com o maior tamanho de imagem.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-122">In RGB mixing mode, the VMR selects the stream with the largest image size.</span></span> <span data-ttu-id="7bd6e-123">Se houver mais de um, ele selecionará aquele com a ordem z mais alta; e se ainda houver um vínculo, ele selecionará o fluxo com o número de PIN mais baixo.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-123">If there is more than one, it selects the one with the highest z-order; and if there is still a tie, it selects the stream with the lowest pin number.</span></span>

<span data-ttu-id="7bd6e-124">**Exemplos de operação**</span><span class="sxs-lookup"><span data-stu-id="7bd6e-124">**Examples of Operation**</span></span>

<span data-ttu-id="7bd6e-125">**Exemplo 1.**</span><span class="sxs-lookup"><span data-stu-id="7bd6e-125">**Example 1.**</span></span> <span data-ttu-id="7bd6e-126">O fluxo 0 é 720 x 480 pixels com uma taxa de proporção de imagem de 16:9.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-126">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="7bd6e-127">O fluxo 1 é um 640 x 480 pixels com uma taxa de proporção de imagem de 4:3.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-127">Stream 1 is a 640 x 480 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="7bd6e-128">Neste exemplo, o fluxo 0 tem o maior tamanho de imagem, portanto, o VMR escolhe esse fluxo, independentemente do modo de mistura RGB ou do modo de combinação de YUB.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-128">In this example, stream 0 has the largest image size, so the VMR chooses this stream, regardless of RGB mixing mode or YUB mixing mode.</span></span> <span data-ttu-id="7bd6e-129">O PAR é 32:27 (16:9/720:480), o que significa que a imagem deve ser esticada horizontalmente por essa proporção para produzir a taxa de proporção de imagem 16:9 correta.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-129">The PAR is 32:27 (16:9 / 720:480), meaning the image must be stretched horizontally by this ratio to produce the correct 16:9 picture aspect ratio.</span></span>

<span data-ttu-id="7bd6e-130">Para corresponder ao PAR de destino, o mixer do VMR dimensiona o fluxo 1 pela taxa inversa (27:32), resultando em uma imagem 540 x 480.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-130">To match the target PAR, the VMR mixer scales stream 1 by the inverse ratio (27:32), resulting in a 540 x 480 image.</span></span> <span data-ttu-id="7bd6e-131">Os dois fluxos são então compostos em uma superfície.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-131">The two streams are then composited onto one surface.</span></span> <span data-ttu-id="7bd6e-132">Para exibir a imagem resultante corretamente, o apresentador de alocador deve alongar a imagem horizontalmente para se ajustar à taxa de proporção da imagem 16:9.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-132">To display the resulting image correctly, the allocator presenter must stretch the image horizontally to fit the 16:9 picture aspect ratio.</span></span>

![exemplo 1.](images/vmr-nonsquare-mixing2.png)

<span data-ttu-id="7bd6e-134">**Exemplo 2.**</span><span class="sxs-lookup"><span data-stu-id="7bd6e-134">**Example 2.**</span></span> <span data-ttu-id="7bd6e-135">O fluxo 0 é 720 x 480 pixels com uma taxa de proporção de imagem de 16:9.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-135">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="7bd6e-136">O fluxo 1 é um 1024 x 768 pixels com uma taxa de proporção de imagem de 4:3.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-136">Stream 1 is a 1024 x 768 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="7bd6e-137">Se o VMR-9 estiver usando o modo de mixagem YUV, ele sempre selecionará o fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-137">If the VMR-9 is using YUV mixing mode, it always selects stream 0.</span></span> <span data-ttu-id="7bd6e-138">Portanto, ele amplia o fluxo de 1 a 540 x 480 pixels, para corresponder ao PAR do fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-138">Therefore, it stretches stream 1 to 540 x 480 pixels, to match the PAR of stream 0.</span></span>

<span data-ttu-id="7bd6e-139">Se o VMR-9 estiver usando o modo de mixagem RGB, ele selecionará o fluxo 1 como o destino, pois esse fluxo tem o maior tamanho de imagem.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-139">If the VMR-9 is using RGB mixing mode, it selects stream 1 as the target, because that stream has the largest image size.</span></span> <span data-ttu-id="7bd6e-140">Ele amplia o fluxo 0 para um tamanho de imagem de 1024 x 576 pixels.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-140">It stretches stream 0 to an image size of 1024 x 576 pixels.</span></span> <span data-ttu-id="7bd6e-141">Observe que, nesse caso, a imagem compostada tem um PAR de 1:1, portanto, o alocador-apresentador não precisa corrigir para pixels não quadrados.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-141">Note that in this case, the composited image has a PAR of 1:1, so the allocator-presenter does not have to correct for non-square pixels.</span></span> <span data-ttu-id="7bd6e-142">(Talvez ainda precise ampliar o vídeo para considerar o retângulo de destino.)</span><span class="sxs-lookup"><span data-stu-id="7bd6e-142">(It might still need to stretch the video to account for the destination rectangle.)</span></span>

<span data-ttu-id="7bd6e-143">**Usando o modo de combinação não quadrado**</span><span class="sxs-lookup"><span data-stu-id="7bd6e-143">**Using Non-Square Mixing Mode**</span></span>

<span data-ttu-id="7bd6e-144">O modo de mixagem não quadrado é recomendado se qualquer uma das condições a seguir for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="7bd6e-144">Non-square mixing mode is recommended if either of the following conditions are true:</span></span>

-   <span data-ttu-id="7bd6e-145">Seu aplicativo nunca envia mais de um fluxo de vídeo para o VMR-9.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-145">Your application never sends more than one video stream to the VMR-9.</span></span>
-   <span data-ttu-id="7bd6e-146">Seu aplicativo processa arquivos de DVD, televisão ou MS-DVR.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-146">Your application renders DVD, television, or ms-dvr files.</span></span> <span data-ttu-id="7bd6e-147">Você também deve usar o modo de mixagem YUV nesse caso, se o hardware de gráficos oferecer suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-147">You should also use YUV mixing mode in this case, if the graphics hardware supports it.</span></span>

<span data-ttu-id="7bd6e-148">Se seu aplicativo misturar vários fluxos de vídeo que podem ter tamanhos de imagem ou proporções de pixel variáveis, o modo de combinação de quadrado padrão é recomendado.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-148">If your application mixes multiple video streams that may have varying image sizes or pixel aspect ratios, the default square mixing mode is recommended.</span></span>

<span data-ttu-id="7bd6e-149">Para configurar o modo de mistura não-quadrado, o grafo de filtro deve ser interrompido e todos os Pins de entrada desconectados no VMR-9.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-149">To configure non-square mixing mode, the filter graph must be stopped and all input pins disconnected on the VMR-9.</span></span> <span data-ttu-id="7bd6e-150">Em seguida, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o \_ sinalizador MixerPref9 NonSquareMixing:</span><span class="sxs-lookup"><span data-stu-id="7bd6e-150">Then call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_NonSquareMixing flag:</span></span>


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> <span data-ttu-id="7bd6e-151">Se você combinar o \_ sinalizador MixerPref9 NonSquareMixing com o \_ sinalizador MixerPref9 ARAdjustXorY, o VMR-9 ignorará o \_ sinalizador MixerPref9 ARAdjustXorY.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-151">If you combine the MixerPref9\_NonSquareMixing flag with the MixerPref9\_ARAdjustXorY flag, the VMR-9 ignores the MixerPref9\_ARAdjustXorY flag.</span></span>

 

<span data-ttu-id="7bd6e-152">Se seu aplicativo usar um apresentador de alocador personalizado com modo de combinação não quadrado, lembre-se de que a imagem compostada pode ter um PAR não quadrado.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-152">If your application uses a custom allocator-presenter with non-square mixing mode, be aware that the composited image may have a non-square PAR.</span></span> <span data-ttu-id="7bd6e-153">O apresentador de alocador deve escalar a imagem para um quadrado (1:1) PAR.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-153">The allocator-presenter must scale the image to a square (1:1) PAR.</span></span>

<span data-ttu-id="7bd6e-154">**Bitmaps estáticos**</span><span class="sxs-lookup"><span data-stu-id="7bd6e-154">**Static Bitmaps**</span></span>

<span data-ttu-id="7bd6e-155">Se você usar a interface [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) para misturar um bitmap estático no vídeo, considere o bitmap para ser um segundo fluxo de vídeo para fins do modo de combinação do VMR.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-155">If you use the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend a static bitmap onto the video, you should consider the bitmap to be a second video stream for purposes of the VMR mixing mode.</span></span>

<span data-ttu-id="7bd6e-156">O VMR trata o bitmap como tendo o mesmo PAR que o destino.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-156">The VMR treats the bitmap as having the same PAR as the target.</span></span> <span data-ttu-id="7bd6e-157">Ele não dimensiona o bitmap para ajustar a taxa de proporção de pixel do destino.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-157">It does not scale the bitmap to adjust for the target's pixel aspect ratio.</span></span> <span data-ttu-id="7bd6e-158">Na configuração padrão do VMR, o destino tem um PAR de 1:1, que corresponde à maioria dos bitmaps.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-158">In the VMR's default configuration, the target has a 1:1 PAR, which matches most bitmaps.</span></span> <span data-ttu-id="7bd6e-159">No modo de mistura não quadrada, o destino pode ter pixels não quadrados.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-159">In non-square mixing mode, the target might have non-square pixels.</span></span> <span data-ttu-id="7bd6e-160">Para garantir que o bitmap seja exibido corretamente, o aplicativo deve fornecer uma imagem cujo PAR corresponda ao PAR de destino.</span><span class="sxs-lookup"><span data-stu-id="7bd6e-160">To ensure that the bitmap is displayed correctly, the application should supply an image whose PAR matches the target PAR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bd6e-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bd6e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bd6e-162">Usando o modo de mixagem do VMR</span><span class="sxs-lookup"><span data-stu-id="7bd6e-162">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



