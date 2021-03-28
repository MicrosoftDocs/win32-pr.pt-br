---
description: Alguns aplicativos fornecem recursos que distorcem objetos desenhados na área do cliente.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Quantidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170535"
---
# <a name="shear"></a><span data-ttu-id="44063-103">Quantidade</span><span class="sxs-lookup"><span data-stu-id="44063-103">Shear</span></span>

<span data-ttu-id="44063-104">Alguns aplicativos fornecem recursos que distorcem objetos desenhados na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="44063-104">Some applications provide features that shear objects drawn in the client area.</span></span> <span data-ttu-id="44063-105">Os aplicativos que usam recursos de distorção usam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir os valores apropriados no espaço mundial para a transformação de espaço em página.</span><span class="sxs-lookup"><span data-stu-id="44063-105">Applications that use shear capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="44063-106">Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="44063-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="44063-107">Os membros eM12 e eM21 do XFORM especificam as constantes Proportionality horizontais e verticais, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="44063-107">The eM12 and eM21 members of XFORM specify the horizontal and vertical proportionality constants, respectively.</span></span>

<span data-ttu-id="44063-108">Há dois componentes da *transformação distorcer*.</span><span class="sxs-lookup"><span data-stu-id="44063-108">There are two components of the *shear transformation*.</span></span> <span data-ttu-id="44063-109">O primeiro altera as linhas verticais em um objeto; o segundo altera as linhas horizontais.</span><span class="sxs-lookup"><span data-stu-id="44063-109">The first alters the vertical lines in an object; the second alters the horizontal lines.</span></span> <span data-ttu-id="44063-110">A ilustração a seguir mostra um retângulo de 20 por 20 unidades distorcido horizontalmente quando copiado do espaço de mundo para o espaço de página.</span><span class="sxs-lookup"><span data-stu-id="44063-110">The following illustration shows a 20-by-20-unit rectangle sheared horizontally when copied from world space to page space.</span></span>

![ilustração mostrando um retângulo no espaço do mundo e um trapeziod no espaço da página](images/cstrn-13.png)

<span data-ttu-id="44063-112">Uma distorção horizontal pode ser representada pelo seguinte algoritmo:</span><span class="sxs-lookup"><span data-stu-id="44063-112">A horizontal shear can be represented by the following algorithm:</span></span>

``` syntax
x' = x + (Sx * y) 
```

<span data-ttu-id="44063-113">em que x é a coordenada x original, SX é a constante Proportionality e x ' é o resultado da transformação distorcer.</span><span class="sxs-lookup"><span data-stu-id="44063-113">where x is the original x-coordinate, Sx is the proportionality constant, and x' is the result of the shear transformation.</span></span>

<span data-ttu-id="44063-114">Uma distorção vertical pode ser representada pelo seguinte algoritmo:</span><span class="sxs-lookup"><span data-stu-id="44063-114">A vertical shear can be represented by the following algorithm:</span></span>

``` syntax
y' = y + (Sy * x) 
```

<span data-ttu-id="44063-115">em que y é a coordenada y original, Sy é a constante Proportionality e y ' é o resultado da transformação distorcer.</span><span class="sxs-lookup"><span data-stu-id="44063-115">where y is the original y-coordinate, Sy is the proportionality constant, and y' is the result of the shear transformation.</span></span>

<span data-ttu-id="44063-116">As transformações horizontal de distorção e de distorção vertical podem ser combinadas em uma única operação usando uma matriz 2-por-2.</span><span class="sxs-lookup"><span data-stu-id="44063-116">The horizontal-shear and vertical-shear transformations can be combined into a single operation using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

<span data-ttu-id="44063-117">A matriz 2-por-2 que produziu a distorção contém os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="44063-117">The 2-by-2 matrix that produced the shear contains the following values:</span></span>

``` syntax
|1    1| 
|0    1| 
```

 

 



