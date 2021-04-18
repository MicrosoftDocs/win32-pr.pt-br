---
description: 'Normalmente, os aplicativos gráficos 3D usam dois tipos de sistemas de coordenadas cartesianas: canhoto e canhoto.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Sistemas de coordenadas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb9fa389b2bf11bec9ee4f8053bbeb4c822f422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763905"
---
# <a name="coordinate-systems-direct3d-9"></a><span data-ttu-id="5fa2a-103">Sistemas de coordenadas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5fa2a-103">Coordinate Systems (Direct3D 9)</span></span>

<span data-ttu-id="5fa2a-104">Normalmente, os aplicativos gráficos 3D usam dois tipos de sistemas de coordenadas cartesianas: canhoto e canhoto.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-104">Typically 3D graphics applications use two types of Cartesian coordinate systems: left-handed and right-handed.</span></span> <span data-ttu-id="5fa2a-105">Em ambos os sistemas de coordenadas, o eixo x positivo aponta para a direita e o eixo y positivo aponta para cima.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-105">In both coordinate systems, the positive x-axis points to the right, and the positive y-axis points up.</span></span> <span data-ttu-id="5fa2a-106">Você pode lembrar para qual direção o eixo z positivo aponta, apontando os dedos de sua mão direita ou esquerda na direção x positiva e curvando-os na direção y positiva.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-106">You can remember which direction the positive z-axis points by pointing the fingers of either your left or right hand in the positive x-direction and curling them into the positive y-direction.</span></span> <span data-ttu-id="5fa2a-107">A direção do seu polegar aponta em sua direção ou para longe de você, é a direção em que o eixo z positivo aponta para esse sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-107">The direction your thumb points, either toward or away from you, is the direction that the positive z-axis points for that coordinate system.</span></span> <span data-ttu-id="5fa2a-108">A ilustração a seguir mostra esses dois sistemas de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-108">The following illustration shows these two coordinate systems.</span></span>

![ilustração dos sistemas de coordenadas cartesianas à esquerda e à direita](images/leftrght.png)

<span data-ttu-id="5fa2a-110">O Direct3D usa um sistema de coordenadas à esquerda.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-110">Direct3D uses a left-handed coordinate system.</span></span> <span data-ttu-id="5fa2a-111">Se você estiver portando um aplicativo baseado em um sistema de coordenadas à direita, deverá fazer duas alterações nos dados passados para o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-111">If you are porting an application that is based on a right-handed coordinate system, you must make two changes to the data passed to Direct3D.</span></span>

-   <span data-ttu-id="5fa2a-112">Inverter a ordem dos vértices de triângulos, de modo que o sistema os percorra em sentido horário, a partir da frente.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-112">Flip the order of triangle vertices so that the system traverses them clockwise from the front.</span></span> <span data-ttu-id="5fa2a-113">Em outras palavras, se os vértices forem v0, v1, v2, passe-os para o Direct3D como v0, v2, v1.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-113">In other words, if the vertices are v0, v1, v2, pass them to Direct3D as v0, v2, v1.</span></span>
-   <span data-ttu-id="5fa2a-114">Use a matriz de visualização para dimensionar o espaço do mundo em -1 na direção z.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-114">Use the view matrix to scale world space by -1 in the z-direction.</span></span> <span data-ttu-id="5fa2a-115">Para fazer isso, inverta o sinal do \_ membro 31, \_ 32, \_ 33 e \_ 34 da estrutura [**D3DMATRIX**](d3dmatrix.md) que você usa para sua matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-115">To do this, flip the sign of the \_31, \_32, \_33, and \_34 member of the [**D3DMATRIX**](d3dmatrix.md) structure that you use for your view matrix.</span></span>

<span data-ttu-id="5fa2a-116">Para obter os valores para um mundo com direito, use as funções [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) e [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) para definir a transformação projeção.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-116">To obtain what amounts to a right-handed world, use the [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) and [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) functions to define the projection transform.</span></span> <span data-ttu-id="5fa2a-117">No entanto, tenha cuidado ao usar a função [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) correspondente, inverta a ordem de remoção do backface e faça o layout dos mapas do cubo de acordo.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-117">However, be careful to use the corresponding [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) function, reverse the backface-culling order, and lay out the cube maps accordingly.</span></span>

<span data-ttu-id="5fa2a-118">Apesar das coordenadas de esquerda e direita serem os sistemas mais comuns, há uma variedade de outros sistemas de coordenadas usados no software 3D.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-118">Although left-handed and right-handed coordinates are the most common systems, there is a variety of other coordinate systems used in 3D software.</span></span> <span data-ttu-id="5fa2a-119">Por exemplo, não é incomum para apps de modelagem 3D usar um sistema de coordenadas no qual o eixo y aponta para o visualizador ou para longe dele, e o eixo z aponta para cima.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-119">For example, it is not unusual for 3D modeling applications to use a coordinate system in which the y-axis points toward or away from the viewer, and the z-axis points up.</span></span>

<span data-ttu-id="5fa2a-120">Formalmente, a orientação de um conjunto de vetores de base (ou seja, um sistema de coordenadas) pode ser encontrada pela computação do determinante da matriz definida pelo conjunto específico de vetores de base.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-120">Formally, the orientation of a set of basis vectors (i.e. a coordinate system) can be found by the computing the determinant of the matrix defined by the particular set of basis vectors.</span></span> <span data-ttu-id="5fa2a-121">Se o determinante for positivo, a base será considerada "positivamente" orientada (ou de mão direita).</span><span class="sxs-lookup"><span data-stu-id="5fa2a-121">If the determinant is positive, the basis is said to be "positively" oriented (or right-handed).</span></span> <span data-ttu-id="5fa2a-122">Se o determinante for negativo, a base será considerada "negativamente" orientada (ou canhoto).</span><span class="sxs-lookup"><span data-stu-id="5fa2a-122">If the determinant is negative, the basis is said to be "negatively" oriented (or left-handed).</span></span> <span data-ttu-id="5fa2a-123">Para obter uma explicação do que é um determinante, consulte qualquer recurso de algebra linear.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-123">For an explanation of what a determinant is, see any linear algebra resource.</span></span>

<span data-ttu-id="5fa2a-124">Informalmente, você pode usar a "regra direita/esquerda" para determinar se um determinado conjunto de vetores de base formam um sistema de coordenadas da mão direita ou esquerda.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-124">Informally, you can use the "right/left hand rule" to determine if a given set of basis vectors form either a right or left handed coordinate system.</span></span>

<span data-ttu-id="5fa2a-125">As operações essenciais executadas em objetos definidos em um sistema de coordenadas 3D são tradução, rotação e dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-125">The essential operations performed on objects defined in a 3D coordinate system are translation, rotation, and scaling.</span></span> <span data-ttu-id="5fa2a-126">Você pode combinar essas transformações básicas para criar uma matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-126">You can combine these basic transformations to create a transform matrix.</span></span> <span data-ttu-id="5fa2a-127">Para obter detalhes, consulte [transformações (Direct3D 9)](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="5fa2a-127">For details, see [Transforms (Direct3D 9)](transforms.md).</span></span>

<span data-ttu-id="5fa2a-128">Quando você combina essas operações, os resultados não são comutativos; a ordem em que você faz multiplicação das matrizes é importante.</span><span class="sxs-lookup"><span data-stu-id="5fa2a-128">When you combine these operations, the results are not commutative; the order in which you multiply matrices is important.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fa2a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fa2a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fa2a-130">Coordenar sistemas e geometria</span><span class="sxs-lookup"><span data-stu-id="5fa2a-130">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



