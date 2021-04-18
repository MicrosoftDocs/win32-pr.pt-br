---
title: Posicionar e mover os retângulos de vídeo no espaço de composição
description: Posicionando e movendo os retângulos de vídeo no espaço de composição
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105766988"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="21978-103">Posicionar e mover os retângulos de vídeo no espaço de composição</span><span class="sxs-lookup"><span data-stu-id="21978-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="21978-104">Quando o VMR combina vários fluxos de entrada, ele posiciona cada fluxo dentro de um retângulo normalizado, chamado "espaço de composição".</span><span class="sxs-lookup"><span data-stu-id="21978-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="21978-105">No espaço de composição, as coordenadas (0,0, 0,0) a (1,0, 1,0) formam o retângulo de vídeo visível.</span><span class="sxs-lookup"><span data-stu-id="21978-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="21978-106">Todas as coordenadas que estão fora deste retângulo são recortadas.</span><span class="sxs-lookup"><span data-stu-id="21978-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="21978-107">Um aplicativo pode executar efeitos especiais com a movimentação, o alongamento e a redução do vídeo de um fluxo de entrada, alterando o retângulo de destino no espaço de composição para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="21978-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="21978-108">Se o retângulo especificado for um tamanho diferente do retângulo de vídeo nativo, o vídeo nativo será reduzido ou ampliado para caber.</span><span class="sxs-lookup"><span data-stu-id="21978-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="21978-109">O retângulo de destino é especificado chamando o método [**IVMRMixerControl:: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .</span><span class="sxs-lookup"><span data-stu-id="21978-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="21978-110">Por exemplo, suponha que o fluxo 0 (que corresponde ao pino 0) contenha o fluxo de vídeo principal, e o fluxo 1 (que corresponde ao pino 1) contenha um vídeo secundário.</span><span class="sxs-lookup"><span data-stu-id="21978-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="21978-111">O fluxo 1 pode ser posicionado completamente fora da tela, especificando um retângulo normalizado de {-1,0 f, 0,0 f, 0,0 f, 1,0 f}.</span><span class="sxs-lookup"><span data-stu-id="21978-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="21978-112">O fluxo 1 pode então ser movido para a área visível modificando os lados esquerdo e direito do retângulo sobre as chamadas sucessivas para **SetOutputRect**:</span><span class="sxs-lookup"><span data-stu-id="21978-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



|        |                             |
|--------|-----------------------------|
| <span data-ttu-id="21978-113">Hora</span><span class="sxs-lookup"><span data-stu-id="21978-113">Time</span></span>   | <span data-ttu-id="21978-114">Retângulo</span><span class="sxs-lookup"><span data-stu-id="21978-114">Rectangle</span></span>                   |
| <span data-ttu-id="21978-115">t + 0</span><span class="sxs-lookup"><span data-stu-id="21978-115">t + 0</span></span>  | <span data-ttu-id="21978-116">{-1,0 f, 0,0 f, 0,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="21978-116">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="21978-117">t + 1</span><span class="sxs-lookup"><span data-stu-id="21978-117">t + 1</span></span>  | <span data-ttu-id="21978-118">{-0,9 f, 0,0 f, 0,1 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="21978-118">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="21978-119">t + 2</span><span class="sxs-lookup"><span data-stu-id="21978-119">t + 2</span></span>  | <span data-ttu-id="21978-120">{-0,8 f, 0,0 f, 0,2 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="21978-120">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="21978-121">...</span><span class="sxs-lookup"><span data-stu-id="21978-121">...</span></span>    | <span data-ttu-id="21978-122">...</span><span class="sxs-lookup"><span data-stu-id="21978-122">...</span></span>                         |
| <span data-ttu-id="21978-123">t + 10</span><span class="sxs-lookup"><span data-stu-id="21978-123">t + 10</span></span> | <span data-ttu-id="21978-124">{0,0 f, 0,0 f, 1,0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="21978-124">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![movendo um fluxo de vídeo no espaço de composição](images/composition-space.png)

<span data-ttu-id="21978-126">No tempo t + 10, o vídeo do fluxo 1 fica completamente visível.</span><span class="sxs-lookup"><span data-stu-id="21978-126">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="21978-127">Neste exemplo, o tamanho nativo do fluxo 1 foi mantido enquanto estava sendo movido.</span><span class="sxs-lookup"><span data-stu-id="21978-127">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="21978-128">Você também pode alongar ou reduzir o retângulo para produzir efeitos interessantes.</span><span class="sxs-lookup"><span data-stu-id="21978-128">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="21978-129">Você também pode virar o vídeo verticalmente, especificando um valor maior para o topo da parte inferior ou espelhar o vídeo horizontalmente, especificando um valor maior para o lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="21978-129">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21978-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21978-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21978-131">Usando o modo de mixagem do VMR</span><span class="sxs-lookup"><span data-stu-id="21978-131">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



