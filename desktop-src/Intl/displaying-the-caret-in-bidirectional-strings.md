---
description: No texto unidirecional, a posição do cursor não tem nenhuma ambiguidade porque a borda esquerda de um caractere está no mesmo local que a borda direita do caractere anterior.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Exibindo o cursor em cadeias bidirecionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748994"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a><span data-ttu-id="562fa-103">Exibindo o cursor em cadeias bidirecionais</span><span class="sxs-lookup"><span data-stu-id="562fa-103">Displaying the Caret in Bidirectional Strings</span></span>

<span data-ttu-id="562fa-104">No texto unidirecional, a posição do cursor não tem nenhuma ambiguidade porque a borda esquerda de um caractere está no mesmo local que a borda direita do caractere anterior.</span><span class="sxs-lookup"><span data-stu-id="562fa-104">In unidirectional text, the caret position has no ambiguity because the leading edge of a character is at the same place as the trailing edge of the previous character.</span></span> <span data-ttu-id="562fa-105">No entanto, no texto bidirecional, a posição do cursor entre as execuções de direção oposta é ambígua.</span><span class="sxs-lookup"><span data-stu-id="562fa-105">However, in bidirectional text, the caret position between runs of opposing direction is ambiguous.</span></span> <span data-ttu-id="562fa-106">Por exemplo, no parágrafo da esquerda para a direita "hellosalaam", a última letra de "Olá" precede imediatamente a primeira letra de "Salaam".</span><span class="sxs-lookup"><span data-stu-id="562fa-106">For example, in the left-to-right paragraph "hellosalaam", the last letter of "hello" immediately precedes the first letter of "salaam".</span></span> <span data-ttu-id="562fa-107">A melhor posição na qual exibir o cursor depende se é considerado seguir o "o" de "Olá" ou preceder o "s" de "Salaam".</span><span class="sxs-lookup"><span data-stu-id="562fa-107">The best position in which to display the caret depends on whether it is considered to follow the "o" of "hello" or to precede the "s" of "salaam".</span></span>

<span data-ttu-id="562fa-108">O Uniscribe usa as convenções de posicionamento do cursor mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="562fa-108">Uniscribe uses the caret positioning conventions shown in the next table.</span></span>



| <span data-ttu-id="562fa-109">Situação</span><span class="sxs-lookup"><span data-stu-id="562fa-109">Situation</span></span>       | <span data-ttu-id="562fa-110">Posicionamento do cursor Visual</span><span class="sxs-lookup"><span data-stu-id="562fa-110">Visual caret placement</span></span>                       |
|-----------------|----------------------------------------------|
| <span data-ttu-id="562fa-111">Digitação</span><span class="sxs-lookup"><span data-stu-id="562fa-111">Typing</span></span>          | <span data-ttu-id="562fa-112">Borda direita do último caractere digitado.</span><span class="sxs-lookup"><span data-stu-id="562fa-112">Trailing edge of last character typed.</span></span>       |
| <span data-ttu-id="562fa-113">Colando</span><span class="sxs-lookup"><span data-stu-id="562fa-113">Pasting</span></span>         | <span data-ttu-id="562fa-114">Borda direita do último caractere colado.</span><span class="sxs-lookup"><span data-stu-id="562fa-114">Trailing edge of last character pasted.</span></span>      |
| <span data-ttu-id="562fa-115">Avançando no cursor</span><span class="sxs-lookup"><span data-stu-id="562fa-115">Caret advancing</span></span> | <span data-ttu-id="562fa-116">Borda direita do último caractere passada.</span><span class="sxs-lookup"><span data-stu-id="562fa-116">Trailing edge of last character passed over.</span></span> |
| <span data-ttu-id="562fa-117">Desativação do cursor</span><span class="sxs-lookup"><span data-stu-id="562fa-117">Caret retiring</span></span>  | <span data-ttu-id="562fa-118">Borda esquerda do último caractere passada.</span><span class="sxs-lookup"><span data-stu-id="562fa-118">Leading edge of last character passed over.</span></span>  |
| <span data-ttu-id="562fa-119">Página Inicial</span><span class="sxs-lookup"><span data-stu-id="562fa-119">Home</span></span>            | <span data-ttu-id="562fa-120">Borda à esquerda da linha.</span><span class="sxs-lookup"><span data-stu-id="562fa-120">Leading edge of line.</span></span>                        |
| <span data-ttu-id="562fa-121">End</span><span class="sxs-lookup"><span data-stu-id="562fa-121">End</span></span>             | <span data-ttu-id="562fa-122">Borda à direita da linha.</span><span class="sxs-lookup"><span data-stu-id="562fa-122">Trailing edge of line.</span></span>                       |



 

<span data-ttu-id="562fa-123">O cursor pode ser posicionado conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="562fa-123">The caret can be positioned as shown in the following example:</span></span>


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



<span data-ttu-id="562fa-124">O posicionamento do cursor pode ser mais simples, como mostrado abaixo, dado um valor *fAdvancing* restrito a **true** ou **false**:</span><span class="sxs-lookup"><span data-stu-id="562fa-124">Positioning of the caret can be simpler, as shown below, given an *fAdvancing* value restricted to **TRUE** or **FALSE**:</span></span>


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



<span data-ttu-id="562fa-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) manipula as posições fora do intervalo logicamente.</span><span class="sxs-lookup"><span data-stu-id="562fa-125">[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) handles out-of-range positions logically.</span></span> <span data-ttu-id="562fa-126">Ele retorna a borda à esquerda da execução para *iCharPos* <0 e a borda à direita da execução de *iCharPos* >= Length.</span><span class="sxs-lookup"><span data-stu-id="562fa-126">It returns the leading edge of the run for *iCharPos* <0, and the trailing edge of the run for *iCharPos* >= length.</span></span> <span data-ttu-id="562fa-127">Para obter mais informações, consulte [Gerenciando o posicionamento do cursor e teste de clique](managing-caret-placement-and-hit-testing.md)</span><span class="sxs-lookup"><span data-stu-id="562fa-127">For more information, see [Managing Caret Placement and Hit Testing](managing-caret-placement-and-hit-testing.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="562fa-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="562fa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="562fa-129">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="562fa-129">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



