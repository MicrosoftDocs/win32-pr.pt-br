---
description: No modo de sombreamento simples, a seguinte pirâmide é exibida com uma borda nítida entre rostos adjacentes. No modo de sombreamento Gouraud, no entanto, os valores de sombreamento são interpolados na borda e a aparência final é de uma superfície curvada.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparando modos de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089685"
---
# <a name="comparing-shading-modes-direct3d-9"></a><span data-ttu-id="35155-104">Comparando modos de sombreamento (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="35155-104">Comparing Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="35155-105">No modo de sombreamento simples, a seguinte pirâmide é exibida com uma borda nítida entre rostos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="35155-105">In flat shading mode, the following pyramid is displayed with a sharp edge between adjoining faces.</span></span> <span data-ttu-id="35155-106">No modo de sombreamento Gouraud, no entanto, os valores de sombreamento são interpolados na borda e a aparência final é de uma superfície curvada.</span><span class="sxs-lookup"><span data-stu-id="35155-106">In Gouraud shading mode, however, shading values are interpolated across the edge, and the final appearance is of a curved surface.</span></span>

![ilustração de uma pirâmide com bordas nítidas e setas que apontam para a face normal](images/shade2.png)

<span data-ttu-id="35155-108">O sombreamento Gouraud ilumina as superfícies simples de forma realista do que o sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="35155-108">Gouraud shading lights flat surfaces more realistically than flat shading.</span></span> <span data-ttu-id="35155-109">Uma face no modo de sombreamento simples é uma cor uniforme, mas o sombreamento Gouraud permite que a luz caia em um rosto mais corretamente.</span><span class="sxs-lookup"><span data-stu-id="35155-109">A face in the flat shading mode is a uniform color, but Gouraud shading enables light to fall across a face more correctly.</span></span> <span data-ttu-id="35155-110">Esse efeito é particularmente óbvio se houver uma fonte de ponto próximo.</span><span class="sxs-lookup"><span data-stu-id="35155-110">This effect is particularly obvious if there is a nearby point source.</span></span>

<span data-ttu-id="35155-111">O sombreamento de Gouraud suaviza as bordas nítidas entre polígonos visíveis com sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="35155-111">Gouraud shading smoothes the sharp edges between polygons that are visible with flat shading.</span></span> <span data-ttu-id="35155-112">No entanto, isso pode resultar em bandas de Mach, que são faixas de cor ou luz que não são mescladas suavemente entre polígonos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="35155-112">However, it can result in mach bands, which are bands of color or light that are not smoothly blended across adjacent polygons.</span></span> <span data-ttu-id="35155-113">Seu aplicativo pode reduzir a aparência das bandas de Mach aumentando o número de polígonos em um objeto, aumentando a resolução da tela ou aumentando a intensidade da cor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35155-113">Your application can reduce the appearance of Mach bands by increasing the number of polygons in an object, increasing screen resolution, or increasing the color depth of the application.</span></span>

<span data-ttu-id="35155-114">O sombreamento Gouraud pode perder alguns detalhes.</span><span class="sxs-lookup"><span data-stu-id="35155-114">Gouraud shading can miss some details.</span></span> <span data-ttu-id="35155-115">Por exemplo, na ilustração a seguir, um destaque está completamente contido em uma face de polígono.</span><span class="sxs-lookup"><span data-stu-id="35155-115">For example, in the following illustration, a spotlight is completely contained within a polygon face.</span></span>

![ilustração de um Spotlight em uma face de polígono](images/gouraud.png)

<span data-ttu-id="35155-117">Nesse caso, o sombreamento Gouraud, que interpola entre vértices, perderia o destaque completamente; a face seria renderizada como se o Spotlight não existisse.</span><span class="sxs-lookup"><span data-stu-id="35155-117">In this case, Gouraud shading, which interpolates between vertices, would miss the spotlight altogether; the face would be rendered as though the spotlight did not exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35155-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35155-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35155-119">Sombreamento</span><span class="sxs-lookup"><span data-stu-id="35155-119">Shading</span></span>](shading.md)
</dt> </dl>

 

 



