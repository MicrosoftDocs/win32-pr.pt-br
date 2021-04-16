---
description: Direção da transição
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Direção da transição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559830"
---
# <a name="transition-direction"></a><span data-ttu-id="9ce2a-103">Direção da transição</span><span class="sxs-lookup"><span data-stu-id="9ce2a-103">Transition Direction</span></span>

<span data-ttu-id="9ce2a-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9ce2a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9ce2a-105">Uma transição vai de entrada A para entrada B e de hora t ₀ para t ₁.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-105">A transition goes from input A to input B, and from time t₀ to t₁.</span></span> <span data-ttu-id="9ce2a-106">Portanto, a *direção* de uma transição pode significar uma destas duas coisas:</span><span class="sxs-lookup"><span data-stu-id="9ce2a-106">Therefore, the *direction* of a transition can mean one of two things:</span></span>

-   <span data-ttu-id="9ce2a-107">O mapeamento de camadas da linha do tempo para entradas.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-107">The mapping of timeline layers to inputs.</span></span>
-   <span data-ttu-id="9ce2a-108">A progressão ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-108">The progression over time.</span></span>

<span data-ttu-id="9ce2a-109">A primeira é a *direção de entrada* e a segunda é a *direção do progresso*.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-109">The first is the *input direction*, and the second is the *progress direction*.</span></span> <span data-ttu-id="9ce2a-110">Você pode controlar ambas as direções.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-110">You can control both directions.</span></span>

-   <span data-ttu-id="9ce2a-111">Direção de entrada: por padrão, uma transição vai da composição das camadas de prioridade inferior para a camada que contém a transição.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-111">Input direction: By default, a transition goes from the composite of the lower-priority layers to the layer that contains the transition.</span></span> <span data-ttu-id="9ce2a-112">Para inverter essa direção, chame o método [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .</span><span class="sxs-lookup"><span data-stu-id="9ce2a-112">To reverse this direction, call the [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md) method.</span></span>
-   <span data-ttu-id="9ce2a-113">Direção do progresso: a maioria das transições dá suporte a uma propriedade de **progresso** padrão, que especifica qual porcentagem da transição é refletida na saída em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-113">Progress direction: Most transitions support a standard **Progress** property, which specifies what percentage of the transition is reflected in the output at a given moment.</span></span> <span data-ttu-id="9ce2a-114">Por padrão, o valor da propriedade **Progress** passa de 0,0 para 1,0 ao longo da duração da transição.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-114">By default, the value of the **Progress** property goes from 0.0 to 1.0 over the duration of the transition.</span></span> <span data-ttu-id="9ce2a-115">Para inverter o progresso, defina a propriedade **Progress** para ir de 1,0 para 0,0.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-115">To reverse the progress, set the **Progress** property to go from 1.0 to 0.0.</span></span>

<span data-ttu-id="9ce2a-116">O diagrama a seguir ilustra a diferença entre a direção de entrada e a direção do progresso.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-116">The following diagram illustrates the difference between input direction and progress direction.</span></span> <span data-ttu-id="9ce2a-117">Ele mostra quatro variações em uma transição de [apagamento SMPTE](smpte-wipe-transition.md) padrão.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-117">It shows four variations on a standard [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

![instruções de apagamento](images/wipedirections.png)

<span data-ttu-id="9ce2a-119">A transição reside no Track 1.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-119">The transition resides on track 1.</span></span> <span data-ttu-id="9ce2a-120">Por padrão, o apagamento vai da esquerda para a direita e do Track 0 para o Track 1.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-120">By default, the wipe goes from left to right and from track 0 to track 1.</span></span> <span data-ttu-id="9ce2a-121">A troca de entradas faz com que o apagamento continue do Track 1 para acompanhar 0, mas ainda da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-121">Swapping inputs causes the wipe to go from track 1 to track 0, but still from left to right.</span></span> <span data-ttu-id="9ce2a-122">A reversão do progresso faz a transição passar da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-122">Reversing the progress makes the transition go from right to left.</span></span> <span data-ttu-id="9ce2a-123">Você pode combinar ambos, conforme mostrado na extrema esquerda.</span><span class="sxs-lookup"><span data-stu-id="9ce2a-123">You can combine both, as shown on the far left.</span></span>

<span data-ttu-id="9ce2a-124">Para obter mais informações sobre como o DES renderiza as transições, consulte [o modelo de linha do tempo](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="9ce2a-124">For more information about how DES renders transitions, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ce2a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ce2a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ce2a-126">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="9ce2a-126">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



