---
description: Esta seção apresenta os conceitos básicos da exibição de transformação e fornece detalhes sobre como configurar uma matriz de transformação de exibição em um aplicativo do Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Exibir transformação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500514"
---
# <a name="view-transform-direct3d-9"></a><span data-ttu-id="a601b-103">Exibir transformação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a601b-103">View Transform (Direct3D 9)</span></span>

<span data-ttu-id="a601b-104">Esta seção apresenta os conceitos básicos da exibição de transformação e fornece detalhes sobre como configurar uma matriz de transformação de exibição em um aplicativo do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a601b-104">This section introduces the basic concepts of the view transform and provides details on how to set up a view transform matrix in a Direct3D application.</span></span>

<span data-ttu-id="a601b-105">A transformação de exibição localiza o visualizador no espaço do mundo, transformando vértices em espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="a601b-105">The view transform locates the viewer in world space, transforming vertices into camera space.</span></span> <span data-ttu-id="a601b-106">No espaço de câmera, a câmera ou visualizador está na origem, olhando na direção z positiva.</span><span class="sxs-lookup"><span data-stu-id="a601b-106">In camera space, the camera, or viewer, is at the origin, looking in the positive z-direction.</span></span> <span data-ttu-id="a601b-107">Lembre-se de que o Direct3D usa um sistema de coordenadas à esquerda, portanto, z é positivo em uma cena.</span><span class="sxs-lookup"><span data-stu-id="a601b-107">Recall that Direct3D uses a left-handed coordinate system, so z is positive into a scene.</span></span> <span data-ttu-id="a601b-108">A matriz de exibição realoca os objetos no mundo ao redor de uma posição de câmera - a origem do espaço da câmera - e orientação.</span><span class="sxs-lookup"><span data-stu-id="a601b-108">The view matrix relocates the objects in the world around a camera's position - the origin of camera space - and orientation.</span></span>

<span data-ttu-id="a601b-109">Há muitas maneiras de criar uma matriz de exibição.</span><span class="sxs-lookup"><span data-stu-id="a601b-109">There are many ways to create a view matrix.</span></span> <span data-ttu-id="a601b-110">Em todos os casos, a câmera tem algumas posições e orientações lógicas no espaço do mundo que são usadas como ponto de partida para criar uma matriz de exibição que será aplicada aos modelos em uma cena.</span><span class="sxs-lookup"><span data-stu-id="a601b-110">In all cases, the camera has some logical position and orientation in world space that is used as a starting point to create a view matrix that will be applied to the models in a scene.</span></span> <span data-ttu-id="a601b-111">A matriz de visualização é convertida e gira objetos para colocá-los no espaço da câmera, onde a câmera está na origem.</span><span class="sxs-lookup"><span data-stu-id="a601b-111">The view matrix translates and rotates objects to place them in camera space, where the camera is at the origin.</span></span> <span data-ttu-id="a601b-112">Uma maneira de criar uma matriz de exibição é combinar uma matriz de translação com matrizes de rotação para cada eixo.</span><span class="sxs-lookup"><span data-stu-id="a601b-112">One way to create a view matrix is to combine a translation matrix with rotation matrices for each axis.</span></span> <span data-ttu-id="a601b-113">Nesta abordagem, a seguinte equação de matriz geral se aplica.</span><span class="sxs-lookup"><span data-stu-id="a601b-113">In this approach, the following general matrix equation applies.</span></span>

![equação de transformação de exibição](images/viewtran.png)

<span data-ttu-id="a601b-115">Nessa fórmula, V é a matriz de visualização que está sendo criada, T é uma matriz de tradução que reposiciona objetos no mundo e Rₓ por R<sub>z</sub> são matrizes de rotação que giram objetos ao longo do eixo x, y e z.</span><span class="sxs-lookup"><span data-stu-id="a601b-115">In this formula, V is the view matrix being created, T is a translation matrix that repositions objects in the world, and Rₓ through R<sub>z</sub> are rotation matrices that rotate objects along the x-, y-, and z-axis.</span></span> <span data-ttu-id="a601b-116">As matrizes de translação e rotação se baseiam na posição e orientação lógicas da câmera no espaço do mundo.</span><span class="sxs-lookup"><span data-stu-id="a601b-116">The translation and rotation matrices are based on the camera's logical position and orientation in world space.</span></span> <span data-ttu-id="a601b-117">Portanto, se a posição lógica da câmera no mundo for <10, 20100>, o objetivo da matriz de conversão é mover objetos-10 unidades ao longo das unidades do eixo x,-20, ao longo do eixo y e-100 ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="a601b-117">So, if the camera's logical position in the world is <10,20,100>, the aim of the translation matrix is to move objects -10 units along the x-axis, -20 units along the y-axis, and -100 units along the z-axis.</span></span> <span data-ttu-id="a601b-118">As matrizes de rotação na fórmula são baseadas na orientação da câmera, em termos de quanto os eixos do espaço da câmera são girados para fora do alinhamento com o espaço do mundo.</span><span class="sxs-lookup"><span data-stu-id="a601b-118">The rotation matrices in the formula are based on the camera's orientation, in terms of how much the axes of camera space are rotated out of alignment with world space.</span></span> <span data-ttu-id="a601b-119">Por exemplo, se a câmera mencionada anteriormente estiver apontando diretamente para baixo, o seu eixo z é de 90 graus (pi/2 radianos) desalinhado com o eixo z do espaço do mundo, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="a601b-119">For example, if the camera mentioned earlier is pointing straight down, its z-axis is 90 degrees (pi/2 radians) out of alignment with the z-axis of world space, as shown in the following illustration.</span></span>

![Ilustração do espaço de exibição da câmera em comparação com o espaço do mundo](images/camtop.png)

<span data-ttu-id="a601b-121">As matrizes de rotação aplicam rotações de magnitude igual, porém oposta, aos modelos na cena.</span><span class="sxs-lookup"><span data-stu-id="a601b-121">The rotation matrices apply rotations of equal, but opposite, magnitude to the models in the scene.</span></span> <span data-ttu-id="a601b-122">A matriz de visualização de câmera inclui uma rotação de -90 graus em torno do eixo x.</span><span class="sxs-lookup"><span data-stu-id="a601b-122">The view matrix for this camera includes a rotation of -90 degrees around the x-axis.</span></span> <span data-ttu-id="a601b-123">A matriz de rotação é combinada com a matriz de translação para criar uma matriz de exibição que ajusta a posição e a orientação dos objetos na cena para que sua parte superior fique voltada para a câmera, dando a impressão de que a câmera está acima do modelo.</span><span class="sxs-lookup"><span data-stu-id="a601b-123">The rotation matrix is combined with the translation matrix to create a view matrix that adjusts the position and orientation of the objects in the scene so that their top is facing the camera, giving the appearance that the camera is above the model.</span></span>

## <a name="setting-up-a-view-matrix"></a><span data-ttu-id="a601b-124">Configurando uma matriz de exibição</span><span class="sxs-lookup"><span data-stu-id="a601b-124">Setting Up a View Matrix</span></span>

<span data-ttu-id="a601b-125">As funções auxiliares [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) e [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) criam uma matriz de exibição com base no local da câmera e um ponto de visão.</span><span class="sxs-lookup"><span data-stu-id="a601b-125">The [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) and [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) helper functions create a view matrix based on the camera location and a look-at point.</span></span>

<span data-ttu-id="a601b-126">O exemplo a seguir cria uma matriz de exibição para coordenadas da mão esquerda.</span><span class="sxs-lookup"><span data-stu-id="a601b-126">The following example creates a view matrix for left-handed coordinates.</span></span>


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



<span data-ttu-id="a601b-127">O Direct3D usa as matrizes de mundo e modo de exibição para configurar várias estruturas de dados internas.</span><span class="sxs-lookup"><span data-stu-id="a601b-127">Direct3D uses the world and view matrices to configure several internal data structures.</span></span> <span data-ttu-id="a601b-128">Cada vez que você define um novo mundo ou uma matriz de exibição, o sistema recalcula as estruturas internas associadas.</span><span class="sxs-lookup"><span data-stu-id="a601b-128">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="a601b-129">Definir essas matrizes com frequência é algo computacionalmente demorado.</span><span class="sxs-lookup"><span data-stu-id="a601b-129">Setting these matrices frequently is computationally time-consuming.</span></span> <span data-ttu-id="a601b-130">Você pode minimizar o número de cálculos necessários concatenando as matrizes de mundo e modo de exibição em uma matriz de exibição de mundo que você define como matriz de mundo, e, em seguida, definindo a matriz de visualização para a identidade.</span><span class="sxs-lookup"><span data-stu-id="a601b-130">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="a601b-131">Mantenha cópias em cache das matrizes individuais de mundo e modo de exibição para que você possa modificar, concatenar e restaurar a matriz de mundo conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="a601b-131">Keep cached copies of individual world and view matrices that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="a601b-132">Para maior clareza, os exemplos raramente empregam essa otimização.</span><span class="sxs-lookup"><span data-stu-id="a601b-132">For clarity, the samples rarely employ this optimization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a601b-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a601b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a601b-134">Transformações</span><span class="sxs-lookup"><span data-stu-id="a601b-134">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



