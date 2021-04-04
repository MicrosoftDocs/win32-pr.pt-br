---
title: O pipeline de transformação do Direct3D
description: Este artigo fornece uma explicação técnica para desenvolvedores de aplicativos Direct3D sobre como definir os parâmetros do pipeline de transformação Direct3D pela manipulação direta de matrizes de Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103837542"
---
# <a name="the-direct3d-transformation-pipeline"></a><span data-ttu-id="17bd9-103">O pipeline de transformação do Direct3D</span><span class="sxs-lookup"><span data-stu-id="17bd9-103">The Direct3D Transformation Pipeline</span></span>

<span data-ttu-id="17bd9-104">Este artigo fornece uma explicação técnica para desenvolvedores de aplicativos Direct3D sobre como definir os parâmetros do pipeline de transformação Direct3D pela manipulação direta de matrizes de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="17bd9-104">This article provides a technical explanation for Direct3D application developers on how to set the parameters of the Direct3D Transformation Pipeline by the direct manipulation of Direct3D matrices.</span></span>

-   [<span data-ttu-id="17bd9-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="17bd9-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="17bd9-106">O pipeline de transformação</span><span class="sxs-lookup"><span data-stu-id="17bd9-106">The Transformation Pipeline</span></span>](#the-transformation-pipeline)
-   [<span data-ttu-id="17bd9-107">Dicas de uso</span><span class="sxs-lookup"><span data-stu-id="17bd9-107">Usage Tips</span></span>](#usage-tips)

## <a name="overview"></a><span data-ttu-id="17bd9-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="17bd9-108">Overview</span></span>

<span data-ttu-id="17bd9-109">O Direct3D usa três transformações para alterar suas coordenadas de modelo 3D em coordenadas de pixel (espaço da tela).</span><span class="sxs-lookup"><span data-stu-id="17bd9-109">Direct3D uses three transformations to change your 3D model coordinates into pixel coordinates (screen space).</span></span> <span data-ttu-id="17bd9-110">Essas transformações são transformação de mundo, transformação de exibição e transformação de projeção.</span><span class="sxs-lookup"><span data-stu-id="17bd9-110">These transformations are world transform, view transform, and projection transform.</span></span>

<span data-ttu-id="17bd9-111">A transformação mundial controla como as coordenadas de modelo são transformadas em coordenadas mundiais.</span><span class="sxs-lookup"><span data-stu-id="17bd9-111">World transform controls how model coordinates are transformed into world coordinates.</span></span> <span data-ttu-id="17bd9-112">A transformação mundial pode incluir traduções, rotações e escalas, mas não se aplica a luzes.</span><span class="sxs-lookup"><span data-stu-id="17bd9-112">World transform can include translations, rotations, and scalings, but it does not apply to lights.</span></span> <span data-ttu-id="17bd9-113">Para obter mais informações sobre como trabalhar com transformações mundiais, consulte [World Transform](/windows/desktop/direct3d9/world-transform).</span><span class="sxs-lookup"><span data-stu-id="17bd9-113">For more information on working with world transforms, see [World Transform](/windows/desktop/direct3d9/world-transform).</span></span>

<span data-ttu-id="17bd9-114">Exibir os controles de transformação a transição do mundo coordena para "espaço da câmera", determinando a posição da câmera no mundo.</span><span class="sxs-lookup"><span data-stu-id="17bd9-114">View transform controls the transition from world coordinates into "camera space," determining camera position in the world.</span></span> <span data-ttu-id="17bd9-115">Para obter um exemplo de como trabalhar com transformações de exibição, consulte [Exibir transformação](/windows/desktop/direct3d9/view-transform).</span><span class="sxs-lookup"><span data-stu-id="17bd9-115">For an example of working with view transforms, see [View Transform](/windows/desktop/direct3d9/view-transform).</span></span>

<span data-ttu-id="17bd9-116">A transformação projeção altera a geometria do espaço da câmera para o "espaço do clipe" e aplica a distorção de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="17bd9-116">Projection transform changes the geometry from camera space into "clip space" and applies perspective distortion.</span></span> <span data-ttu-id="17bd9-117">O termo "espaço do clipe" refere-se a como a geometria é recortada para o volume de exibição durante essa transformação.</span><span class="sxs-lookup"><span data-stu-id="17bd9-117">The term "clip space" refers to how the geometry is clipped to the view volume during this transform.</span></span> <span data-ttu-id="17bd9-118">Para obter um exemplo de como trabalhar com transformações de projeção, consulte [projetion Transform](/windows/desktop/direct3d9/projection-transform).</span><span class="sxs-lookup"><span data-stu-id="17bd9-118">For an example of working with projection transforms, see [Projection Transform](/windows/desktop/direct3d9/projection-transform).</span></span>

<span data-ttu-id="17bd9-119">Por fim, a geometria no espaço do clipe é transformada em coordenadas de pixel (espaço na tela).</span><span class="sxs-lookup"><span data-stu-id="17bd9-119">Finally, the geometry in clip space is transformed into pixel coordinates (screen space).</span></span> <span data-ttu-id="17bd9-120">Essa transformação é controlada pelas configurações do visor.</span><span class="sxs-lookup"><span data-stu-id="17bd9-120">This transformation is controlled by the viewport settings.</span></span>

<span data-ttu-id="17bd9-121">Os vértices de recorte e transformação devem ocorrer no espaço homogêneo (simplesmente put, espaço no qual o sistema de coordenadas inclui um quarto elemento), mas o resultado final para a maioria dos aplicativos precisa ser coordenadas tridimensionais (3D) não homogêneas definidas no "espaço da tela".</span><span class="sxs-lookup"><span data-stu-id="17bd9-121">Clipping and transforming vertices must take place in homogenous space (simply put, space in which the coordinate system includes a fourth element), but the final result for most applications needs to be non-homogenous three-dimensional (3D) coordinates defined in "screen space."</span></span> <span data-ttu-id="17bd9-122">Isso significa que os vértices de entrada e o volume de recorte devem ser convertidos em espaço homogêneo para executar o recorte e, em seguida, convertidos novamente em espaço não homogêneo para serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="17bd9-122">This means that both the input vertices and the clipping volume must be translated into homogenous space to perform the clipping and then translated back into non-homogenous space to be displayed.</span></span>

<span data-ttu-id="17bd9-123">As três transformações do Direct3D – mundo, exibição e transformação de projeção – são definidas por matrizes de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="17bd9-123">The three Direct3D transformations-world, view, and projection transform-are defined by Direct3D matrices.</span></span> <span data-ttu-id="17bd9-124">Uma matriz de Direct3D é uma matriz homogênea 4x4 definida por uma estrutura [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) .</span><span class="sxs-lookup"><span data-stu-id="17bd9-124">A Direct3D matrix is a 4x4 homogenous matrix defined by a [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) structure.</span></span> <span data-ttu-id="17bd9-125">Embora as matrizes de Direct3D não sejam objetos padrão-elas não são representadas por uma interface COM, você pode criá-las e defini-las como faria com qualquer outro objeto do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="17bd9-125">Although Direct3D matrices are not standard objects-they are not represented by a COM interface-you can create and set them just as you would any other Direct3D object.</span></span> <span data-ttu-id="17bd9-126">Para obter mais informações sobre matrizes de Direct3D, consulte [transformações](/windows/desktop/direct3d9/transforms).</span><span class="sxs-lookup"><span data-stu-id="17bd9-126">For more information on Direct3D matrices, see [Transforms](/windows/desktop/direct3d9/transforms).</span></span>

## <a name="the-transformation-pipeline"></a><span data-ttu-id="17bd9-127">O pipeline de transformação</span><span class="sxs-lookup"><span data-stu-id="17bd9-127">The Transformation Pipeline</span></span>

<span data-ttu-id="17bd9-128">Se um vértice na coordenada de modelo for fornecido por PM = (XM, YM, ZM, 1), as transformações mostradas na figura a seguir serão aplicadas às coordenadas da tela de computação PS = (XS, haves, ZS, WS).</span><span class="sxs-lookup"><span data-stu-id="17bd9-128">If a vertex in the model coordinate is given by Pm = (Xm, Ym, Zm, 1), then the transformations shown in the following figure are applied to compute screen coordinates Ps = (Xs, Ys, Zs, Ws).</span></span>

![espaço de modelo para transformação de espaço na tela](images/d3dxfrm61.gif)

<span data-ttu-id="17bd9-130">Aqui estão as descrições dos estágios mostrados na figura anterior:</span><span class="sxs-lookup"><span data-stu-id="17bd9-130">Here are descriptions of the stages that are shown in the preceding figure:</span></span>

1.  <span data-ttu-id="17bd9-131">O World Matrix Mworld transforma os vértices do espaço do modelo no espaço do mundo.</span><span class="sxs-lookup"><span data-stu-id="17bd9-131">World matrix Mworld transforms vertices from the model space to the world space.</span></span> <span data-ttu-id="17bd9-132">Essa matriz é definida por:</span><span class="sxs-lookup"><span data-stu-id="17bd9-132">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    <span data-ttu-id="17bd9-133">A implementação do Direct3D pressupõe que a última coluna dessa matriz é (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="17bd9-133">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="17bd9-134">Nenhum erro será retornado se o usuário especificar uma matriz com uma última coluna diferente, mas a iluminação e a neblina estarão incorretas.</span><span class="sxs-lookup"><span data-stu-id="17bd9-134">No error is returned if the user specifies a matrix with a different last column, but the lighting and fog will be incorrect.</span></span>

2.  <span data-ttu-id="17bd9-135">Exibir MVIEW de matriz transforma vértices do espaço do mundo para o espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="17bd9-135">View matrix Mview transforms vertices from the world space to the camera space.</span></span> <span data-ttu-id="17bd9-136">Essa matriz é definida por:</span><span class="sxs-lookup"><span data-stu-id="17bd9-136">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    <span data-ttu-id="17bd9-137">A implementação do Direct3D pressupõe que a última coluna dessa matriz é (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="17bd9-137">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="17bd9-138">Nenhum erro será retornado se o usuário especificar uma matriz com a última coluna diferente, mas a iluminação e a neblina ficarão incorretas.</span><span class="sxs-lookup"><span data-stu-id="17bd9-138">No error is returned if the user specifies a matrix with different last column, but the lighting and fog will be incorrect.</span></span>

3.  <span data-ttu-id="17bd9-139">A matriz de projeção mproj transforma os vértices do espaço da câmera no espaço de projeção.</span><span class="sxs-lookup"><span data-stu-id="17bd9-139">Projection matrix Mproj transforms vertices from the camera space to the projection space.</span></span> <span data-ttu-id="17bd9-140">Essa matriz é definida por:</span><span class="sxs-lookup"><span data-stu-id="17bd9-140">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    <span data-ttu-id="17bd9-141">A última coluna da matriz de projeção deve ser (0, 0, 1, 0) ou (0, 0, a, 0) para efeitos corretos de neblina e iluminação; o formulário (0, 0, 1, 0) é preferencial.</span><span class="sxs-lookup"><span data-stu-id="17bd9-141">The last column of the projection matrix should be (0, 0, 1, 0), or (0, 0, a, 0) for correct fog and lighting effects; (0, 0, 1, 0) form is preferred.</span></span>

    <span data-ttu-id="17bd9-142">O volume de recorte para todos os pontos XP = (XP, YP, ZP, WP) no espaço de projeção é definido como:</span><span class="sxs-lookup"><span data-stu-id="17bd9-142">Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:</span></span>

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    <span data-ttu-id="17bd9-143">Todos os pontos que não atenderem a essas equações serão recortados.</span><span class="sxs-lookup"><span data-stu-id="17bd9-143">All points that do not satisfy these equations will be clipped.</span></span>

    <span data-ttu-id="17bd9-144">Se um volume de exibição for definido como:</span><span class="sxs-lookup"><span data-stu-id="17bd9-144">If a view volume is defined as:</span></span>

    -   <span data-ttu-id="17bd9-145">SW-largura da janela de tela no espaço da câmera no plano de recorte próximo</span><span class="sxs-lookup"><span data-stu-id="17bd9-145">Sw-screen window width in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="17bd9-146">SH-altura da janela de tela no espaço da câmera no plano de recorte próximo</span><span class="sxs-lookup"><span data-stu-id="17bd9-146">Sh-screen window height in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="17bd9-147">Zn-distância ao próximo plano de recorte ao longo dos eixos Z no espaço da câmera</span><span class="sxs-lookup"><span data-stu-id="17bd9-147">Zn-distance to the near clipping plane along Z axes in camera space</span></span>
    -   <span data-ttu-id="17bd9-148">ZF-distância até o plano de recorte distante ao longo dos eixos Z no espaço da câmera</span><span class="sxs-lookup"><span data-stu-id="17bd9-148">Zf-distance to the far clipping plane along Z axes in camera space</span></span>

    <span data-ttu-id="17bd9-149">em seguida, uma matriz de projeção em perspectiva poderia ser escrita da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="17bd9-149">then a perspective projection matrix could be written as follows:</span></span>

    ![Mostra uma matriz de projeção em perspectiva.](images/d3dxfrm62.gif)

    <span data-ttu-id="17bd9-151">em que MIJ são membros de mproj.</span><span class="sxs-lookup"><span data-stu-id="17bd9-151">where Mij are members of Mproj.</span></span>

    <span data-ttu-id="17bd9-152">Para a projeção ortogonal, temos:</span><span class="sxs-lookup"><span data-stu-id="17bd9-152">For the orthogonal projection we have:</span></span>

    ![projeção ortogonal](images/d3dxfrm63.gif)

    <span data-ttu-id="17bd9-154">O Direct3D pressupõe que a matriz de projeção de perspectiva tem o formato:</span><span class="sxs-lookup"><span data-stu-id="17bd9-154">Direct3D assumes that the perspective projection matrix has the form:</span></span>

    ![matriz de projeção em perspectiva](images/d3dxfrm64.gif)

    <span data-ttu-id="17bd9-156">Se a matriz de projeção de perspectiva não tiver esse formulário, haverá alguns artefatos.</span><span class="sxs-lookup"><span data-stu-id="17bd9-156">If the perspective projection matrix does not have this form, there will be some artifacts.</span></span> <span data-ttu-id="17bd9-157">Por exemplo, a sombra da tabela não funcionará.</span><span class="sxs-lookup"><span data-stu-id="17bd9-157">For example, table fog will not work.</span></span>

4.  <span data-ttu-id="17bd9-158">O Direct3D permite que o usuário altere o volume do clipe da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="17bd9-158">Direct3D allows the user to change the clip volume as follows:</span></span>

    ![alterar o volume do clipe](images/d3dxfrm65.gif)

    <span data-ttu-id="17bd9-160">Isso pode ser reescrito como:</span><span class="sxs-lookup"><span data-stu-id="17bd9-160">This can be rewritten as:</span></span>

    ![alterar o volume do clipe regravado](images/d3dxfrm66.gif)

    <span data-ttu-id="17bd9-162">onde:</span><span class="sxs-lookup"><span data-stu-id="17bd9-162">where:</span></span>

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    <span data-ttu-id="17bd9-163">Essa transformação pode fornecer maior precisão e equivale a dimensionar e deslocar o volume de recorte.</span><span class="sxs-lookup"><span data-stu-id="17bd9-163">This transformation can provide increased precision and is equivalent to scaling and shifting the clipping volume.</span></span>

    <span data-ttu-id="17bd9-164">A matriz Mclip correspondente é:</span><span class="sxs-lookup"><span data-stu-id="17bd9-164">The corresponding Mclip matrix is:</span></span>

    ![matriz mclip](images/d3dxfrm67.gif)

    <span data-ttu-id="17bd9-166">Um vértice é transformado por:</span><span class="sxs-lookup"><span data-stu-id="17bd9-166">A vertex is transformed by:</span></span>

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    <span data-ttu-id="17bd9-167">Se você não quiser dimensionar o volume do clipe, poderá definir os parâmetros do visor para os valores padrão:</span><span class="sxs-lookup"><span data-stu-id="17bd9-167">If you do not want to scale the clip volume, you can set viewport parameters to default values:</span></span>

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  <span data-ttu-id="17bd9-168">O estágio de recorte será opcional se o usuário especificar o \_ sinalizador D3DDP DONOTCLIP em uma chamada DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="17bd9-168">The clipping stage is optional if the user specifies the D3DDP\_DONOTCLIP flag in a DrawPrimitive call.</span></span> <span data-ttu-id="17bd9-169">Nesse caso, todas as matrizes (incluindo MVS) podem ser combinadas.</span><span class="sxs-lookup"><span data-stu-id="17bd9-169">In this case, all matrices (including Mvs) can be combined.</span></span>
6.  <span data-ttu-id="17bd9-170">A matriz de escala do visor MVS dimensiona as coordenadas para estar dentro da janela viewport e inverte o eixo Y de cima para baixo:</span><span class="sxs-lookup"><span data-stu-id="17bd9-170">The viewport scale matrix Mvs scales coordinates to be within the viewport window and flips the Y axis from up to down:</span></span>

    ![MVS da matriz de escala do visor](images/d3dxfrm68.gif)

    <span data-ttu-id="17bd9-172">onde:</span><span class="sxs-lookup"><span data-stu-id="17bd9-172">where:</span></span>

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  <span data-ttu-id="17bd9-173">Por fim, as coordenadas da tela são computadas e passadas para o rasterizador:</span><span class="sxs-lookup"><span data-stu-id="17bd9-173">Finally, screen coordinates are computed and passed to the rasterizer:</span></span>

    ![coordenadas de tela computadas e passadas para o rasterizador](images/d3dxfrm69.gif)

## <a name="usage-tips"></a><span data-ttu-id="17bd9-175">Dicas de uso</span><span class="sxs-lookup"><span data-stu-id="17bd9-175">Usage Tips</span></span>

<span data-ttu-id="17bd9-176">Aqui estão algumas dicas sobre como usar o pipeline de transformação do Direct3D:</span><span class="sxs-lookup"><span data-stu-id="17bd9-176">Here are some tips for how to use the Direct3D Transformation Pipeline:</span></span>

-   <span data-ttu-id="17bd9-177">A última coluna do mundo e as matrizes de exibição devem ser (0, 0, 0, 1) ou a iluminação estará incorreta.</span><span class="sxs-lookup"><span data-stu-id="17bd9-177">The last column of the world and view matrices should be (0, 0, 0, 1), or the lighting will be incorrect.</span></span>
-   <span data-ttu-id="17bd9-178">Defina os parâmetros do visor para criar uma matriz de identidade Mclip, a menos que você entenda exatamente o que é necessário para o.</span><span class="sxs-lookup"><span data-stu-id="17bd9-178">Set the viewport parameters to build an identity Mclip matrix, unless you understand exactly what it is needed for.</span></span>

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 