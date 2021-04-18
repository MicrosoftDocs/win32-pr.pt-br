---
description: Usando o codec de tela do Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Usando o codec de tela do Windows Media Video 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759685"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a><span data-ttu-id="89e70-103">Usando o codec de tela do Windows Media Video 9 (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="89e70-103">Using the Windows Media Video 9 Screen Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="89e70-104">O codec de tela do Windows Media Video 9 é otimizado para compactação de *vídeo do aplicativo*, que consiste em capturas de tela consecutivas para uma exibição do computador.</span><span class="sxs-lookup"><span data-stu-id="89e70-104">The Windows Media Video 9 Screen codec is optimized for compressing *application video*, which consists of consecutive screen shots for a computer display.</span></span> <span data-ttu-id="89e70-105">O codec aproveita a simplicidade da imagem típica (relativamente poucas cores, muitas linhas retas e assim por diante) e a falta de movimento relativa para atingir uma taxa de compactação muito alta.</span><span class="sxs-lookup"><span data-stu-id="89e70-105">The codec takes advantage of the typical image simplicity (relatively few colors, lots of straight lines, and so on) and relative lack of motion to achieve a very high compression ratio.</span></span> <span data-ttu-id="89e70-106">A desvantagem dessa otimização é que o vídeo que não está em conformidade com as características esperadas do vídeo do aplicativo pode ser difícil de compactar com um nível aceitável de qualidade.</span><span class="sxs-lookup"><span data-stu-id="89e70-106">The disadvantage of this optimization is that video that doesn't conform to the expected characteristics of application video can be difficult to compress with an acceptable level of quality.</span></span>

<span data-ttu-id="89e70-107">O codificador de tela do Windows Media Video 9 é identificado pelo CLSID do identificador de classe \_ CMSSEncMediaObject2, e o decodificador é identificado como o CLSID do identificador de classe \_ CMSSDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="89e70-107">The Windows Media Video 9 Screen encoder is identified by the class identifier CLSID\_CMSSEncMediaObject2, and the decoder is identified the class identifier CLSID\_CMSSDecMediaObject.</span></span> <span data-ttu-id="89e70-108">O valor FOURCC para os tipos de mídia usando esse codec é "MSS2".</span><span class="sxs-lookup"><span data-stu-id="89e70-108">The FOURCC value for media types using this codec is "MSS2".</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="89e70-109">Configurando o codificador</span><span class="sxs-lookup"><span data-stu-id="89e70-109">Configuring the Encoder</span></span>

<span data-ttu-id="89e70-110">O codificador do codec de tela do Windows Media Video 9 é configurado da mesma forma que o decodificador de vídeo padrão.</span><span class="sxs-lookup"><span data-stu-id="89e70-110">The encoder of the Windows Media Video 9 Screen codec is configured in the same way as the standard video decoder.</span></span>

> [!Note]  
> <span data-ttu-id="89e70-111">O codificador de tela dá suporte apenas à codificação de uma passagem.</span><span class="sxs-lookup"><span data-stu-id="89e70-111">The screen encoder supports only one-pass encoding.</span></span> <span data-ttu-id="89e70-112">Você pode definir a propriedade [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) como 2 e processar as entradas duas vezes sem erro, mas não há nenhum benefício para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="89e70-112">You can set the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2 and process the inputs twice without error, but there is no benefit to doing so.</span></span> <span data-ttu-id="89e70-113">Esse é um problema conhecido e pode ser corrigido em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="89e70-113">This is a known issue and may be corrected in future releases.</span></span>

 

## <a name="getting-the-best-results"></a><span data-ttu-id="89e70-114">Obtendo os melhores resultados</span><span class="sxs-lookup"><span data-stu-id="89e70-114">Getting the Best Results</span></span>

<span data-ttu-id="89e70-115">Se você descobrir que a qualidade desejada em seu conteúdo de captura de tela requer uma taxa de bits maior do que você pode usar para o cenário de entrega, você pode tentar as seguintes técnicas para obter mais eficiência do Codec:</span><span class="sxs-lookup"><span data-stu-id="89e70-115">If you discover that the quality you want in your screen capture content requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec:</span></span>

-   <span data-ttu-id="89e70-116">Use uma resolução menor para a captura de tela.</span><span class="sxs-lookup"><span data-stu-id="89e70-116">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="89e70-117">Capturar uma resolução de tela maior do que o necessário pode confundir o visualizador apresentando informações desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="89e70-117">Capturing a larger screen resolution than needed can confuse the viewer by presenting unnecessary information.</span></span>
-   <span data-ttu-id="89e70-118">Use uma taxa de quadros mais lenta.</span><span class="sxs-lookup"><span data-stu-id="89e70-118">Use a slower frame rate.</span></span> <span data-ttu-id="89e70-119">Capturas de tela geralmente podem ser eficazes em taxas de quadros muito baixas (às vezes, com 4 ou 5 quadros por segundo).</span><span class="sxs-lookup"><span data-stu-id="89e70-119">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="89e70-120">Use menos elementos gráficos na captura de tela.</span><span class="sxs-lookup"><span data-stu-id="89e70-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="89e70-121">O codec de tela do Windows Media Video 9 é otimizado para codificar primitivos e texto do Windows com alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="89e70-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="89e70-122">Geralmente, ocorrem problemas devido a gráficos de bitmap, que geralmente contêm milhares de cores individuais.</span><span class="sxs-lookup"><span data-stu-id="89e70-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="89e70-123">Quanto menos bitmaps estiverem na tela quando você capturar, melhor será seus resultados.</span><span class="sxs-lookup"><span data-stu-id="89e70-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="89e70-124">Se você não puder eliminar gráficos da captura de tela, há várias maneiras de minimizar o impacto que um bitmap tem na qualidade da imagem:</span><span class="sxs-lookup"><span data-stu-id="89e70-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact that a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="89e70-125">Reduza o tamanho do gráfico.</span><span class="sxs-lookup"><span data-stu-id="89e70-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="89e70-126">Reduza o número de gráficos individuais que aparecem na tela ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="89e70-126">Reduce the number of individual graphics that appear on the screen at the same time.</span></span>
    -   <span data-ttu-id="89e70-127">Reduza a quantidade de movimento do gráfico.</span><span class="sxs-lookup"><span data-stu-id="89e70-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="89e70-128">Por exemplo, se o elemento gráfico estiver em uma janela, mantenha a janela como estático como possível.</span><span class="sxs-lookup"><span data-stu-id="89e70-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="89e70-129">Evite mover o ponteiro do mouse sobre o gráfico ou arrastar o Windows ou outros elementos sobre o gráfico.</span><span class="sxs-lookup"><span data-stu-id="89e70-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>

## <a name="decoding"></a><span data-ttu-id="89e70-130">Decodificação</span><span class="sxs-lookup"><span data-stu-id="89e70-130">Decoding</span></span>

<span data-ttu-id="89e70-131">Não há requisitos especiais para decodificar vídeo de captura de tela.</span><span class="sxs-lookup"><span data-stu-id="89e70-131">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="89e70-132">No entanto, assim como acontece com todos os codecs do Windows Media Video 9, o decodificador de captura de tela não pode descompactar corretamente o conteúdo codificado sem os dados privados do codec.</span><span class="sxs-lookup"><span data-stu-id="89e70-132">However, as with all Windows Media Video 9 codecs, the screen capture decoder cannot properly decompress the encoded content without the codec private data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89e70-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89e70-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89e70-134">Configurando a codificação de vídeo</span><span class="sxs-lookup"><span data-stu-id="89e70-134">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="89e70-135">Usando dados privados do codec de vídeo</span><span class="sxs-lookup"><span data-stu-id="89e70-135">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="89e70-136">Codificador de tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="89e70-136">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> <dt>

[<span data-ttu-id="89e70-137">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="89e70-137">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



