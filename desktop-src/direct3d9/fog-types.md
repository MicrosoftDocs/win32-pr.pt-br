---
description: 'Há duas maneiras de adicionar a neblina a uma cena: com sombra de pixel e/ou sombra de vértice.'
ms.assetid: 96531830-2df1-40d4-af46-09b1ca153834
title: Tipos de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5dd845373ac4a42a32ab7a9965501df4894568
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087388"
---
# <a name="fog-types-direct3d-9"></a><span data-ttu-id="9145e-103">Tipos de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9145e-103">Fog Types (Direct3D 9)</span></span>

<span data-ttu-id="9145e-104">Há duas maneiras de adicionar a neblina a uma cena: com sombra de pixel e/ou sombra de vértice.</span><span class="sxs-lookup"><span data-stu-id="9145e-104">There are two ways to add fog to a scene: with pixel fog and/or vertex fog.</span></span> <span data-ttu-id="9145e-105">Os tópicos a seguir ilustram as fórmulas usadas em equações de neblina, bem como a implementação de vértice e sombra de pixel.</span><span class="sxs-lookup"><span data-stu-id="9145e-105">The following topics illustrate the formulas used in fog equations, as well as implementing vertex and pixel fog.</span></span> <span data-ttu-id="9145e-106">Um aplicativo pode implementar a neblina com um sombreador de vértice e sombra de pixel simultaneamente, se desejado.</span><span class="sxs-lookup"><span data-stu-id="9145e-106">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

-   [<span data-ttu-id="9145e-107">Fórmulas de neblina</span><span class="sxs-lookup"><span data-stu-id="9145e-107">Fog Formulas</span></span>](fog-formulas.md)
-   [<span data-ttu-id="9145e-108">Parâmetros de neblina</span><span class="sxs-lookup"><span data-stu-id="9145e-108">Fog Parameters</span></span>](fog-parameters.md)
-   [<span data-ttu-id="9145e-109">Mesclagem de neblina</span><span class="sxs-lookup"><span data-stu-id="9145e-109">Fog Blending</span></span>](fog-blending.md)
-   [<span data-ttu-id="9145e-110">Cor da neblina</span><span class="sxs-lookup"><span data-stu-id="9145e-110">Fog Color</span></span>](fog-color.md)
-   [<span data-ttu-id="9145e-111">Neblina de vértice</span><span class="sxs-lookup"><span data-stu-id="9145e-111">Vertex Fog</span></span>](vertex-fog.md)
-   [<span data-ttu-id="9145e-112">Neblina de pixel</span><span class="sxs-lookup"><span data-stu-id="9145e-112">Pixel Fog</span></span>](pixel-fog.md)

<span data-ttu-id="9145e-113">A fusão de neblina é controlada por Estados de renderização; Ele não faz parte do pipeline de pixel programável.</span><span class="sxs-lookup"><span data-stu-id="9145e-113">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9145e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9145e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9145e-115">Buffer de quadros</span><span class="sxs-lookup"><span data-stu-id="9145e-115">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 



