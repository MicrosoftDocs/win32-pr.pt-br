---
description: Em todo o Direct3D, os vértices descrevem a posição e a orientação. Cada vértice em uma primitiva é descrito por um vetor que oferece suas coordenadas de textura, cor e posição, e um vetor normal que oferece a sua orientação.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vetores, vértices e quaternions (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500328"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a><span data-ttu-id="88ca7-104">Vetores, vértices e quaternions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="88ca7-104">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>

<span data-ttu-id="88ca7-105">Em todo o Direct3D, os vértices descrevem a posição e a orientação.</span><span class="sxs-lookup"><span data-stu-id="88ca7-105">Throughout Direct3D, vertices describe position and orientation.</span></span> <span data-ttu-id="88ca7-106">Cada vértice em uma primitiva é descrito por um vetor que oferece suas coordenadas de textura, cor e posição, e um vetor normal que oferece a sua orientação.</span><span class="sxs-lookup"><span data-stu-id="88ca7-106">Each vertex in a primitive is described by a vector that gives its position, color, texture coordinates, and a normal vector that gives its orientation.</span></span>

<span data-ttu-id="88ca7-107">Os quaternions adicionam um quarto elemento aos \[ valores x, y, z \] que definem um vetor de três componentes.</span><span class="sxs-lookup"><span data-stu-id="88ca7-107">Quaternions add a fourth element to the \[x, y, z\] values that define a three-component-vector.</span></span> <span data-ttu-id="88ca7-108">Os quatérnios são uma alternativa aos métodos de matriz que são normalmente usados para rotações 3D.</span><span class="sxs-lookup"><span data-stu-id="88ca7-108">Quaternions are an alternative to the matrix methods that are typically used for 3D rotations.</span></span> <span data-ttu-id="88ca7-109">Um quatérnio representa um eixo no espaço 3D e uma rotação em torno do eixo em questão.</span><span class="sxs-lookup"><span data-stu-id="88ca7-109">A quaternion represents an axis in 3D space and a rotation around that axis.</span></span> <span data-ttu-id="88ca7-110">Por exemplo, um quatérnio pode representar um eixo (1,1,2) e uma rotação de 1 radiano.</span><span class="sxs-lookup"><span data-stu-id="88ca7-110">For example, a quaternion might represent a (1,1,2) axis and a rotation of 1 radian.</span></span> <span data-ttu-id="88ca7-111">Os quatérnios transportam informações úteis, mas seu verdadeiro valor é proveniente das duas operações que você pode executar neles: composição e interpolação.</span><span class="sxs-lookup"><span data-stu-id="88ca7-111">Quaternions carry valuable information, but their true power comes from the two operations that you can perform on them: composition and interpolation.</span></span>

<span data-ttu-id="88ca7-112">Realizar a composição em quatérnios é semelhante a combiná-los.</span><span class="sxs-lookup"><span data-stu-id="88ca7-112">Performing composition on quaternions is similar to combining them.</span></span> <span data-ttu-id="88ca7-113">A composição de dois quatérnios é representada como a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="88ca7-113">The composition of two quaternions is notated like the following illustration.</span></span>

![Ilustração de notação de quatérnio](images/quateq.png)

<span data-ttu-id="88ca7-115">A composição de dois quatérnios aplicados a uma geometria significa "girar a geometria ao redor do eixo₂ com rotação₂ e, em seguida, girá-la ao redor do eixo₁ com rotação₁."</span><span class="sxs-lookup"><span data-stu-id="88ca7-115">The composition of two quaternions applied to a geometry means "rotate the geometry around axis₂ by rotation₂, then rotate it around axis₁ by rotation₁."</span></span> <span data-ttu-id="88ca7-116">Nesse caso, Q representa uma rotação em torno de um eixo único que é o resultado da aplicação de q₂, e, em seguida, q₁ à geometria.</span><span class="sxs-lookup"><span data-stu-id="88ca7-116">In this case, Q represents a rotation around a single axis that is the result of applying q₂, then q₁ to the geometry.</span></span>

<span data-ttu-id="88ca7-117">Usando a interpolação de quatérnio, um aplicativo pode calcular um caminho suave e razoável de um eixo e orientação para outro.</span><span class="sxs-lookup"><span data-stu-id="88ca7-117">Using quaternion interpolation, an application can calculate a smooth and reasonable path from one axis and orientation to another.</span></span> <span data-ttu-id="88ca7-118">Portanto, a interpolação entre q₁ e q₂ fornece uma maneira simples de fazer a animação de uma orientação para outra.</span><span class="sxs-lookup"><span data-stu-id="88ca7-118">Therefore, interpolation between q₁ and q₂ provides a simple way to animate from one orientation to another.</span></span>

<span data-ttu-id="88ca7-119">Quando você usa composição e interpolação juntos, eles fornecem uma maneira simples de manipular uma geometria de maneira que se pareça complexa.</span><span class="sxs-lookup"><span data-stu-id="88ca7-119">When you use composition and interpolation together, they provide you with a simple way to manipulate a geometry in a manner that appears complex.</span></span> <span data-ttu-id="88ca7-120">Por exemplo, imagine que você tenha uma geometria que você deseja girar para uma determinada orientação.</span><span class="sxs-lookup"><span data-stu-id="88ca7-120">For example, imagine that you have a geometry that you want to rotate to a given orientation.</span></span> <span data-ttu-id="88ca7-121">Você sabe que você deseja girá-la r₂ graus em torno do eixo₂, em seguida, girá-la r₁ graus em torno do eixo₁, mas você não sabe o quatérnio final.</span><span class="sxs-lookup"><span data-stu-id="88ca7-121">You know that you want to rotate it r₂ degrees around axis₂, then rotate it r₁ degrees around axis₁, but you don't know the final quaternion.</span></span> <span data-ttu-id="88ca7-122">Usando a composição, você pode combinar as duas rotações na geometria para obter um único quaternion que é o resultado.</span><span class="sxs-lookup"><span data-stu-id="88ca7-122">By using composition, you could combine the two rotations on the geometry to get a single quaternion that is the result.</span></span> <span data-ttu-id="88ca7-123">Em seguida, você pode interpolar do original para o quaternion composto para atingir uma transição suave de um para outro.</span><span class="sxs-lookup"><span data-stu-id="88ca7-123">Then, you could interpolate from the original to the composed quaternion to achieve a smooth transition from one to the other.</span></span>

<span data-ttu-id="88ca7-124">A biblioteca do utilitário D3DX inclui funções que ajudam você a trabalhar com quaternions.</span><span class="sxs-lookup"><span data-stu-id="88ca7-124">The D3DX utility library includes functions that help you work with quaternions.</span></span> <span data-ttu-id="88ca7-125">Por exemplo, a função [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) adiciona um valor de rotação a um vetor que define um eixo de rotação e retorna o resultado em um Quaternion definido por uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="88ca7-125">For example, the [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) function adds a rotation value to a vector that defines an axis of rotation, and returns the result in a quaternion defined by a [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span> <span data-ttu-id="88ca7-126">Além disso, a função [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) compõe quaternions e o [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) executa interpolação linear esférica entre dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="88ca7-126">Additionally, the [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) function composes quaternions and the [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) performs spherical linear interpolation between two quaternions.</span></span>

<span data-ttu-id="88ca7-127">Os aplicativos Direct3D podem usar as seguintes funções para simplificar a tarefa de trabalhar com quaternions.</span><span class="sxs-lookup"><span data-stu-id="88ca7-127">Direct3D applications can use the following functions to simplify the task of working with quaternions.</span></span>

-   [<span data-ttu-id="88ca7-128">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="88ca7-128">**D3DXQuaternionBaryCentric**</span></span>](d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="88ca7-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="88ca7-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
-   [<span data-ttu-id="88ca7-130">**D3DXQuaternionDot**</span><span class="sxs-lookup"><span data-stu-id="88ca7-130">**D3DXQuaternionDot**</span></span>](d3dxquaterniondot.md)
-   [<span data-ttu-id="88ca7-131">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="88ca7-131">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
-   [<span data-ttu-id="88ca7-132">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="88ca7-132">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
-   [<span data-ttu-id="88ca7-133">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="88ca7-133">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
-   [<span data-ttu-id="88ca7-134">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="88ca7-134">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
-   [<span data-ttu-id="88ca7-135">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="88ca7-135">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
-   [<span data-ttu-id="88ca7-136">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="88ca7-136">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
-   [<span data-ttu-id="88ca7-137">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="88ca7-137">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
-   [<span data-ttu-id="88ca7-138">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="88ca7-138">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
-   [<span data-ttu-id="88ca7-139">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="88ca7-139">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
-   [<span data-ttu-id="88ca7-140">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="88ca7-140">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="88ca7-141">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="88ca7-141">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="88ca7-142">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="88ca7-142">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="88ca7-143">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="88ca7-143">**D3DXQuaternionSlerp**</span></span>](d3dxquaternionslerp.md)
-   [<span data-ttu-id="88ca7-144">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="88ca7-144">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
-   [<span data-ttu-id="88ca7-145">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="88ca7-145">**D3DXQuaternionToAxisAngle**</span></span>](d3dxquaterniontoaxisangle.md)

<span data-ttu-id="88ca7-146">Os aplicativos do Direct3D podem usar as seguintes funções para simplificar a tarefa de trabalhar com vetores de três componentes.</span><span class="sxs-lookup"><span data-stu-id="88ca7-146">Direct3D applications can use the following functions to simplify the task of working with three-component-vectors.</span></span>

-   [<span data-ttu-id="88ca7-147">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="88ca7-147">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
-   [<span data-ttu-id="88ca7-148">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="88ca7-148">**D3DXVec3BaryCentric**</span></span>](d3dxvec3barycentric.md)
-   [<span data-ttu-id="88ca7-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="88ca7-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
-   [<span data-ttu-id="88ca7-150">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="88ca7-150">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
-   [<span data-ttu-id="88ca7-151">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="88ca7-151">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
-   [<span data-ttu-id="88ca7-152">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="88ca7-152">**D3DXVec3Hermite**</span></span>](d3dxvec3hermite.md)
-   [<span data-ttu-id="88ca7-153">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="88ca7-153">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
-   [<span data-ttu-id="88ca7-154">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="88ca7-154">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
-   [<span data-ttu-id="88ca7-155">**D3DXVec3Lerp**</span><span class="sxs-lookup"><span data-stu-id="88ca7-155">**D3DXVec3Lerp**</span></span>](d3dxvec3lerp.md)
-   [<span data-ttu-id="88ca7-156">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="88ca7-156">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
-   [<span data-ttu-id="88ca7-157">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="88ca7-157">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
-   [<span data-ttu-id="88ca7-158">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="88ca7-158">**D3DXVec3Normalize**</span></span>](d3dxvec3normalize.md)
-   [<span data-ttu-id="88ca7-159">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="88ca7-159">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
-   [<span data-ttu-id="88ca7-160">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="88ca7-160">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
-   [<span data-ttu-id="88ca7-161">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="88ca7-161">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
-   [<span data-ttu-id="88ca7-162">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="88ca7-162">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
-   [<span data-ttu-id="88ca7-163">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="88ca7-163">**D3DXVec3TransformCoord**</span></span>](d3dxvec3transformcoord.md)
-   [<span data-ttu-id="88ca7-164">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="88ca7-164">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
-   [<span data-ttu-id="88ca7-165">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="88ca7-165">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)

<span data-ttu-id="88ca7-166">Muitas funções adicionais que simplificam tarefas usando dois e quatro componentes-vetores são incluídas entre as [funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md) fornecidas pela biblioteca do utilitário D3DX.</span><span class="sxs-lookup"><span data-stu-id="88ca7-166">Many additional functions that simplify tasks using two- and four-component-vectors are included among the [Math Functions](dx9-graphics-reference-d3dx-functions-math.md) supplied by the D3DX utility library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88ca7-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88ca7-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88ca7-168">Coordenar sistemas e geometria</span><span class="sxs-lookup"><span data-stu-id="88ca7-168">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



