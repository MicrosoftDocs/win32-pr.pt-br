---
description: Alguns aplicativos traduzem (ou deslocam) objetos desenhados na área do cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Tradução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988289"
---
# <a name="translation"></a><span data-ttu-id="04fb1-103">Tradução</span><span class="sxs-lookup"><span data-stu-id="04fb1-103">Translation</span></span>

<span data-ttu-id="04fb1-104">Alguns aplicativos traduzem (ou deslocam) objetos desenhados na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="04fb1-104">Some applications translate (or shift) objects drawn in the client area.</span></span> <span data-ttu-id="04fb1-105">chamando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir o espaço mundial apropriado para a transformação de espaço em página.</span><span class="sxs-lookup"><span data-stu-id="04fb1-105">by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="04fb1-106">A função SetWorldTransform recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="04fb1-106">The SetWorldTransform function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="04fb1-107">Os membros eDx e eDy do XFORM especificam os componentes de tradução horizontal e vertical, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="04fb1-107">The eDx and eDy members of XFORM specify the horizontal and vertical translation components, respectively.</span></span>

<span data-ttu-id="04fb1-108">Quando ocorre a *conversão* , cada ponto em um objeto é deslocado verticalmente, horizontalmente ou ambos, por um valor especificado.</span><span class="sxs-lookup"><span data-stu-id="04fb1-108">When *translation* occurs, each point in an object is shifted vertically, horizontally, or both, by a specified amount.</span></span> <span data-ttu-id="04fb1-109">A ilustração a seguir mostra um retângulo de 20 por 20 unidades que foi traduzido para a direita por 10 unidade quando copiado do espaço de coordenadas mundiais para o espaço de coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="04fb1-109">The following illustration shows a 20- by 20-unit rectangle that was translated to the right by 10 units when copied from world-coordinate space to page-coordinate space.</span></span>

![ilustração mostrando um retângulo em uma posição no espaço do mundo e em uma posição diferente no espaço da página](images/cstrn-09.png)

<span data-ttu-id="04fb1-111">Na ilustração anterior, a coordenada x de cada ponto no retângulo é de 10 unidades acima da coordenada x original.</span><span class="sxs-lookup"><span data-stu-id="04fb1-111">In the preceding illustration, the x-coordinate of each point in the rectangle is 10 units greater than the original x-coordinate.</span></span>

<span data-ttu-id="04fb1-112">A tradução horizontal pode ser representada pelo seguinte algoritmo.</span><span class="sxs-lookup"><span data-stu-id="04fb1-112">Horizontal translation can be represented by the following algorithm.</span></span>

``` syntax
x' = x + Dx 
```

<span data-ttu-id="04fb1-113">Em que x ' é a nova coordenada x, x é a coordenada x original e DX é a distância horizontal movida.</span><span class="sxs-lookup"><span data-stu-id="04fb1-113">Where x' is the new x-coordinate, x is the original x-coordinate, and Dx is the horizontal distance moved.</span></span>

<span data-ttu-id="04fb1-114">A tradução vertical pode ser representada pelo algoritmo a seguir.</span><span class="sxs-lookup"><span data-stu-id="04fb1-114">Vertical translation can be represented by the following algorithm.</span></span>

``` syntax
y' = y + Dy 
```

<span data-ttu-id="04fb1-115">Onde y ' é a nova coordenada y, y é a coordenada y original e dy é a distância vertical movida.</span><span class="sxs-lookup"><span data-stu-id="04fb1-115">Where y' is the new y-coordinate, y is the original y-coordinate, and Dy is the vertical distance moved.</span></span>

<span data-ttu-id="04fb1-116">As transformações de translação horizontal e vertical podem ser combinadas em uma única operação usando uma matriz 3-by-3.</span><span class="sxs-lookup"><span data-stu-id="04fb1-116">The horizontal and vertical translation transformations can be combined into a single operation by using a 3-by-3 matrix.</span></span>

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

<span data-ttu-id="04fb1-117">(As regras de estado de multiplicação de matriz que o número de linhas em uma matriz devem ser iguais ao número de colunas no outro.</span><span class="sxs-lookup"><span data-stu-id="04fb1-117">(The rules of matrix multiplication state that the number of rows in one matrix must equal the number of columns in the other.</span></span> <span data-ttu-id="04fb1-118">O inteiro 1 na matriz \| x y 1 \| é um espaço reservado que foi adicionado para atender a esse requisito.)</span><span class="sxs-lookup"><span data-stu-id="04fb1-118">The integer 1 in the matrix \|x y 1\| is a placeholder that was added to meet this requirement.)</span></span>

<span data-ttu-id="04fb1-119">A matriz 3-by-3 que produziu a transformação de tradução ilustrada contém os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="04fb1-119">The 3-by-3 matrix that produced the illustrated translation transformation contains the following values.</span></span>

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



