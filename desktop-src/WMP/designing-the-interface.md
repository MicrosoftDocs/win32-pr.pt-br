---
title: Criando a interface
description: Criando a interface
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Capas móveis do Windows Media Player, interfaces do usuário
- capas, interfaces do usuário
- Criando capas, interfaces do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084109"
---
# <a name="designing-the-interface"></a><span data-ttu-id="3306f-106">Criando a interface</span><span class="sxs-lookup"><span data-stu-id="3306f-106">Designing the Interface</span></span>

<span data-ttu-id="3306f-107">Depois que as funções forem escolhidas, a interface poderá ser projetada.</span><span class="sxs-lookup"><span data-stu-id="3306f-107">Once the functions have been chosen, the interface can be designed.</span></span> <span data-ttu-id="3306f-108">Uma interface simples foi escolhida para corresponder à funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="3306f-108">A simple interface was chosen to match the functionality.</span></span> <span data-ttu-id="3306f-109">Os símbolos para os controles foram escolhidos dos controles VCR padrão.</span><span class="sxs-lookup"><span data-stu-id="3306f-109">Symbols for the controls were chosen from standard VCR controls.</span></span>

<span data-ttu-id="3306f-110">A imagem a seguir mostra como será a aparência da interface.</span><span class="sxs-lookup"><span data-stu-id="3306f-110">The following image shows what the interface will look like.</span></span>

![interface de exemplo](images/ceswmful.png)

-   <span data-ttu-id="3306f-112">**Botão PlayPause ou PlayPauseStop.**</span><span class="sxs-lookup"><span data-stu-id="3306f-112">**PlayPause or PlayPauseStop button.**</span></span> <span data-ttu-id="3306f-113">O usuário ficará mais tocando, então você pode considerar um botão maior.</span><span class="sxs-lookup"><span data-stu-id="3306f-113">The user will be tapping this the most, so you might consider a larger button.</span></span> <span data-ttu-id="3306f-114">O canto superior direito faz um bom local que o usuário pode encontrar rapidamente.</span><span class="sxs-lookup"><span data-stu-id="3306f-114">The upper-right corner makes a good location that the user can find quickly.</span></span> <span data-ttu-id="3306f-115">Uma seta sólida é usada para indicar que a reprodução e duas barras verticais (não mostradas aqui) serão usadas para indicar pausa.</span><span class="sxs-lookup"><span data-stu-id="3306f-115">A solid arrow is used to indicate play and two vertical bars (not shown here) will be used to indicate pause.</span></span>
    > [!Note]  
    > <span data-ttu-id="3306f-116">O botão PlayPauseStop só pode ser usado ao criar uma capa para o Windows Media Player 10 Mobile ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3306f-116">The PlayPauseStop button can only be used when creating a skin for Windows Media Player 10 Mobile or later.</span></span>

     

-   <span data-ttu-id="3306f-117">**Botão parar.**</span><span class="sxs-lookup"><span data-stu-id="3306f-117">**Stop button.**</span></span> <span data-ttu-id="3306f-118">Para facilitar a localização, ele é colocado no canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="3306f-118">To make this easy to find, it is placed at the upper-left corner.</span></span> <span data-ttu-id="3306f-119">Um quadrado é usado para indicar a parada.</span><span class="sxs-lookup"><span data-stu-id="3306f-119">A square is used to indicate stop.</span></span> <span data-ttu-id="3306f-120">Se você estiver criando uma capa para o Windows Media Player 10 Mobile ou posterior, o botão PlayPauseStop já fornecerá essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="3306f-120">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop button already provides this functionality.</span></span>
-   <span data-ttu-id="3306f-121">**Botões próximo e anterior.**</span><span class="sxs-lookup"><span data-stu-id="3306f-121">**Next and Prev buttons.**</span></span> <span data-ttu-id="3306f-122">Como eles não serão usados com frequência, eles são colocados à esquerda.</span><span class="sxs-lookup"><span data-stu-id="3306f-122">Since these will not be used as often, they are placed on the left.</span></span> <span data-ttu-id="3306f-123">A seguir está acima do botão anterior, pois as pessoas provavelmente desejarão avançar em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3306f-123">The Next is above the Prev button because people will more likely want to move forward in a playlist.</span></span> <span data-ttu-id="3306f-124">Os símbolos de seta dupla são usados porque são semelhantes na função a um controle de avanço rápido.</span><span class="sxs-lookup"><span data-stu-id="3306f-124">The double-arrow symbols are used because they are similar in function to a fast-forward control.</span></span>
-   <span data-ttu-id="3306f-125">**Volume TrackBar.**</span><span class="sxs-lookup"><span data-stu-id="3306f-125">**Volume trackbar.**</span></span> <span data-ttu-id="3306f-126">Isso é colocado na parte inferior da tela e é uma linha simples com um botão de polegar sobre ela.</span><span class="sxs-lookup"><span data-stu-id="3306f-126">This is placed at the bottom of the screen and is a simple line with a thumb button on top of it.</span></span>
-   <span data-ttu-id="3306f-127">**Caixa de texto do letreiro.**</span><span class="sxs-lookup"><span data-stu-id="3306f-127">**Marquee text box.**</span></span> <span data-ttu-id="3306f-128">Isso é colocado sob o botão PlayPause ou PlayPauseStop para que seja fácil de ver.</span><span class="sxs-lookup"><span data-stu-id="3306f-128">This is placed under the PlayPause or PlayPauseStop button so that it is easy to see.</span></span>

<span data-ttu-id="3306f-129">Você pode querer esboçar isso primeiro e experimentar o posicionamento de cada elemento da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3306f-129">You may want to sketch this first and experiment with the placement of each user interface element.</span></span> <span data-ttu-id="3306f-130">O design mostrado aqui foi escolhido para simplificar e facilitar o uso.</span><span class="sxs-lookup"><span data-stu-id="3306f-130">The design shown here was chosen for simplicity and ease of use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3306f-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3306f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3306f-132">**Guia de aparência**</span><span class="sxs-lookup"><span data-stu-id="3306f-132">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




