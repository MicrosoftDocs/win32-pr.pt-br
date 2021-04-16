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
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a>Vetores, vértices e quaternions (Direct3D 9)

Em todo o Direct3D, os vértices descrevem a posição e a orientação. Cada vértice em uma primitiva é descrito por um vetor que oferece suas coordenadas de textura, cor e posição, e um vetor normal que oferece a sua orientação.

Os quaternions adicionam um quarto elemento aos \[ valores x, y, z \] que definem um vetor de três componentes. Os quatérnios são uma alternativa aos métodos de matriz que são normalmente usados para rotações 3D. Um quatérnio representa um eixo no espaço 3D e uma rotação em torno do eixo em questão. Por exemplo, um quatérnio pode representar um eixo (1,1,2) e uma rotação de 1 radiano. Os quatérnios transportam informações úteis, mas seu verdadeiro valor é proveniente das duas operações que você pode executar neles: composição e interpolação.

Realizar a composição em quatérnios é semelhante a combiná-los. A composição de dois quatérnios é representada como a ilustração a seguir.

![Ilustração de notação de quatérnio](images/quateq.png)

A composição de dois quatérnios aplicados a uma geometria significa "girar a geometria ao redor do eixo₂ com rotação₂ e, em seguida, girá-la ao redor do eixo₁ com rotação₁." Nesse caso, Q representa uma rotação em torno de um eixo único que é o resultado da aplicação de q₂, e, em seguida, q₁ à geometria.

Usando a interpolação de quatérnio, um aplicativo pode calcular um caminho suave e razoável de um eixo e orientação para outro. Portanto, a interpolação entre q₁ e q₂ fornece uma maneira simples de fazer a animação de uma orientação para outra.

Quando você usa composição e interpolação juntos, eles fornecem uma maneira simples de manipular uma geometria de maneira que se pareça complexa. Por exemplo, imagine que você tenha uma geometria que você deseja girar para uma determinada orientação. Você sabe que você deseja girá-la r₂ graus em torno do eixo₂, em seguida, girá-la r₁ graus em torno do eixo₁, mas você não sabe o quatérnio final. Usando a composição, você pode combinar as duas rotações na geometria para obter um único quaternion que é o resultado. Em seguida, você pode interpolar do original para o quaternion composto para atingir uma transição suave de um para outro.

A biblioteca do utilitário D3DX inclui funções que ajudam você a trabalhar com quaternions. Por exemplo, a função [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) adiciona um valor de rotação a um vetor que define um eixo de rotação e retorna o resultado em um Quaternion definido por uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) . Além disso, a função [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) compõe quaternions e o [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) executa interpolação linear esférica entre dois quaternions.

Os aplicativos Direct3D podem usar as seguintes funções para simplificar a tarefa de trabalhar com quaternions.

-   [**D3DXQuaternionBaryCentric**](d3dxquaternionbarycentric.md)
-   [**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
-   [**D3DXQuaternionDot**](d3dxquaterniondot.md)
-   [**D3DXQuaternionExp**](d3dxquaternionexp.md)
-   [**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
-   [**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
-   [**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
-   [**D3DXQuaternionLength**](d3dxquaternionlength.md)
-   [**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
-   [**D3DXQuaternionLn**](d3dxquaternionln.md)
-   [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
-   [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
-   [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
-   [**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
-   [**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
-   [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md)
-   [**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
-   [**D3DXQuaternionToAxisAngle**](d3dxquaterniontoaxisangle.md)

Os aplicativos do Direct3D podem usar as seguintes funções para simplificar a tarefa de trabalhar com vetores de três componentes.

-   [**D3DXVec3Add**](d3dxvec3add.md)
-   [**D3DXVec3BaryCentric**](d3dxvec3barycentric.md)
-   [**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
-   [**D3DXVec3Cross**](d3dxvec3cross.md)
-   [**D3DXVec3Dot**](d3dxvec3dot.md)
-   [**D3DXVec3Hermite**](d3dxvec3hermite.md)
-   [**D3DXVec3Length**](d3dxvec3length.md)
-   [**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
-   [**D3DXVec3Lerp**](d3dxvec3lerp.md)
-   [**D3DXVec3Maximize**](d3dxvec3maximize.md)
-   [**D3DXVec3Minimize**](d3dxvec3minimize.md)
-   [**D3DXVec3Normalize**](d3dxvec3normalize.md)
-   [**D3DXVec3Project**](d3dxvec3project.md)
-   [**D3DXVec3Scale**](d3dxvec3scale.md)
-   [**D3DXVec3Subtract**](d3dxvec3subtract.md)
-   [**D3DXVec3Transform**](d3dxvec3transform.md)
-   [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md)
-   [**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
-   [**D3DXVec3Unproject**](d3dxvec3unproject.md)

Muitas funções adicionais que simplificam tarefas usando dois e quatro componentes-vetores são incluídas entre as [funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md) fornecidas pela biblioteca do utilitário D3DX.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenar sistemas e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



