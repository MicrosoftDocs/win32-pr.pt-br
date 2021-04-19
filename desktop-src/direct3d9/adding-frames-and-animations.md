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
# <a name="adding-frames-and-animations-direct3d-9"></a><span data-ttu-id="b4825-103">Adicionando quadros e animações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4825-103">Adding Frames and Animations (Direct3D 9)</span></span>

<span data-ttu-id="b4825-104">Esta seção mostra como adicionar quadros e animações a um cubo simples.</span><span class="sxs-lookup"><span data-stu-id="b4825-104">This section shows how to add frames and animations to a simple cube.</span></span>

## <a name="working-with-frames"></a><span data-ttu-id="b4825-105">Trabalhando com quadros</span><span class="sxs-lookup"><span data-stu-id="b4825-105">Working with Frames</span></span>

<span data-ttu-id="b4825-106">Espera-se que um quadro faça a seguinte estrutura.</span><span class="sxs-lookup"><span data-stu-id="b4825-106">A frame is expected to take the following structure.</span></span>


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



<span data-ttu-id="b4825-107">Coloque a malha de cubo definida dentro de um quadro com uma transformação de identidade.</span><span class="sxs-lookup"><span data-stu-id="b4825-107">Place the defined cube mesh inside a frame with an identity transform.</span></span> <span data-ttu-id="b4825-108">Em seguida, aplique uma animação a este quadro.</span><span class="sxs-lookup"><span data-stu-id="b4825-108">Then apply an animation to this frame.</span></span>


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



## <a name="working-with-animations"></a><span data-ttu-id="b4825-109">Trabalhando com animações</span><span class="sxs-lookup"><span data-stu-id="b4825-109">Working with Animations</span></span>

<span data-ttu-id="b4825-110">Uma animação é definida por um conjunto de chaves.</span><span class="sxs-lookup"><span data-stu-id="b4825-110">An animation is defined by a set of keys.</span></span> <span data-ttu-id="b4825-111">Uma chave é um valor de tempo associado a uma operação de dimensionamento, uma orientação ou uma posição.</span><span class="sxs-lookup"><span data-stu-id="b4825-111">A key is a time value associated with a scaling operation, an orientation, or a position.</span></span>


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



<span data-ttu-id="b4825-112">Em seguida, as animações são agrupadas em AnimationSets:</span><span class="sxs-lookup"><span data-stu-id="b4825-112">Animations are then grouped into AnimationSets:</span></span>


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



<span data-ttu-id="b4825-113">Agora, pegue o cubo por meio de uma animação.</span><span class="sxs-lookup"><span data-stu-id="b4825-113">Now take the cube through an animation.</span></span>


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



<span data-ttu-id="b4825-114">Para obter mais informações, consulte a [**animação**](animation.md) e os modelos de [**animação**](animationset.md) .</span><span class="sxs-lookup"><span data-stu-id="b4825-114">For more information, see the [**Animation**](animation.md) and [**AnimationSet**](animationset.md) templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4825-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4825-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4825-116">Arquivos X (herdados)</span><span class="sxs-lookup"><span data-stu-id="b4825-116">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



