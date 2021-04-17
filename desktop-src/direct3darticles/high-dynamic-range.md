---
title: Usar DirectX com exibições de alto alcance dinâmico e cor avançada
description: Este tópico fornece uma visão geral técnica da renderização do conteúdo do Direct3D 11 e do Direct3D 12 de intervalo dinâmico para uma exibição HDR10 usando o suporte a cores avançadas do Windows 10.
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104567962"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a><span data-ttu-id="2a24a-103">Usando o DirectX com altas exibições de intervalo dinâmico e cor avançada</span><span class="sxs-lookup"><span data-stu-id="2a24a-103">Using DirectX with high dynamic range Displays and Advanced Color</span></span>

<span data-ttu-id="2a24a-104">Este tópico fornece uma visão geral técnica da saída do conteúdo do Direct3D 11 e do Direct3D 12 de intervalo dinâmico para uma exibição HDR10 usando o suporte a cores avançadas do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2a24a-104">This topic provides a technical overview of outputting high dynamic range (HDR) Direct3D 11 and Direct3D 12 content to an HDR10 display using Windows 10 advanced color support.</span></span> <span data-ttu-id="2a24a-105">Ele resume algumas das principais diferenças conceituais entre a saída para HDR10, em comparação com os monitores de SDR (intervalo dinâmico padrão) tradicionais.</span><span class="sxs-lookup"><span data-stu-id="2a24a-105">It summarizes some key conceptual differences between outputting to HDR10 displays as compared to traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="2a24a-106">Ele também aborda os principais requisitos técnicos de seu aplicativo para dar suporte adequado à cor avançada do Windows, bem como recomendações e práticas recomendadas.</span><span class="sxs-lookup"><span data-stu-id="2a24a-106">It also covers the key technical requirements for your app to properly support Windows advanced color, as well as recommendations and best practices.</span></span>

## <a name="introduction"></a><span data-ttu-id="2a24a-107">Introdução</span><span class="sxs-lookup"><span data-stu-id="2a24a-107">Introduction</span></span>

<span data-ttu-id="2a24a-108">O Windows 10 dá suporte a HDR e a outros monitores de cores avançadas, que fornecem uma fidelidade de cor significativamente maior do que a exibição do SDR tradicional.</span><span class="sxs-lookup"><span data-stu-id="2a24a-108">Windows 10 supports HDR and other advanced color displays, which provide significantly higher color fidelity than traditional SDR displays.</span></span> <span data-ttu-id="2a24a-109">Você pode usar Direct3D, Direct2D e outras APIs de gráficos para renderizar conteúdo HDR para uma exibição compatível.</span><span class="sxs-lookup"><span data-stu-id="2a24a-109">You can use Direct3D, Direct2D and other graphics APIs to render HDR content to a capable display.</span></span>

<span data-ttu-id="2a24a-110">A cor avançada do Windows refere-se a várias tecnologias relacionadas, introduzidas pela primeira vez com o Windows 10 versão 1703, que fornecem suporte para exibições que excedem os recursos de cores das telas tradicionais de alcance dinâmico Standard (SDR).</span><span class="sxs-lookup"><span data-stu-id="2a24a-110">Windows advanced color refers to several related technologies, first introduced with Windows 10 version 1703, that provide support for displays that exceed the color capabilities of traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="2a24a-111">Os três principais recursos estendidos são descritos abaixo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-111">The three major extended capabilities are described below.</span></span> <span data-ttu-id="2a24a-112">O tipo mais comum de exibição de cor avançada, HDR10, dá suporte a todos os três recursos estendidos.</span><span class="sxs-lookup"><span data-stu-id="2a24a-112">The most common type of advanced color display, HDR10, supports all three extended capabilities.</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="2a24a-113">Intervalo dinâmico alto</span><span class="sxs-lookup"><span data-stu-id="2a24a-113">High dynamic range</span></span>

<span data-ttu-id="2a24a-114">Intervalo dinâmico refere-se à diferença entre a luminância máxima e a mínima em uma cena; Isso geralmente é medido em nits (candelas por centímetro quadrado).</span><span class="sxs-lookup"><span data-stu-id="2a24a-114">Dynamic range refers to the difference between the maximum and minimum luminance in a scene; this is often measured in nits (candelas per square centimeter).</span></span> <span data-ttu-id="2a24a-115">Os bastidores do mundo real, como este pôr-no-sol, geralmente têm intervalos dinâmicos de 10 ordens de magnitude; o olho humano pode discernir um intervalo ainda maior após a adaptação.</span><span class="sxs-lookup"><span data-stu-id="2a24a-115">Real world scenes, such as this sunset, often have dynamic ranges of 10 orders of magnitude of luminance; the human eye can discern an even greater range after adaptation.</span></span>

![imagem de um sol com brilho e pontos mais escuros na cena rotulados](images/HDR-HDR.jpg)

<span data-ttu-id="2a24a-117">Desde o Direct3D 9, os mecanismos gráficos conseguiram renderizar internamente suas cenas com esse nível de fidelidade fisicamente precisa.</span><span class="sxs-lookup"><span data-stu-id="2a24a-117">Ever since Direct3D 9, graphics engines have been able to internally render their scenes with this level of physically accurate fidelity.</span></span> <span data-ttu-id="2a24a-118">No entanto, uma exibição de faixa dinâmica padrão típica pode reproduzir apenas um pouco mais de três ordens de magnitude de luminância e, portanto, qualquer conteúdo processado por HDR tinha que ser tonemapped (compactado) no intervalo limitado da exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-118">However, a typical standard dynamic range display can reproduce only a little more than 3 orders of magnitude of luminance, and therefore any HDR-rendered content had to be tonemapped (compressed) into the limited range of the display.</span></span> <span data-ttu-id="2a24a-119">Novas exibições HDR, incluindo aquelas que estão em conformidade com o padrão HDR10 (BT. 2100), passam por essa limitação.</span><span class="sxs-lookup"><span data-stu-id="2a24a-119">New HDR displays, including those that comply with the HDR10 (BT.2100) standard, break through this limitation.</span></span>

### <a name="wide-color-gamut-with-automatic-system-color-management"></a><span data-ttu-id="2a24a-120">Ampla gama de cores com o gerenciamento automático de cores do sistema</span><span class="sxs-lookup"><span data-stu-id="2a24a-120">Wide color gamut with automatic system color management</span></span>

<span data-ttu-id="2a24a-121">A gama de cores refere-se ao intervalo e à saturação de matizes que uma exibição pode reproduzir.</span><span class="sxs-lookup"><span data-stu-id="2a24a-121">Color gamut refers to the range and saturation of hues that a display can reproduce.</span></span> <span data-ttu-id="2a24a-122">A cor natural mais saturada que o olho humano pode perceber é pura, leve em monodesvio, como o que é produzido por uma laser.</span><span class="sxs-lookup"><span data-stu-id="2a24a-122">The most saturated natural color the human eye can perceive is pure, monochromatic light such as what is produced by a laser.</span></span> <span data-ttu-id="2a24a-123">No entanto, as exibições de consumidor principais podem, muitas vezes, reproduzir cores apenas na gama de sRGB, que representa apenas cerca de 35% de todas as cores que podem ser exibidas pelo homem.</span><span class="sxs-lookup"><span data-stu-id="2a24a-123">However, mainstream consumer displays can often reproduce colors only within the sRGB gamut, which represents only about 35% of all human-perceivable colors.</span></span> <span data-ttu-id="2a24a-124">O diagrama a seguir é uma representação do "Spectral local" humano ou de todas as cores experceptívels (em um determinado nível de luminância), onde o triângulo menor é a gama de sRGB.</span><span class="sxs-lookup"><span data-stu-id="2a24a-124">The diagram below is a representation of the human "spectral locus", or all perceivable colors (at a given luminance level), where the smaller triangle is the sRGB gamut.</span></span>

![diagrama da gama de Spectral humana local e sRGB](images/HDR-WCG.jpg)

<span data-ttu-id="2a24a-126">O high-end, Professional PC, exibe as gamas de cores com suporte muito mais amplas do que sRGB, como Adobe RGB e D65-P3.</span><span class="sxs-lookup"><span data-stu-id="2a24a-126">High end, professional PC displays have long supported color gamuts that are significantly wider than sRGB, such as Adobe RGB and D65-P3.</span></span> <span data-ttu-id="2a24a-127">E esses monitores de ampla gama estão se tornando mais comuns.</span><span class="sxs-lookup"><span data-stu-id="2a24a-127">And these wide gamut displays are becoming more common.</span></span> <span data-ttu-id="2a24a-128">No entanto, antes da cor avançada, o Windows não executou nenhum gerenciamento de cores no nível do sistema para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2a24a-128">However, prior to advanced color, Windows didn't perform any system-level color management for applications.</span></span> <span data-ttu-id="2a24a-129">Isso significava que, se um aplicativo do DirectX renderizasse, por exemplo, um puro vermelho ou RGB (1,0, 0,0, 0,0) para sua cadeia de permuta, o Windows simplesmente examinaria o vermelho mais saturado que a exibição poderia reproduzir, independentemente da gama de cores real da exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-129">This meant that if a DirectX app rendered, for example, a pure red or RGB(1.0, 0.0, 0.0) to its swap chain, then Windows would simply scan out the most saturated red that the display could reproduce, regardless of what the actual color gamut of the display was.</span></span>

<span data-ttu-id="2a24a-130">Os aplicativos que precisavam de alta precisão de cor poderiam consultar os recursos de cores da exibição (por exemplo, usando perfis ICC) e executar seu próprio gerenciamento de cores em processo para direcionar corretamente a gama de cores da exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-130">Apps that needed high color accuracy could query the color capabilities of the display (for example, using ICC profiles), and perform their own in-process color management to correctly target the display's color gamut.</span></span> <span data-ttu-id="2a24a-131">No entanto, a grande maioria dos aplicativos e do conteúdo Visual pressupõe que a exibição é sRGB e depende do sistema operacional para atender a essa suposição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-131">However, the vast majority of apps and visual content assume that the display is sRGB, and they rely on the operating system to fulfill this assumption.</span></span>

<span data-ttu-id="2a24a-132">A cor avançada do Windows adiciona o gerenciamento automático de cores no nível do sistema.</span><span class="sxs-lookup"><span data-stu-id="2a24a-132">Windows advanced color adds automatic system-level color management.</span></span> <span data-ttu-id="2a24a-133">O Gerenciador de Janelas da Área de Trabalho (DWM) é o compositor do Windows.</span><span class="sxs-lookup"><span data-stu-id="2a24a-133">The Desktop Window Manager (DWM) is Windows' compositor.</span></span> <span data-ttu-id="2a24a-134">Quando a cor avançada está habilitada, o DWM executa uma conversão de cor explícita do conteúdo visual do aplicativo colorspace para um espaço de cor de composição canônico, que é scRGB.</span><span class="sxs-lookup"><span data-stu-id="2a24a-134">When advanced color is enabled, the DWM performs an explicit color conversion from the app visual content's colorspace to a canonical composition color space, which is scRGB.</span></span> <span data-ttu-id="2a24a-135">Em seguida, o Windows converte por cor o conteúdo do framebuffer composto no espaço de cores nativa da exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-135">Windows then color-converts the composed framebuffer content to the display's native color space.</span></span> <span data-ttu-id="2a24a-136">Dessa forma, o conteúdo tradicional do sRGB obtém automaticamente o comportamento preciso de cor, enquanto os aplicativos avançados com reconhecimento de cores podem aproveitar os recursos de cores completas da tela.</span><span class="sxs-lookup"><span data-stu-id="2a24a-136">In this way, traditional sRGB content automatically gets color-accurate behavior, while advanced color-aware apps can take advantage of the full color capabilities of the display.</span></span>

### <a name="deep-precisionbit-depth"></a><span data-ttu-id="2a24a-137">Profundidade de bit/precisão profunda</span><span class="sxs-lookup"><span data-stu-id="2a24a-137">Deep precision/bit depth</span></span>

<span data-ttu-id="2a24a-138">Precisão numérica ou profundidade de bits, refere-se à representação ou distinção entre cores semelhantes, mas distintas, sem faixas nem artefatos.</span><span class="sxs-lookup"><span data-stu-id="2a24a-138">Numerical precision, or bit depth, refers to representing or distinguishing between similar but distinct colors without banding nor artifacts.</span></span> <span data-ttu-id="2a24a-139">O PC principal exibe suporte a 8 bits por canal de cor, enquanto o olho humano requer pelo menos 10-12 bits de precisão para evitar distorções perceptível, sem recorrer a técnicas como pontilhamento ou dependendo das condições de exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-139">Mainstream PC displays support 8 bits per color channel, while the human eye requires at least 10-12 bits of precision to avoid perceivable distortions, without resorting to techniques such as dithering or depending on viewing conditions.</span></span>

![imagem de Windmills em um canal de 2 bits simulado por cor versus 8 bits por canal](images/HDR-bitdepth.jpg)

<span data-ttu-id="2a24a-141">Antes da cor avançada, os aplicativos de janela restritas do DWM para produzir conteúdo de saída em apenas 8 bits por canal de cor, mesmo que a exibição tenha suporte para uma profundidade de bits mais alta.</span><span class="sxs-lookup"><span data-stu-id="2a24a-141">Prior to advanced color, the DWM restricted windowed apps to output content at only 8 bits per color channel, even if the display supported a higher bit depth.</span></span> <span data-ttu-id="2a24a-142">Quando a cor avançada está habilitada, o DWM executa sua composição usando o ponto flutuante de metade de precisão do IEEE (FP16), eliminando quaisquer afunilamentos e permitindo a precisão total da exibição a ser usada.</span><span class="sxs-lookup"><span data-stu-id="2a24a-142">When advanced color is enabled, the DWM performs its composition using IEEE half-precision floating point (FP16), eliminating any bottlenecks, and allowing the full precision of the display to be used.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="2a24a-143">Requisitos do Sistema</span><span class="sxs-lookup"><span data-stu-id="2a24a-143">System Requirements</span></span>

### <a name="operating-system-os"></a><span data-ttu-id="2a24a-144">OS (sistema operacional)</span><span class="sxs-lookup"><span data-stu-id="2a24a-144">Operating system (OS)</span></span>

<span data-ttu-id="2a24a-145">O suporte avançado a cores fornecido pela primeira vez com o Windows 10, versão 1703, e foi significativamente melhorado com cada atualização.</span><span class="sxs-lookup"><span data-stu-id="2a24a-145">Advanced color support first shipped with Windows 10, version 1703, and it has been significantly improved with each update.</span></span> <span data-ttu-id="2a24a-146">Este tópico pressupõe que seu aplicativo está direcionando para o Windows 10, versão 1903 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2a24a-146">This topic assumes that your app is targeting Windows 10, version 1903, or later.</span></span>

### <a name="display"></a><span data-ttu-id="2a24a-147">Monitor</span><span class="sxs-lookup"><span data-stu-id="2a24a-147">Display</span></span>

<span data-ttu-id="2a24a-148">Para aproveitar o alto intervalo dinâmico, você deve ter uma exibição que dê suporte ao padrão HDR10.</span><span class="sxs-lookup"><span data-stu-id="2a24a-148">To take advantage of high dynamic range, you must have a display that supports the HDR10 standard.</span></span> <span data-ttu-id="2a24a-149">O Windows funciona melhor com exibições que são [certificadas pela VESA DisplayHDR](https://displayhdr.org/).</span><span class="sxs-lookup"><span data-stu-id="2a24a-149">Windows works best with displays that are [VESA DisplayHDR certified](https://displayhdr.org/).</span></span>

### <a name="graphics-processor-gpu"></a><span data-ttu-id="2a24a-150">Processador gráfico (GPU)</span><span class="sxs-lookup"><span data-stu-id="2a24a-150">Graphics processor (GPU)</span></span>

<span data-ttu-id="2a24a-151">Uma GPU recente é necessária.</span><span class="sxs-lookup"><span data-stu-id="2a24a-151">A recent GPU is required.</span></span> <span data-ttu-id="2a24a-152">Para dar suporte a exibições do HDR10, o Windows 10 requer um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="2a24a-152">To support HDR10 displays, Windows 10 requires one of the following.</span></span>

* <span data-ttu-id="2a24a-153">NVIDIA GeForce 1000 Series (Pascal) ou mais recente</span><span class="sxs-lookup"><span data-stu-id="2a24a-153">Nvidia GeForce 1000 series (Pascal), or newer</span></span>
* <span data-ttu-id="2a24a-154">AMD Radeon RX 400 Series (Polaris) ou mais recente</span><span class="sxs-lookup"><span data-stu-id="2a24a-154">AMD Radeon RX 400 series (Polaris), or newer</span></span>
* <span data-ttu-id="2a24a-155">Série Intel Core 7 selecionada (KABY Lake) ou mais recente</span><span class="sxs-lookup"><span data-stu-id="2a24a-155">Selected Intel Core 7 series (Kaby Lake), or newer</span></span>

<span data-ttu-id="2a24a-156">Observe que os requisitos de hardware adicionais se aplicam dependendo dos cenários, incluindo aceleração de codec de hardware (HEVC de 10 bits, VP9 de 10 bits etc.) e suporte do PlayReady (SL3000).</span><span class="sxs-lookup"><span data-stu-id="2a24a-156">Note that additional hardware requirements apply depending on the scenarios, including hardware codec acceleration (10 bit HEVC, 10 bit VP9, etc.) and PlayReady support (SL3000).</span></span> <span data-ttu-id="2a24a-157">Entre em contato com seu fornecedor de GPU para obter informações mais específicas.</span><span class="sxs-lookup"><span data-stu-id="2a24a-157">Contact your GPU vendor for more specific information.</span></span>

### <a name="graphics-driver-wddm"></a><span data-ttu-id="2a24a-158">Driver de gráficos (WDDM)</span><span class="sxs-lookup"><span data-stu-id="2a24a-158">Graphics driver (WDDM)</span></span>

<span data-ttu-id="2a24a-159">O driver de gráficos mais recente disponível é altamente recomendado, seja de Windows Update ou do site do fabricante do computador ou fornecedor da GPU.</span><span class="sxs-lookup"><span data-stu-id="2a24a-159">The latest available graphics driver is strongly recommended, either from Windows Update or from the GPU vendor or PC manufacturer's website.</span></span> <span data-ttu-id="2a24a-160">Para o Windows 10, versão 1903 e posterior, recomendamos drivers que suportam pelo menos o Windows Display Driver Model (WDDM) versão 2,6.</span><span class="sxs-lookup"><span data-stu-id="2a24a-160">For Windows 10, version 1903, and later, we recommend drivers that support at least Windows Display Driver Model (WDDM) version 2.6.</span></span>

## <a name="supported-rendering-apis"></a><span data-ttu-id="2a24a-161">APIs de renderização com suporte</span><span class="sxs-lookup"><span data-stu-id="2a24a-161">Supported rendering APIs</span></span>

<span data-ttu-id="2a24a-162">O Windows 10 dá suporte a uma ampla variedade de APIs e estruturas de renderização.</span><span class="sxs-lookup"><span data-stu-id="2a24a-162">Windows 10 supports a wide variety of rendering APIs and frameworks.</span></span> <span data-ttu-id="2a24a-163">O suporte à cor avançada depende fundamentalmente de seu aplicativo ser capaz de executar uma apresentação moderna usando DXGI ou as APIs de camada Visual.</span><span class="sxs-lookup"><span data-stu-id="2a24a-163">Advanced color support fundamentally relies on your app being able to perform modern presentation using either DXGI or the Visual Layer APIs.</span></span>

* [<span data-ttu-id="2a24a-164">DXGI (infraestrutura gráfica do DirectX)</span><span class="sxs-lookup"><span data-stu-id="2a24a-164">DirectX Graphics Infrastructure (DXGI)</span></span>](../direct3ddxgi/dx-graphics-dxgi.md)
* [<span data-ttu-id="2a24a-165">Camada Visual (Windows. UI. composição)</span><span class="sxs-lookup"><span data-stu-id="2a24a-165">Visual Layer (Windows.UI.Composition)</span></span>](/windows/uwp/composition/visual-layer)

<span data-ttu-id="2a24a-166">Portanto, qualquer API de renderização que possa produzir saída para um desses métodos de apresentação pode dar suporte à cor avançada.</span><span class="sxs-lookup"><span data-stu-id="2a24a-166">Therefore, any rendering API that can output to one of these presentations methods can support advanced color.</span></span> <span data-ttu-id="2a24a-167">Isso inclui, mas não se limita a esses.</span><span class="sxs-lookup"><span data-stu-id="2a24a-167">This includes but is not limited to these.</span></span>

* [<span data-ttu-id="2a24a-168">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2a24a-168">Direct3D 11</span></span>](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="2a24a-169">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2a24a-169">Direct3D 12</span></span>](../direct3d12/direct3d-12-graphics.md)
* [<span data-ttu-id="2a24a-170">Direct2D</span><span class="sxs-lookup"><span data-stu-id="2a24a-170">Direct2D</span></span>](../direct2d/direct2d-portal.md)
* [<span data-ttu-id="2a24a-171">Win2D</span><span class="sxs-lookup"><span data-stu-id="2a24a-171">Win2D</span></span>](https://github.com/Microsoft/Win2D)
  * <span data-ttu-id="2a24a-172">Requer o uso das APIs de nível inferior **CanvasSwapChain** ou **CanvasSwapChainPanel** .</span><span class="sxs-lookup"><span data-stu-id="2a24a-172">Requires using the lower level **CanvasSwapChain** or **CanvasSwapChainPanel** APIs.</span></span>
* [<span data-ttu-id="2a24a-173">**Windows.UI.Input.Inking**</span><span class="sxs-lookup"><span data-stu-id="2a24a-173">**Windows.UI.Input.Inking**</span></span>](/uwp/api/Windows.UI.Input.Inking)
  * <span data-ttu-id="2a24a-174">Dá suporte à renderização de tinta seca personalizada usando DirectX.</span><span class="sxs-lookup"><span data-stu-id="2a24a-174">Supports custom dry ink rendering using DirectX.</span></span>
* [<span data-ttu-id="2a24a-175">XAML</span><span class="sxs-lookup"><span data-stu-id="2a24a-175">XAML</span></span>](/windows/uwp/xaml-platform/)
  * <span data-ttu-id="2a24a-176">Dá suporte à reprodução de vídeos HDR usando o **mediaplayerelement**.</span><span class="sxs-lookup"><span data-stu-id="2a24a-176">Supports playback of HDR videos using **MediaPlayerElement**.</span></span>
  * <span data-ttu-id="2a24a-177">Dá suporte à decodificação de imagens JPEG XR usando o elemento **Image** .</span><span class="sxs-lookup"><span data-stu-id="2a24a-177">Supports decode of JPEG XR images using **Image** element.</span></span>
  * <span data-ttu-id="2a24a-178">Dá suporte à interoperabilidade do DirectX usando **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="2a24a-178">Supports DirectX interop using **SwapChainPanel**.</span></span>

## <a name="handling-dynamic-display-capabilities"></a><span data-ttu-id="2a24a-179">Manipulando recursos de exibição dinâmica</span><span class="sxs-lookup"><span data-stu-id="2a24a-179">Handling dynamic display capabilities</span></span>

<span data-ttu-id="2a24a-180">O Windows 10 dá suporte a uma enorme variedade de monitores avançados com capacidade de cor, desde painéis integrados de energia e eficiência até monitores e TVs de jogos de ponta.</span><span class="sxs-lookup"><span data-stu-id="2a24a-180">Windows 10 supports an enormous range of advanced color-capable displays, from power-efficient integrated panels to high end gaming monitors and TVs.</span></span> <span data-ttu-id="2a24a-181">Os usuários do Windows esperam que seu aplicativo manipule integralmente todas essas variações, incluindo exibições de SDR existentes.</span><span class="sxs-lookup"><span data-stu-id="2a24a-181">Windows users expect that your app will seamlessly handle all of these variations, including ubiquitous existing SDR displays.</span></span>

<span data-ttu-id="2a24a-182">O Windows 10 fornece controle sobre o HDR e recursos de cores avançados para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2a24a-182">Windows 10 provides control over HDR and advanced color capabilities to the user.</span></span> <span data-ttu-id="2a24a-183">Seu aplicativo deve detectar a configuração atual do vídeo e responder dinamicamente a quaisquer alterações no recurso.</span><span class="sxs-lookup"><span data-stu-id="2a24a-183">Your app must detect the current display's configuration, and respond dynamically to any changes in capability.</span></span> <span data-ttu-id="2a24a-184">Isso pode ocorrer por vários motivos, por exemplo, porque o usuário habilitou ou desabilitou um recurso ou moveu o aplicativo entre diferentes monitores ou o estado de energia do sistema mudou.</span><span class="sxs-lookup"><span data-stu-id="2a24a-184">This could occur for many reasons, for example, because the user enabled or disabled a feature, or moved the app between different displays, or the system's power state changed.</span></span>

### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="2a24a-185">Aplicativos da Plataforma Universal do Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="2a24a-185">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="2a24a-186">Se você estiver escrevendo um aplicativo UWP, independentemente da API de renderização de gráficos que estiver usando, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obter recursos de exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-186">If you're writing a UWP app, regardless of the graphics rendering API you're using, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get display capabilities.</span></span> <span data-ttu-id="2a24a-187">Obtenha uma instância de **AdvancedColorInfo** de [**DisplayInformation:: GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span><span class="sxs-lookup"><span data-stu-id="2a24a-187">Obtain an instance of **AdvancedColorInfo** from [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span></span>

<span data-ttu-id="2a24a-188">Para verificar qual tipo de cor avançado está ativo no momento, use a propriedade [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) .</span><span class="sxs-lookup"><span data-stu-id="2a24a-188">To check what advanced color kind is currently active, use the [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) property.</span></span> <span data-ttu-id="2a24a-189">No Windows 10, versão 1903 e posterior, isso retorna um dos três valores possíveis: **SDR**, **WCG** ou **HDR**.</span><span class="sxs-lookup"><span data-stu-id="2a24a-189">In Windows 10, version 1903, and later, this returns one of three possible values: **SDR**, **WCG**, or **HDR**.</span></span> <span data-ttu-id="2a24a-190">Essa é a propriedade mais importante a ser verificada e você deve configurar seu pipeline de renderização e de apresentação em resposta ao tipo ativo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-190">This is the most important property to check, and you should configure your render and presentation pipeline in response to the active kind.</span></span>

<span data-ttu-id="2a24a-191">Para verificar quais tipos de cores avançados têm suporte, mas não necessariamente ativos, chame [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span><span class="sxs-lookup"><span data-stu-id="2a24a-191">To check what advanced color kinds are supported, but not necessarily active, call [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span></span> <span data-ttu-id="2a24a-192">Você pode usar essas informações, por exemplo, para solicitar que o usuário navegue até o aplicativo de configurações do Windows para que ele possa habilitar HDR ou WCG.</span><span class="sxs-lookup"><span data-stu-id="2a24a-192">You could use this information, for example, to prompt the user to navigate to the Windows Settings app so that they can enable HDR or WCG.</span></span>

<span data-ttu-id="2a24a-193">Os outros membros de **AdvancedColorInfo** fornecem informações quantitativas sobre o volume de cores físicas do painel (luminescência e crominância), correspondentes aos metadados HDR estáticos SMPTE St. 2086.</span><span class="sxs-lookup"><span data-stu-id="2a24a-193">The other members of **AdvancedColorInfo** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="2a24a-194">Você deve usar essas informações para configurar o mapeamento de gamut e tonemapping HDR do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-194">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="2a24a-195">Para lidar com alterações em recursos de cores avançadas, registre-se para o evento [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) .</span><span class="sxs-lookup"><span data-stu-id="2a24a-195">To handle changes in advanced color capabilities, register for the [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) event.</span></span> <span data-ttu-id="2a24a-196">Esse evento será gerado se qualquer parâmetro dos recursos de cores avançados da exibição for alterado por qualquer motivo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-196">This event is raised if any parameter of the display's advanced color capabilities changes for any reason.</span></span>

<span data-ttu-id="2a24a-197">Manipule esse evento obtendo uma nova instância de **AdvancedColorInfo** e verificando quais valores foram alterados.</span><span class="sxs-lookup"><span data-stu-id="2a24a-197">Handle this event by obtaining a new instance of **AdvancedColorInfo**, and checking which values have changed.</span></span>

### <a name="desktop-win32-directx-apps"></a><span data-ttu-id="2a24a-198">Aplicativos DirectX da área de trabalho (Win32)</span><span class="sxs-lookup"><span data-stu-id="2a24a-198">Desktop (Win32) DirectX apps</span></span>

<span data-ttu-id="2a24a-199">Se você estiver escrevendo um aplicativo Win32 e usando o DirectX para renderizar, use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obter recursos de exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-199">If you're writing a Win32 app, and using DirectX to render, then use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get display capabilities.</span></span> <span data-ttu-id="2a24a-200">Obtenha uma instância desta estrutura por meio de [**IDXGIOutput6:: GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span><span class="sxs-lookup"><span data-stu-id="2a24a-200">Obtain an instance of this struct via [**IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span></span>

<span data-ttu-id="2a24a-201">Para verificar qual tipo de cor avançado está ativo no momento, use a propriedade **colorspace** , que é do tipo [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)e contém um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2a24a-201">To check what advanced color kind is currently active, use the **ColorSpace** property, which is of type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), and contains one of the following values:</span></span>

* <span data-ttu-id="2a24a-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span><span class="sxs-lookup"><span data-stu-id="2a24a-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span></span>
* <span data-ttu-id="2a24a-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span><span class="sxs-lookup"><span data-stu-id="2a24a-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span></span>

> [!Note]
> <span data-ttu-id="2a24a-204">Outros tipos de cores avançados, como WCG, são tratados como SDR por DXGI.</span><span class="sxs-lookup"><span data-stu-id="2a24a-204">Other advanced color kinds such as WCG are treated as SDR by DXGI.</span></span> <span data-ttu-id="2a24a-205">Não é possível usar DXGI para identificar uma exibição WCG.</span><span class="sxs-lookup"><span data-stu-id="2a24a-205">You can't use DXGI to identify a WCG display.</span></span>

> [!Note]
> <span data-ttu-id="2a24a-206">DXGI não permite verificar quais tipos de cores avançados têm suporte, mas não estão ativos no momento.</span><span class="sxs-lookup"><span data-stu-id="2a24a-206">DXGI doesn't let you check what advanced color kinds are supported but not active at the moment.</span></span>

<span data-ttu-id="2a24a-207">A maioria dos outros membros de **DXGI_OUTPUT_DESC1** fornece informações quantitativas sobre o volume de cores físicas do painel (luminescência e crominância), que corresponde aos metadados HDR estáticos SMPTE St. 2086.</span><span class="sxs-lookup"><span data-stu-id="2a24a-207">Most of the other members of **DXGI_OUTPUT_DESC1** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="2a24a-208">Você deve usar essas informações para configurar o mapeamento de gamut e tonemapping HDR do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-208">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="2a24a-209">Os aplicativos Win32 não têm um mecanismo nativo para responder a alterações de recursos de cores avançadas.</span><span class="sxs-lookup"><span data-stu-id="2a24a-209">Win32 apps don't have a native mechanism to respond to advanced color capability changes.</span></span> <span data-ttu-id="2a24a-210">Em vez disso, se seu aplicativo usar um loop de renderização, você deverá consultar [**IDXGIFactory1:: IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) com cada quadro.</span><span class="sxs-lookup"><span data-stu-id="2a24a-210">Instead, if your app uses a render loop, then you should query [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) with each frame.</span></span> <span data-ttu-id="2a24a-211">Se ele reportar **false**, você deverá obter um novo **DXGI_OUTPUT_DESC1** e verificar quais valores foram alterados.</span><span class="sxs-lookup"><span data-stu-id="2a24a-211">If it reports **FALSE**, then you should obtain a new **DXGI_OUTPUT_DESC1**, and check which values have changed.</span></span>

<span data-ttu-id="2a24a-212">Além disso, a bomba de mensagens Win32 deve lidar com a [**WM_SIZE**](../winmsg/wm-size.md) mensagem, que indica que seu aplicativo pode ter sido movido entre diferentes exibições.</span><span class="sxs-lookup"><span data-stu-id="2a24a-212">In addition, your Win32 message pump should handle the [**WM_SIZE**](../winmsg/wm-size.md) message, which indicates that your app may have moved between different displays.</span></span>

> [!Note]
> <span data-ttu-id="2a24a-213">Para obter uma nova **DXGI_OUTPUT_DESC1**, você deve obter a exibição atual.</span><span class="sxs-lookup"><span data-stu-id="2a24a-213">To obtain a new **DXGI_OUTPUT_DESC1**, you must obtain the current display.</span></span> <span data-ttu-id="2a24a-214">No entanto, você não deve chamar **IDXGISwapChain:: GetContainingOutput**.</span><span class="sxs-lookup"><span data-stu-id="2a24a-214">However, you should not call **IDXGISwapChain::GetContainingOutput**.</span></span> <span data-ttu-id="2a24a-215">Isso ocorre porque as cadeias de permuta retornarão uma saída DXGI obsoleta quando **DXGIFactory:: IsCurrent** for false e recriar a cadeia de permuta para obter uma saída atual resultará em uma tela preta temporária.</span><span class="sxs-lookup"><span data-stu-id="2a24a-215">This is because swap chains will return a stale DXGI output once **DXGIFactory::IsCurrent** is false, and recreating the swap chain to get a current output results in a temporary black screen.</span></span> <span data-ttu-id="2a24a-216">Em vez disso, recomendamos que você enumere os limites de todas as saídas de DXGI e determine qual delas tem a maior interseção com os limites da janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-216">Instead, we recommend that you enumerate through the bounds of all DXGI outputs, and determine which one has the greatest intersection with your app window's bounds.</span></span>

<span data-ttu-id="2a24a-217">O exemplo de código a seguir vem do [repositório DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="2a24a-217">The following code example comes from the [DirectX-Graphics-Samples repository](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span>

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a><span data-ttu-id="2a24a-218">Configurando sua cadeia de permuta do DirectX</span><span class="sxs-lookup"><span data-stu-id="2a24a-218">Setting up Your DirectX swap chain</span></span>

<span data-ttu-id="2a24a-219">Depois de determinar que a exibição atualmente dá suporte a recursos de cores avançados, configure sua cadeia de permuta da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="2a24a-219">Once you have determined that the display currently supports advanced color capabilities, configure your swap chain as follows.</span></span>

### <a name="use-a-flip-presentation-model-effect"></a><span data-ttu-id="2a24a-220">Usar um efeito de modelo de apresentação de inversão</span><span class="sxs-lookup"><span data-stu-id="2a24a-220">Use a flip presentation model effect</span></span>

<span data-ttu-id="2a24a-221">Ao criar sua cadeia de permuta usando o **CreateSwapChainFor [HWND | Composição | CoreWindow]** , você deve usar o modelo de flip dxgi selecionando a opção **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** ou **DXGI_SWAP_EFFECT_FLIP_DISCARD** , que torna sua cadeia de permuta qualificada para o processamento avançado de cores do DWM e várias otimizações de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="2a24a-221">When creating your swap chain using the **CreateSwapChainFor[Hwnd|Composition|CoreWindow]** methods, you must use the DXGI flip model by selecting either the **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** or **DXGI_SWAP_EFFECT_FLIP_DISCARD** option, which makes your swap chain eligible for advanced color processing from DWM and various fullscreen optimizations.</span></span> <span data-ttu-id="2a24a-222">Para obter mais informações, consulte o tópico [para obter o melhor desempenho, use o modelo de flip-dxgi](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) .</span><span class="sxs-lookup"><span data-stu-id="2a24a-222">For more information, refer to the [For best performance, use DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) topic.</span></span>

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a><span data-ttu-id="2a24a-223">Opção 1.</span><span class="sxs-lookup"><span data-stu-id="2a24a-223">Option 1.</span></span> <span data-ttu-id="2a24a-224">Usar o formato de pixel FP16 e o espaço de cores scRGB</span><span class="sxs-lookup"><span data-stu-id="2a24a-224">Use FP16 pixel format and scRGB color space</span></span>

<span data-ttu-id="2a24a-225">O Windows 10 dá suporte a duas combinações principais de formato de pixel e espaço de cores para a cor avançada.</span><span class="sxs-lookup"><span data-stu-id="2a24a-225">Windows 10 supports two main combinations of pixel format and color space for advanced color.</span></span> <span data-ttu-id="2a24a-226">Selecione uma com base nos requisitos específicos do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-226">Select one based on your app's specific requirements.</span></span>

<span data-ttu-id="2a24a-227">Para aplicativos de uso geral, ao criar sua cadeia de permuta, é recomendável especificar [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2a24a-227">For general-purpose apps, when creating your swap chain we recommend specifying [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="2a24a-228">Isso também é conhecido como *FP16* em sua [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="2a24a-228">That's also known as *FP16* in your [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="2a24a-229">Por padrão, uma cadeia de permuta criada com um formato de pixel de ponto flutuante é tratada como se ela usa o espaço de cores [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) , que também é conhecido como *ScRGB*.</span><span class="sxs-lookup"><span data-stu-id="2a24a-229">By default, a swap chain created with a floating point pixel format is treated as if it uses the [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color space, which is also known as *scRGB*.</span></span>

<span data-ttu-id="2a24a-230">Essa combinação fornece o intervalo numérico e a precisão para especificar quase qualquer cor possível fisicamente e executar processamento arbitrário, incluindo a mesclagem.</span><span class="sxs-lookup"><span data-stu-id="2a24a-230">This combination provides you with the numeric range and precision to specify almost any physically possible color, and perform arbitrary processing including blending.</span></span> <span data-ttu-id="2a24a-231">Além disso, se você estiver usando Direct2D, Win2D ou Windows. UI. composição, essa será a única combinação com suporte para qualquer cadeia de permuta ou destino intermediário que contenha conteúdo de cores avançado.</span><span class="sxs-lookup"><span data-stu-id="2a24a-231">In addition, if you're using Direct2D, Win2D, or Windows.UI.Composition, then this is the only supported combination for any swap chain or intermediate target that contains advanced color content.</span></span> 

<span data-ttu-id="2a24a-232">A principal compensação dessa opção é que ela consome 64 bits por pixel, o que dobra a largura de banda da GPU e o consumo de memória em comparação com os formatos de pixel UINT8 SDR tradicionais.</span><span class="sxs-lookup"><span data-stu-id="2a24a-232">The main tradeoff of this option is that it consumes 64 bits per pixel, which doubles GPU bandwidth and memory consumption compared to the traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="2a24a-233">Além disso, o scRGB usa valores numéricos que estão fora do intervalo [0, 1] normalizado para representar cores que estão fora da gama sRGB e/ou maior que 80 nits de luminância.</span><span class="sxs-lookup"><span data-stu-id="2a24a-233">In addition, scRGB uses numeric values that are outside the normalized [0, 1] range to represent colors that are outside the sRGB gamut and/or greater than 80 nits of luminance.</span></span> <span data-ttu-id="2a24a-234">Por exemplo, scRGB (1,0, 1,0, 1,0) codifica o branco D65 padrão às 80 nits; Mas scRGB (12,5, 12,5, 12,5) codifica o mesmo D65 branco com um número muito mais brilhante de 1000 nits.</span><span class="sxs-lookup"><span data-stu-id="2a24a-234">For example, scRGB (1.0, 1.0, 1.0) encodes the standard D65 white at 80 nits; but scRGB (12.5, 12.5, 12.5) encodes the same D65 white at a much brighter 1000 nits.</span></span> <span data-ttu-id="2a24a-235">Algumas operações gráficas exigem um intervalo numérico normalizado, e você deve modificar a operação ou renormalizar os valores de cor.</span><span class="sxs-lookup"><span data-stu-id="2a24a-235">Some graphics operations require a normalized numeric range, and you must either modify the operation, or re-normalize color values.</span></span>

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a><span data-ttu-id="2a24a-236">Opção 2: usar o formato de pixel UINT10/RGB10 e o espaço de cores HDR10/BT. 2100</span><span class="sxs-lookup"><span data-stu-id="2a24a-236">Option 2: Use UINT10/RGB10 pixel format and HDR10/BT.2100 color space</span></span>

<span data-ttu-id="2a24a-237">Para aplicativos que consomem conteúdo codificado em HDR10, como players de mídia ou aplicativos que devem ser usados principalmente em cenários de tela inteira, como jogos, ao criar sua cadeia de permuta, você deve considerar a especificação de [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) em [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span><span class="sxs-lookup"><span data-stu-id="2a24a-237">For apps that consume HDR10-encoded content, such as media players, or apps that are expected to be used mainly in fullscreen scenarios such as games, when creating your swap chain you should consider specifying [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="2a24a-238">Por padrão, isso é tratado como usando o espaço de cores sRGB; Portanto, você deve chamar explicitamente [**IDXGISwapChain3:: SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)e definir como seu espaço de cor [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), também conhecido como HDR10/BT. 2100.</span><span class="sxs-lookup"><span data-stu-id="2a24a-238">By default, this is treated as using the sRGB color space; therefore, you must explicitly call [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1), and set as your color space [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), also known as HDR10/BT.2100.</span></span>

<span data-ttu-id="2a24a-239">Essa combinação tem restrições mais rígidas do que FP16.</span><span class="sxs-lookup"><span data-stu-id="2a24a-239">This combination has more stringent restrictions than FP16.</span></span> <span data-ttu-id="2a24a-240">Você pode usar isso somente com o Direct3D 11 ou o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="2a24a-240">You can use this only with Direct3D 11 or Direct3D 12.</span></span> <span data-ttu-id="2a24a-241">Além disso, o UINT10/HDR10 tem limitações como um formato intermediário porque usa a função ST. 2084 EOTF ("gama"), que é altamente não linear e otimizada como um formato de conexão e oferece apenas 2 bits de alfa.</span><span class="sxs-lookup"><span data-stu-id="2a24a-241">In addition, UINT10/HDR10 has limitations as an intermediate format because it uses the ST.2084 EOTF ("gamma" function), which is highly nonlinear, and optimized as a wire format, and because it offers only 2 bits of alpha.</span></span>

<span data-ttu-id="2a24a-242">No entanto, essa combinação pode oferecer otimizações de desempenho poderosas quando usadas na saída final do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-242">However, this combination can offer powerful performance optimizations when used in your app's final output.</span></span> <span data-ttu-id="2a24a-243">Ele consome os mesmos 32 bits por pixel que os formatos de pixel UINT8 SDR tradicionais.</span><span class="sxs-lookup"><span data-stu-id="2a24a-243">It consumes the same 32 bits per pixel as traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="2a24a-244">Além disso, em determinados cenários de tela inteira, o sistema operacional pode otimizar o desempenho verificando diretamente a superfície HDR10.</span><span class="sxs-lookup"><span data-stu-id="2a24a-244">In addition, in certain fullscreen scenarios, the OS can optimize performance by directly scanning out the HDR10 surface.</span></span>

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a><span data-ttu-id="2a24a-245">Usando uma cadeia de troca de cor avançada quando a exibição está no modo de SDR</span><span class="sxs-lookup"><span data-stu-id="2a24a-245">Using an advanced color swap chain when the display is in SDR mode</span></span>

<span data-ttu-id="2a24a-246">Você pode usar uma cadeia de troca de cor avançada mesmo que a exibição não dê suporte a alguns ou todos os recursos de cores avançados que seu conteúdo requer.</span><span class="sxs-lookup"><span data-stu-id="2a24a-246">You can use an advanced color swap chain even if the display doesn't support some or all of the advanced color capabilities your content requires.</span></span> <span data-ttu-id="2a24a-247">Nesses casos, o Gerenciador de Janelas da Área de Trabalho (DWM) downconvertá seu conteúdo para se ajustar aos recursos da exibição.</span><span class="sxs-lookup"><span data-stu-id="2a24a-247">In those cases, the Desktop Window Manager (DWM) will downconvert your content to fit the display's capabilities.</span></span> <span data-ttu-id="2a24a-248">No Windows 10, versão 1903 e posterior, ele executará o recorte numérico; por exemplo, se você renderizar para uma cadeia de permuta FP16 scRGB, tudo fora do intervalo numérico [0, 1] será recortado.</span><span class="sxs-lookup"><span data-stu-id="2a24a-248">In Windows 10, version 1903, and later, it will perform numeric clipping; for example, if you render to an FP16 scRGB swap chain, then everything outside of the [0, 1] numeric range is clipped.</span></span>

<span data-ttu-id="2a24a-249">Esse comportamento de downconversion também ocorrerá se a janela do aplicativo estiver ampliando duas ou mais exibições com diferentes recursos de cores avançados.</span><span class="sxs-lookup"><span data-stu-id="2a24a-249">This downconversion behavior will also occur if your app window is straddling two or more displays with differing advanced color capabilities.</span></span> <span data-ttu-id="2a24a-250">**AdvancedColorInfo** e **IDXGIOutput6** são abstrados para relatar apenas as características da exibição "Main" (definidas como a exibição que contém o centro da janela).</span><span class="sxs-lookup"><span data-stu-id="2a24a-250">**AdvancedColorInfo** and **IDXGIOutput6** are abstracted to report only the "main" display's characteristics (defined as the display containing the center of the window).</span></span>

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a><span data-ttu-id="2a24a-251">Renderizar corretamente o conteúdo do SDR com o nível de referência do SDR</span><span class="sxs-lookup"><span data-stu-id="2a24a-251">Correctly render SDR content with SDR reference white level</span></span>

<span data-ttu-id="2a24a-252">Em muitos cenários, seu aplicativo desejará renderizar o conteúdo do SDR e do HDR; por exemplo, a renderização de legendas ou controles de transporte sobre o vídeo HDR ou a interface do usuário em uma cena de jogo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-252">In many scenarios, your app will want to render both SDR and HDR content; for example, rendering subtitles or transport controls over HDR video, or UI into a game scene.</span></span> <span data-ttu-id="2a24a-253">É importante entender o conceito de *nível branco de referência do SDR* para garantir que o conteúdo do SDR fique correto em uma tela HDR.</span><span class="sxs-lookup"><span data-stu-id="2a24a-253">It is important to understand the concept of *SDR reference white level* to ensure that your SDR content looks correct on an HDR display.</span></span>

<span data-ttu-id="2a24a-254">O Windows trata o conteúdo HDR como _mencionado na cena_, o que significa que um valor de cor específico deve ser exibido em um nível de luminância específico; por exemplo, scRGB (1,0, 1,0, 1,0) e HDR10 (497, 497, 497) codificam exatamente D65 branco à luminância de 80 nits.</span><span class="sxs-lookup"><span data-stu-id="2a24a-254">Windows treats HDR content as _scene-referred_, meaning that a particular color value should be displayed at a specific luminance level; for example, scRGB (1.0, 1.0, 1.0) and HDR10 (497, 497, 497) both encode exactly D65 white at 80 nits luminance.</span></span> <span data-ttu-id="2a24a-255">Enquanto isso, o conteúdo do SDR tradicionalmente tem sido _de saída – referenciado_ (ou exibido como referência), o que significa que sua luminância é deixada para o usuário ou para o dispositivo; por exemplo, sRGB (1,0, 1,0, 1,0) codifica D65 em branco como nos exemplos de HDR, mas em qualquer nível máximo de luminosidade em que a exibição é configurada.</span><span class="sxs-lookup"><span data-stu-id="2a24a-255">Meanwhile, SDR content traditionally has been _output-referred_ (or display-referred), meaning that its luminance is left up to the user or the device; for example sRGB (1.0, 1.0, 1.0) encodes D65 white as in the HDR examples, but at whatever maximum luminance the display is configured for.</span></span> <span data-ttu-id="2a24a-256">O Windows permite que o usuário ajuste o _nível de referência do SDR_ para sua preferência; Essa é a luminância que o Windows processará sRGB (1,0, 1,0, 1,0) em.</span><span class="sxs-lookup"><span data-stu-id="2a24a-256">Windows allows the user to adjust the _SDR reference white level_ to their preference; this is the luminance that Windows will render sRGB (1.0, 1.0, 1.0) at.</span></span> <span data-ttu-id="2a24a-257">Nos monitores HDR da área de trabalho, os níveis brancos de referência do SDR normalmente são definidos como cerca de 200 nits.</span><span class="sxs-lookup"><span data-stu-id="2a24a-257">On desktop HDR monitors, SDR reference white levels are typically set to around 200 nits.</span></span>

> [!Note]
> <span data-ttu-id="2a24a-258">Em uma exibição que dá suporte a um controle de brilho, como em um laptop, o Windows também ajustará a luminância do conteúdo HDR (referenciado pela cena) para corresponder ao nível de brilho desejado do usuário, mas isso é invisível para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-258">On a display that supports a brightness control, such as on a laptop, Windows will also adjust the luminance of HDR (scene-referred) content to match the user's desired brightness level, but this is invisible to the app.</span></span> <span data-ttu-id="2a24a-259">A menos que você esteja tentando garantir a reprodução precisa de bit do sinal HDR, geralmente é possível ignorar isso.</span><span class="sxs-lookup"><span data-stu-id="2a24a-259">Unless you're trying to guarantee bit-accurate reproduction of the HDR signal, you can generally ignore this.</span></span>

<span data-ttu-id="2a24a-260">Se seu aplicativo sempre renderiza SDR e HDR em superfícies separadas e se baseia na composição do sistema operacional, o Windows executará automaticamente o ajuste correto para aumentar o conteúdo do SDR para o nível de branco desejado.</span><span class="sxs-lookup"><span data-stu-id="2a24a-260">If your app always renders SDR and HDR to separate surfaces, and relies on OS composition, then Windows will automatically perform the correct adjustment to boost SDR content to the desired white level.</span></span> <span data-ttu-id="2a24a-261">Por exemplo, se seu aplicativo usar XAML e renderizar conteúdo HDR para seu próprio **SwapChainPanel**.</span><span class="sxs-lookup"><span data-stu-id="2a24a-261">For example, if your app uses XAML and renders HDR content to its own **SwapChainPanel**.</span></span>

<span data-ttu-id="2a24a-262">No entanto, se seu aplicativo executar sua própria composição de conteúdo de SDR e HDR em uma única superfície, você será responsável por executar o ajuste de nível de referência do SDR por conta própria.</span><span class="sxs-lookup"><span data-stu-id="2a24a-262">However, if your app performs its own composition of SDR and HDR content into a single surface, then you're responsible for performing the SDR reference white level adjustment yourself.</span></span> <span data-ttu-id="2a24a-263">Caso contrário, o conteúdo do SDR pode parecer muito escuro, supondo condições de exibição de desktop típicas.</span><span class="sxs-lookup"><span data-stu-id="2a24a-263">Otherwise the SDR content might appear too dim assuming typical desktop viewing conditions.</span></span> <span data-ttu-id="2a24a-264">Primeiro, você deve obter o nível branco de referência do SDR atual e, em seguida, ajustar os valores de cor de qualquer conteúdo SDR que esteja renderizando.</span><span class="sxs-lookup"><span data-stu-id="2a24a-264">First, you must obtain the current SDR reference white level, and then you must adjust the color values of any SDR content you're rendering.</span></span>

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a><span data-ttu-id="2a24a-265">Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="2a24a-265">Step 1.</span></span> <span data-ttu-id="2a24a-266">Obter o nível branco de referência do SDR atual</span><span class="sxs-lookup"><span data-stu-id="2a24a-266">Obtain the current SDR reference white level</span></span>

<span data-ttu-id="2a24a-267">Atualmente, somente os aplicativos UWP podem obter o nível de referência do SDR atual por meio de [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span><span class="sxs-lookup"><span data-stu-id="2a24a-267">Currently, only UWP apps can obtain the current SDR reference white level via [**AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span></span> <span data-ttu-id="2a24a-268">Essa API requer um [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="2a24a-268">This API requires a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

### <a name="step-2-adjust-color-values-of-sdr-content"></a><span data-ttu-id="2a24a-269">Etapa 2.</span><span class="sxs-lookup"><span data-stu-id="2a24a-269">Step 2.</span></span> <span data-ttu-id="2a24a-270">Ajustar valores de cor do conteúdo do SDR</span><span class="sxs-lookup"><span data-stu-id="2a24a-270">Adjust color values of SDR content</span></span>

<span data-ttu-id="2a24a-271">O Windows define o nível branco de referência nominal, ou padrão, às 80 nits; Portanto, se você fosse processar um branco sRGB (1,0, 1,0, 1,0) padrão para uma cadeia de permuta FP16, ele seria reproduzido a uma luminância de 80 nits.</span><span class="sxs-lookup"><span data-stu-id="2a24a-271">Windows defines the nominal, or default, reference white level at 80 nits; therefore if you were to render a standard sRGB (1.0, 1.0, 1.0) white to an FP16 swap chain, it would be reproduced at 80 nits luminance.</span></span> <span data-ttu-id="2a24a-272">Para corresponder ao nível branco de referência definido pelo usuário real, você deve ajustar o conteúdo do SDR de 80 nits para o nível especificado por meio de **AdvancedColorInfo. SdrWhiteLevelInNits**.</span><span class="sxs-lookup"><span data-stu-id="2a24a-272">In order to match the actual user-defined reference white level, you must adjust SDR content from 80 nits to the level specified via **AdvancedColorInfo.SdrWhiteLevelInNits**.</span></span>

<span data-ttu-id="2a24a-273">Se você estiver renderizando usando FP16 e ScRGB, ou qualquer espaço de cores que usa gama linear (1,0), poderá simplesmente multiplicar o valor de cor do SDR por _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_.</span><span class="sxs-lookup"><span data-stu-id="2a24a-273">If you're rendering using FP16 and scRGB, or any color space that uses linear (1.0) gamma, then you can simply multiply the SDR color value by _AdvancedColorInfo.SdrWhiteLevelInNits_ / _80_.</span></span> <span data-ttu-id="2a24a-274">Se você estiver usando Direct2D, haverá uma constante predefinida [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), que tem um valor de 80.</span><span class="sxs-lookup"><span data-stu-id="2a24a-274">If you're using Direct2D, there is a predefined constant [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), which has a value of 80.</span></span>

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

<span data-ttu-id="2a24a-275">Se você estiver renderizando usando um espaço de cores gama não linear, como HDR10, executar o ajuste de nível de branco do SDR será mais complexo; Se você estiver escrevendo seu próprio sombreador de pixel, considere a possibilidade de converter em gama linear para aplicar o ajuste.</span><span class="sxs-lookup"><span data-stu-id="2a24a-275">If you're rendering using a nonlinear gamma color space such as HDR10, then performing SDR white level adjustment is more complex; if you're writing your own pixel shader you should consider converting into linear gamma to apply the adjustment.</span></span>

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a><span data-ttu-id="2a24a-276">Adapte o conteúdo do HDR aos recursos do vídeo usando o tonemapping</span><span class="sxs-lookup"><span data-stu-id="2a24a-276">Adapt HDR content to the display's capabilities using tonemapping</span></span>

<span data-ttu-id="2a24a-277">As telas de cores HDR e avançadas variam muito em termos de seus recursos.</span><span class="sxs-lookup"><span data-stu-id="2a24a-277">HDR and advanced color displays vary greatly in terms of their capabilities.</span></span> <span data-ttu-id="2a24a-278">Por exemplo, a luminância mínima e máxima e a gama de cores são capazes de reproduzir.</span><span class="sxs-lookup"><span data-stu-id="2a24a-278">For example, the minimum and maximum luminance and the color gamut they are capable of reproducing.</span></span> <span data-ttu-id="2a24a-279">Em muitos casos, o conteúdo HDR conterá cores que excedem os recursos do vídeo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-279">In many cases, your HDR content will contain colors that exceed the display's capabilities.</span></span> <span data-ttu-id="2a24a-280">Para obter a melhor qualidade de imagem, é importante que você execute o HDR tonemapping, basicamente compactando o intervalo de cores para se ajustar à exibição, melhor preservando a intenção visual do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-280">For the best image quality it is important for you to perform HDR tonemapping, essentially compressing the range of colors to fit the display while best preserving the visual intent of the content.</span></span>

<span data-ttu-id="2a24a-281">O parâmetro único mais importante para se adaptar é a luminância máxima, também conhecida como MaxCLL (nível de luz de conteúdo); tonemappers mais sofisticados também adaptarão a luminância mín (MinCLL) e/ou primárias de cores.</span><span class="sxs-lookup"><span data-stu-id="2a24a-281">The most important single parameter to adapt for is max luminance, also known as MaxCLL (content light level); more sophisticated tonemappers will also adapt min luminance (MinCLL) and/or color primaries.</span></span>

### <a name="step-1-get-the-displays-color-volume-capabilities"></a><span data-ttu-id="2a24a-282">Etapa 1.</span><span class="sxs-lookup"><span data-stu-id="2a24a-282">Step 1.</span></span> <span data-ttu-id="2a24a-283">Obter os recursos de volume de cores da tela</span><span class="sxs-lookup"><span data-stu-id="2a24a-283">Get the display's color volume capabilities</span></span>

#### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="2a24a-284">Aplicativos da Plataforma Universal do Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="2a24a-284">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="2a24a-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) para obter o volume de cores da tela.</span><span class="sxs-lookup"><span data-stu-id="2a24a-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get the display's color volume.</span></span>

#### <a name="win32-desktop-directx-apps"></a><span data-ttu-id="2a24a-286">Aplicativos DirectX do Win32 (Desktop)</span><span class="sxs-lookup"><span data-stu-id="2a24a-286">Win32 (desktop) DirectX apps</span></span>

<span data-ttu-id="2a24a-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) para obter o volume de cores da tela.</span><span class="sxs-lookup"><span data-stu-id="2a24a-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get the display's color volume.</span></span>

### <a name="step-2-get-the-contents-color-volume-information"></a><span data-ttu-id="2a24a-288">Etapa 2.</span><span class="sxs-lookup"><span data-stu-id="2a24a-288">Step 2.</span></span> <span data-ttu-id="2a24a-289">Obter as informações de volume de cores do conteúdo</span><span class="sxs-lookup"><span data-stu-id="2a24a-289">Get the content's color volume information</span></span>

<span data-ttu-id="2a24a-290">Dependendo de onde veio seu conteúdo HDR, há várias maneiras possíveis de determinar suas informações de luminância e de gama de cores.</span><span class="sxs-lookup"><span data-stu-id="2a24a-290">Depending on where your HDR content came from, there are multiple potential ways to determine its luminance and color gamut information.</span></span> <span data-ttu-id="2a24a-291">Determinados arquivos de vídeo e imagem HDR contêm metadados SMPTE ST. 2086.</span><span class="sxs-lookup"><span data-stu-id="2a24a-291">Certain HDR video and image files contain SMPTE ST.2086 metadata.</span></span> <span data-ttu-id="2a24a-292">Se o conteúdo tiver sido renderizado dinamicamente, você poderá extrair informações de cena dos estágios de renderização internos, por exemplo, a fonte de luz mais brilhante em uma cena.</span><span class="sxs-lookup"><span data-stu-id="2a24a-292">If your content was rendered dynamically, then you may be able to extract scene information from the internal rendering stages, for example the brightest light source in a scene.</span></span>

<span data-ttu-id="2a24a-293">Uma solução mais geral, mas computacionalmente dispendiosa, é executar um histograma ou outra passagem de análise no quadro renderizado.</span><span class="sxs-lookup"><span data-stu-id="2a24a-293">A more general but computationally expensive solution is to run a histogram or other analysis pass on the rendered frame.</span></span> <span data-ttu-id="2a24a-294">O [exemplo do SDK de imagens de cores avançadas do Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstra como fazer isso usando o Direct2D; os trechos de código mais relevantes estão incluídos abaixo:</span><span class="sxs-lookup"><span data-stu-id="2a24a-294">The [Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstrates how to do this using Direct2D; the most relevant code snippets are included below:</span></span>

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a><span data-ttu-id="2a24a-295">Etapa 3.</span><span class="sxs-lookup"><span data-stu-id="2a24a-295">Step 3.</span></span> <span data-ttu-id="2a24a-296">Executar a operação HDR tonemapping</span><span class="sxs-lookup"><span data-stu-id="2a24a-296">Perform the HDR tonemapping operation</span></span>

<span data-ttu-id="2a24a-297">O tonemapping é inerentemente a um processo com perdas e pode ser otimizado para várias métricas de perceptiva ou objetivo, portanto, não há um algoritmo padrão.</span><span class="sxs-lookup"><span data-stu-id="2a24a-297">Tonemapping is inherently a lossy process, and can be optimized for a number of perceptual or objective metrics, so there is no one standard algorithm.</span></span> <span data-ttu-id="2a24a-298">O Windows fornece um efeito interno de [Tonemapper HDR](../direct2d/hdr-tone-map-effect.md) como parte do Direct2D, bem como no pipeline de reprodução de vídeo Media Foundation HDR.</span><span class="sxs-lookup"><span data-stu-id="2a24a-298">Windows provides a built-in [HDR tonemapper effect](../direct2d/hdr-tone-map-effect.md) as part of Direct2D as well as in the Media Foundation HDR video playback pipeline.</span></span> <span data-ttu-id="2a24a-299">Alguns outros algoritmos comumente usados incluem ACES Películaal, Reinhard e ITU-R BT. 2390-3 EETF (função de transferência elétrica elétrica).</span><span class="sxs-lookup"><span data-stu-id="2a24a-299">Some other commonly used algorithms include ACES Filmic, Reinhard, and ITU-R BT.2390-3 EETF (electrical-electrical transfer function).</span></span>

<span data-ttu-id="2a24a-300">Um operador Reinhard tonemapper simplificado é mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="2a24a-300">A simplified Reinhard tonemapper operator is shown below.</span></span>

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a><span data-ttu-id="2a24a-301">Capturando conteúdo HDR e WCG</span><span class="sxs-lookup"><span data-stu-id="2a24a-301">Capturing HDR and WCG content</span></span>

<span data-ttu-id="2a24a-302">APIs que dão suporte à especificação de formatos de pixel, como aqueles no namespace [**Windows. Graphics. Capture**](/uwp/api/windows.graphics.capture) e o método [**IDXGIOutput5::D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) , fornecem a capacidade de capturar conteúdo de cabeçalho e WCG sem perder informações de pixel.</span><span class="sxs-lookup"><span data-stu-id="2a24a-302">APIs that support specifying pixel formats, such as those in the [**Windows.Graphics.Capture**](/uwp/api/windows.graphics.capture) namespace, and the [**IDXGIOutput5::DuplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) method, provide the capability to capture HDR and WCG content without losing pixel information.</span></span> <span data-ttu-id="2a24a-303">Observe que, após a aquisição de quadros de conteúdo, será necessário processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="2a24a-303">Note that after acquiring content frames, additional processing is required.</span></span> <span data-ttu-id="2a24a-304">Por exemplo, o mapeamento de tons de HDR para SDR (por exemplo, a cópia de captura de tela do SDR para compartilhamento da Internet) e o salvamento de conteúdo com o formato adequado (por exemplo, JPEG XR).</span><span class="sxs-lookup"><span data-stu-id="2a24a-304">For example, HDR-to-SDR tone mapping (for example, SDR screenshot copy for Internet sharing) and content saving with proper format (for example, JPEG XR).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a24a-305">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="2a24a-305">Additional resources</span></span>

* <span data-ttu-id="2a24a-306">*Usando a renderização HDR com o DirectX Tool Kit* para [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)  /  [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span><span class="sxs-lookup"><span data-stu-id="2a24a-306">*Using HDR Rendering with the DirectX Tool Kit* for [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering) / [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span></span> <span data-ttu-id="2a24a-307">Walkthrough de como adicionar suporte a HDR a um aplicativo DirectX usando o DirectX Tool Kit (DirectXTK).</span><span class="sxs-lookup"><span data-stu-id="2a24a-307">Walkthrough of how to add HDR support to a DirectX app using the DirectX Tool Kit (DirectXTK).</span></span>
* <span data-ttu-id="2a24a-308">[Exemplo do SDK de imagens de cores avançadas do Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span><span class="sxs-lookup"><span data-stu-id="2a24a-308">[Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span></span> <span data-ttu-id="2a24a-309">Exemplo de SDK do UWP implementando um WCG com reconhecimento de cor avançado e um visualizador de imagem do amDirect2D.</span><span class="sxs-lookup"><span data-stu-id="2a24a-309">UWP SDK sample implementing an advanced color-aware HDR and WCG image viewer using Direct2D.</span></span> <span data-ttu-id="2a24a-310">Demonstra a gama completa de práticas recomendadas para aplicativos UWP, incluindo a resposta às alterações de funcionalidade de vídeo e o ajuste do nível branco do SDR.</span><span class="sxs-lookup"><span data-stu-id="2a24a-310">Demonstrates the full range of best practices for UWP apps, including responding to display capability changes and adjusting for SDR white level.</span></span>
* <span data-ttu-id="2a24a-311">[Exemplo de área de trabalho HDR do Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="2a24a-311">[Direct3D 12 HDR desktop sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span> <span data-ttu-id="2a24a-312">Exemplo de SDK de desktop implementando uma cena HDR básica do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="2a24a-312">Desktop SDK sample implementing a basic Direct3D 12 HDR scene.</span></span>
* <span data-ttu-id="2a24a-313">[Exemplo de UWP de HDR do Direct3D 12](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span><span class="sxs-lookup"><span data-stu-id="2a24a-313">[Direct3D 12 HDR UWP sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span></span> <span data-ttu-id="2a24a-314">UWP equivalente da amostra acima.</span><span class="sxs-lookup"><span data-stu-id="2a24a-314">UWP equivalent of the above sample.</span></span>
* <span data-ttu-id="2a24a-315">[Exemplo de PC do Xbox ATG SimpleHDR](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span><span class="sxs-lookup"><span data-stu-id="2a24a-315">[Xbox ATG SimpleHDR PC sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span></span> <span data-ttu-id="2a24a-316">Exemplo de SDK de desktop implementando uma cena HDR básica do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="2a24a-316">Desktop SDK sample implementing a basic Direct3D 11 HDR scene.</span></span>
