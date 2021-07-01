---
title: Transforms (DirectComposition)
description: Este tópico discute o suporte do Microsoft DirectComposition para transformaçãos de afinidade (linear) bidimensionais e descreve os tipos de transformação aos quais o DirectComposition dá suporte.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118651"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="3398a-103">Transforms (DirectComposition)</span><span class="sxs-lookup"><span data-stu-id="3398a-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="3398a-104">Para aplicativos Windows 10, é recomendável usar APIs Windows.UI.Composition em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3398a-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="3398a-105">Para obter mais informações, consulte [Modernizar seu aplicativo da área de trabalho usando a camada visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="3398a-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="3398a-106">Este tópico discute o suporte do Microsoft DirectComposition para transformaçãos de afinidade (linear) bidimensionais e descreve os tipos de transformação aos quais o DirectComposition dá suporte.</span><span class="sxs-lookup"><span data-stu-id="3398a-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="3398a-107">DirectComposition também dá suporte a transformaçãos de perspectiva 3D, mas como elas exigem a criação de um bitmap intermediário, DirectComposition as considera como efeitos em vez de transformaçãos.</span><span class="sxs-lookup"><span data-stu-id="3398a-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="3398a-108">Para obter informações sobre efeitos de transformação de perspectiva 3D, consulte [Efeitos](effects.md).</span><span class="sxs-lookup"><span data-stu-id="3398a-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="3398a-109">Este tópico inclui as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="3398a-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="3398a-110">O que é uma transformação DirectComposition 2D?</span><span class="sxs-lookup"><span data-stu-id="3398a-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="3398a-111">O espaço de coordenadas 2D do DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3398a-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="3398a-112">Suporte para transformar 2D affine</span><span class="sxs-lookup"><span data-stu-id="3398a-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="3398a-113">Transformaçãos de Matriz 2D</span><span class="sxs-lookup"><span data-stu-id="3398a-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="3398a-114">Transformar grupos</span><span class="sxs-lookup"><span data-stu-id="3398a-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="3398a-115">Transformar animação</span><span class="sxs-lookup"><span data-stu-id="3398a-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="3398a-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3398a-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="3398a-117">O que é uma transformação DirectComposition 2D?</span><span class="sxs-lookup"><span data-stu-id="3398a-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="3398a-118">Uma transformação 2D permite alterar a posição, o tamanho ou a natureza de um visual em duas dimensões movendo o visual para outro local (tradução), tornando-o maior ou menor (dimensionamento), transformando-o (rotação) ou distorcendo sua forma (distorção).</span><span class="sxs-lookup"><span data-stu-id="3398a-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="3398a-119">Uma transformação 2D é feita mapeando os pontos de um visual de uma posição para outra dentro do mesmo espaço de coordenadas ou de um espaço de coordenadas para outro.</span><span class="sxs-lookup"><span data-stu-id="3398a-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="3398a-120">Esse mapeamento é descrito por uma tabela de valores chamada matriz de transformação, definida como uma coleção de três linhas com três colunas de valores de ponto flutuante, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3398a-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="3398a-121">M11Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="3398a-121">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="3398a-122">M21Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-122">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="3398a-123">M31OffsetX: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-123">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="3398a-124">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-124">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="3398a-125">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="3398a-125">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="3398a-126">M32OffsetY: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-126">M32OffsetY: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="3398a-127">0,0</span><span class="sxs-lookup"><span data-stu-id="3398a-127">0.0</span></span><br/>
        <span data-ttu-id="3398a-128">0,0</span><span class="sxs-lookup"><span data-stu-id="3398a-128">0.0</span></span><br/>
        <span data-ttu-id="3398a-129">1,0</span><span class="sxs-lookup"><span data-stu-id="3398a-129">1.0</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="3398a-130">A matriz de transformação para transformações 2D de afinidade é uma matriz 3 por 2 que omite a terceira coluna da matriz de transformação anterior.</span><span class="sxs-lookup"><span data-stu-id="3398a-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="3398a-131">A tabela a seguir mostra o layout dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="3398a-131">The following table shows the layout of this matrix.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="3398a-132">M11Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="3398a-132">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="3398a-133">M21Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-133">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="3398a-134">M31OffsetX: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-134">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="3398a-135">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-135">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="3398a-136">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="3398a-136">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="3398a-137">M32OffsetY: 0.0</span><span class="sxs-lookup"><span data-stu-id="3398a-137">M32OffsetY: 0.0</span></span>
    :::column-end:::
:::row-end:::

> [!Note]  
> <span data-ttu-id="3398a-138">DirectComposition não faz nenhum processamento especial ao aplicar as transformaçãos 2D ao conteúdo estéreo.</span><span class="sxs-lookup"><span data-stu-id="3398a-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="3398a-139">Isso significa que o conteúdo 3D pode parecer distorcido quando uma transformação 2D é aplicada a ele.</span><span class="sxs-lookup"><span data-stu-id="3398a-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="3398a-140">O espaço de coordenadas 2D do DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3398a-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="3398a-141">DirectComposition usa um espaço de coordenadas 2D à esquerda; ou seja, os valores positivos do eixo x aumentam para a direita e os valores positivos do eixo y aumentam para baixo.</span><span class="sxs-lookup"><span data-stu-id="3398a-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="3398a-142">Os visuais são posicionados em relação à origem, que é o ponto em que o eixo x e o eixo y interseccionam (0, 0), conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="3398a-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![o eixo x e o eixo y de um espaço de coordenadas à esquerda](images/coordinatespace.png)

<span data-ttu-id="3398a-144">Manipulando valores em uma matriz de transformação 3 por 2, você pode girar, dimensionar, distorcer e converter um objeto em duas dimensões.</span><span class="sxs-lookup"><span data-stu-id="3398a-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="3398a-145">Por exemplo, se você definir OffsetX como 100 e OffsetY como 200, mova o objeto para a direita 100 pixels e 200 pixels para baixo.</span><span class="sxs-lookup"><span data-stu-id="3398a-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="3398a-146">Suporte para transformar 2D affine</span><span class="sxs-lookup"><span data-stu-id="3398a-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="3398a-147">A tabela a seguir descreve os tipos de transformações 2D affine com suporte pelo DirectComposition e lista as interfaces que você pode usar para executar os vários tipos de transformações.</span><span class="sxs-lookup"><span data-stu-id="3398a-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="3398a-148">Transformar/interface</span><span class="sxs-lookup"><span data-stu-id="3398a-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="3398a-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="3398a-149">Description</span></span>                                                                                              | <span data-ttu-id="3398a-150">Ilustração</span><span class="sxs-lookup"><span data-stu-id="3398a-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3398a-151">Girar [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)newline 2D \[\]</span><span class="sxs-lookup"><span data-stu-id="3398a-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="3398a-152">girar um visual pelo ângulo especificado sobre o ponto central especificado.</span><span class="sxs-lookup"><span data-stu-id="3398a-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![ilustração de um quadrado girado 45 graus no sentido horário sobre o centro do quadrado original](images/rotate.png)               |
| <span data-ttu-id="3398a-154">Dimensionar [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="3398a-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="3398a-155">dimensionar um visual pelo fator especificado sobre o ponto central especificado.</span><span class="sxs-lookup"><span data-stu-id="3398a-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![ilustração de um quadrado dimensionado em 130%](images/scale.png)                                                                  |
| <span data-ttu-id="3398a-157">Distorcer [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)newline 2D \[\]</span><span class="sxs-lookup"><span data-stu-id="3398a-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="3398a-158">distorce um visual pelo ângulo especificado ao longo do eixo x e do eixo y e ao redor do ponto central especificado.</span><span class="sxs-lookup"><span data-stu-id="3398a-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![ilustração de um quadrado distorceu 30 graus no sentido anti-horário do eixo y](images/skew.png)                                   |
| <span data-ttu-id="3398a-160">Traduzir [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)newline 2D \[\]</span><span class="sxs-lookup"><span data-stu-id="3398a-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="3398a-161">altere a posição de um visual na direção do eixo x e eixo y.</span><span class="sxs-lookup"><span data-stu-id="3398a-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![ilustração de um quadrado movido 20 unidades ao longo do eixo x positivo e 10 unidades ao longo do eixo y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="3398a-163">Transformaçãos de Matriz 2D</span><span class="sxs-lookup"><span data-stu-id="3398a-163">Matrix 2D transforms</span></span>

<span data-ttu-id="3398a-164">A interface [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite que você defina sua própria matriz de transformação 2D de afinidade 3 por 2 e aplicá-la a um visual.</span><span class="sxs-lookup"><span data-stu-id="3398a-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="3398a-165">Essa interface será útil se você precisar aplicar um tipo de transformação 2D affine que não está disponível por meio de outras interfaces de transformação DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3398a-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="3398a-166">Defina a matriz preenchendo uma estrutura [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) e passando-a para o [**método IDCompositionMatrixTransform::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix)</span><span class="sxs-lookup"><span data-stu-id="3398a-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="3398a-167">Transformar grupos</span><span class="sxs-lookup"><span data-stu-id="3398a-167">Transform Groups</span></span>

<span data-ttu-id="3398a-168">Você pode usar transformar grupos para combinar várias transformaçãos em uma.</span><span class="sxs-lookup"><span data-stu-id="3398a-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="3398a-169">Um grupo de transformação define uma coleção de objetos de transformação cujas matrizes são multiplicadas juntas na ordem em que são especificadas na coleção.</span><span class="sxs-lookup"><span data-stu-id="3398a-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="3398a-170">A matriz de transformação resultante é aplicada ao visual.</span><span class="sxs-lookup"><span data-stu-id="3398a-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="3398a-171">Um grupo de transformação produz o mesmo resultado que aplicar cada transformação separadamente.</span><span class="sxs-lookup"><span data-stu-id="3398a-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="3398a-172">Tenha em mente que a ordem dos objetos de transformação em um grupo de transformação é importante.</span><span class="sxs-lookup"><span data-stu-id="3398a-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="3398a-173">Por exemplo, se um visual for girado primeiro, depois dimensionado e, em seguida, convertido, o resultado será diferente de se o visual for convertido pela primeira vez, depois girado e, em seguida, dimensionado.</span><span class="sxs-lookup"><span data-stu-id="3398a-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="3398a-174">DirectComposition sempre aplica as transformação a um visual na ordem em que elas são especificadas na coleção.</span><span class="sxs-lookup"><span data-stu-id="3398a-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="3398a-175">Para criar um grupo de transformação, primeiro crie os objetos de transformação que você deseja incluir no grupo e, em seguida, passe uma matriz de ponteiros de objeto de transformação para o método [**IDCompositionDevice::CreateTransformGroup.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup)</span><span class="sxs-lookup"><span data-stu-id="3398a-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="3398a-176">Depois de criar um grupo de transformação, você não pode adicionar ou remover nenhum objeto de transformação.</span><span class="sxs-lookup"><span data-stu-id="3398a-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="3398a-177">No entanto, você pode modificar as propriedades dos objetos de transformação individuais na coleção e as alterações serão refletidas na matriz de transformação resultante.</span><span class="sxs-lookup"><span data-stu-id="3398a-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="3398a-178">Transformar animação</span><span class="sxs-lookup"><span data-stu-id="3398a-178">Transform animation</span></span>

<span data-ttu-id="3398a-179">As propriedades de uma transformação podem ser animadas.</span><span class="sxs-lookup"><span data-stu-id="3398a-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="3398a-180">Quando uma propriedade é animada, DirectComposition altera o valor da propriedade ao longo do tempo, em vez de tudo de uma vez.</span><span class="sxs-lookup"><span data-stu-id="3398a-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="3398a-181">Isso é particularmente útil ao criar transições.</span><span class="sxs-lookup"><span data-stu-id="3398a-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="3398a-182">Para obter mais informações, consulte [Animação](animation.md).</span><span class="sxs-lookup"><span data-stu-id="3398a-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3398a-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3398a-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3398a-184">Conceitos do DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3398a-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
