---
description: Um script complexo é um script para o qual o membro fComplex das \_ Propriedades de script está definido como true. Este tópico detalha as propriedades que um script complexo pode ter.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Sobre scripts complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011305"
---
# <a name="about-complex-scripts"></a><span data-ttu-id="43548-104">Sobre scripts complexos</span><span class="sxs-lookup"><span data-stu-id="43548-104">About Complex Scripts</span></span>

<span data-ttu-id="43548-105">Um [script complexo](uniscribe-glossary.md) é um script para o qual  o membro FComplex [**das \_ Propriedades de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) está definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="43548-105">A [complex script](uniscribe-glossary.md) is a script for which the **fComplex** member of [**SCRIPT\_PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) is set to **TRUE**.</span></span> <span data-ttu-id="43548-106">Este tópico detalha as propriedades que um script complexo pode ter.</span><span class="sxs-lookup"><span data-stu-id="43548-106">This topic details the properties that a complex script might have.</span></span>

## <a name="bidirectional-rendering"></a><span data-ttu-id="43548-107">Renderização bidirecional</span><span class="sxs-lookup"><span data-stu-id="43548-107">Bidirectional Rendering</span></span>

<span data-ttu-id="43548-108">A renderização bidirecional é o manuseio de texto que é lido da esquerda para a direita e da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="43548-108">Bidirectional rendering is handling of text that reads both left-to-right and right-to-left.</span></span> <span data-ttu-id="43548-109">Por exemplo, na renderização bidirecional de árabe, a direção de leitura padrão para texto é da direita para a esquerda, mas é da esquerda para a direita para alguns números.</span><span class="sxs-lookup"><span data-stu-id="43548-109">For example, in the bidirectional rendering of Arabic, the default reading direction for text is right-to-left, but it is left-to-right for some numbers.</span></span> <span data-ttu-id="43548-110">O processamento de um script complexo deve considerar a diferença entre a ordem lógica (pressionamento de tecla) e a ordem visual dos glifos.</span><span class="sxs-lookup"><span data-stu-id="43548-110">Processing a complex script must account for the difference between the logical (keystroke) order and the visual order of the glyphs.</span></span> <span data-ttu-id="43548-111">Além disso, o processamento deve lidar corretamente com movimentação de cursor e teste de clique.</span><span class="sxs-lookup"><span data-stu-id="43548-111">In addition, processing must properly deal with caret movement and hit testing.</span></span> <span data-ttu-id="43548-112">O mapeamento entre a posição da tela e um índice de caracteres requer uma compreensão dos algoritmos de layout para a exibição específica, por exemplo, a seleção da exibição de texto ou de cursor.</span><span class="sxs-lookup"><span data-stu-id="43548-112">The mapping between screen position and a character index requires an understanding of the layout algorithms for the particular display, for example, selection of text or caret display.</span></span>

## <a name="contextual-shaping"></a><span data-ttu-id="43548-113">Shaping contextual</span><span class="sxs-lookup"><span data-stu-id="43548-113">Contextual Shaping</span></span>

<span data-ttu-id="43548-114">No shaping contextual, os caracteres do script alteram a forma dependendo dos caracteres que os circundam.</span><span class="sxs-lookup"><span data-stu-id="43548-114">In contextual shaping, script characters change shape depending on the characters that surround them.</span></span> <span data-ttu-id="43548-115">Tal Shaping ocorre em escrita em modo cursivo em inglês quando uma forma "l" de letras minúsculas, dependendo do caractere que a precede, como "a" (conecta-se insuficiente ao "l") ou a um "o" (conecta-se alta).</span><span class="sxs-lookup"><span data-stu-id="43548-115">Such shaping occurs in English cursive writing when a lowercase "l" changes shape depending on the character that precedes it, such as an "a" (connects low to the "l") or an "o" (connects high).</span></span> <span data-ttu-id="43548-116">Por exemplo, o árabe é um script que exibe o shaping contextual.</span><span class="sxs-lookup"><span data-stu-id="43548-116">For example, Arabic is a script that exhibits contextual shaping.</span></span>

## <a name="combining-characters"></a><span data-ttu-id="43548-117">Combinação de caracteres</span><span class="sxs-lookup"><span data-stu-id="43548-117">Combining Characters</span></span>

<span data-ttu-id="43548-118">A combinação de caracteres, também chamadas de "ligaturas", são caracteres que entram em um caractere quando colocados juntos.</span><span class="sxs-lookup"><span data-stu-id="43548-118">Combining characters, also called "ligatures," are characters that join into one character when placed together.</span></span> <span data-ttu-id="43548-119">O árabe é um script que tem muitos caracteres de combinação.</span><span class="sxs-lookup"><span data-stu-id="43548-119">Arabic is a script that has many combining characters.</span></span> <span data-ttu-id="43548-120">Um exemplo do uso de caracteres combináveis é o "a" seguido por "combinar acento grave", para o qual a representação renderizada é "à".</span><span class="sxs-lookup"><span data-stu-id="43548-120">One example of the use of combining characters is the "a" followed by "combining grave", for which the rendered representation is "à".</span></span> <span data-ttu-id="43548-121">O fluxo Unicode "U + 0061 U + 0300" requer algum processamento para garantir que a "combinação de acento grave" esteja posicionada corretamente acima de "a".</span><span class="sxs-lookup"><span data-stu-id="43548-121">The Unicode stream "U+0061 U+0300" requires some processing to make sure the "combining grave" is correctly positioned above the "a".</span></span>

## <a name="specialized-word-break-and-justification"></a><span data-ttu-id="43548-122">Quebra de palavra especializada e justificativa</span><span class="sxs-lookup"><span data-stu-id="43548-122">Specialized Word Break and Justification</span></span>

<span data-ttu-id="43548-123">Alguns scripts, por exemplo, tailandês, têm regras complexas para dividir palavras entre linhas ou justificar texto em uma linha.</span><span class="sxs-lookup"><span data-stu-id="43548-123">Some scripts, for example, Thai, have complex rules for dividing words between lines or justifying text on a line.</span></span>

## <a name="filtering-for-illegal-character-combinations"></a><span data-ttu-id="43548-124">Filtragem de combinações de caracteres ilegais</span><span class="sxs-lookup"><span data-stu-id="43548-124">Filtering for Illegal Character Combinations</span></span>

<span data-ttu-id="43548-125">Um script complexo, por exemplo, tailandês, pode filtrar combinações de caracteres ilegais quando um idioma não permite determinadas combinações de caracteres.</span><span class="sxs-lookup"><span data-stu-id="43548-125">A complex script, for example, Thai, can filter out illegal character combinations when a language does not allow certain character combinations.</span></span>

## <a name="font-fallback"></a><span data-ttu-id="43548-126">Fallback de fonte</span><span class="sxs-lookup"><span data-stu-id="43548-126">Font Fallback</span></span>

<span data-ttu-id="43548-127">Fallback de fonte é a seleção automatizada de uma fonte diferente da fonte selecionada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="43548-127">Font fallback is the automated selection of a font other than the font selected by the user.</span></span> <span data-ttu-id="43548-128">No Uniscribe, o fallback de fonte é aplicado pela função [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando todo ou parte do texto está em um script para o qual a fonte selecionada pelo usuário não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="43548-128">In Uniscribe, font fallback is applied by the [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) function when all or part of the text is in a script that the user-selected font does not support.</span></span> <span data-ttu-id="43548-129">Para obter mais informações, consulte [usando o fallback de fonte](using-font-fallback.md).</span><span class="sxs-lookup"><span data-stu-id="43548-129">For more information, see [Using Font Fallback](using-font-fallback.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43548-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43548-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43548-131">Sobre o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="43548-131">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



