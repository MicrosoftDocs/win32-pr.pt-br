---
title: Transformações (DirectComposition)
description: Este tópico discute o suporte do Microsoft DirectComposition para transformações de afinidade (linear) bidimensionais e descreve os tipos de transformações com suporte do DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27a1fec5774d208f240e6d2f1c8b7df09d25c486
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104555467"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="dc5a3-103">Transformações (DirectComposition)</span><span class="sxs-lookup"><span data-stu-id="dc5a3-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="dc5a3-104">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="dc5a3-105">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="dc5a3-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="dc5a3-106">Este tópico discute o suporte do Microsoft DirectComposition para transformações de afinidade (linear) bidimensionais e descreve os tipos de transformações com suporte do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="dc5a3-107">O DirectComposition também dá suporte a transformações de perspectiva 3D, mas, como elas exigem a criação de um bitmap intermediário, o DirectComposition considera que eles são efeitos em vez de transformações.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="dc5a3-108">Para obter informações sobre efeitos de transformação de perspectiva 3D, consulte [efeitos](effects.md).</span><span class="sxs-lookup"><span data-stu-id="dc5a3-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="dc5a3-109">Este tópico inclui as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="dc5a3-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="dc5a3-110">O que é uma transformação 2D DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="dc5a3-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="dc5a3-111">O espaço de coordenadas 2D DirectComposition</span><span class="sxs-lookup"><span data-stu-id="dc5a3-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="dc5a3-112">Suporte para transformações 2D afim</span><span class="sxs-lookup"><span data-stu-id="dc5a3-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="dc5a3-113">Transformações 2D da matriz</span><span class="sxs-lookup"><span data-stu-id="dc5a3-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="dc5a3-114">Transformar grupos</span><span class="sxs-lookup"><span data-stu-id="dc5a3-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="dc5a3-115">Transformar animação</span><span class="sxs-lookup"><span data-stu-id="dc5a3-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="dc5a3-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc5a3-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="dc5a3-117">O que é uma transformação 2D DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="dc5a3-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="dc5a3-118">Uma transformação 2D permite que você altere a posição, o tamanho ou a natureza de um Visual em duas dimensões movendo o Visual para outro local (tradução), tornando-o maior ou menor (dimensionando), virando-o (rotação) ou distorcendo sua forma (distorção).</span><span class="sxs-lookup"><span data-stu-id="dc5a3-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="dc5a3-119">Uma transformação 2D é obtida mapeando os pontos de um Visual de uma posição para outra dentro do mesmo espaço de coordenadas ou de um espaço de coordenadas para outro.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="dc5a3-120">Esse mapeamento é descrito por uma tabela de valores chamada matriz de transformação, definida como uma coleção de três linhas com três colunas de valores de ponto flutuante, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>



|                 |                 |     |
|-----------------|-----------------|-----|
| <span data-ttu-id="dc5a3-121">M11Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-121">M11Default: 1.0</span></span> | <span data-ttu-id="dc5a3-122">M12Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-122">M12Default: 0.0</span></span> | <span data-ttu-id="dc5a3-123">0.0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-123">0.0</span></span> |
| <span data-ttu-id="dc5a3-124">M21Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-124">M21Default: 0.0</span></span> | <span data-ttu-id="dc5a3-125">M22Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-125">M22Default: 1.0</span></span> | <span data-ttu-id="dc5a3-126">0.0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-126">0.0</span></span> |
| <span data-ttu-id="dc5a3-127">M31OffsetX: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-127">M31OffsetX: 0.0</span></span> | <span data-ttu-id="dc5a3-128">M32OffsetY: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-128">M32OffsetY: 0.0</span></span> | <span data-ttu-id="dc5a3-129">1,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-129">1.0</span></span> |



 

<span data-ttu-id="dc5a3-130">A matriz de transformação para transformações 2D afim é uma matriz 3-por-2 que omite a terceira coluna da matriz de transformação anterior.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="dc5a3-131">A tabela a seguir mostra o layout desta matriz.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-131">The following table shows the layout of this matrix.</span></span>



|                 |                 |
|-----------------|-----------------|
| <span data-ttu-id="dc5a3-132">M11Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-132">M11Default: 1.0</span></span> | <span data-ttu-id="dc5a3-133">M12Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-133">M12Default: 0.0</span></span> |
| <span data-ttu-id="dc5a3-134">M21Default: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-134">M21Default: 0.0</span></span> | <span data-ttu-id="dc5a3-135">M22Default: 1,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-135">M22Default: 1.0</span></span> |
| <span data-ttu-id="dc5a3-136">M31OffsetX: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-136">M31OffsetX: 0.0</span></span> | <span data-ttu-id="dc5a3-137">M32OffsetY: 0,0</span><span class="sxs-lookup"><span data-stu-id="dc5a3-137">M32OffsetY: 0.0</span></span> |



 

> [!Note]  
> <span data-ttu-id="dc5a3-138">O DirectComposition não faz nenhum processamento especial ao aplicar transformações 2D ao conteúdo estéreo.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="dc5a3-139">Isso significa que o conteúdo 3D pode parecer distorcido quando uma transformação 2D é aplicada a ele.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="dc5a3-140">O espaço de coordenadas 2D DirectComposition</span><span class="sxs-lookup"><span data-stu-id="dc5a3-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="dc5a3-141">DirectComposition usa um espaço de coordenadas 2D de mão esquerda; ou seja, os valores positivos do eixo x aumentam para a direita e os valores positivos do eixo y aumentam para baixo.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="dc5a3-142">Os visuais são posicionados em relação à origem, que é o ponto em que o eixo x e o eixo y interseccionam (0,0), conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![o eixo x e eixo y de um espaço de coordenadas da mão esquerda](images/coordinatespace.png)

<span data-ttu-id="dc5a3-144">Ao manipular valores em uma matriz de transformação 3-by-2, você pode girar, dimensionar, inclinar e traduzir um objeto em duas dimensões.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="dc5a3-145">Por exemplo, se você definir OffsetX como 100 e OffsetY como 200, moverá o objeto para a direita de 100 pixels e para baixo em 200 pixels.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="dc5a3-146">Suporte para transformações 2D afim</span><span class="sxs-lookup"><span data-stu-id="dc5a3-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="dc5a3-147">A tabela a seguir descreve os tipos de transformações 2D afim com suporte do DirectComposition e lista as interfaces que você pode usar para executar os vários tipos de transformações.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="dc5a3-148">Transformação/interface</span><span class="sxs-lookup"><span data-stu-id="dc5a3-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="dc5a3-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc5a3-149">Description</span></span>                                                                                              | <span data-ttu-id="dc5a3-150">Ilustração</span><span class="sxs-lookup"><span data-stu-id="dc5a3-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5a3-151">Girar[](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ nova linha idcompositionrotatetransform 2D\]</span><span class="sxs-lookup"><span data-stu-id="dc5a3-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="dc5a3-152">girar um Visual pelo ângulo especificado sobre o ponto central especificado.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![ilustração de um quadrado girado em 45 graus no sentido horário sobre o centro do quadrado original](images/rotate.png)               |
| <span data-ttu-id="dc5a3-154">Dimensionar nova linha de [**Idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)2D \[\]</span><span class="sxs-lookup"><span data-stu-id="dc5a3-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="dc5a3-155">dimensionar um Visual pelo fator especificado sobre o ponto central especificado.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![ilustração de um percentual de escala em quadrado de 130%](images/scale.png)                                                                  |
| <span data-ttu-id="dc5a3-157">Distorcer linha de [**Idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)2D \[\]</span><span class="sxs-lookup"><span data-stu-id="dc5a3-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="dc5a3-158">distorcer um Visual pelo ângulo especificado ao longo do eixo x e eixo y e ao lado do ponto central especificado.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![ilustração de um quadrado inclinado em 30 graus no sentido anti-horário do eixo y](images/skew.png)                                   |
| <span data-ttu-id="dc5a3-160">Traduzir nova linha de [**Idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)2D \[\]</span><span class="sxs-lookup"><span data-stu-id="dc5a3-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="dc5a3-161">Altere a posição de um Visual na direção do eixo x e eixo y.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![ilustração de um quadrado moveu 20 unidades ao longo do eixo x positivo e 10 unidades ao longo do eixo y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="dc5a3-163">Transformações 2D da matriz</span><span class="sxs-lookup"><span data-stu-id="dc5a3-163">Matrix 2D transforms</span></span>

<span data-ttu-id="dc5a3-164">A interface [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite que você defina sua própria matriz de transformação 2D afim 3 por 2 e a aplica a um Visual.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="dc5a3-165">Essa interface será útil se você precisar aplicar um tipo de transformação 2D afim que não esteja disponível por meio de outras interfaces de transformação DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="dc5a3-166">Você define a matriz preenchendo uma estrutura [**D2D \_ matriz \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) e passando-a para o método [**IDCompositionMatrixTransform:: setmatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) .</span><span class="sxs-lookup"><span data-stu-id="dc5a3-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="dc5a3-167">Transformar grupos</span><span class="sxs-lookup"><span data-stu-id="dc5a3-167">Transform Groups</span></span>

<span data-ttu-id="dc5a3-168">Você pode usar grupos de transformação para combinar várias transformações em uma.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="dc5a3-169">Um grupo de transformação define uma coleção de objetos de transformação cujas matrizes são multiplicadas em conjunto na ordem em que são especificadas na coleção.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="dc5a3-170">A matriz de transformação resultante é então aplicada ao Visual.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="dc5a3-171">Um grupo de transformação produz o mesmo resultado que aplicar cada transformação separadamente.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="dc5a3-172">Tenha em mente que a ordem dos objetos de transformação em um grupo de transformação é importante.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="dc5a3-173">Por exemplo, se um Visual for girado primeiro, em escala e, em seguida, traduzido, o resultado será diferente de se o Visual for convertido primeiro, então girado e então dimensionado.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="dc5a3-174">DirectComposition sempre aplica as transformações a um Visual na ordem em que elas são especificadas na coleção.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="dc5a3-175">Para criar um grupo de transformação, primeiro crie os objetos de transformação que você deseja incluir no grupo e, em seguida, passe uma matriz de ponteiros de objeto de transformação para o método [**IDCompositionDevice:: CreateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) .</span><span class="sxs-lookup"><span data-stu-id="dc5a3-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="dc5a3-176">Depois de criar um grupo de transformação, você não pode adicionar ou remover objetos de transformação.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="dc5a3-177">No entanto, você pode modificar as propriedades dos objetos de transformação individuais na coleção e as alterações serão refletidas na matriz de transformação resultante.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="dc5a3-178">Transformar animação</span><span class="sxs-lookup"><span data-stu-id="dc5a3-178">Transform animation</span></span>

<span data-ttu-id="dc5a3-179">As propriedades de uma transformação podem ser animadas.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="dc5a3-180">Quando uma propriedade é animada, DirectComposition altera o valor da propriedade ao longo do tempo, em vez de tudo de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="dc5a3-181">Isso é particularmente útil ao criar transições.</span><span class="sxs-lookup"><span data-stu-id="dc5a3-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="dc5a3-182">Para obter mais informações, consulte [animação](animation.md).</span><span class="sxs-lookup"><span data-stu-id="dc5a3-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc5a3-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc5a3-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc5a3-184">Conceitos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="dc5a3-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
