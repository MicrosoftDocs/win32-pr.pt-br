---
title: Obtendo bons resultados com o codec de tela do Windows Media Video 9
description: Obtendo bons resultados com o codec de tela do Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- SDK do Windows Media Format, codec de tela do Windows Media Video 9
- ASF (Advanced Systems Format), codec de tela do Windows Media Video 9
- ASF (formato de sistemas avançados), codec de tela do Windows Media Video 9
- codecs, tela do Windows Media Video 9
- Codec de tela do Windows Media Video 9, resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917008"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a><span data-ttu-id="3dcea-108">Obtendo bons resultados com o codec de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="3dcea-108">Getting Good Results with the Windows Media Video 9 Screen Codec</span></span>

<span data-ttu-id="3dcea-109">O codec de tela do Windows Media Video 9 foi projetado para produzir vídeo altamente compactado para captura de tela.</span><span class="sxs-lookup"><span data-stu-id="3dcea-109">The Windows Media Video 9 Screen codec is designed to produce highly compressed video for screen capture.</span></span> <span data-ttu-id="3dcea-110">Como a maior parte da necessidade de captura de tela envolve imagens razoavelmente simples e estáticas, os altos níveis de compactação obtidos geralmente não significam um grande sacrifício na qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="3dcea-110">Because most of the need for screen capture involves fairly simple and static images, the high levels of compression attained do not usually mean a great sacrifice in image quality.</span></span> <span data-ttu-id="3dcea-111">No entanto, cada captura de tela é diferente e a qualidade da imagem resultante pode variar consideravelmente dependendo das circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="3dcea-111">However, each screen capture is different, and the resulting image quality can vary considerably depending upon the circumstances.</span></span>

<span data-ttu-id="3dcea-112">A melhor maneira de determinar as configurações de perfil para uma sessão de codec de tela é codificar um arquivo de teste usando um fluxo de taxa de bits variável com base em qualidade.</span><span class="sxs-lookup"><span data-stu-id="3dcea-112">The best way to determine the profile settings for a screen codec session is to encode a test file using a quality-based variable bit rate stream.</span></span> <span data-ttu-id="3dcea-113">Defina a qualidade para o valor desejado e codifique uma captura de tela como se estivesse gravando o arquivo final.</span><span class="sxs-lookup"><span data-stu-id="3dcea-113">Set the quality to the value you desire, and encode a screen capture as if you were recording the final file.</span></span> <span data-ttu-id="3dcea-114">Quando o arquivo for gravado, execute-o usando o objeto leitor assíncrono, fazendo chamadas regulares para [**IWMReaderAdvanced:: Getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics).</span><span class="sxs-lookup"><span data-stu-id="3dcea-114">When the file is written, play it using the asynchronous reader object, making regular calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics).</span></span> <span data-ttu-id="3dcea-115">Ao monitorar o valor do membro **dwBandwidth** da estrutura de [**\_ \_ estatísticas do WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) para cada chamada, você pode determinar a taxa de bits aproximada necessária para atingir a qualidade desejada.</span><span class="sxs-lookup"><span data-stu-id="3dcea-115">By monitoring the value of the **dwBandwidth** member of the [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure for each call, you can determine the approximate bit rate required to achieve the quality you want.</span></span> <span data-ttu-id="3dcea-116">Em seguida, você pode usar essa taxa de bits para a codificação de taxa de bits constante.</span><span class="sxs-lookup"><span data-stu-id="3dcea-116">You can then use that bit rate for constant bit rate encoding.</span></span>

<span data-ttu-id="3dcea-117">Se você descobrir que a qualidade desejada requer uma taxa de bits maior do que você pode usar para o cenário de entrega, você pode tentar as técnicas a seguir para obter mais eficiência do codec.</span><span class="sxs-lookup"><span data-stu-id="3dcea-117">If you discover that the quality you want requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec.</span></span>

-   <span data-ttu-id="3dcea-118">Use uma resolução menor para a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="3dcea-118">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="3dcea-119">Capturar uma resolução de tela maior do que você precisa também pode criar confusão para o visualizador apresentando mais informações do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="3dcea-119">Capturing a larger screen resolution than you need can also create confusion for the viewer by presenting more information than is needed.</span></span>
-   <span data-ttu-id="3dcea-120">Use menos elementos gráficos na captura de tela.</span><span class="sxs-lookup"><span data-stu-id="3dcea-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="3dcea-121">O codec de tela do Windows Media Video 9 é otimizado para codificar primitivos e texto do Windows com alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="3dcea-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="3dcea-122">Geralmente, ocorrem problemas devido a gráficos de bitmap, que geralmente contêm milhares de cores individuais.</span><span class="sxs-lookup"><span data-stu-id="3dcea-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="3dcea-123">Quanto menos bitmaps estiverem na tela quando você capturar, melhor será seus resultados.</span><span class="sxs-lookup"><span data-stu-id="3dcea-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="3dcea-124">Se você não puder eliminar gráficos da captura de tela, há várias maneiras de minimizar o impacto que um bitmap tem na qualidade da imagem:</span><span class="sxs-lookup"><span data-stu-id="3dcea-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="3dcea-125">Reduza o tamanho do gráfico.</span><span class="sxs-lookup"><span data-stu-id="3dcea-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="3dcea-126">Reduza o número de gráficos individuais que aparecem na tela simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="3dcea-126">Reduce the number of individual graphics that appear on the screen concurrently.</span></span>
    -   <span data-ttu-id="3dcea-127">Reduza a quantidade de movimento do gráfico.</span><span class="sxs-lookup"><span data-stu-id="3dcea-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="3dcea-128">Por exemplo, se o elemento gráfico estiver em uma janela, mantenha a janela como estático como possível.</span><span class="sxs-lookup"><span data-stu-id="3dcea-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="3dcea-129">Evite mover o ponteiro do mouse sobre o gráfico ou arrastar o Windows ou outros elementos sobre o gráfico.</span><span class="sxs-lookup"><span data-stu-id="3dcea-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>
-   <span data-ttu-id="3dcea-130">Use uma taxa de [*quadros*](wmformat-glossary.md)mais lenta.</span><span class="sxs-lookup"><span data-stu-id="3dcea-130">Use a slower [*frame rate*](wmformat-glossary.md).</span></span> <span data-ttu-id="3dcea-131">Capturas de tela geralmente podem ser eficazes em taxas de quadros muito baixas (às vezes, com 4 ou 5 quadros por segundo).</span><span class="sxs-lookup"><span data-stu-id="3dcea-131">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="3dcea-132">Reduza a taxa de bits do áudio que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="3dcea-132">Reduce the bit rate of the accompanying audio.</span></span>

<span data-ttu-id="3dcea-133">Além disso, o codec não oferece suporte ao redimensionamento do retângulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3dcea-133">Also, the codec does not support resizing of the video rectangle.</span></span> <span data-ttu-id="3dcea-134">Em outras palavras, se você tentar usar o codec para codificar uma tela de 800 x 600 para um retângulo de vídeo 640 x 480, o vídeo resultante terá artefatos significativos que podem tornar grande parte do texto na tela ilegível.</span><span class="sxs-lookup"><span data-stu-id="3dcea-134">In other words, if you try to use the codec to encode a 800 x 600 screen down into to a 640 x 480 video rectangle, the resulting video will have significant artifacts that may make much of the text on the screen illegible.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dcea-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3dcea-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dcea-136">**Configurando fluxos de captura de tela**</span><span class="sxs-lookup"><span data-stu-id="3dcea-136">**Configuring Screen Capture Streams**</span></span>](configuring-screen-capture-streams.md)
</dt> <dt>

[<span data-ttu-id="3dcea-137">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="3dcea-137">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




