---
description: Transições
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837011"
---
# <a name="transitions"></a><span data-ttu-id="3ad34-103">Transições</span><span class="sxs-lookup"><span data-stu-id="3ad34-103">Transitions</span></span>

<span data-ttu-id="3ad34-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="3ad34-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3ad34-105">Uma transição é uma maneira de transiçãor de uma faixa de vídeo para outra, usando um efeito visual, como um esmaecimento ou um apagamento.</span><span class="sxs-lookup"><span data-stu-id="3ad34-105">A transition is a way to segue from one video track to another, using a visual effect such as a fade or a wipe.</span></span> <span data-ttu-id="3ad34-106">A ilustração a seguir mostra uma linha do tempo com uma transição:</span><span class="sxs-lookup"><span data-stu-id="3ad34-106">The following illustration shows a timeline with a transition:</span></span>

![linha do tempo com transição](images/timeline3.png)

<span data-ttu-id="3ad34-108">O objeto de transição está no Track 1 e representa uma transição do Track 0 para o Track 1.</span><span class="sxs-lookup"><span data-stu-id="3ad34-108">The transition object is on track 1, and it represents a transition from track 0 to track 1.</span></span> <span data-ttu-id="3ad34-109">No início da transição, o vídeo renderizado é inteiramente do Track 0 (origem A).</span><span class="sxs-lookup"><span data-stu-id="3ad34-109">At the start of the transition, the rendered video is entirely from Track 0 (source A).</span></span> <span data-ttu-id="3ad34-110">No final, o vídeo é totalmente do Track 1 (fonte C).</span><span class="sxs-lookup"><span data-stu-id="3ad34-110">At the end, the video is entirely from Track 1 (source C).</span></span> <span data-ttu-id="3ad34-111">No between, a saída faz a transição da origem A para a fonte C. Por exemplo, em uma transição de esmaecimento, uma fonte desaparece progressivamente para a outra.</span><span class="sxs-lookup"><span data-stu-id="3ad34-111">In between, the output transitions from source A to source C. For example, in a fade transition, one source progressively fades to the other.</span></span> <span data-ttu-id="3ad34-112">A saída final é esquematizados ao longo da parte inferior da ilustração.</span><span class="sxs-lookup"><span data-stu-id="3ad34-112">The final output is schematized along the bottom of the illustration.</span></span>

<span data-ttu-id="3ad34-113">As transições não podem se sobrepor no tempo dentro da mesma faixa, mas você pode criar transições sobrepostas usando o objeto de composição, conforme descrito em [composição e camadas](composition-and-layering.md).</span><span class="sxs-lookup"><span data-stu-id="3ad34-113">Transitions cannot overlap in time within the same track, but you can create overlapping transitions by using the composition object, as described in [Composition and Layering](composition-and-layering.md).</span></span>

<span data-ttu-id="3ad34-114">Uma transição tem uma direção.</span><span class="sxs-lookup"><span data-stu-id="3ad34-114">A transition has a direction.</span></span> <span data-ttu-id="3ad34-115">Por padrão, ele começa da faixa de prioridade mais baixa (origem A, no exemplo anterior) e termina na faixa de prioridade mais alta (fonte C).</span><span class="sxs-lookup"><span data-stu-id="3ad34-115">By default, it starts from the lower priority track (source A, in the previous example.) and ends at the higher-priority track (source C).</span></span> <span data-ttu-id="3ad34-116">No, o vídeo é uma mistura das duas fontes.</span><span class="sxs-lookup"><span data-stu-id="3ad34-116">In between, the video is a mixture of the two sources.</span></span> <span data-ttu-id="3ad34-117">No entanto, você pode especificar o comportamento oposto, conforme mostrado na ilustração a seguir:</span><span class="sxs-lookup"><span data-stu-id="3ad34-117">However, you can specify the opposite behavior, as shown in the following illustration:</span></span>

![ntrack com duas transições](images/fade.png)

<span data-ttu-id="3ad34-119">Aqui, a primeira transição esmaece de Track 0 esmaece Track 1, que é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="3ad34-119">Here, the first transition fades from track 0 fades track 1, which is the default behavior.</span></span> <span data-ttu-id="3ad34-120">A segunda transição esmaece do Track 1 de volta para o Track 0.</span><span class="sxs-lookup"><span data-stu-id="3ad34-120">The second transition fades from track 1 back to Track 0.</span></span> <span data-ttu-id="3ad34-121">Observe que ambas as transições estão localizadas no Track 1.</span><span class="sxs-lookup"><span data-stu-id="3ad34-121">Note that both transitions are located on track 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ad34-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ad34-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad34-123">Introdução com os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3ad34-123">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="3ad34-124">Transições e efeitos</span><span class="sxs-lookup"><span data-stu-id="3ad34-124">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> <dt>

[<span data-ttu-id="3ad34-125">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="3ad34-125">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



