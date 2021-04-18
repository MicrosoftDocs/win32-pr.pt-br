---
title: Fonte de imagem secundária normal
description: Fonte de imagem secundária normal
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781359"
---
# <a name="normal-secondary-image-source"></a><span data-ttu-id="7a4de-108">Fonte de imagem secundária normal</span><span class="sxs-lookup"><span data-stu-id="7a4de-108">Normal Secondary Image Source</span></span>

<span data-ttu-id="7a4de-109">Dependendo da função do botão, talvez seja necessário definir o local da imagem normal para o estado secundário do botão.</span><span class="sxs-lookup"><span data-stu-id="7a4de-109">Depending on the button function, you may need to define the location of the normal image for the secondary state of the button.</span></span> <span data-ttu-id="7a4de-110">Essa será a imagem que os usuários veem quando enviam por push um botão de função PlayPause na primeira vez.</span><span class="sxs-lookup"><span data-stu-id="7a4de-110">This will be the image users see when they push a PlayPause function button the first time.</span></span>

<span data-ttu-id="7a4de-111">Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço.</span><span class="sxs-lookup"><span data-stu-id="7a4de-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="7a4de-112">Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.</span><span class="sxs-lookup"><span data-stu-id="7a4de-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="7a4de-113">Por exemplo, para definir a imagem normal para uma origem de imagem secundária, se a imagem estiver dentro do bitmap enviado por push, digite:</span><span class="sxs-lookup"><span data-stu-id="7a4de-113">For example, to define the normal image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 210,0

```



<span data-ttu-id="7a4de-114">Os Estados secundários não podem ter uma imagem desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7a4de-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="7a4de-115">As imagens secundárias devem ter a mesma largura e altura que a imagem primária.</span><span class="sxs-lookup"><span data-stu-id="7a4de-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a4de-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a4de-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a4de-117">**Botões**</span><span class="sxs-lookup"><span data-stu-id="7a4de-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




