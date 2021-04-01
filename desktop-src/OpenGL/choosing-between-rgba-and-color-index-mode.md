---
title: Escolhendo entre o modo RGBA e Color-Index
description: Em geral, use o modo RGBA para seus aplicativos OpenGL; Ele fornece mais flexibilidade do que o modo de índice de cor para efeitos como sombreamento, iluminação, mapeamento de cores, neblina, antialiasing e mistura.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL no Windows, modo RGBA
- OpenGL no Windows, modo de índice de cor
- Modo RGBA OpenGL
- modo de índice de cor OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635876"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a><span data-ttu-id="8c946-107">Escolhendo entre o modo RGBA e Color-Index</span><span class="sxs-lookup"><span data-stu-id="8c946-107">Choosing Between RGBA and Color-Index Mode</span></span>

<span data-ttu-id="8c946-108">Em geral, use o modo RGBA para seus aplicativos OpenGL; Ele fornece mais flexibilidade do que o modo de índice de cor para efeitos como sombreamento, iluminação, mapeamento de cores, neblina, antialiasing e mistura.</span><span class="sxs-lookup"><span data-stu-id="8c946-108">In general, use the RGBA mode for your OpenGL applications; it provides more flexibility than the color-index mode for effects such as shading, lighting, color mapping, fog, antialiasing, and blending.</span></span>

<span data-ttu-id="8c946-109">Considere o uso do modo de índice de cor nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="8c946-109">Consider using the color-index mode in the following cases:</span></span>

-   <span data-ttu-id="8c946-110">Se você tiver um número limitado de bitplanes disponíveis; o modo de índice de cor pode produzir sombreamento menos baixo que o modo RGBA.</span><span class="sxs-lookup"><span data-stu-id="8c946-110">If you have a limited number of bitplanes available; the color-index mode can produce less-coarse shading than the RGBA mode.</span></span>
-   <span data-ttu-id="8c946-111">Se você não estiver preocupado com o uso de cores "reais"; por exemplo, usar várias cores em um mapa Topographic para designar elevações relativas.</span><span class="sxs-lookup"><span data-stu-id="8c946-111">If you are not concerned about using "real" colors; for example, using several colors in a topographic map to designate relative elevations.</span></span>
-   <span data-ttu-id="8c946-112">Quando você está portando um aplicativo existente que usa o modo de índice de cor extensivamente.</span><span class="sxs-lookup"><span data-stu-id="8c946-112">When you're porting an existing application that uses color-index mode extensively.</span></span>
-   <span data-ttu-id="8c946-113">Quando você quiser usar a animação de mapa de cores e efeitos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c946-113">When you want to use color-map animation and effects in your application.</span></span> <span data-ttu-id="8c946-114">(Isso não é possível em dispositivos true-color.)</span><span class="sxs-lookup"><span data-stu-id="8c946-114">(This is not possible on true-color devices.)</span></span>

 

 




