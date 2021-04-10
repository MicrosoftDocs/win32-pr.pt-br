---
description: 'A posição, a velocidade e a orientação das fontes de som e dos ouvintes no espaço 3D são representadas por coordenadas cartesianas, que são valores em três eixos: o eixo x, o eixo y e o eixo z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordenadas do espaço 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170281"
---
# <a name="coordinates-of-3d-space"></a><span data-ttu-id="eec78-103">Coordenadas do espaço 3D</span><span class="sxs-lookup"><span data-stu-id="eec78-103">Coordinates of 3D Space</span></span>

<span data-ttu-id="eec78-104">A posição, a velocidade e a orientação das fontes de som e dos ouvintes no espaço 3D são representadas por coordenadas cartesianas, que são valores em três eixos: o eixo x, o eixo y e o eixo z.</span><span class="sxs-lookup"><span data-stu-id="eec78-104">The position, velocity, and orientation of sound sources and listeners in 3D space are represented by Cartesian coordinates, which are values on three axes: the x-axis, the y-axis, and the z-axis.</span></span>

<span data-ttu-id="eec78-105">Os eixos são relativos a um ponto de vista estabelecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eec78-105">The axes are relative to a viewpoint established by the application.</span></span> <span data-ttu-id="eec78-106">Os valores no eixo x aumentam da esquerda para a direita, no eixo y de baixo para cima e no eixo z de perto de longe.</span><span class="sxs-lookup"><span data-stu-id="eec78-106">Values on the x-axis increase from left to right, on the y-axis from down to up, and on the z-axis from near to far.</span></span>

<span data-ttu-id="eec78-107">A estrutura de **\_ vetor X3DAUDIO** contém valores que descrevem a posição, a velocidade ou a orientação nos três eixos.</span><span class="sxs-lookup"><span data-stu-id="eec78-107">The **X3DAUDIO\_VECTOR** structure contains values describing position, velocity, or orientation on the three axes.</span></span>

<span data-ttu-id="eec78-108">De forma convencional, os vetores são expressos como três valores entre parênteses e separados por vírgulas, na ordem (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="eec78-108">Conventionally, vectors are expressed as three values enclosed in parentheses and separated by commas, in the order (x, y, z).</span></span>

<span data-ttu-id="eec78-109">Para posição, os valores estão em unidades mundiais definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="eec78-109">For position, the values are in user-defined world units.</span></span>

<span data-ttu-id="eec78-110">Para a velocidade, o vetor descreve a taxa de movimentação ao longo de cada eixo em unidades mundiais por segundo.</span><span class="sxs-lookup"><span data-stu-id="eec78-110">For velocity, the vector describes the rate of movement along each axis in world units per second.</span></span>

<span data-ttu-id="eec78-111">Para orientação, os valores estão em unidades arbitrárias e são relativos uns aos outros.</span><span class="sxs-lookup"><span data-stu-id="eec78-111">For orientation, the values are in arbitrary units, and they are relative to one another.</span></span> <span data-ttu-id="eec78-112">Por exemplo, se a exibição de base do mundo 3D estiver voltada para o norte em direção ao horizonte, e a orientação do ouvinte for (-1, 0, 1), o ouvinte voltará para o noroeste.</span><span class="sxs-lookup"><span data-stu-id="eec78-112">For example, if the base view of the 3D world is facing north toward the horizon, and the orientation of the listener is (-1, 0, 1), then the listener is facing northwest.</span></span> <span data-ttu-id="eec78-113">Como os valores dentro de um vetor não estão em unidades absolutas, o vetor igualmente poderia ser expresso como (-5, 0, 5) ou (-0,25, 0, 0,25).</span><span class="sxs-lookup"><span data-stu-id="eec78-113">Because the values within a vector are not in absolute units, the vector equally could be expressed as (-5, 0, 5) or (-0.25, 0, 0.25).</span></span>

<span data-ttu-id="eec78-114">os vetores 3D funcionam de maneira muito semelhante a vetores 2D, mas com um eixo adicional na direção de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="eec78-114">3D vectors work much like 2D vectors, but with an additional axis in the up-down direction.</span></span> <span data-ttu-id="eec78-115">Você pode ver como os vetores funcionam em espaço 2D desenhando-os em uma folha de papel gráfico.</span><span class="sxs-lookup"><span data-stu-id="eec78-115">You can see how vectors work in 2D space by drawing them on a sheet of graph paper.</span></span> <span data-ttu-id="eec78-116">Deixe os valores aumentarem de baixo para a parte superior do papel e da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="eec78-116">Let the values increase from the bottom to the top of the paper, and from left to right.</span></span> <span data-ttu-id="eec78-117">Uma linha desenhada de (0, 0) para (1, 1) tem a mesma orientação, ou direção, como uma desenhada de (0, 0) para (5, 5).</span><span class="sxs-lookup"><span data-stu-id="eec78-117">A line drawn from (0, 0) to (1, 1) has the same orientation, or direction, as one drawn from (0, 0) to (5, 5).</span></span> <span data-ttu-id="eec78-118">No entanto, a segunda linha indica uma maior distância ou velocidade.</span><span class="sxs-lookup"><span data-stu-id="eec78-118">However, the second line indicates a greater distance, or velocity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eec78-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eec78-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eec78-120">Conceitos comuns de áudio</span><span class="sxs-lookup"><span data-stu-id="eec78-120">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="eec78-121">Visão geral do X3DAudio</span><span class="sxs-lookup"><span data-stu-id="eec78-121">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> </dl>

 

 



