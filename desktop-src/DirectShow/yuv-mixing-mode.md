---
description: Modo de mixagem YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modo de mixagem YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829572"
---
# <a name="yuv-mixing-mode"></a><span data-ttu-id="6165d-103">Modo de mixagem YUV</span><span class="sxs-lookup"><span data-stu-id="6165d-103">YUV Mixing Mode</span></span>

<span data-ttu-id="6165d-104">Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6165d-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="6165d-105">A partir do Windows XP Service Pack 2, o VMR dá suporte a um modo de combinação chamado modo de mixagem de YUV.</span><span class="sxs-lookup"><span data-stu-id="6165d-105">Starting in Windows XP Service Pack 2, the VMR supports a mixing mode called YUV mixing mode.</span></span> <span data-ttu-id="6165d-106">Esse modo é mais útil para aplicativos avançados de TV ou DVD.</span><span class="sxs-lookup"><span data-stu-id="6165d-106">This mode is most useful for advanced TV or DVD applications.</span></span> <span data-ttu-id="6165d-107">Ele negocia parte do poder do mixer do VMR para melhorar o desempenho em hardware de gráficos de baixo nível que usa um design de arquitetura de memória unificada.</span><span class="sxs-lookup"><span data-stu-id="6165d-107">It trades some of the power of the VMR mixer for better performance on low end graphics hardware that uses a unified memory architecture design.</span></span> <span data-ttu-id="6165d-108">O modo de mixagem de YUV tem suporte no VMR-7 e no VMR-9.</span><span class="sxs-lookup"><span data-stu-id="6165d-108">YUV mixing mode is supported on both the VMR-7 and VMR-9.</span></span>

<span data-ttu-id="6165d-109">**Vantagens**</span><span class="sxs-lookup"><span data-stu-id="6165d-109">**Advantages**</span></span>

<span data-ttu-id="6165d-110">O modo de mixagem YUV tem várias vantagens relacionadas ao desempenho de renderização sobre o modo de mixagem RGB original com suporte no VMR:</span><span class="sxs-lookup"><span data-stu-id="6165d-110">YUV mixing mode has several advantages relating to rendering performance over the original RGB mixing mode supported by the VMR:</span></span>

-   <span data-ttu-id="6165d-111">Quando o VMR está no modo de mistura YUV, todas as operações de composição de fluxo de vídeo e desentrelaçamento são executadas no espaço de cores YUV.</span><span class="sxs-lookup"><span data-stu-id="6165d-111">When the VMR is in YUV mixing mode, all de-interlacing and video stream composition operations are performed in YUV color space.</span></span> <span data-ttu-id="6165d-112">As superfícies YUV geralmente exigem de 50% a 60% menos largura de banda de memória do que as superfícies RGB equivalentes.</span><span class="sxs-lookup"><span data-stu-id="6165d-112">YUV surfaces typically require from 50% to 60% less memory bandwidth than equivalent RGB surfaces.</span></span>
-   <span data-ttu-id="6165d-113">A composição de desentrelaçamento e de fluxo são executadas por uma única chamada para o driver de gráficos.</span><span class="sxs-lookup"><span data-stu-id="6165d-113">The deinterlacing and stream composition are performed by a single call to the graphics driver.</span></span> <span data-ttu-id="6165d-114">O driver pode usar os recursos texturing do hardware de gráficos, resultando em mais economia de largura de banda de memória.</span><span class="sxs-lookup"><span data-stu-id="6165d-114">The driver can use the graphics hardware's multi-texturing capabilities, resulting in additional memory bandwidth savings.</span></span>

<span data-ttu-id="6165d-115">Embora qualquer aplicativo de vídeo possa usar o modo de mixagem YUV, ele destina-se principalmente a dois tipos de aplicativo de reprodução de vídeo:</span><span class="sxs-lookup"><span data-stu-id="6165d-115">Although any video application can use YUV mixing mode, it is primarily intended for two types of video playback application:</span></span>

1.  <span data-ttu-id="6165d-116">Aplicativos de TV que exibem legendas codificadas ou teletexto.</span><span class="sxs-lookup"><span data-stu-id="6165d-116">TV applications that display closed captions or teletext.</span></span>
2.  <span data-ttu-id="6165d-117">Os aplicativos de DVD exibem dados de subimagem de DVD ou legendas codificadas.</span><span class="sxs-lookup"><span data-stu-id="6165d-117">DVD applications display DVD subpicture data or closed captions.</span></span>

<span data-ttu-id="6165d-118">**Restrições**</span><span class="sxs-lookup"><span data-stu-id="6165d-118">**Restrictions**</span></span>

<span data-ttu-id="6165d-119">Várias restrições são impostas pelo VMR quando ele é colocado no modo de mixagem YUV:</span><span class="sxs-lookup"><span data-stu-id="6165d-119">A number of restrictions are enforced by the VMR when it is put into YUV mixing mode:</span></span>

-   <span data-ttu-id="6165d-120">O fluxo 0 (o fluxo conectado ao pino de entrada 0) pode ser progressivo ou entrelaçado; todos os outros fluxos devem ser progressivos.</span><span class="sxs-lookup"><span data-stu-id="6165d-120">Stream 0 (the stream connected to Input Pin 0) can be progressive or interlaced; all other streams must be progressive.</span></span>
-   <span data-ttu-id="6165d-121">GUID \_ NULL (modo de weave) não é permitido para o fluxo 0.</span><span class="sxs-lookup"><span data-stu-id="6165d-121">GUID\_NULL (weave mode) is not allowed for stream 0.</span></span>
-   <span data-ttu-id="6165d-122">DeinterlacePref \_ weave não pode ser usada como um modo de fallback porque isso pode impedir que um dispositivo de desentrelaçamento seja criado.</span><span class="sxs-lookup"><span data-stu-id="6165d-122">DeinterlacePref\_Weave cannot be used as a fallback mode because this could prevent a de-interlace device from being created.</span></span> <span data-ttu-id="6165d-123">O modo de mixagem YUV requer um dispositivo de desentrelaçamento, mesmo se o vídeo de entrada não estiver entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="6165d-123">YUV mixing mode requires a deinterlace device even if the incoming video is not interlaced.</span></span>
-   <span data-ttu-id="6165d-124">Nenhuma alteração pode ser feita no valor alfa do planar associado a cada fluxo de entrada do VMR.</span><span class="sxs-lookup"><span data-stu-id="6165d-124">No changes can be made to the planar alpha value associated with each VMR input stream.</span></span>
-   <span data-ttu-id="6165d-125">O usuário não pode alterar a ordem Z dos fluxos de vídeo conectados.</span><span class="sxs-lookup"><span data-stu-id="6165d-125">The user cannot alter the Z-order of the connected video streams.</span></span> <span data-ttu-id="6165d-126">A ordem Z padrão é retirada da ordem do PIN.</span><span class="sxs-lookup"><span data-stu-id="6165d-126">The default Z-order is taken from the pin order.</span></span>
-   <span data-ttu-id="6165d-127">Não há suporte para o chaveamento de cor.</span><span class="sxs-lookup"><span data-stu-id="6165d-127">Color keying is not supported.</span></span>
-   <span data-ttu-id="6165d-128">O pino de entrada 0 deve receber o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6165d-128">Input pin 0 must receive the video stream.</span></span>
-   <span data-ttu-id="6165d-129">Os outros Pins de entradas só podem receber dados de Subfluxo de vídeo, como subimagem de DVD, legendas codificadas ou teletexto.</span><span class="sxs-lookup"><span data-stu-id="6165d-129">The other inputs pins can only receive video sub-stream data such as DVD sub-picture, closed captions or teletext.</span></span>
-   <span data-ttu-id="6165d-130">Os outros Pins de entradas só podem aceitar formatos de YUV alfa por pixel, como AYUV, AI44 e IA44.</span><span class="sxs-lookup"><span data-stu-id="6165d-130">The other inputs pins can only accept per-pixel alpha YUV formats, such as AYUV, AI44 and IA44.</span></span>
-   <span data-ttu-id="6165d-131">Nenhum dos Pins de entrada do VMR pode aceitar todos os formatos RGB.</span><span class="sxs-lookup"><span data-stu-id="6165d-131">None of the VMR's input pins can accept any RGB formats.</span></span>
-   <span data-ttu-id="6165d-132">Imagens de bitmap fornecidas pelo aplicativo não podem mais ser combinadas com o vídeo antes da apresentação para a exibição.</span><span class="sxs-lookup"><span data-stu-id="6165d-132">Application supplied bitmap images can no longer be combined with the video prior to presentation to the display.</span></span>
-   <span data-ttu-id="6165d-133">Os subfluxos individuais não podem ser invertidos horizontal ou verticalmente usando as funções do mixer "retângulo de saída" do VMR.</span><span class="sxs-lookup"><span data-stu-id="6165d-133">Individual sub-streams cannot be inverted horizontally or vertically using the VMR's mixer "output rectangle" functions.</span></span> <span data-ttu-id="6165d-134">Há suporte para o redimensionamento de fluxo "normal" e redimensionar.</span><span class="sxs-lookup"><span data-stu-id="6165d-134">"Normal" stream re-positioning and re-sizing is supported.</span></span>
-   <span data-ttu-id="6165d-135">A cor do plano de fundo de mistura (especificada por [**IVMRMixerControl:: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) ainda é especificada no espaço de cores RGB, assim como no modo de mistura RGB.</span><span class="sxs-lookup"><span data-stu-id="6165d-135">The mixing background color (specified by [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) is still specified in the RGB color space, just as in RGB mixing mode.</span></span>

<span data-ttu-id="6165d-136">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="6165d-136">**Configuration**</span></span>

<span data-ttu-id="6165d-137">Os aplicativos devem configurar explicitamente o VMR para tirar proveito do modo de mixagem YUV; o modo de mixagem RGB original permanece o modo de combinação padrão.</span><span class="sxs-lookup"><span data-stu-id="6165d-137">Applications must explicitly configure the VMR to take advantage of YUV mixing mode; the original RGB mixing mode remains the default mixing mode.</span></span> <span data-ttu-id="6165d-138">Para habilitar o modo de mixagem YUV no VMR-7, chame [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) com o \_ sinalizador MixerPref RenderTargetYUV.</span><span class="sxs-lookup"><span data-stu-id="6165d-138">To enable YUV mixing mode in the VMR-7, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_RenderTargetYUV flag.</span></span> <span data-ttu-id="6165d-139">Essa chamada deve ser feita antes que qualquer um dos Pins de entrada do VMR esteja conectado.</span><span class="sxs-lookup"><span data-stu-id="6165d-139">This call must be made before any of the VMR's input pins are connected.</span></span> <span data-ttu-id="6165d-140">Para habilitar o modo de mixagem YUV no VMR-9, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o \_ sinalizador MixerPref9 RenderTargetYUV.</span><span class="sxs-lookup"><span data-stu-id="6165d-140">To enable YUV mixing mode in the VMR-9, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_RenderTargetYUV flag.</span></span>

<span data-ttu-id="6165d-141">A única maneira de determinar se o VMR-7 dá suporte ao novo modo de mixagem YUV é tentar configurar o VMR nesse modo.</span><span class="sxs-lookup"><span data-stu-id="6165d-141">The only way to determine if the VMR-7 supports the new YUV mixing mode is to try setting the VMR into that mode.</span></span> <span data-ttu-id="6165d-142">Se a chamada for realizada com sucesso, você ainda poderá colocar o VMR novamente no modo de mistura RGB, se necessário.</span><span class="sxs-lookup"><span data-stu-id="6165d-142">If the call succeeds, you can still put the VMR back into RGB mixing mode if necessary.</span></span> <span data-ttu-id="6165d-143">Depois que ele é definido no modo de mistura YUV, o VMR só pode ser alterado para o modo de mistura RGB depois que todos os Pins de entrada tiverem sido desconectados.</span><span class="sxs-lookup"><span data-stu-id="6165d-143">After it is set into YUV mixing mode, the VMR can only be changed back to RGB mixing mode after all input pins have been disconnected.</span></span>

<span data-ttu-id="6165d-144">No modo de mixagem YUV, você pode reduzir a carga na GPU (unidade de processamento gráfico) aplicando os seguintes sinalizadores no método **SetMixingPrefs** :</span><span class="sxs-lookup"><span data-stu-id="6165d-144">In YUV mixing mode, you can reduce the load on the graphics processing unit (GPU) by applying the following flags in the **SetMixingPrefs** method:</span></span>



| <span data-ttu-id="6165d-145">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="6165d-145">Flag</span></span>                                                                                 | <span data-ttu-id="6165d-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="6165d-146">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6165d-147">VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB</span><span class="sxs-lookup"><span data-stu-id="6165d-147">VMR-7: MixerPref\_DynamicSwitchToBOBVMR-9: MixerPref9\_DynamicSwitchToBOB</span></span><br/> | <span data-ttu-id="6165d-148">Mude para Bob desentrelaçar.</span><span class="sxs-lookup"><span data-stu-id="6165d-148">Switch to bob deinterlacing.</span></span>                                     |
| <span data-ttu-id="6165d-149">VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2</span><span class="sxs-lookup"><span data-stu-id="6165d-149">VMR-7: MixerPref\_DynamicDecimateBy2VMR-9: MixerPref\_DynamicDecimateBy2</span></span><br/>  | <span data-ttu-id="6165d-150">DECIMATE a imagem por um fator de 2 na horizontal e na vertical.</span><span class="sxs-lookup"><span data-stu-id="6165d-150">Decimate the image by a factor of 2 horizontally and vertically.</span></span> |



 

<span data-ttu-id="6165d-151">Você pode adicionar ou remover esses sinalizadores enquanto o grafo de filtro está em execução; a alteração é aplicada quando o mixer do VMR compõe o próximo quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6165d-151">You can add or remove these flags while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.</span></span> <span data-ttu-id="6165d-152">Os sinalizadores não são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="6165d-152">The flags are not mutually exclusive.</span></span> <span data-ttu-id="6165d-153">Essas configurações reduzem a qualidade da imagem, portanto, normalmente você as aplicaria somente quando a qualidade do vídeo for menos importante — por exemplo, se o vídeo estiver sendo reproduzido em uma pequena parte da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6165d-153">These settings reduce the quality of the image, so typically you would apply them only when video quality is less important — for example, if video is playing in a small portion of the user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6165d-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6165d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6165d-155">Usando o modo de mixagem do VMR</span><span class="sxs-lookup"><span data-stu-id="6165d-155">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




