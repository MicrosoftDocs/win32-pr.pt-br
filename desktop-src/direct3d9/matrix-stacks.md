---
description: A biblioteca do utilitário D3DX fornece a interface ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Pilhas de matrizes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825832"
---
# <a name="matrix-stacks-direct3d-9"></a><span data-ttu-id="4d0ca-103">Pilhas de matrizes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4d0ca-103">Matrix Stacks (Direct3D 9)</span></span>

<span data-ttu-id="4d0ca-104">A biblioteca do utilitário D3DX fornece a interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="4d0ca-104">The D3DX utility library provides the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span> <span data-ttu-id="4d0ca-105">Ele fornece um mecanismo para permitir que as matrizes sejam enviadas e retiradas de uma pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-105">It supplies a mechanism to enable matrices to be pushed onto and popped off of a matrix stack.</span></span> <span data-ttu-id="4d0ca-106">A implementação de uma pilha de matriz é uma maneira eficiente de rastrear matrizes durante a passagem de uma hierarquia de transformação.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-106">Implementing a matrix stack is an efficient way to track matrices while traversing a transform hierarchy.</span></span>

<span data-ttu-id="4d0ca-107">A biblioteca do utilitário D3DX usa uma pilha de matriz para armazenar transformações como matrizes.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-107">The D3DX utility library uses a matrix stack to store transformations as matrices.</span></span> <span data-ttu-id="4d0ca-108">Os vários métodos da interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) lidam com a matriz atual ou com a matriz localizada na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-108">The various methods of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface deal with the current matrix, or the matrix located on top of the stack.</span></span> <span data-ttu-id="4d0ca-109">Você pode limpar a matriz atual com o método [**ID3DXMATRIXStack:: loadidentity**](id3dxmatrixstack--loadidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="4d0ca-109">You can clear the current matrix with the [**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md) method.</span></span> <span data-ttu-id="4d0ca-110">Para especificar explicitamente uma determinada matriz a ser carregada como a matriz de transformação atual, use o método [**ID3DXMATRIXStack:: loadmatrix**](id3dxmatrixstack--loadmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="4d0ca-110">To explicitly specify a certain matrix to load as the current transformation matrix, use the [**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md) method.</span></span> <span data-ttu-id="4d0ca-111">Em seguida, você pode chamar o método [**ID3DXMATRIXStack:: MultMatrix**](id3dxmatrixstack--multmatrix.md) ou o método [**ID3DXMATRIXStack:: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) para multiplicar a matriz atual pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-111">Then you can call either the [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) method or the [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) method to multiply the current matrix by the specified matrix.</span></span>

<span data-ttu-id="4d0ca-112">O método [**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) permite retornar à matriz de transformação anterior e o método [**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md) adiciona uma matriz de transformação à pilha.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-112">The [**ID3DXMATRIXStack::Pop**](id3dxmatrixstack--pop.md) method enables you to return to the previous transformation matrix and the [**ID3DXMATRIXStack::Push**](id3dxmatrixstack--push.md) method adds a transformation matrix to the stack.</span></span>

<span data-ttu-id="4d0ca-113">As matrizes individuais na pilha de matriz são representadas como matrizes homogêneos 4x4, definidas pela estrutura [**D3DXMATRIX**](d3dxmatrix.md) de biblioteca D3DX Utility.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-113">The individual matrices on the matrix stack are represented as 4x4 homogeneous matrices, defined by the D3DX utility library [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

<span data-ttu-id="4d0ca-114">A biblioteca do utilitário D3DX fornece uma pilha de matriz por meio de um objeto COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="4d0ca-114">The D3DX utility library provides a matrix stack through a component object model (COM) object.</span></span>

## <a name="implementing-a-scene-hierarchy"></a><span data-ttu-id="4d0ca-115">Implementando uma hierarquia de cena</span><span class="sxs-lookup"><span data-stu-id="4d0ca-115">Implementing a Scene Hierarchy</span></span>

<span data-ttu-id="4d0ca-116">Uma pilha de matriz simplifica a construção de modelos hierárquicos, em que objetos complicados são construídos a partir de uma série de objetos mais simples.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-116">A matrix stack simplifies the construction of hierarchical models, in which complicated objects are constructed from a series of simpler objects.</span></span>

<span data-ttu-id="4d0ca-117">Uma cena, ou uma hierarquia, geralmente é representada por uma estrutura de dados de árvore.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-117">A scene, or transform, hierarchy is usually represented by a tree data structure.</span></span> <span data-ttu-id="4d0ca-118">Cada nó na estrutura de dados de árvore contém uma matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-118">Each node in the tree data structure contains a matrix.</span></span> <span data-ttu-id="4d0ca-119">Uma matriz específica representa a alteração em sistemas de coordenadas do pai do nó para o nó.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-119">A particular matrix represents the change in coordinate systems from the node's parent to the node.</span></span> <span data-ttu-id="4d0ca-120">Por exemplo, se você estiver modelando um braço humano, poderá implementar a hierarquia que é mostrada no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-120">For example, if you are modeling a human arm, you might implement the hierarchy that is shown in the following diagram.</span></span>

![diagrama da hierarquia de um braço humano](images/stack1.png)

<span data-ttu-id="4d0ca-122">Nessa hierarquia, a matriz de corpo coloca o corpo do mundo.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-122">In this hierarchy, the Body matrix places the body in the world.</span></span> <span data-ttu-id="4d0ca-123">A matriz UpperArm contém a rotação do ressalto, a matriz LowerArm contém a rotação do cotovelo e a matriz Hand contém a rotação do pulso.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-123">The UpperArm matrix contains the rotation of the shoulder, the LowerArm matrix contains the rotation of the elbow, and the Hand matrix contains the rotation of the wrist.</span></span> <span data-ttu-id="4d0ca-124">Para determinar onde a mão é relativa ao mundo, você multiplica todas as matrizes do corpo até a mão.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-124">To determine where the hand is relative to the world, you multiply all the matrices from Body down through Hand together.</span></span>

<span data-ttu-id="4d0ca-125">A hierarquia anterior é excessivamente simplista, pois cada nó tem apenas um filho.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-125">The previous hierarchy is overly simplistic, because each node has only one child.</span></span> <span data-ttu-id="4d0ca-126">Se você começar a modelar a mão com mais detalhes, provavelmente adicionará dedos e um polegar.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-126">If you begin to model the hand in more detail, you will probably add fingers and a thumb.</span></span> <span data-ttu-id="4d0ca-127">Cada dígito pode ser adicionado à hierarquia como filhos de mão, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-127">Each digit can be added to the hierarchy as children of Hand, as shown in the following diagram.</span></span>

![diagrama da hierarquia de uma mão humana](images/stack2.png)

<span data-ttu-id="4d0ca-129">Se você percorrer o grafo completo do ARM em ordem decrescente – atravessando o máximo possível de um caminho antes de passar para o próximo caminho – para desenhar a cena, execute uma sequência de renderização segmentada.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-129">If you traverse the complete graph of the arm in depth-first order - traversing as far down one path as possible before moving on to the next path - to draw the scene, you perform a sequence of segmented rendering.</span></span> <span data-ttu-id="4d0ca-130">Por exemplo, para renderizar a mão e os dedos, você implementa o padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-130">For example, to render the hand and fingers, you implement the following pattern.</span></span>

1.  <span data-ttu-id="4d0ca-131">Pressione a matriz de mãos para a pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-131">Push the Hand matrix onto the matrix stack.</span></span>
2.  <span data-ttu-id="4d0ca-132">Desenhe a mão.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-132">Draw the hand.</span></span>
3.  <span data-ttu-id="4d0ca-133">Envie a matriz Thumb para a pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-133">Push the Thumb matrix onto the matrix stack.</span></span>
4.  <span data-ttu-id="4d0ca-134">Desenhe o polegar.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-134">Draw the thumb.</span></span>
5.  <span data-ttu-id="4d0ca-135">Retirar a matriz Thumb da pilha.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-135">Pop the Thumb matrix off the stack.</span></span>
6.  <span data-ttu-id="4d0ca-136">Empurrar a matriz de dedo 1 para a pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-136">Push the Finger 1 matrix onto the matrix stack.</span></span>
7.  <span data-ttu-id="4d0ca-137">Desenhe o primeiro dedo.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-137">Draw the first finger.</span></span>
8.  <span data-ttu-id="4d0ca-138">Retirar a matriz do dedo 1 da pilha.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-138">Pop the Finger 1 matrix off the stack.</span></span>
9.  <span data-ttu-id="4d0ca-139">Envie por push a matriz Finger 2 para a pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-139">Push the Finger 2 matrix onto the matrix stack.</span></span> <span data-ttu-id="4d0ca-140">Você continua dessa maneira até que todos os dedos e thumbs sejam renderizados.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-140">You continue in this manner until all the fingers and thumb are rendered.</span></span>

<span data-ttu-id="4d0ca-141">Depois de concluir a renderização dos dedos, você colocaria a matriz na pilha.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-141">After you have completed rendering the fingers, you would pop the Hand matrix off the stack.</span></span>

<span data-ttu-id="4d0ca-142">Você pode seguir esse processo básico em código com os exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-142">You can follow this basic process in code with the following examples.</span></span> <span data-ttu-id="4d0ca-143">Quando você encontrar um nó durante a pesquisa de profundidade da estrutura de dados de árvore, envie a matriz para a parte superior da pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-143">When you encounter a node during the depth-first search of the tree data structure, push the matrix onto the top of the matrix stack.</span></span>


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



<span data-ttu-id="4d0ca-144">Quando você terminar com um nó, a matriz será exibida na parte superior da pilha de matriz.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-144">When you are finished with a node, pop the matrix off the top of the matrix stack.</span></span>


```
MatrixStack->Pop();
```



<span data-ttu-id="4d0ca-145">Dessa forma, a matriz na parte superior da pilha sempre representa a transformação mundial do nó atual.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-145">In this way, the matrix on the top of the stack always represents the world-transform of the current node.</span></span> <span data-ttu-id="4d0ca-146">Portanto, antes de desenhar cada nó, você deve definir a matriz Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-146">Therefore, before drawing each node, you should set the Direct3D matrix.</span></span>


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



<span data-ttu-id="4d0ca-147">Para obter mais informações sobre os métodos específicos que você pode executar em uma pilha do D3DX Matrix, consulte o tópico de referência do [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="4d0ca-147">For more information about the specific methods that you can perform on a D3DX matrix stack, see the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) reference topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d0ca-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d0ca-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d0ca-149">Pipeline de vértice</span><span class="sxs-lookup"><span data-stu-id="4d0ca-149">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



