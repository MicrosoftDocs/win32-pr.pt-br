---
description: A biblioteca do utilitário D3DX fornece a interface ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Pilhas de matrizes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a480236bc42142b725e232a9fb92807be73fb03097104a0cc4fc08643f4361af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044316"
---
# <a name="matrix-stacks-direct3d-9"></a>Pilhas de matrizes (Direct3D 9)

A biblioteca do utilitário D3DX fornece a interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) . Ele fornece um mecanismo para permitir que as matrizes sejam enviadas e retiradas de uma pilha de matriz. A implementação de uma pilha de matriz é uma maneira eficiente de rastrear matrizes durante a passagem de uma hierarquia de transformação.

A biblioteca do utilitário D3DX usa uma pilha de matriz para armazenar transformações como matrizes. Os vários métodos da interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) lidam com a matriz atual ou com a matriz localizada na parte superior da pilha. Você pode limpar a matriz atual com o método [**ID3DXMATRIXStack:: loadidentity**](id3dxmatrixstack--loadidentity.md) . Para especificar explicitamente uma determinada matriz a ser carregada como a matriz de transformação atual, use o método [**ID3DXMATRIXStack:: loadmatrix**](id3dxmatrixstack--loadmatrix.md) . Em seguida, você pode chamar o método [**ID3DXMATRIXStack:: MultMatrix**](id3dxmatrixstack--multmatrix.md) ou o método [**ID3DXMATRIXStack:: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) para multiplicar a matriz atual pela matriz especificada.

O método [**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) permite retornar à matriz de transformação anterior e o método [**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md) adiciona uma matriz de transformação à pilha.

As matrizes individuais na pilha de matriz são representadas como matrizes homogêneos 4x4, definidas pela estrutura [**D3DXMATRIX**](d3dxmatrix.md) de biblioteca D3DX Utility.

A biblioteca do utilitário D3DX fornece uma pilha de matriz por meio de um objeto COM (Component Object Model).

## <a name="implementing-a-scene-hierarchy"></a>Implementando uma hierarquia de cena

Uma pilha de matriz simplifica a construção de modelos hierárquicos, em que objetos complicados são construídos a partir de uma série de objetos mais simples.

Uma cena, ou uma hierarquia, geralmente é representada por uma estrutura de dados de árvore. Cada nó na estrutura de dados de árvore contém uma matriz. Uma matriz específica representa a alteração em sistemas de coordenadas do pai do nó para o nó. Por exemplo, se você estiver modelando um braço humano, poderá implementar a hierarquia que é mostrada no diagrama a seguir.

![diagrama da hierarquia de um braço humano](images/stack1.png)

Nessa hierarquia, a matriz de corpo coloca o corpo do mundo. A matriz UpperArm contém a rotação do ressalto, a matriz LowerArm contém a rotação do cotovelo e a matriz Hand contém a rotação do pulso. Para determinar onde a mão é relativa ao mundo, você multiplica todas as matrizes do corpo até a mão.

A hierarquia anterior é excessivamente simplista, pois cada nó tem apenas um filho. Se você começar a modelar a mão com mais detalhes, provavelmente adicionará dedos e um polegar. Cada dígito pode ser adicionado à hierarquia como filhos de mão, conforme mostrado no diagrama a seguir.

![diagrama da hierarquia de uma mão humana](images/stack2.png)

Se você percorrer o grafo completo do ARM em ordem decrescente – atravessando o máximo possível de um caminho antes de passar para o próximo caminho – para desenhar a cena, execute uma sequência de renderização segmentada. Por exemplo, para renderizar a mão e os dedos, você implementa o padrão a seguir.

1.  Pressione a matriz de mãos para a pilha de matriz.
2.  Desenhe a mão.
3.  Envie a matriz Thumb para a pilha de matriz.
4.  Desenhe o polegar.
5.  Retirar a matriz Thumb da pilha.
6.  Empurrar a matriz de dedo 1 para a pilha de matriz.
7.  Desenhe o primeiro dedo.
8.  Retirar a matriz do dedo 1 da pilha.
9.  Envie por push a matriz Finger 2 para a pilha de matriz. Você continua dessa maneira até que todos os dedos e thumbs sejam renderizados.

Depois de concluir a renderização dos dedos, você colocaria a matriz na pilha.

Você pode seguir esse processo básico em código com os exemplos a seguir. Quando você encontrar um nó durante a pesquisa de profundidade da estrutura de dados de árvore, envie a matriz para a parte superior da pilha de matriz.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Quando você terminar com um nó, a matriz será exibida na parte superior da pilha de matriz.


```
MatrixStack->Pop();
```



Dessa forma, a matriz na parte superior da pilha sempre representa a transformação mundial do nó atual. Portanto, antes de desenhar cada nó, você deve definir a matriz Direct3D.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Para obter mais informações sobre os métodos específicos que você pode executar em uma pilha do D3DX Matrix, consulte o tópico de referência do [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 



