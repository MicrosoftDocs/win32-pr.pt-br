---
description: Muitas vezes, os pontos especificados para vértices não correspondem exatamente aos pixels na tela. Quando isso acontece, o Direct3D aplica as regras de rasterização de triângulo para decidir quais pixels se aplicam a um determinado triângulo.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Regras de rasterização (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172398"
---
# <a name="rasterization-rules-direct3d-9"></a><span data-ttu-id="df489-104">Regras de rasterização (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="df489-104">Rasterization Rules (Direct3D 9)</span></span>

<span data-ttu-id="df489-105">Muitas vezes, os pontos especificados para vértices não correspondem exatamente aos pixels na tela.</span><span class="sxs-lookup"><span data-stu-id="df489-105">Often, the points specified for vertices do not precisely match the pixels on the screen.</span></span> <span data-ttu-id="df489-106">Quando isso acontece, o Direct3D aplica as regras de rasterização de triângulo para decidir quais pixels se aplicam a um determinado triângulo.</span><span class="sxs-lookup"><span data-stu-id="df489-106">When this happens, Direct3D applies triangle rasterization rules to decide which pixels apply to a given triangle.</span></span>

-   [<span data-ttu-id="df489-107">Regras de rasterização de triângulo</span><span class="sxs-lookup"><span data-stu-id="df489-107">Triangle Rasterization Rules</span></span>](#triangle-rasterization-rules)
-   [<span data-ttu-id="df489-108">Regras de ponto e linha</span><span class="sxs-lookup"><span data-stu-id="df489-108">Point and Line Rules</span></span>](#point-and-line-rules)
-   [<span data-ttu-id="df489-109">Regras de Sprite de ponto</span><span class="sxs-lookup"><span data-stu-id="df489-109">Point Sprite Rules</span></span>](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a><span data-ttu-id="df489-110">Regras de rasterização de triângulo</span><span class="sxs-lookup"><span data-stu-id="df489-110">Triangle Rasterization Rules</span></span>

<span data-ttu-id="df489-111">O Direct3D usa uma convenção de preenchimento superior esquerdo para preencher a geometria.</span><span class="sxs-lookup"><span data-stu-id="df489-111">Direct3D uses a top-left filling convention for filling geometry.</span></span> <span data-ttu-id="df489-112">Essa é a mesma convenção utilizada para retângulos em GDI e OpenGL.</span><span class="sxs-lookup"><span data-stu-id="df489-112">This is the same convention that is used for rectangles in GDI and OpenGL.</span></span> <span data-ttu-id="df489-113">No Direct3D, o centro do pixel é o ponto determinante.</span><span class="sxs-lookup"><span data-stu-id="df489-113">In Direct3D, the center of the pixel is the decisive point.</span></span> <span data-ttu-id="df489-114">Se o centro está dentro de um triângulo, o pixel é parte do triângulo.</span><span class="sxs-lookup"><span data-stu-id="df489-114">If the center is inside a triangle, the pixel is part of the triangle.</span></span> <span data-ttu-id="df489-115">Os centros de pixel estão localizados em coordenadas de números inteiros.</span><span class="sxs-lookup"><span data-stu-id="df489-115">Pixel centers are at integer coordinates.</span></span>

<span data-ttu-id="df489-116">Essa descrição das regras de rasterização de triângulos utilizada pelo Direct3D não se aplica necessariamente a todo o hardware disponível.</span><span class="sxs-lookup"><span data-stu-id="df489-116">This description of triangle-rasterization rules used by Direct3D does not necessarily apply to all available hardware.</span></span> <span data-ttu-id="df489-117">O teste pode revelar pequenas variações na implementação dessas regras.</span><span class="sxs-lookup"><span data-stu-id="df489-117">Your testing may uncover minor variations in the implementation of these rules.</span></span>

<span data-ttu-id="df489-118">A ilustração a seguir mostra um retângulo cujo canto superior esquerdo está em (0, 0) e o canto inferior direito em (5, 5).</span><span class="sxs-lookup"><span data-stu-id="df489-118">The following illustration shows a rectangle whose upper-left corner is at (0, 0) and whose lower-right corner is at (5, 5).</span></span> <span data-ttu-id="df489-119">Esse retângulo preenche 25 pixels, como esperado.</span><span class="sxs-lookup"><span data-stu-id="df489-119">This rectangle fills 25 pixels, just as you would expect.</span></span> <span data-ttu-id="df489-120">A largura do retângulo é definida como direita menos esquerda.</span><span class="sxs-lookup"><span data-stu-id="df489-120">The width of the rectangle is defined as right minus left.</span></span> <span data-ttu-id="df489-121">A altura é definida como parte inferior menos superior.</span><span class="sxs-lookup"><span data-stu-id="df489-121">The height is defined as bottom minus top.</span></span>

![ilustração de um quadrado numerado dividido em seis linhas e colunas](images/pixmap.png)

<span data-ttu-id="df489-123">Na convenção de preenchimento superior esquerdo, *superior* refere-se à localização vertical dos trechos horizontais e *esquerdo* refere-se à localização horizontal dos pixels em uma extensão.</span><span class="sxs-lookup"><span data-stu-id="df489-123">In the top-left filling convention, *top* refers to the vertical location of horizontal spans, and *left* refers to the horizontal location of pixels within a span.</span></span> <span data-ttu-id="df489-124">Uma borda não pode ser superior, a menos que seja horizontal.</span><span class="sxs-lookup"><span data-stu-id="df489-124">An edge cannot be a top edge unless it is horizontal.</span></span> <span data-ttu-id="df489-125">Em geral, a maioria dos triângulos tem somente as margens esquerda e direita.</span><span class="sxs-lookup"><span data-stu-id="df489-125">In general, most triangles have only left and right edges.</span></span> <span data-ttu-id="df489-126">A ilustração a seguir mostra uma borda superior e uma borda direita.</span><span class="sxs-lookup"><span data-stu-id="df489-126">The following illustration shows a top edge and a right edge.</span></span>

![ilustração de um quadrado numerado que contém dois triângulos](images/triedge.png)

<span data-ttu-id="df489-128">A convenção de preenchimento superior esquerdo determina a ação executada pelo Direct3D quando um triângulo passa pelo centro de um pixel.</span><span class="sxs-lookup"><span data-stu-id="df489-128">The top-left filling convention determines the action taken by Direct3D when a triangle passes through the center of a pixel.</span></span> <span data-ttu-id="df489-129">A ilustração a seguir mostra dois triângulos, um em (0, 0), (5, 0) e (5, 5) e o outro em (0, 5), (0, 0) e (5, 5).</span><span class="sxs-lookup"><span data-stu-id="df489-129">The following illustration shows two triangles, one at (0, 0), (5, 0), and (5, 5), and the other at (0, 5), (0, 0), and (5, 5).</span></span> <span data-ttu-id="df489-130">O primeiro triângulo nesse caso tem 15 pixels (mostrado em preto), enquanto o segundo tem apenas 10 pixels (mostrado em cinza), pois a borda compartilhada é a esquerda do primeiro triângulo.</span><span class="sxs-lookup"><span data-stu-id="df489-130">The first triangle in this case gets 15 pixels (shown in black), whereas the second gets only 10 pixels (shown in gray) because the shared edge is the left edge of the first triangle.</span></span>

![ilustração de um quadrado numerado que mostra dois triângulos](images/twotris.png)

<span data-ttu-id="df489-132">Se você definir um retângulo com o canto superior esquerdo em (0,5; 0,5) e o canto inferior direito em (2,5; 4,5), o ponto central desse retângulo é em (2,5; 1,5).</span><span class="sxs-lookup"><span data-stu-id="df489-132">If you define a rectangle with its upper-left corner at (0.5, 0.5) and its lower-right corner at (2.5, 4.5), the center point of this rectangle is at (1.5, 2.5).</span></span> <span data-ttu-id="df489-133">Quando o rasterizador Direct3D criar mosaicos com esse retângulo, o centro de cada pixel está especificamente dentro de cada um dos quatro triângulos e não requer a convenção de preenchimento superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="df489-133">When the Direct3D rasterizer tessellates this rectangle, the center of each pixel is unambiguously inside each of the four triangles, and the top-left filling convention is not needed.</span></span> <span data-ttu-id="df489-134">A ilustração a seguir mostra isso.</span><span class="sxs-lookup"><span data-stu-id="df489-134">The following illustration shows this.</span></span> <span data-ttu-id="df489-135">Os pixels do retângulo são identificados de acordo com o triângulo no qual o Direct3D os inclui.</span><span class="sxs-lookup"><span data-stu-id="df489-135">The pixels in the rectangle are labeled according to the triangle in which Direct3D includes them.</span></span>

![Mostra um quadrado numerado que contém um retângulo dividido em quatro triângulos.](images/noambig.png)

<span data-ttu-id="df489-137">Se você mover o retângulo na ilustração anterior para que o canto superior esquerdo fique em (1,0; 1,0), o canto inferior direito em (3,0; 5,0) e o centro aponte para (2,0; 3,0), o Direct3D aplica a convenção de preenchimento superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="df489-137">If you move the rectangle in the preceding illustration so that its upper-left corner is at (1.0, 1.0), its lower-right corner at (3.0, 5.0), and its center point at (2.0, 3.0), Direct3D applies the top-left filling convention.</span></span> <span data-ttu-id="df489-138">A maioria dos pixels desse retângulo amplia a fronteira entre dois ou mais triângulos, como demonstrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="df489-138">Most pixels in this rectangle straddle the border between two or more triangles, as the following illustration shows.</span></span>

![ilustração de um quadrado numerado que contém um retângulo dividido em quatro triângulos](images/fillrule.png)

<span data-ttu-id="df489-140">Para os dois retângulos, os mesmos pixels são afetados, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="df489-140">For both rectangles, the same pixels are affected, as shown in the following illustration.</span></span>

![ilustração de pixels que são afetados pelos dois quadrados numerados anteriores](images/samepix.png)

## <a name="point-and-line-rules"></a><span data-ttu-id="df489-142">Regras de ponto e linha</span><span class="sxs-lookup"><span data-stu-id="df489-142">Point and Line Rules</span></span>

<span data-ttu-id="df489-143">Os pontos são renderizados igual aos sprites de ponto, que são renderizado como quadrilaterais alinhado à tela e, portanto, seguem as mesmas regras de renderização do polígono.</span><span class="sxs-lookup"><span data-stu-id="df489-143">Points are rendered the same as point sprites, which are both rendered as screen-aligned quadrilaterals and thus adhere to the same rules as polygon rendering.</span></span>

<span data-ttu-id="df489-144">As regras de renderização de linha não as mesmas para [linhas de GDI](../gdi/lines.md).</span><span class="sxs-lookup"><span data-stu-id="df489-144">Non-antialiased line rendering rules are exactly the same as those for [GDI lines](../gdi/lines.md).</span></span>

<span data-ttu-id="df489-145">Para obter informações sobre a renderização de linha AntiAlias, consulte [**ID3DXLine**](id3dxline.md).</span><span class="sxs-lookup"><span data-stu-id="df489-145">For information about antialiased line rendering, see [**ID3DXLine**](id3dxline.md).</span></span>

## <a name="point-sprite-rules"></a><span data-ttu-id="df489-146">Regras de sprite de ponto</span><span class="sxs-lookup"><span data-stu-id="df489-146">Point Sprite Rules</span></span>

<span data-ttu-id="df489-147">Os sprites de ponto e os primitivos de patch são rasterizados como se os primitivos fossem transformados em triângulos antes e os triângulos resultante fossem rasterizados.</span><span class="sxs-lookup"><span data-stu-id="df489-147">Point sprites and patch primitives are rasterized as if the primitives were first tessellated into triangles and the resulting triangles rasterized.</span></span> <span data-ttu-id="df489-148">Para obter mais informações, consulte [Point sprites (Direct3D 9)](point-sprites.md).</span><span class="sxs-lookup"><span data-stu-id="df489-148">For more information, see [Point Sprites (Direct3D 9)](point-sprites.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df489-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="df489-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df489-150">Coordenar sistemas e geometria</span><span class="sxs-lookup"><span data-stu-id="df489-150">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
