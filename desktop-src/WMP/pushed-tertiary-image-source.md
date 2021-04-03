---
title: Fonte de imagem terciário enviada por push
description: Fonte de imagem terciário enviada por push
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916297"
---
# <a name="pushed-tertiary-image-source"></a><span data-ttu-id="47494-108">Fonte de imagem terciário enviada por push</span><span class="sxs-lookup"><span data-stu-id="47494-108">Pushed Tertiary Image Source</span></span>

<span data-ttu-id="47494-109">A função de botão PlayPauseStop requer que você defina o local da imagem enviada para o estado terciário do botão.</span><span class="sxs-lookup"><span data-stu-id="47494-109">The PlayPauseStop button function requires that you define the location of the pushed image for the tertiary state of the button.</span></span> <span data-ttu-id="47494-110">Essa será a imagem que os usuários veem quando enviam o botão PlayPauseStop durante o streaming de uma transmissão ao vivo.</span><span class="sxs-lookup"><span data-stu-id="47494-110">This will be the image users see when they push the PlayPauseStop button while streaming a live broadcast.</span></span>

<span data-ttu-id="47494-111">Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço.</span><span class="sxs-lookup"><span data-stu-id="47494-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="47494-112">Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.</span><span class="sxs-lookup"><span data-stu-id="47494-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="47494-113">Por exemplo, para definir a imagem enviada por push para uma fonte de imagem terciário, se a imagem estiver dentro do bitmap enviado por push, digite:</span><span class="sxs-lookup"><span data-stu-id="47494-113">For example, to define the pushed image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 324,0

```



<span data-ttu-id="47494-114">Os Estados terciários não podem ter uma imagem desabilitada.</span><span class="sxs-lookup"><span data-stu-id="47494-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="47494-115">São consideradas imagens terciários com a mesma largura e altura das imagens primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="47494-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47494-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47494-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47494-117">**Botões**</span><span class="sxs-lookup"><span data-stu-id="47494-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




