---
title: Fonte de imagem secundária enviada por push
description: Fonte de imagem secundária enviada por push
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de50f72c8af34fa4f3e44507e172cae6890dc47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005593"
---
# <a name="pushed-secondary-image-source"></a><span data-ttu-id="0a0cd-108">Fonte de imagem secundária enviada por push</span><span class="sxs-lookup"><span data-stu-id="0a0cd-108">Pushed Secondary Image Source</span></span>

<span data-ttu-id="0a0cd-109">Dependendo da função do botão, talvez seja necessário definir o local da imagem enviada para o estado secundário do botão.</span><span class="sxs-lookup"><span data-stu-id="0a0cd-109">Depending on the button function, you may need to define the location of the pushed image for the secondary state of the button.</span></span> <span data-ttu-id="0a0cd-110">Essa será a imagem que os usuários veem quando enviam um botão de função PlayPause da segunda vez.</span><span class="sxs-lookup"><span data-stu-id="0a0cd-110">This will be the image users see when they push a PlayPause function button the second time.</span></span>

<span data-ttu-id="0a0cd-111">Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço.</span><span class="sxs-lookup"><span data-stu-id="0a0cd-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="0a0cd-112">Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de imagem do qual você está desenhando.</span><span class="sxs-lookup"><span data-stu-id="0a0cd-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the image type you are drawing from.</span></span>

<span data-ttu-id="0a0cd-113">Por exemplo, para definir a imagem enviada por push para uma origem de imagem secundária, se a imagem estiver dentro do bitmap enviado por push, digite:</span><span class="sxs-lookup"><span data-stu-id="0a0cd-113">For example, to define the Pushed image for a secondary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 248,0

```



<span data-ttu-id="0a0cd-114">Os Estados secundários não podem ter uma imagem desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0a0cd-114">Secondary states cannot have a Disabled image.</span></span> <span data-ttu-id="0a0cd-115">As imagens secundárias devem ter a mesma largura e altura que a imagem primária.</span><span class="sxs-lookup"><span data-stu-id="0a0cd-115">Secondary images are assumed to be the same width and height as the primary image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a0cd-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a0cd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a0cd-117">**Botões**</span><span class="sxs-lookup"><span data-stu-id="0a0cd-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




