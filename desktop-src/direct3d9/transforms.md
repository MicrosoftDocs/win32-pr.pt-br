---
description: A parte do Direct3D que leva a geometria através do pipeline de geometria de funções fixas é o mecanismo de transformação.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformações (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370331"
---
# <a name="transforms-direct3d-9"></a><span data-ttu-id="985cf-103">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="985cf-103">Transforms (Direct3D 9)</span></span>

<span data-ttu-id="985cf-104">A parte do Direct3D que leva a geometria através do pipeline de geometria de funções fixas é o mecanismo de transformação.</span><span class="sxs-lookup"><span data-stu-id="985cf-104">The part of Direct3D that pushes geometry through the fixed function geometry pipeline is the transform engine.</span></span> <span data-ttu-id="985cf-105">Ele localiza o modelo e o visualizador do mundo, projeta vértices para a exibição na tela e corta os vértices no visor.</span><span class="sxs-lookup"><span data-stu-id="985cf-105">It locates the model and viewer in the world, projects vertices for display on the screen, and clips vertices to the viewport.</span></span> <span data-ttu-id="985cf-106">O mecanismo de transformação também executa cálculos de iluminação para determinar os componentes difusos e especulares em cada vértice.</span><span class="sxs-lookup"><span data-stu-id="985cf-106">The transform engine also performs lighting computations to determine diffuse and specular components at each vertex.</span></span>

<span data-ttu-id="985cf-107">O pipeline de geometria leva vértices como entrada.</span><span class="sxs-lookup"><span data-stu-id="985cf-107">The geometry pipeline takes vertices as input.</span></span> <span data-ttu-id="985cf-108">O mecanismo de transformação aplica as transformações do mundo, modo de exibição e projeção para os vértices, recorta o resultado e passa tudo para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="985cf-108">The transform engine applies the world, view, and projection transforms to the vertices, clips the result, and passes everything to the rasterizer.</span></span>

<span data-ttu-id="985cf-109">No topo do pipeline, os vértices de um modelo são declarados em relação a um sistema de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="985cf-109">At the head of the pipeline, a model's vertices are declared relative to a local coordinate system.</span></span> <span data-ttu-id="985cf-110">Isso é uma origem local e uma orientação.</span><span class="sxs-lookup"><span data-stu-id="985cf-110">This is a local origin and an orientation.</span></span> <span data-ttu-id="985cf-111">Essa orientação de coordenadas é geralmente conhecida como espaço de modelo, e coordenadas individuais são chamadas de coordenadas de modelo.</span><span class="sxs-lookup"><span data-stu-id="985cf-111">This orientation of coordinates is often referred to as model space, and individual coordinates are called model coordinates.</span></span>

<span data-ttu-id="985cf-112">O primeiro estágio do pipeline de geometria transforma os vértices de um modelo de seu sistema de coordenadas local em um sistema de coordenadas usado por todos os objetos em uma cena.</span><span class="sxs-lookup"><span data-stu-id="985cf-112">The first stage of the geometry pipeline transforms a model's vertices from their local coordinate system to a coordinate system that is used by all the objects in a scene.</span></span> <span data-ttu-id="985cf-113">O processo de reorientação dos vértices é chamado de transformação mundial.</span><span class="sxs-lookup"><span data-stu-id="985cf-113">The process of reorienting the vertices is called the world transform.</span></span> <span data-ttu-id="985cf-114">Essa nova orientação é comumente conhecida como espaço de mundo, e cada vértice no espaço de mundo é declarado usando coordenadas mundiais.</span><span class="sxs-lookup"><span data-stu-id="985cf-114">This new orientation is commonly referred to as world space, and each vertex in world space is declared using world coordinates.</span></span>

<span data-ttu-id="985cf-115">No próximo estágio, os vértices que descrevem o mundo 3D são orientados com relação a uma câmera.</span><span class="sxs-lookup"><span data-stu-id="985cf-115">In the next stage, the vertices that describe your 3D world are oriented with respect to a camera.</span></span> <span data-ttu-id="985cf-116">Ou seja, seu aplicativo escolhe um ponto de vista para a cena, e as coordenadas de espaço do mundo são realocadas e giradas ao lado da exibição da câmera, virando o espaço do mundo para o espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="985cf-116">That is, your application chooses a point-of-view for the scene, and world space coordinates are relocated and rotated around the camera's view, turning world space into camera space.</span></span> <span data-ttu-id="985cf-117">Esta é a transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="985cf-117">This is the view transform.</span></span>

<span data-ttu-id="985cf-118">O próximo estágio é a transformação projeção.</span><span class="sxs-lookup"><span data-stu-id="985cf-118">The next stage is the projection transform.</span></span> <span data-ttu-id="985cf-119">Nesta parte do pipeline, os objetos geralmente são dimensionados com relação à sua distância do visualizador para dar a ilusão de profundidade a uma cena; os objetos fechados são feitos para aparecer maiores do que objetos distantes e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="985cf-119">In this part of the pipeline, objects are usually scaled with relation to their distance from the viewer in order to give the illusion of depth to a scene; close objects are made to appear larger than distant objects, and so on.</span></span> <span data-ttu-id="985cf-120">Para fins de simplicidade, esta documentação refere-se ao espaço no qual os vértices existem após a transformação de projeção como espaço de projeção.</span><span class="sxs-lookup"><span data-stu-id="985cf-120">For simplicity, this documentation refers to the space in which vertices exist after the projection transform as projection space.</span></span> <span data-ttu-id="985cf-121">Alguns livros de elementos gráficos podem se referir ao espaço de projeção como espaço homogêneo de pós-perspectiva.</span><span class="sxs-lookup"><span data-stu-id="985cf-121">Some graphics books might refer to projection space as post-perspective homogeneous space.</span></span> <span data-ttu-id="985cf-122">Nem todas as transformações de projeção dimensionam o tamanho dos objetos em uma cena.</span><span class="sxs-lookup"><span data-stu-id="985cf-122">Not all projection transforms scale the size of objects in a scene.</span></span> <span data-ttu-id="985cf-123">Uma projeção como essa às vezes é chamada de um afim ou projeção ortogonal.</span><span class="sxs-lookup"><span data-stu-id="985cf-123">A projection such as this is sometimes called an affine or orthogonal projection.</span></span>

<span data-ttu-id="985cf-124">Na parte final do pipeline, qualquer vértice que não ficará visível na tela é removido, para que o rasterizador não reserve um tempo para calcular as cores e o sombreamento para algo que jamais será visto.</span><span class="sxs-lookup"><span data-stu-id="985cf-124">In the final part of the pipeline, any vertices that will not be visible on the screen are removed, so that the rasterizer doesn't take the time to calculate the colors and shading for something that will never be seen.</span></span> <span data-ttu-id="985cf-125">Esse processo é denominado recorte.</span><span class="sxs-lookup"><span data-stu-id="985cf-125">This process is called clipping.</span></span> <span data-ttu-id="985cf-126">Depois de recorte, os vértices restantes são dimensionados de acordo com os parâmetros do visor e convertidos em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="985cf-126">After clipping, the remaining vertices are scaled according to the viewport parameters and converted into screen coordinates.</span></span> <span data-ttu-id="985cf-127">Os vértices resultantes, vistos na tela quando a cena é rasterizada, existem no espaço de tela.</span><span class="sxs-lookup"><span data-stu-id="985cf-127">The resulting vertices, seen on the screen when the scene is rasterized, exist in screen space.</span></span>

<span data-ttu-id="985cf-128">As transformações são usadas para converter a geometria de objeto de um espaço de coordenadas em outro.</span><span class="sxs-lookup"><span data-stu-id="985cf-128">Transforms are used to convert object geometry from one coordinate space to another.</span></span> <span data-ttu-id="985cf-129">O Direct3D usa matrizes para realizar transformações 3D.</span><span class="sxs-lookup"><span data-stu-id="985cf-129">Direct3D uses matrices to perform 3D transforms.</span></span> <span data-ttu-id="985cf-130">Esta seção explica como as matrizes criam transformações 3D, descreve alguns usos comuns para transformações e detalha como é possível combinar matrizes para produzir uma única matriz que abrange várias transformações.</span><span class="sxs-lookup"><span data-stu-id="985cf-130">This section explains how matrices create 3D transforms, describes some common uses for transforms, and details how you can combine matrices to produce a single matrix that encompasses multiple transforms.</span></span>

-   <span data-ttu-id="985cf-131">[Transformação mundial (Direct3D 9)](world-transform.md) – converter do espaço do modelo para o espaço mundial</span><span class="sxs-lookup"><span data-stu-id="985cf-131">[World Transform (Direct3D 9)](world-transform.md) - convert from model space to world space</span></span>
-   <span data-ttu-id="985cf-132">[Exibir transformação (Direct3D 9)](view-transform.md) – converter do espaço de mundo para exibir espaço</span><span class="sxs-lookup"><span data-stu-id="985cf-132">[View Transform (Direct3D 9)](view-transform.md) - convert from world space to view space</span></span>
-   <span data-ttu-id="985cf-133">[Transformação de projeção (Direct3D 9)](projection-transform.md) – Converta do espaço de exibição para o espaço de projeção</span><span class="sxs-lookup"><span data-stu-id="985cf-133">[Projection Transform (Direct3D 9)](projection-transform.md) - convert from view space to projection space</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="985cf-134">Transformações de matriz</span><span class="sxs-lookup"><span data-stu-id="985cf-134">Matrix Transforms</span></span>

<span data-ttu-id="985cf-135">Em aplicativos que trabalham com elementos gráficos 3D, você pode usar transformações geométricas para fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="985cf-135">In applications that work with 3D graphics, you can use geometrical transforms to do the following:</span></span>

-   <span data-ttu-id="985cf-136">Expressar a localização de um objeto em relação a outro objeto.</span><span class="sxs-lookup"><span data-stu-id="985cf-136">Express the location of an object relative to another object.</span></span>
-   <span data-ttu-id="985cf-137">Rotacionar e dimensionar objetos</span><span class="sxs-lookup"><span data-stu-id="985cf-137">Rotate and size objects.</span></span>
-   <span data-ttu-id="985cf-138">Alterar as posições de visualização, trajetos e perspectivas.</span><span class="sxs-lookup"><span data-stu-id="985cf-138">Change viewing positions, directions, and perspectives.</span></span>

<span data-ttu-id="985cf-139">Você pode transformar qualquer ponto (x, y, z) em outro ponto (x', y', z'), usando uma matriz 4x4, conforme mostrado na seguinte equação.</span><span class="sxs-lookup"><span data-stu-id="985cf-139">You can transform any point (x,y,z) into another point (x', y', z') by using a 4x4 matrix, as shown in the following equation.</span></span>

![equação para transformar qualquer ponto em outro ponto](images/matmult.png)

<span data-ttu-id="985cf-141">Execute as seguintes equações em (x, y, z) e na matriz para produzir o ponto (x', y', z').</span><span class="sxs-lookup"><span data-stu-id="985cf-141">Perform the following equations on (x, y, z) and the matrix to produce the point (x', y', z').</span></span>

![equações para o novo ponto](images/matexpnd.png)

<span data-ttu-id="985cf-143">As transformações mais comuns são conversão, rotação e dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="985cf-143">The most common transforms are translation, rotation, and scaling.</span></span> <span data-ttu-id="985cf-144">Você pode combinar as matrizes que produzem esses efeitos em uma única matriz para calcular várias transformações ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="985cf-144">You can combine the matrices that produce these effects into a single matrix to calculate several transforms at once.</span></span> <span data-ttu-id="985cf-145">Por exemplo, você pode criar uma matriz única para traduzir e girar uma série de pontos.</span><span class="sxs-lookup"><span data-stu-id="985cf-145">For example, you can build a single matrix to translate and rotate a series of points.</span></span>

<span data-ttu-id="985cf-146">Matrizes são escritas na ordem das colunas de linha.</span><span class="sxs-lookup"><span data-stu-id="985cf-146">Matrices are written in row-column order.</span></span> <span data-ttu-id="985cf-147">Uma matriz que dimensiona uniformemente os vértices em cada eixo, conhecida como dimensionamento uniforme, é representada pela matriz de seguir usando a notação matemática.</span><span class="sxs-lookup"><span data-stu-id="985cf-147">A matrix that evenly scales vertices along each axis, known as uniform scaling, is represented by the following matrix using mathematical notation.</span></span>

![equação de uma matriz de dimensionamento uniforme](images/matrix.png)

<span data-ttu-id="985cf-149">Em C++, o Direct3D declara matrizes como uma matriz bidimensional, usando a estrutura [**D3DMATRIX**](d3dmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="985cf-149">In C++, Direct3D declares matrices as a two-dimensional array, using the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="985cf-150">O exemplo a seguir mostra como inicializar uma estrutura **D3DMATRIX** para atuar como uma matriz de dimensionamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="985cf-150">The following example shows how to initialize a **D3DMATRIX** structure to act as a uniform scaling matrix.</span></span>


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a><span data-ttu-id="985cf-151">Translate</span><span class="sxs-lookup"><span data-stu-id="985cf-151">Translate</span></span>

<span data-ttu-id="985cf-152">A seguinte equação traduz o ponto (x, y, z) para um novo ponto (x', y', z').</span><span class="sxs-lookup"><span data-stu-id="985cf-152">The following equation translates the point (x, y, z) to a new point (x', y', z').</span></span>

![equação de uma matriz de translação para um novo ponto](images/transl8.png)

<span data-ttu-id="985cf-154">Você pode criar manualmente uma matriz de translação em C++.</span><span class="sxs-lookup"><span data-stu-id="985cf-154">You can manually create a translation matrix in C++.</span></span> <span data-ttu-id="985cf-155">O exemplo a seguir mostra o código-fonte para uma função que cria uma matriz para traduzir vértices.</span><span class="sxs-lookup"><span data-stu-id="985cf-155">The following example shows the source code for a function that creates a matrix to translate vertices.</span></span>


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



<span data-ttu-id="985cf-156">Para sua conveniência, a biblioteca do utilitário D3DX fornece a função [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .</span><span class="sxs-lookup"><span data-stu-id="985cf-156">For convenience, the D3DX utility library supplies the [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) function.</span></span>

## <a name="scale"></a><span data-ttu-id="985cf-157">Escala</span><span class="sxs-lookup"><span data-stu-id="985cf-157">Scale</span></span>

<span data-ttu-id="985cf-158">A seguinte equação dimensiona o ponto (x, y, z) por valores arbitrários nas direções x, y e z para um novo ponto (x', y', z').</span><span class="sxs-lookup"><span data-stu-id="985cf-158">The following equation scales the point (x, y, z) by arbitrary values in the x-, y-, and z-directions to a new point (x', y', z').</span></span>

![equação de uma matriz de escala para um novo ponto](images/matscale.png)

## <a name="rotate"></a><span data-ttu-id="985cf-160">Rotate</span><span class="sxs-lookup"><span data-stu-id="985cf-160">Rotate</span></span>

<span data-ttu-id="985cf-161">As transformações descritas aqui destinam-se aos sistemas de coordenadas à esquerda e, portanto, podem ser diferentes das matrizes de transformação que você já viu em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="985cf-161">The transforms described here are for left-handed coordinate systems, and so may be different from transform matrices that you have seen elsewhere.</span></span>

<span data-ttu-id="985cf-162">A seguinte equação rotaciona o ponto (x, y, z) em torno do eixo x, produzindo um novo ponto (x', y', z').</span><span class="sxs-lookup"><span data-stu-id="985cf-162">The following equation rotates the point (x, y, z) around the x-axis, producing a new point (x', y', z').</span></span>

![equação de uma matriz de rotação x para um novo ponto](images/matxrot.png)

<span data-ttu-id="985cf-164">A seguinte equação gira o ponto em torno do eixo y.</span><span class="sxs-lookup"><span data-stu-id="985cf-164">The following equation rotates the point around the y-axis.</span></span>

![equação de uma matriz de rotação y para um novo ponto](images/matyrot.png)

<span data-ttu-id="985cf-166">A seguinte equação gira o ponto em torno do eixo z.</span><span class="sxs-lookup"><span data-stu-id="985cf-166">The following equation rotates the point around the z-axis.</span></span>

![equação de uma matriz de rotação z para um novo ponto](images/matzrot.png)

<span data-ttu-id="985cf-168">Nessas matrizes de exemplo, a letra grega "teta" significa o ângulo de rotação, em radianos.</span><span class="sxs-lookup"><span data-stu-id="985cf-168">In these example matrices, the Greek letter theta stands for the angle of rotation, in radians.</span></span> <span data-ttu-id="985cf-169">Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.</span><span class="sxs-lookup"><span data-stu-id="985cf-169">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

<span data-ttu-id="985cf-170">Em um aplicativo C++, use as funções [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)e [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) fornecidas pela biblioteca do utilitário D3DX para criar matrizes de rotação.</span><span class="sxs-lookup"><span data-stu-id="985cf-170">In a C++ application, use the [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md), and [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) functions supplied by the D3DX utility library to create rotation matrices.</span></span> <span data-ttu-id="985cf-171">Este é o código para a função **D3DXMatrixRotationX** .</span><span class="sxs-lookup"><span data-stu-id="985cf-171">The following is the code for the **D3DXMatrixRotationX** function.</span></span>


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a><span data-ttu-id="985cf-172">Concatenação de matrizes</span><span class="sxs-lookup"><span data-stu-id="985cf-172">Concatenating Matrices</span></span>

<span data-ttu-id="985cf-173">Uma vantagem de usar matrizes é que você pode combinar os efeitos de duas ou mais matrizes multiplicando-as.</span><span class="sxs-lookup"><span data-stu-id="985cf-173">One advantage of using matrices is that you can combine the effects of two or more matrices by multiplying them.</span></span> <span data-ttu-id="985cf-174">Isso significa que, para girar um modelo e, em seguida, convertê-lo em um local, você não precisa aplicar duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="985cf-174">This means that, to rotate a model and then translate it to some location, you don't need to apply two matrices.</span></span> <span data-ttu-id="985cf-175">Em vez disso, multiplique as matrizes de rotação e conversão para produzir uma matriz de composição que contém todos os seus efeitos.</span><span class="sxs-lookup"><span data-stu-id="985cf-175">Instead, you multiply the rotation and translation matrices to produce a composite matrix that contains all their effects.</span></span> <span data-ttu-id="985cf-176">Esse processo, chamado de concatenação de matriz, pode ser escrito com a seguinte equação.</span><span class="sxs-lookup"><span data-stu-id="985cf-176">This process, called matrix concatenation, can be written with the following equation.</span></span>

![equação da concatenação de matriz](images/matrxcat.png)

<span data-ttu-id="985cf-178">Nesta equação, C é a matriz de composição que está sendo criada e M₁ por Mₙ são as matrizes individuais.</span><span class="sxs-lookup"><span data-stu-id="985cf-178">In this equation, C is the composite matrix being created, and M₁ through Mₙ are the individual matrices.</span></span> <span data-ttu-id="985cf-179">Na maioria dos casos, apenas duas ou três matrizes são concatenadas, mas não há nenhum limite.</span><span class="sxs-lookup"><span data-stu-id="985cf-179">In most cases, only two or three matrices are concatenated, but there is no limit.</span></span>

<span data-ttu-id="985cf-180">Use a função [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) para executar a multiplicação de matriz.</span><span class="sxs-lookup"><span data-stu-id="985cf-180">Use the [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) function to perform matrix multiplication.</span></span>

<span data-ttu-id="985cf-181">A ordem em que a multiplicação da matriz é realizada é essencial.</span><span class="sxs-lookup"><span data-stu-id="985cf-181">The order in which the matrix multiplication is performed is crucial.</span></span> <span data-ttu-id="985cf-182">A fórmula anterior reflete a regra da esquerda para a direita da concatenação de matriz.</span><span class="sxs-lookup"><span data-stu-id="985cf-182">The preceding formula reflects the left-to-right rule of matrix concatenation.</span></span> <span data-ttu-id="985cf-183">Ou seja, os efeitos visíveis das matrizes que você usa para criar uma matriz composta ocorrem na ordem da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="985cf-183">That is, the visible effects of the matrices that you use to create a composite matrix occur in left-to-right order.</span></span> <span data-ttu-id="985cf-184">Uma matriz de mundo típica é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="985cf-184">A typical world matrix is shown in the following example.</span></span> <span data-ttu-id="985cf-185">Imagine que você está criando a matriz do mundo para um disco voador estereotipado.</span><span class="sxs-lookup"><span data-stu-id="985cf-185">Imagine that you are creating the world matrix for a stereotypical flying saucer.</span></span> <span data-ttu-id="985cf-186">Provavelmente, você desejaria girar o disco voador em torno de seu centro - eixo y do espaço de modelo - e levá-lo para algum outro local em sua cena.</span><span class="sxs-lookup"><span data-stu-id="985cf-186">You would probably want to spin the flying saucer around its center - the y-axis of model space - and translate it to some other location in your scene.</span></span> <span data-ttu-id="985cf-187">Para realizar esse efeito, você primeiro cria uma matriz de rotação e, em seguida, multiplica ela pela matriz de translação, conforme mostrado na seguinte equação.</span><span class="sxs-lookup"><span data-stu-id="985cf-187">To accomplish this effect, you first create a rotation matrix, and then multiply it by a translation matrix, as shown in the following equation.</span></span>

![equação de rotação com base em uma matriz de rotação e uma matriz de translação](images/wrldexpl.png)

<span data-ttu-id="985cf-189">Nessa fórmula, R<sub>y</sub> é uma matriz de rotação sobre o eixo y e T<sub>w</sub> é uma translação para alguma posição nas coordenadas do mundo.</span><span class="sxs-lookup"><span data-stu-id="985cf-189">In this formula, R<sub>y</sub> is a matrix for rotation about the y-axis, and T<sub>w</sub> is a translation to some position in world coordinates.</span></span>

<span data-ttu-id="985cf-190">A ordem na qual você multiplica as matrizes é importante porque, ao contrário da multiplicação de dois valores escalares, a multiplicação de matrizes não é comutativa.</span><span class="sxs-lookup"><span data-stu-id="985cf-190">The order in which you multiply the matrices is important because, unlike multiplying two scalar values, matrix multiplication is not commutative.</span></span> <span data-ttu-id="985cf-191">Multiplicar as matrizes na ordem oposta tem o efeito visual de levar o disco voador para a sua posição do espaço de mundo e, em seguida, girando-o em torno da origem do mundo.</span><span class="sxs-lookup"><span data-stu-id="985cf-191">Multiplying the matrices in the opposite order has the visual effect of translating the flying saucer to its world space position, and then rotating it around the world origin.</span></span>

<span data-ttu-id="985cf-192">Não importa qual tipo de matriz você está criando, lembre-se da regra da esquerda para a direita para garantir que você obterá os efeitos esperados.</span><span class="sxs-lookup"><span data-stu-id="985cf-192">No matter what type of matrix you are creating, remember the left-to-right rule to ensure that you achieve the expected effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="985cf-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="985cf-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="985cf-194">Introdução</span><span class="sxs-lookup"><span data-stu-id="985cf-194">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



