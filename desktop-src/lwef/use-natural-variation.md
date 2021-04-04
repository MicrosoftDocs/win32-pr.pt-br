---
title: Usar variação natural
description: Usar variação natural
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084043"
---
# <a name="use-natural-variation"></a><span data-ttu-id="c17c1-103">Usar variação natural</span><span class="sxs-lookup"><span data-stu-id="c17c1-103">Use Natural Variation</span></span>

<span data-ttu-id="c17c1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c17c1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c17c1-105">Embora a consistência da apresentação na interface convencional de seu aplicativo, como menus e caixas de diálogo, torne a interface mais previsível, varie a animação e a saída falada na interface do caractere.</span><span class="sxs-lookup"><span data-stu-id="c17c1-105">While consistency of presentation in your application's conventional interface, such as menus and dialog boxes, makes the interface more predictable, vary the animation and spoken output in the character's interface.</span></span> <span data-ttu-id="c17c1-106">Adequadamente, a variação das respostas do caractere fornece uma interface mais natural.</span><span class="sxs-lookup"><span data-stu-id="c17c1-106">Appropriately varying the character's responses provides a more natural interface.</span></span> <span data-ttu-id="c17c1-107">Se um caractere sempre endereçar o usuário exatamente da mesma forma; por exemplo, sempre dizendo as mesmas palavras, é provável que o usuário considere o caractere enfadonho, disinterested ou até mesmo rude.</span><span class="sxs-lookup"><span data-stu-id="c17c1-107">If a character always addresses the user exactly the same way; for example, always saying the same words, the user is likely to consider the character boring, disinterested, or even rude.</span></span> <span data-ttu-id="c17c1-108">A comunicação humana raramente envolve a repetição precisa.</span><span class="sxs-lookup"><span data-stu-id="c17c1-108">Human communication rarely involves precise repetition.</span></span> <span data-ttu-id="c17c1-109">Mesmo ao repetir algo em uma situação semelhante, podemos alterar o texto, os gestos ou a expressão facial.</span><span class="sxs-lookup"><span data-stu-id="c17c1-109">Even when repeating something in a similar situation, we may change wording, gestures, or facial expression.</span></span>

<span data-ttu-id="c17c1-110">O Microsoft Agent permite que você crie em alguma variação um caractere.</span><span class="sxs-lookup"><span data-stu-id="c17c1-110">Microsoft Agent enables you to build in some variation for a character.</span></span> <span data-ttu-id="c17c1-111">Ao definir as animações de um caractere, você pode usar probabilidades de ramificação em qualquer quadro de animação para alterar uma animação quando ela for reproduzida.</span><span class="sxs-lookup"><span data-stu-id="c17c1-111">When defining a character's animations, you can use branching probabilities on any animation frame to change an animation when it plays.</span></span> <span data-ttu-id="c17c1-112">Você também pode atribuir várias animações a cada Estado.</span><span class="sxs-lookup"><span data-stu-id="c17c1-112">You can also assign multiple animations to each state.</span></span> <span data-ttu-id="c17c1-113">O Microsoft Agent escolhe aleatoriamente uma das animações atribuídas cada vez que inicia um estado.</span><span class="sxs-lookup"><span data-stu-id="c17c1-113">Microsoft Agent randomly chooses one of the assigned animations each time it initiates a state.</span></span> <span data-ttu-id="c17c1-114">Para saída de fala, você também pode incluir caracteres de barra vertical no texto de saída para variar automaticamente o texto falado.</span><span class="sxs-lookup"><span data-stu-id="c17c1-114">For speech output, you can also include vertical bar characters in your output text to automatically vary the text spoken.</span></span> <span data-ttu-id="c17c1-115">Por exemplo, o Microsoft Agent selecionará aleatoriamente uma das seguintes instruções ao processar este texto como parte do método [**Speak**](speak-method.md) :</span><span class="sxs-lookup"><span data-stu-id="c17c1-115">For example, Microsoft Agent will randomly select one of the following statements when processing this text as part of the [**Speak**](speak-method.md) method:</span></span>

<span data-ttu-id="c17c1-116">"Eu posso dizer isso. \| Posso dizer isso. \| Posso dizer algo mais. "</span><span class="sxs-lookup"><span data-stu-id="c17c1-116">"I can say this.\|I can say that.\|I can say something else."</span></span>

 

 




