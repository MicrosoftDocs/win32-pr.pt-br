---
description: A maioria dos aplicativos de CAD e de desenho fornece recursos que dimensionam a saída criada pelo usuário.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Scaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968088"
---
# <a name="scaling"></a><span data-ttu-id="f73a3-103">Scaling</span><span class="sxs-lookup"><span data-stu-id="f73a3-103">Scaling</span></span>

<span data-ttu-id="f73a3-104">A maioria dos aplicativos de CAD e de desenho fornece recursos que dimensionam a saída criada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f73a3-104">Most CAD and drawing applications provide features that scale output created by the user.</span></span> <span data-ttu-id="f73a3-105">Os aplicativos que incluem recursos de dimensionamento (ou zoom) chamam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir o espaço mundial apropriado para a transformação de espaço em página.</span><span class="sxs-lookup"><span data-stu-id="f73a3-105">Applications that include scaling (or zoom) capabilities call the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="f73a3-106">Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="f73a3-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="f73a3-107">Os membros eM11 e eM22 do XFORM especificam os componentes de dimensionamento horizontal e vertical, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f73a3-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical scaling components, respectively.</span></span>

<span data-ttu-id="f73a3-108">Quando ocorre o *dimensionamento* , as linhas vertical e horizontal (ou vetores), que constituem um objeto, são ampliadas ou compactadas com relação ao eixo x ou y.</span><span class="sxs-lookup"><span data-stu-id="f73a3-108">When *scaling* occurs, the vertical and horizontal lines (or vectors), that constitute an object, are stretched or compressed with respect to the x- or y-axis.</span></span> <span data-ttu-id="f73a3-109">A ilustração a seguir mostra um retângulo de 20 por 20 unidades dimensionado verticalmente para duas vezes sua altura original quando copiado do espaço de coordenadas mundiais para o espaço de coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="f73a3-109">The following illustration shows a 20-by-20-unit rectangle scaled vertically to twice its original height when copied from world-coordinate space to page-coordinate space.</span></span>

![ilustração mostrando um pequeno retângulo no espaço do mundo e um mais alto no espaço da página](images/cstrn-10.png)

<span data-ttu-id="f73a3-111">Na ilustração anterior, as linhas verticais que definem a medida do lado do retângulo original 20 unidades, enquanto as linhas verticais que definem os lados do retângulo dimensionado medem 40 unidades.</span><span class="sxs-lookup"><span data-stu-id="f73a3-111">In the preceding illustration, the vertical lines that define the original rectangle's side measure 20 units, while the vertical lines that define the scaled rectangle's sides measure 40 units.</span></span>

<span data-ttu-id="f73a3-112">O dimensionamento vertical pode ser representado pelo seguinte algoritmo.</span><span class="sxs-lookup"><span data-stu-id="f73a3-112">Vertical scaling can be represented by the following algorithm.</span></span>

``` syntax
y' = y * Dy 
```

<span data-ttu-id="f73a3-113">Onde y ' é o novo comprimento, y é o comprimento original e dy é o fator de dimensionamento vertical.</span><span class="sxs-lookup"><span data-stu-id="f73a3-113">Where y' is the new length, y is the original length, and Dy is the vertical scaling factor.</span></span>

<span data-ttu-id="f73a3-114">O dimensionamento horizontal pode ser representado pelo seguinte algoritmo.</span><span class="sxs-lookup"><span data-stu-id="f73a3-114">Horizontal scaling can be represented by the following algorithm.</span></span>

``` syntax
x' = x * Dx 
```

<span data-ttu-id="f73a3-115">Onde x ' é o novo comprimento, x é o comprimento original e DX é o fator de dimensionamento horizontal.</span><span class="sxs-lookup"><span data-stu-id="f73a3-115">Where x' is the new length, x is the original length, and Dx is the horizontal scaling factor.</span></span>

<span data-ttu-id="f73a3-116">As transformações de escala vertical e horizontal podem ser combinadas em uma única operação usando uma matriz 2-por-2.</span><span class="sxs-lookup"><span data-stu-id="f73a3-116">The vertical and horizontal scaling transformations can be combined into a single operation by using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

<span data-ttu-id="f73a3-117">A matriz 2-por-2 que produziu a transformação dimensionamento contém os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f73a3-117">The 2-by-2 matrix that produced the scaling transformation contains the following values.</span></span>

``` syntax
|1    0| 
|0    2| 
```

 

 



