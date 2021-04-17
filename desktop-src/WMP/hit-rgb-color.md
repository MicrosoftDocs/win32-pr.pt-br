---
title: Pressione a cor RGB
description: Pressione a cor RGB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Aparências móveis do Windows Media Player, cores de botão
- aparências, cores de botão
- referência para capas, botões
- botões em capas, cores
- referência de cores para capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105779997"
---
# <a name="hit-rgb-color"></a><span data-ttu-id="e2304-108">Pressione a cor RGB</span><span class="sxs-lookup"><span data-stu-id="e2304-108">Hit RGB Color</span></span>

<span data-ttu-id="e2304-109">Se você estiver usando botões de região (PushHit, ToggleHit e 2PushHit), será necessário definir a cor que o Windows Media Player usará para determinar a área de pressionamento do botão.</span><span class="sxs-lookup"><span data-stu-id="e2304-109">If you are using region buttons (PushHit, ToggleHit, and 2PushHit), you must define the color that Windows Media Player will use to determine the hit area of your button.</span></span> <span data-ttu-id="e2304-110">Esse valor deve ser especificado usando três inteiros positivos separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="e2304-110">This value must be specified using three positive integers separated by commas.</span></span> <span data-ttu-id="e2304-111">Esses inteiros representam a quantidade de vermelho, verde e azul para uma cor de bitmap e variam de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="e2304-111">These integers represent the amount of red, green, and blue for a bitmap color, and range from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="e2304-112">Os tipos de botões são preteridos em capas para Windows Media Player 10 Mobile ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e2304-112">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="e2304-113">Você pode usar quaisquer cores para os valores, mas certifique-se de que cada botão de região definido tem uma cor exclusiva no arquivo de imagem de região e que o valor de cor definido aqui como um número corresponde à cor real usada na imagem da região.</span><span class="sxs-lookup"><span data-stu-id="e2304-113">You can use any colors for the values, but be sure that each region button you define has a unique color in the Region image file and that the color value you define here as a number matches the actual color used in the Region image.</span></span>

<span data-ttu-id="e2304-114">A tabela a seguir mostra algumas cores típicas que talvez você queira usar.</span><span class="sxs-lookup"><span data-stu-id="e2304-114">The following table shows some typical colors you might want to use.</span></span>



| <span data-ttu-id="e2304-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e2304-115">Value</span></span>       | <span data-ttu-id="e2304-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2304-116">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="e2304-117">0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="e2304-117">0,0,0</span></span>       | <span data-ttu-id="e2304-118">Preto</span><span class="sxs-lookup"><span data-stu-id="e2304-118">Black</span></span>       |
| <span data-ttu-id="e2304-119">255.255.255</span><span class="sxs-lookup"><span data-stu-id="e2304-119">255,255,255</span></span> | <span data-ttu-id="e2304-120">Branca</span><span class="sxs-lookup"><span data-stu-id="e2304-120">White</span></span>       |
| <span data-ttu-id="e2304-121">255, 0, 0</span><span class="sxs-lookup"><span data-stu-id="e2304-121">255,0,0</span></span>     | <span data-ttu-id="e2304-122">Vermelho</span><span class="sxs-lookup"><span data-stu-id="e2304-122">Red</span></span>         |
| <span data-ttu-id="e2304-123">0255, 0</span><span class="sxs-lookup"><span data-stu-id="e2304-123">0,255,0</span></span>     | <span data-ttu-id="e2304-124">Verde</span><span class="sxs-lookup"><span data-stu-id="e2304-124">Green</span></span>       |
| <span data-ttu-id="e2304-125">0, 0255</span><span class="sxs-lookup"><span data-stu-id="e2304-125">0,0,255</span></span>     | <span data-ttu-id="e2304-126">Azul</span><span class="sxs-lookup"><span data-stu-id="e2304-126">Blue</span></span>        |



 

<span data-ttu-id="e2304-127">Se você não usar botões de região, deverá inserir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e2304-127">If you do not use region buttons, you must enter the following:</span></span>


```C++
0,0,0

```



## <a name="related-topics"></a><span data-ttu-id="e2304-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2304-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2304-129">**Botões**</span><span class="sxs-lookup"><span data-stu-id="e2304-129">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




