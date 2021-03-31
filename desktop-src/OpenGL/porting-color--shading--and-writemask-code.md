---
title: Transportando a cor, o sombreamento e o código Writemask
description: Transportando a cor, o sombreamento e o código Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Portabilidade do íris GL, cor
- portando do íris GL, cor
- portando para OpenGL do íris GL, cor
- Portabilidade do OpenGL do íris GL, cor
- Portabilidade do íris GL, sombreamento
- portando do íris GL, sombreamento
- portando para OpenGL do íris GL, sombreamento
- Portabilidade do OpenGL do íris GL, sombreamento
- Portabilidade do íris GL, writemask
- portando do íris GL, writemask
- portando para OpenGL do íris GL, writemask
- Portabilidade OpenGL do íris GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635224"
---
# <a name="porting-color-shading-and-writemask-code"></a><span data-ttu-id="53a70-115">Transportando a cor, o sombreamento e o código Writemask</span><span class="sxs-lookup"><span data-stu-id="53a70-115">Porting Color, Shading, and Writemask Code</span></span>

<span data-ttu-id="53a70-116">Ao portar a cor, o sombreamento e o código writemask para OpenGL, tenha em mente os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="53a70-116">When porting color, shading, and writemask code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="53a70-117">Embora você possa definir índices de mapa de cores com a função OpenGL [glIndex](glindex-functions.md) , o OpenGL não tem uma função para carregar índices de mapa de cores.</span><span class="sxs-lookup"><span data-stu-id="53a70-117">Though you can set color-map indexes with the OpenGL [glIndex](glindex-functions.md) function, OpenGL does not have a function for loading color-map indexes.</span></span>
-   <span data-ttu-id="53a70-118">Os valores de cor são normalizados para seu tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="53a70-118">Color values are normalized to their data type.</span></span> <span data-ttu-id="53a70-119">(Para obter informações sobre valores de cor, consulte [glColor](glcolor-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="53a70-119">(For information about color values, see [glColor](glcolor-functions.md)).</span></span>
-   <span data-ttu-id="53a70-120">Não há um equivalente simples para **cpack**.</span><span class="sxs-lookup"><span data-stu-id="53a70-120">There is no simple equivalent for **cpack**.</span></span>
-   <span data-ttu-id="53a70-121">Talvez seja necessário converter o código que inclui as funções **c** ou **Color** para [**glClearColor**](glclearcolor.md) ou [**glClearIndex**](glclearindex.md) em vez de **glColor** ou **glIndex**.</span><span class="sxs-lookup"><span data-stu-id="53a70-121">You may have to translate code that includes the **c** or **color** functions to [**glClearColor**](glclearcolor.md) or [**glClearIndex**](glclearindex.md) instead of **glColor** or **glIndex**.</span></span>
-   <span data-ttu-id="53a70-122">O writemask RGBA se aplica a cada componente, mas não a cada bit.</span><span class="sxs-lookup"><span data-stu-id="53a70-122">The RGBA writemask applies to each component but not for each bit.</span></span>
-   <span data-ttu-id="53a70-123">A íris GL fornece constantes de cores definidas: preto, azul, vermelho, verde, MAGENTA, ciano, amarelo e branco.</span><span class="sxs-lookup"><span data-stu-id="53a70-123">IRIS GL provides defined color constants: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW, and WHITE.</span></span> <span data-ttu-id="53a70-124">O OpenGL não fornece essas constantes.</span><span class="sxs-lookup"><span data-stu-id="53a70-124">OpenGL does not provide these constants.</span></span>

<span data-ttu-id="53a70-125">Este tópico inclui informações sobre o seguinte.</span><span class="sxs-lookup"><span data-stu-id="53a70-125">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="53a70-126">Portando chamadas de cores</span><span class="sxs-lookup"><span data-stu-id="53a70-126">Porting Color Calls</span></span>](porting-color-calls.md)
-   [<span data-ttu-id="53a70-127">Modelos de sombreamento de portador</span><span class="sxs-lookup"><span data-stu-id="53a70-127">Porting Shading Models</span></span>](porting-shading-models.md)

 

 




