---
description: Você pode considerar a transformação projeção como controle dos elementos internos da câmera; é análogo a escolher uma lente para a câmera.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Transformação de projeção (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163804"
---
# <a name="projection-transform-direct3d-9"></a><span data-ttu-id="338e7-103">Transformação de projeção (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="338e7-103">Projection Transform (Direct3D 9)</span></span>

<span data-ttu-id="338e7-104">Você pode considerar a transformação projeção como controle dos elementos internos da câmera; é análogo a escolher uma lente para a câmera.</span><span class="sxs-lookup"><span data-stu-id="338e7-104">You can think of the projection transformation as controlling the camera's internals; it is analogous to choosing a lens for the camera.</span></span> <span data-ttu-id="338e7-105">Este é o mais complicado dos três tipos de transformação.</span><span class="sxs-lookup"><span data-stu-id="338e7-105">This is the most complicated of the three transformation types.</span></span> <span data-ttu-id="338e7-106">Essa discussão sobre a transformação projeção é organizada nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="338e7-106">This discussion of the projection transformation is organized into the following topics.</span></span>

<span data-ttu-id="338e7-107">A matriz de projeção costuma ser uma projeção de perspectiva e escala.</span><span class="sxs-lookup"><span data-stu-id="338e7-107">The projection matrix is typically a scale and perspective projection.</span></span> <span data-ttu-id="338e7-108">A transformação da projeção converte o tronco de exibição em uma forma cuboide.</span><span class="sxs-lookup"><span data-stu-id="338e7-108">The projection transformation converts the viewing frustum into a cuboid shape.</span></span> <span data-ttu-id="338e7-109">Como a parte perto do final do tronco de exibição é menor do que a extremidade oposta, isso tem o efeito de expandir objetos próximos da câmera; é assim que a perspectiva é aplicada à cena.</span><span class="sxs-lookup"><span data-stu-id="338e7-109">Because the near end of the viewing frustum is smaller than the far end, this has the effect of expanding objects that are near to the camera; this is how perspective is applied to the scene.</span></span>

<span data-ttu-id="338e7-110">No [tronco de exibição](viewports-and-clipping.md), a distância entre a câmera e a origem do espaço de transformação da exibição é definido arbitrariamente como D. Portanto, a matriz de projeção se parece com a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="338e7-110">In [the viewing frustum](viewports-and-clipping.md), the distance between the camera and the origin of the viewing transform space is defined arbitrarily as D, so the projection matrix looks like the following illustration.</span></span>

![ilustração da matriz de projeção](images/projmat1.png)

<span data-ttu-id="338e7-112">A matriz de visualização converte a câmera para a origem por meio da translação na direção z por - D. A matriz de translação é como a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="338e7-112">The viewing matrix translates the camera to the origin by translating in the z direction by - D. The translation matrix is like the following illustration.</span></span>

![ilustração da matriz de translação](images/projmat2.png)

<span data-ttu-id="338e7-114">Multiplicar a matriz de conversão pela matriz de projeção (T \* P) fornece a matriz de projeção composta, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="338e7-114">Multiplying the translation matrix by the projection matrix (T\*P) gives the composite projection matrix, as shown in the following illustration.</span></span>

![ilustração da matriz de projeção composta](images/projmat3.png)

<span data-ttu-id="338e7-116">A transformação de perspectiva converte um tronco de exibição em um novo espaço de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="338e7-116">The perspective transform converts a viewing frustum into a new coordinate space.</span></span> <span data-ttu-id="338e7-117">Observe que o tronco se torna cuboide e também que a origem se move do canto superior direito da cena para o centro, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="338e7-117">Notice that the frustum becomes cuboid and also that the origin moves from the upper-right corner of the scene to the center, as shown in the following diagram.</span></span>

![diagrama de como a transformação de perspectiva muda o tronco de exibição em um novo espaço de coordenadas](images/cuboid.png)

<span data-ttu-id="338e7-119">Na transformação de perspectiva, os limites das direções x e y são -1 e 1.</span><span class="sxs-lookup"><span data-stu-id="338e7-119">In the perspective transform, the limits of the x- and y-directions are -1 and 1.</span></span> <span data-ttu-id="338e7-120">Os limites da direção z são 0 para o plano frontal e 1 para o plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="338e7-120">The limits of the z-direction are 0 for the front plane and 1 for the back plane.</span></span>

<span data-ttu-id="338e7-121">Essa matriz faz a translação e dimensiona objetos com base em uma distância especificada da câmera ao plano de recorte próximo, mas não considera o campo de visão (fov), e os valores de z que produz para objetos na distância podem ser praticamente idênticos, dificultando comparações de profundidade.</span><span class="sxs-lookup"><span data-stu-id="338e7-121">This matrix translates and scales objects based on a specified distance from the camera to the near clipping plane, but it doesn't consider the field of view (fov), and the z-values that it produces for objects in the distance can be nearly identical, making depth comparisons difficult.</span></span> <span data-ttu-id="338e7-122">A tabela a seguir aborda esses problemas e ajusta vértices para levar em conta a taxa de proporção do visor, sendo uma boa opção para a projeção de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="338e7-122">The following matrix addresses these issues, and it adjusts vertices to account for the aspect ratio of the viewport, making it a good choice for the perspective projection.</span></span>

![ilustração de uma matriz para a projeção de perspectiva](images/prjmatx1.png)

<span data-ttu-id="338e7-124">Nessa matriz, Zₙ é o valor de z do plano de recorte próximo.</span><span class="sxs-lookup"><span data-stu-id="338e7-124">In this matrix, Zₙ is the z-value of the near clipping plane.</span></span> <span data-ttu-id="338e7-125">As variáveis w, h e Q têm os significados a seguir.</span><span class="sxs-lookup"><span data-stu-id="338e7-125">The variables w, h, and Q have the following meanings.</span></span> <span data-ttu-id="338e7-126">Observe que fov<sub>w</sub> e fovₖ representam os campos de visão horizontal e vertical do visor em radianos.</span><span class="sxs-lookup"><span data-stu-id="338e7-126">Note that fov<sub>w</sub> and fovₖ represent the viewport's horizontal and vertical fields of view, in radians.</span></span>

![equações dos significados variáveis](images/prjmatx2.png)

<span data-ttu-id="338e7-128">Para seu app, usar os ângulos de campo de visão para definir os coeficientes dimensionamento de x e y pode não ser tão conveniente quanto usar as dimensões horizontais e verticais do visor (no espaço da câmera).</span><span class="sxs-lookup"><span data-stu-id="338e7-128">For your application, using field-of-view angles to define the x- and y-scaling coefficients might not be as convenient as using the viewport's horizontal and vertical dimensions (in camera space).</span></span> <span data-ttu-id="338e7-129">Após resolução da matemática, as duas equações a seguir para w e h usam dimensões do visor e são equivalentes às equações anteriores.</span><span class="sxs-lookup"><span data-stu-id="338e7-129">As the math works out, the following two equations for w and h use the viewport's dimensions, and are equivalent to the preceding equations.</span></span>

![equações dos significados variáveis de w e h](images/prjmatx3.png)

<span data-ttu-id="338e7-131">Nessas fórmulas, Zₙ representa a posição do plano de recorte próximo e o V<sub>w</sub> e variáveis Vₕ representam a largura e altura do visor no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="338e7-131">In these formulas, Zₙ represents the position of the near clipping plane, and the V<sub>w</sub> and Vₕ variables represent the width and height of the viewport, in camera space.</span></span>

<span data-ttu-id="338e7-132">Para um aplicativo C++, essas duas dimensões correspondem diretamente aos membros Width e Height da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) .</span><span class="sxs-lookup"><span data-stu-id="338e7-132">For a C++ application, these two dimensions correspond directly to the Width and Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span>

<span data-ttu-id="338e7-133">Seja qual fórmula você decidir usar, lembre-se de definir Zₙ para o maior valor possível, pois os valores de z extremamente próximos da câmera não variam muito.</span><span class="sxs-lookup"><span data-stu-id="338e7-133">Whatever formula you decide to use, be sure to set Zₙ to as large a value as possible, because z-values extremely close to the camera don't vary by much.</span></span> <span data-ttu-id="338e7-134">Isso dificulta comparações de profundidade usando buffers de z de 16 bits um pouco complicados.</span><span class="sxs-lookup"><span data-stu-id="338e7-134">This makes depth comparisons using 16-bit z-buffers somewhat complicated.</span></span>

<span data-ttu-id="338e7-135">Assim como nas transformações do mundo e da exibição, você chama o método [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para definir a transformação da projeção.</span><span class="sxs-lookup"><span data-stu-id="338e7-135">As with the world and view transformations, you call the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the projection transform.</span></span>

## <a name="setting-up-a-projection-matrix"></a><span data-ttu-id="338e7-136">Configurando uma matriz de projeção</span><span class="sxs-lookup"><span data-stu-id="338e7-136">Setting Up a Projection Matrix</span></span>

<span data-ttu-id="338e7-137">A função de exemplo ProjectionMatrix a seguir define os planos de recorte frontal e posterior, bem como o campo horizontal e vertical dos ângulos de exibição.</span><span class="sxs-lookup"><span data-stu-id="338e7-137">The following ProjectionMatrix sample function sets the front and back clipping planes, as well as the horizontal and vertical field of view angles.</span></span> <span data-ttu-id="338e7-138">Os campos de exibição devem ser inferiores a pi radianos.</span><span class="sxs-lookup"><span data-stu-id="338e7-138">The fields of view should be less than pi radians.</span></span>


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



<span data-ttu-id="338e7-139">Depois de criar a matriz, defina-a com [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) especificando a \_ projeção D3DTS.</span><span class="sxs-lookup"><span data-stu-id="338e7-139">After creating the matrix, set it with [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specifying D3DTS\_PROJECTION.</span></span>

<span data-ttu-id="338e7-140">A biblioteca do utilitário D3DX fornece as seguintes funções para ajudá-lo a configurar sua matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="338e7-140">The D3DX utility library provides the following functions to help you set up your projection matrix.</span></span>

-   [<span data-ttu-id="338e7-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="338e7-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="338e7-142">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="338e7-142">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="338e7-143">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="338e7-143">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="338e7-144">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="338e7-144">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="338e7-145">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="338e7-145">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="338e7-146">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="338e7-146">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a><span data-ttu-id="338e7-147">Uma matriz de projeção amigável W</span><span class="sxs-lookup"><span data-stu-id="338e7-147">A W-Friendly Projection Matrix</span></span>

<span data-ttu-id="338e7-148">O Direct3D pode usar o componente de w de um vértice que foi transformado pelas matrizes de mundo, exibição e projeção para realizar cálculos baseados em profundidade em buffer de profundidade ou efeitos de nevoeiro.</span><span class="sxs-lookup"><span data-stu-id="338e7-148">Direct3D can use the w-component of a vertex that has been transformed by the world, view, and projection matrices to perform depth-based calculations in depth-buffer or fog effects.</span></span> <span data-ttu-id="338e7-149">Cálculos como esses exigem que sua matriz de projeção normalize w para equivaler ao z do espaço do mundo.</span><span class="sxs-lookup"><span data-stu-id="338e7-149">Computations such as these require that your projection matrix normalize w to be equivalent to world-space z.</span></span> <span data-ttu-id="338e7-150">Em poucas palavras, se sua matriz de projeção inclui um coeficiente (3,4) que não é 1, todos os coeficientes devem ser dimensionados pelo inverso do coeficiente (3,4) para criar uma matriz adequada.</span><span class="sxs-lookup"><span data-stu-id="338e7-150">In short, if your projection matrix includes a (3,4) coefficient that is not 1, you must scale all the coefficients by the inverse of the (3,4) coefficient to make a proper matrix.</span></span> <span data-ttu-id="338e7-151">Se você não fornecer uma matriz em conformidade, efeitos de nevoeiro e buffering de profundidade não serão aplicados corretamente.</span><span class="sxs-lookup"><span data-stu-id="338e7-151">If you don't provide a compliant matrix, fog effects and depth buffering are not applied correctly.</span></span>

<span data-ttu-id="338e7-152">A ilustração a seguir mostra uma matriz de projeção incompatível e a mesma matriz dimensionada de forma que o nevoeiro relativo aos olhos seja habilitado.</span><span class="sxs-lookup"><span data-stu-id="338e7-152">The following illustration shows a noncompliant projection matrix, and the same matrix scaled so that eye-relative fog will be enabled.</span></span>

![ilustrações de uma matriz de projeção incompatível e uma matriz com nevoeiro relativo aos olhos](images/eyerlmx.png)

<span data-ttu-id="338e7-154">Nas matrizes anteriores, todas as variáveis são consideradas diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="338e7-154">In the preceding matrices, all variables are assumed to be nonzero.</span></span> <span data-ttu-id="338e7-155">Para obter mais informações sobre a neblina relacionada a olhos, consulte [profundidade baseada em olho versus Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="338e7-155">For more information about eye-relative fog, see [Eye-Relative vs. Z-Based Depth](pixel-fog.md).</span></span> <span data-ttu-id="338e7-156">Para obter informações sobre o buffer de profundidade baseado em w, consulte [buffers de profundidade (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="338e7-156">For information about w-based depth buffering, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="338e7-157">Direct3D usa matriz de projeção atual definida em seus cálculos de profundidade com base em w.</span><span class="sxs-lookup"><span data-stu-id="338e7-157">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="338e7-158">Como resultado, os apps devem definir uma matriz de projeção em conformidade para receber os recursos desejados com base em w, mesmo que eles não usem Direct3D para transformações.</span><span class="sxs-lookup"><span data-stu-id="338e7-158">As a result, applications must set a compliant projection matrix to receive the desired w-based features, even if they do not use Direct3D for transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="338e7-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="338e7-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="338e7-160">Transformações</span><span class="sxs-lookup"><span data-stu-id="338e7-160">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 
