---
description: Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Estêncil de Two-Sided (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105798524"
---
# <a name="two-sided-stencil-direct3d-9"></a><span data-ttu-id="d9835-103">Estêncil de Two-Sided (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d9835-103">Two-Sided Stencil (Direct3D 9)</span></span>

<span data-ttu-id="d9835-104">Os volumes de sombra são usados para desenhar sombras com o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="d9835-104">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="d9835-105">O app calcula os volumes de sombra convertidos sobrepondo a geometria, calculando as bordas da silhueta e afastando-as da luz em um conjunto de volumes 3D.</span><span class="sxs-lookup"><span data-stu-id="d9835-105">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="d9835-106">Em seguida, esses volumes são renderizados duas vezes no buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="d9835-106">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="d9835-107">A primeira renderização desenha polígonos voltados para frente e aumenta os valores de buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="d9835-107">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="d9835-108">A segunda renderização desenha polígonos voltados para trás do volume de sombra e diminui os valores de buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="d9835-108">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="d9835-109">Normalmente, todos os valores incrementados e decrementados cancelam um ao outro. No entanto, a cena já foi renderizada com geometria normal, fazendo com que alguns pixels falhem no teste de buffer z, conforme o volume de sombra é renderizado.</span><span class="sxs-lookup"><span data-stu-id="d9835-109">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="d9835-110">Os valores restantes no buffer de estêncil correspondem aos pixels que estão na sombra.</span><span class="sxs-lookup"><span data-stu-id="d9835-110">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="d9835-111">Esse conteúdo restante do buffer de estêncil é usado como uma máscara, para fazer a combinação alfa de um quadrupleto preto grande e abrangente na cena.</span><span class="sxs-lookup"><span data-stu-id="d9835-111">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="d9835-112">Com o buffer de estêncil atuando como uma máscara, o resultado será o escurecimento dos pixels que estão nas sombras.</span><span class="sxs-lookup"><span data-stu-id="d9835-112">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="d9835-113">Isso significa que a geometria de sombra é desenhada duas vezes por fonte de luz, exercendo assim pressão sobre a taxa de transferência de vértice da GPU.</span><span class="sxs-lookup"><span data-stu-id="d9835-113">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="d9835-114">O recurso de estêncil de dois lados foi projetado para atenuar essa situação.</span><span class="sxs-lookup"><span data-stu-id="d9835-114">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="d9835-115">Nesta abordagem, existem dois conjuntos de estado de estêncil (nomeados abaixo), um conjunto para os triângulos voltados para a frente e outro para os triângulos voltados para trás.</span><span class="sxs-lookup"><span data-stu-id="d9835-115">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="d9835-116">Dessa forma, somente uma única passagem é desenhada por volume de sombra, por luz.</span><span class="sxs-lookup"><span data-stu-id="d9835-116">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="d9835-117">As alterações de API são restritas a um novo conjunto de Estados de renderização.</span><span class="sxs-lookup"><span data-stu-id="d9835-117">The API changes are restricted to a new set of render states.</span></span> <span data-ttu-id="d9835-118">O novo estado de renderização D3DRS \_ dois \_ estênceis do lado \_ pode ser definido como **verdadeiro** ou **falso**.</span><span class="sxs-lookup"><span data-stu-id="d9835-118">The new render state D3DRS\_Two\_Sided\_StencilMODE can be set to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="d9835-119">Ele é **false** por padrão, o que significa o comportamento atual (DirectX 8).</span><span class="sxs-lookup"><span data-stu-id="d9835-119">It is **FALSE** by default, meaning current (DirectX 8) behavior.</span></span> <span data-ttu-id="d9835-120">Quando definido como **true** (funcionará somente se D3DSTENCILCAPS \_ TWOSIDED for definido), os seguintes Estados de renderização serão aplicados somente aos triângulos (no sentido horário) da frente.</span><span class="sxs-lookup"><span data-stu-id="d9835-120">When this is set to **TRUE** (it will work only if D3DSTENCILCAPS\_TWOSIDED is set), the following render states will apply only to the front-facing (clockwise) triangles.</span></span>



| <span data-ttu-id="d9835-121">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="d9835-121">Render state</span></span>        | <span data-ttu-id="d9835-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9835-122">Description</span></span>                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9835-123">D3DRS \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="d9835-123">D3DRS\_STENCILFAIL</span></span>  | <span data-ttu-id="d9835-124">D3DSTENCILOP para fazer se o teste de estêncil falhar.</span><span class="sxs-lookup"><span data-stu-id="d9835-124">D3DSTENCILOP to do if stencil test fails.</span></span>                                                |
| <span data-ttu-id="d9835-125">D3DRS \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="d9835-125">D3DRS\_STENCILZFAIL</span></span> | <span data-ttu-id="d9835-126">D3DSTENCILOP a fazer se o teste de estêncil passar e o teste de z falhar.</span><span class="sxs-lookup"><span data-stu-id="d9835-126">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                              |
| <span data-ttu-id="d9835-127">D3DRS \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="d9835-127">D3DRS\_STENCILPASS</span></span>  | <span data-ttu-id="d9835-128">D3DSTENCILOP para fazer se os testes de estêncil e z forem aprovados.</span><span class="sxs-lookup"><span data-stu-id="d9835-128">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                     |
| <span data-ttu-id="d9835-129">D3DRS \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="d9835-129">D3DRS\_STENCILFUNC</span></span>  | <span data-ttu-id="d9835-130">D3DCMPFUNC FN.</span><span class="sxs-lookup"><span data-stu-id="d9835-130">D3DCMPFUNC fn.</span></span> <span data-ttu-id="d9835-131">O teste de estêncil passa se ((ref & Mask) stencilfn (estêncil & Mask)) é true.</span><span class="sxs-lookup"><span data-stu-id="d9835-131">Stencil Test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="d9835-132">Um novo conjunto de Estados de renderização se aplica aos triângulos de volta (sentido anti-horário).</span><span class="sxs-lookup"><span data-stu-id="d9835-132">A new set of render states apply to the back-facing (counterclockwise) triangles.</span></span>



| <span data-ttu-id="d9835-133">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="d9835-133">Render state</span></span>             | <span data-ttu-id="d9835-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9835-134">Description</span></span>                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9835-135">D3DRS \_ CCW \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="d9835-135">D3DRS\_CCW\_STENCILFAIL</span></span>  | <span data-ttu-id="d9835-136">D3DSTENCILOP para fazer se o teste de estêncil falhar.</span><span class="sxs-lookup"><span data-stu-id="d9835-136">D3DSTENCILOP to do if stencil test fails.</span></span>                                                      |
| <span data-ttu-id="d9835-137">D3DRS \_ CCW \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="d9835-137">D3DRS\_CCW\_STENCILZFAIL</span></span> | <span data-ttu-id="d9835-138">D3DSTENCILOP a fazer se o teste de estêncil passar e o teste de z falhar.</span><span class="sxs-lookup"><span data-stu-id="d9835-138">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                                    |
| <span data-ttu-id="d9835-139">D3DRS \_ CCW \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="d9835-139">D3DRS\_CCW\_STENCILPASS</span></span>  | <span data-ttu-id="d9835-140">D3DSTENCILOP para fazer se os testes de estêncil e z forem aprovados.</span><span class="sxs-lookup"><span data-stu-id="d9835-140">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                           |
| <span data-ttu-id="d9835-141">D3DRS \_ CCW \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="d9835-141">D3DRS\_CCW\_STENCILFUNC</span></span>  | <span data-ttu-id="d9835-142">Função D3DCMPFUNC.</span><span class="sxs-lookup"><span data-stu-id="d9835-142">D3DCMPFUNC function.</span></span> <span data-ttu-id="d9835-143">O teste de estêncil passa se ((ref & Mask) stencilfn (estêncil & Mask)) é true.</span><span class="sxs-lookup"><span data-stu-id="d9835-143">Stencil test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="d9835-144">Os Estados de renderização de estêncil restantes sempre se aplicam aos triângulos no sentido horário e anti-horário.</span><span class="sxs-lookup"><span data-stu-id="d9835-144">The remaining stencil render states always apply to both clockwise and counterclockwise triangles.</span></span>

<span data-ttu-id="d9835-145">O D3DRS de \_ dois \_ lados laterais \_ é ignorado para linhas e sprites de ponto, o que significa que o comportamento não é alterado do DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="d9835-145">D3DRS\_Two\_Sided\_StencilMODE is ignored for lines and point sprites, which means that the behavior is unchanged from DirectX 8.</span></span> <span data-ttu-id="d9835-146">Os \_ Estados de renderização do estêncil CCW D3DRS \_ \* são ignorados.</span><span class="sxs-lookup"><span data-stu-id="d9835-146">The D3DRS\_CCW\_STENCIL\* render states are ignored.</span></span>

<span data-ttu-id="d9835-147">Um novo bit de extremidade indica se o dispositivo dá suporte a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d9835-147">A new cap bit indicates if the device supports this feature.</span></span> <span data-ttu-id="d9835-148">Espera-se que os drivers que não dão suporte a esse recurso ignorem esses novos Estados de renderização.</span><span class="sxs-lookup"><span data-stu-id="d9835-148">Drivers that do not support this feature are expected to ignore these new render states.</span></span> <span data-ttu-id="d9835-149">Todos os outros bits de extremidade do estêncil se aplicam aos dois modos de buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="d9835-149">All other stencil cap bits apply to both modes of stencil buffering.</span></span> <span data-ttu-id="d9835-150">Como dois \_ estênceis laterais \_ implica a capacidade de desenhar com D3DCULLMODE \_ None definido, a Cap correspondente deve ser definida pelo driver se ele der suporte a esse novo modo de estêncil.</span><span class="sxs-lookup"><span data-stu-id="d9835-150">Because Two\_Sided\_Stencil implies the ability to draw with D3DCULLMODE\_NONE set, the corresponding cap must be set by the driver if it supports this new stencil mode.</span></span> <span data-ttu-id="d9835-151">O Microsoft Windows Hardware Quality Labs (WHQL) deve impor isso.</span><span class="sxs-lookup"><span data-stu-id="d9835-151">Microsoft Windows Hardware Quality Labs (WHQL) should enforce this.</span></span>

<span data-ttu-id="d9835-152">Novos Estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="d9835-152">New render states:</span></span>


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



<span data-ttu-id="d9835-153">Novo limite:</span><span class="sxs-lookup"><span data-stu-id="d9835-153">New cap:</span></span>


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a><span data-ttu-id="d9835-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9835-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9835-155">Técnicas de buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="d9835-155">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> <dt>

[<span data-ttu-id="d9835-156">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="d9835-156">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
