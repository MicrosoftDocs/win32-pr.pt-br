---
title: Arquivos de região
description: Arquivos de região
ms.assetid: 20952eb9-4cd1-4d7d-b5cc-f1741977745f
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos de região
- Capas móveis do Windows Media Player, arquivos de região
- capas, arquivos de região
- Arquivos de região em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d258afeab029df7218d3616b8aecdb62c72806
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292717"
---
# <a name="region-files"></a><span data-ttu-id="b9bd6-110">Arquivos de região</span><span class="sxs-lookup"><span data-stu-id="b9bd6-110">Region Files</span></span>

<span data-ttu-id="b9bd6-111">Os arquivos de região serão necessários se você usar qualquer tipo de botão de pressionamento (2PushHit, PushHit ou ToggleHit).</span><span class="sxs-lookup"><span data-stu-id="b9bd6-111">Region files are required if you use any type of hit button (2PushHit, PushHit, or ToggleHit).</span></span>

<span data-ttu-id="b9bd6-112">Os arquivos de região são usados para definir áreas que responderão a um toque, também conhecido como um pressionamento, em um botão específico.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-112">Region files are used to define areas that will respond to a tap, also known as a hit, on a specific button.</span></span> <span data-ttu-id="b9bd6-113">Para cada botão de clique, uma área no bitmap de região recebe uma cor da Web específica (como \# FF0000, que é o valor para vermelho sólido).</span><span class="sxs-lookup"><span data-stu-id="b9bd6-113">For each hit button, an area in the Region bitmap is given a specific Web color (such as \#FF0000, which is the value for solid red).</span></span> <span data-ttu-id="b9bd6-114">O número de cor é especificado na definição do botão de região.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-114">The color number is specified in the region button definition.</span></span> <span data-ttu-id="b9bd6-115">Quando o usuário exibe a capa, a imagem do botão é sobreposta em segundo plano usando as coordenadas da área no bitmap da região.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-115">When the user displays the skin, the button image is superimposed onto the background using the coordinates of the area in the Region bitmap.</span></span>

<span data-ttu-id="b9bd6-116">Por exemplo, você pode desenhar um círculo vermelho em um local correspondente ao local do botão Next e colorir o vermelho sólido ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="b9bd6-116">For example, you could draw a red circle in a location corresponding to the location of the Next button and color it solid red (\#FF0000).</span></span> <span data-ttu-id="b9bd6-117">Em seguida, na definição do botão, você pode atribuir um valor RGB de pressionamento de 255, 0, 0 (que é o equivalente RGB de \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="b9bd6-117">Then in the button definition, you could assign a hit RGB value of 255,0,0 (which is the RGB equivalent of \#FF0000).</span></span> <span data-ttu-id="b9bd6-118">Nesse caso, o botão Avançar só responderia a toques (ocorrências) dentro do círculo vermelho.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-118">In this case, the Next button would only respond to taps (hits) inside the red circle.</span></span>

<span data-ttu-id="b9bd6-119">Os botões de pressionamento são usados quando você deseja definir formas que não sejam retângulos.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-119">Hit buttons are used when you want to define shapes other than rectangles.</span></span> <span data-ttu-id="b9bd6-120">Você ainda deve definir as coordenadas para cada botão para que imagens secundárias, como push e Disabled, possam estar localizadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-120">You must still define the coordinates for each button so that secondary images such as Pushed and Disabled can be located correctly.</span></span> <span data-ttu-id="b9bd6-121">Na prática, cada botão é limitado por um retângulo, e esses retângulos de limite imaginários não devem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-121">In practice, each button is bounded by a rectangle, and these imaginary boundary rectangles must not overlap.</span></span>

> [!Note]  
> <span data-ttu-id="b9bd6-122">Os arquivos de arte de região não são necessários nas capas móveis do Windows Media Player 10 porque os tipos de botão não têm suporte no Windows Media Player 10 Mobile ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-122">Region art files are not needed in Windows Media Player 10 Mobile skins because button types are not supported in Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="b9bd6-123">A imagem a seguir é um arquivo de região típico.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-123">The following image is a typical Region file.</span></span>

![arquivo de região](images/cesdkreg.png)

<span data-ttu-id="b9bd6-125">Esse arquivo define as partes da capa para cada botão de tipo de clique.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-125">This file defines the parts of the skin for each hit-type button.</span></span> <span data-ttu-id="b9bd6-126">Cada cor será identificada por seu número de cor na seção botões do arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="b9bd6-126">Each color will be identified by its color number in the Buttons section of the skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9bd6-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9bd6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9bd6-128">**Arquivos de arte**</span><span class="sxs-lookup"><span data-stu-id="b9bd6-128">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




