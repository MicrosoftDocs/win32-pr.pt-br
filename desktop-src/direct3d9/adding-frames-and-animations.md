---
description: Esta seção mostra como adicionar quadros e animações a um cubo simples.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Adicionando quadros e animações (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785193"
---
# <a name="adding-frames-and-animations-direct3d-9"></a>Adicionando quadros e animações (Direct3D 9)

Esta seção mostra como adicionar quadros e animações a um cubo simples.

## <a name="working-with-frames"></a>Trabalhando com quadros

Espera-se que um quadro faça a seguinte estrutura.


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



Coloque a malha de cubo definida dentro de um quadro com uma transformação de identidade. Em seguida, aplique uma animação a este quadro.


```
Frame CubeFrame {
FrameTransformMatrix {
1.000000, 0.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000,
0.000000, 0.000000, 1.000000, 0.000000,
0.000000, 0.000000, 0.000000, 1.000000;;
}
{CubeMesh}        // You could have the mesh inline, but this 
                  // uses an object reference instead.
}
```



## <a name="working-with-animations"></a>Trabalhando com animações

Uma animação é definida por um conjunto de chaves. Uma chave é um valor de tempo associado a uma operação de dimensionamento, uma orientação ou uma posição.


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



Em seguida, as animações são agrupadas em AnimationSets:


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



Agora, pegue o cubo por meio de uma animação.


```
AnimationSet AnimationSet0 {
Animation Animation0 {
{CubeFrame}    // Use the frame containing the cube.
AnimationKey {
2;             // Position keys
9;             // 9 keys
10; 3; -100.000000, 0.000000, 0.000000;;,
20; 3; -75.000000, 0.000000, 0.000000;;,
30; 3; -50.000000, 0.000000, 0.000000;;,
40; 3; -25.500000, 0.000000, 0.000000;;,
50; 3; 0.000000, 0.000000, 0.000000;;,
60; 3; 25.500000, 0.000000, 0.000000;;,
70; 3; 50.000000, 0.000000, 0.000000;;,
80; 3; 75.500000, 0.000000, 0.000000;;,
90; 3; 100.000000, 0.000000, 0.000000;;;
}
}
}
```



Para obter mais informações, consulte a [**animação**](animation.md) e os modelos de [**animação**](animationset.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos X (herdados)](x-files--legacy-.md)
</dt> </dl>

 

 



