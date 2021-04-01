---
title: Origem da imagem enviada por push
description: Origem da imagem enviada por push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636253"
---
# <a name="pushed-image-source"></a><span data-ttu-id="af8f1-108">Origem da imagem enviada por push</span><span class="sxs-lookup"><span data-stu-id="af8f1-108">Pushed Image Source</span></span>

<span data-ttu-id="af8f1-109">Você deve definir a origem da imagem que deseja exibir quando o usuário envia um botão.</span><span class="sxs-lookup"><span data-stu-id="af8f1-109">You must define the source of the image you want to display when the user pushes a button.</span></span> <span data-ttu-id="af8f1-110">A imagem é proveniente do arquivo definido como enviado por push na seção bitmaps.</span><span class="sxs-lookup"><span data-stu-id="af8f1-110">The image comes from the file you defined as Pushed in the Bitmaps section.</span></span> <span data-ttu-id="af8f1-111">Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço.</span><span class="sxs-lookup"><span data-stu-id="af8f1-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="af8f1-112">Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior e esquerda (em pixels) da imagem que você deseja usar dentro do arquivo de imagem enviado por push.</span><span class="sxs-lookup"><span data-stu-id="af8f1-112">You must then enter two positive integers that define the top and left coordinates (in pixels) of the image you want to use inside the Pushed image file.</span></span> <span data-ttu-id="af8f1-113">O local no qual a imagem será exibida vem das coordenadas definidas para o botão em relação à imagem de plano de fundo; Mas o local de origem é definido pelos dois números após "Push @" e é relativo à imagem enviada por push da qual você está lendo a imagem.</span><span class="sxs-lookup"><span data-stu-id="af8f1-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image; but the location it comes from is defined by the two numbers following "Pushed @" and is relative to the Pushed image you are reading the image from.</span></span>

<span data-ttu-id="af8f1-114">Por exemplo, para usar uma imagem da imagem enviada por push que está no arquivo enviado cujo local superior esquerdo é 50, 60, você usaria o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="af8f1-114">For example, to use an image from the Pushed image that is in the Pushed file whose top-left location is 50,60 you would use the following code:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="af8f1-115">Se você não quiser exibir uma imagem diferente, poderá definir o bitmap de plano de fundo como seu bitmap enviado por push.</span><span class="sxs-lookup"><span data-stu-id="af8f1-115">If you do not want to display a different image, you can define the Background bitmap as your Pushed bitmap.</span></span> <span data-ttu-id="af8f1-116">Para fazer isso, especifique o arquivo de plano de fundo como o arquivo enviado por push e especifique o deslocamento no canto superior esquerdo do botão:</span><span class="sxs-lookup"><span data-stu-id="af8f1-116">To do this, specify the Background file as your pushed file and specify the offset to the top-left corner of the button:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="af8f1-117">Se você fizer isso, nenhum dos botões poderá exibir uma imagem enviada por push.</span><span class="sxs-lookup"><span data-stu-id="af8f1-117">If you do this, none of your buttons can display a Pushed image.</span></span> <span data-ttu-id="af8f1-118">É recomendável exibir uma imagem enviada por push para todos os botões para dar ao usuário uma indicação visual, pois nem sempre fica claro se um toque produz um resultado, especialmente quando a música está sendo reproduzida ou quando o som de toque está desativado.</span><span class="sxs-lookup"><span data-stu-id="af8f1-118">We recommend that you display a Pushed image for all buttons to give your user a visual indication, because it is not always clear whether a tap produces a result, especially when music is playing or the tapping sound is turned off.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af8f1-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af8f1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af8f1-120">**Botões**</span><span class="sxs-lookup"><span data-stu-id="af8f1-120">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




