---
title: Fonte de imagem terciário normal
description: Fonte de imagem terciário normal
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364293"
---
# <a name="normal-tertiary-image-source"></a><span data-ttu-id="81dad-108">Fonte de imagem terciário normal</span><span class="sxs-lookup"><span data-stu-id="81dad-108">Normal Tertiary Image Source</span></span>

<span data-ttu-id="81dad-109">A função de botão PlayPauseStop requer que você defina o local da imagem normal para o estado terciário do botão.</span><span class="sxs-lookup"><span data-stu-id="81dad-109">The PlayPauseStop button function requires that you define the location of the normal image for the tertiary state of the button.</span></span> <span data-ttu-id="81dad-110">Essa será a imagem que os usuários veem depois de enviarem por push o botão PlayPauseStop para começar a transmitir uma transmissão ao vivo.</span><span class="sxs-lookup"><span data-stu-id="81dad-110">This will be the image users see after they have pushed the PlayPauseStop button to begin streaming a live broadcast.</span></span>

<span data-ttu-id="81dad-111">Para definir essa imagem, você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço.</span><span class="sxs-lookup"><span data-stu-id="81dad-111">To define this image, you must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="81dad-112">Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do tipo de bitmap do qual está desenhando.</span><span class="sxs-lookup"><span data-stu-id="81dad-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="81dad-113">Por exemplo, para definir a imagem normal para uma fonte de imagem terciário, se a imagem estiver dentro do bitmap enviado por push, digite:</span><span class="sxs-lookup"><span data-stu-id="81dad-113">For example, to define the normal image for a tertiary image source, if your image is inside the Pushed bitmap, type:</span></span>


```C++
Pushed @ 286,0

```



<span data-ttu-id="81dad-114">Os Estados terciários não podem ter uma imagem desabilitada.</span><span class="sxs-lookup"><span data-stu-id="81dad-114">Tertiary states cannot have a Disabled image.</span></span> <span data-ttu-id="81dad-115">São consideradas imagens terciários com a mesma largura e altura das imagens primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="81dad-115">Tertiary images are assumed to be the same width and height as the primary and secondary images.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81dad-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81dad-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81dad-117">**Botões**</span><span class="sxs-lookup"><span data-stu-id="81dad-117">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




