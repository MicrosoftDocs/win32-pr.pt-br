---
title: Origem da imagem para o botão desabilitado
description: Origem da imagem para o botão desabilitado
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Aparências móveis do Windows Media Player, origem da imagem do botão
- aparência, origem da imagem do botão
- referência para capas, botões
- botões em capas, origem da imagem
- origem da imagem para capas, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364025"
---
# <a name="image-source-for-disabled-button"></a><span data-ttu-id="84f58-108">Origem da imagem para o botão desabilitado</span><span class="sxs-lookup"><span data-stu-id="84f58-108">Image Source for Disabled Button</span></span>

<span data-ttu-id="84f58-109">Você deve definir a origem da imagem que deseja exibir quando um botão é desabilitado ou tem um estado que corresponde a desativado.</span><span class="sxs-lookup"><span data-stu-id="84f58-109">You must define the source of the image you want to display when a button is disabled or has a state that corresponds to off.</span></span> <span data-ttu-id="84f58-110">A imagem é proveniente do arquivo definido como desabilitado na seção bitmaps.</span><span class="sxs-lookup"><span data-stu-id="84f58-110">The image comes from the file you defined as Disabled in the Bitmaps section.</span></span> <span data-ttu-id="84f58-111">Você deve inserir o tipo de imagem seguido por um espaço e o símbolo @ e outro espaço.</span><span class="sxs-lookup"><span data-stu-id="84f58-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="84f58-112">Em seguida, você deve inserir dois inteiros positivos que definem as coordenadas superior esquerda (em pixels) da imagem que você deseja usar dentro do arquivo de bitmap.</span><span class="sxs-lookup"><span data-stu-id="84f58-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap file.</span></span> <span data-ttu-id="84f58-113">O local no qual a imagem será exibida vem das coordenadas definidas para o botão em relação à imagem de plano de fundo, mas o local de origem é definido pelos dois números após "Disabled @" e é relativo ao bitmap desabilitado do qual você está lendo a imagem.</span><span class="sxs-lookup"><span data-stu-id="84f58-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image, but the location it comes from is defined by the two numbers following "Disabled @" and is relative to the Disabled bitmap you are reading the image from.</span></span>

<span data-ttu-id="84f58-114">Por exemplo, para usar uma imagem do bitmap desabilitado que está no arquivo desabilitado em um local superior e esquerdo de 50, 60 pixels, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="84f58-114">For example, to use an image from the Disabled bitmap that is in the Disabled file at a top and left location of 50,60 pixels, use the following code:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="84f58-115">Você deve definir um bitmap desabilitado.</span><span class="sxs-lookup"><span data-stu-id="84f58-115">You must define a Disabled bitmap.</span></span> <span data-ttu-id="84f58-116">Se você não quiser exibir uma imagem diferente, poderá definir o bitmap de plano de fundo como seu bitmap desabilitado com um deslocamento de 0, 0:</span><span class="sxs-lookup"><span data-stu-id="84f58-116">If you do not want to display a different image, you can define the Background bitmap as your Disabled bitmap with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="84f58-117">No exemplo anterior, 50, 60 é o local do botão com o qual você está trabalhando no arquivo desabilitado (nesse caso, o mesmo local que o botão no bitmap em segundo plano).</span><span class="sxs-lookup"><span data-stu-id="84f58-117">In the preceding example, 50,60 is the location of the button you are working with in the Disabled file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="84f58-118">No entanto, é altamente recomendável que você exiba uma imagem desabilitada para todos os botões para dar a seus usuários uma indicação visual, pois muitos botões não serão utilizáveis em determinadas condições, como uma lista de reprodução vazia.</span><span class="sxs-lookup"><span data-stu-id="84f58-118">However, it is highly recommended that you display a Disabled image for all buttons to give your users a visual indication, because many buttons will not be useable under certain conditions, such as an empty playlist.</span></span> <span data-ttu-id="84f58-119">Se os usuários souberem que um botão está desabilitado, eles não continuarão tentando clicar nele ou acreditar que sua capa não está funcionando como projetado.</span><span class="sxs-lookup"><span data-stu-id="84f58-119">If users know a button is disabled, they will not keep trying to click on it or think your skin is not functioning as designed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84f58-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84f58-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84f58-121">**Botões**</span><span class="sxs-lookup"><span data-stu-id="84f58-121">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




