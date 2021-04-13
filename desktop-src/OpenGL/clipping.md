---
title: Recorte (OpenGL)
description: O recorte ocorre em duas etapas
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Pipeline de processamento de OpenGL, recorte
- OpenGL de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369123"
---
# <a name="clipping-opengl"></a><span data-ttu-id="ea5d7-105">Recorte (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="ea5d7-105">Clipping (OpenGL)</span></span>

<span data-ttu-id="ea5d7-106">O recorte ocorre em duas etapas:</span><span class="sxs-lookup"><span data-stu-id="ea5d7-106">Clipping occurs in two steps:</span></span>

1.  <span data-ttu-id="ea5d7-107">**Exiba o recorte específico do volume clippingApplication.**</span><span class="sxs-lookup"><span data-stu-id="ea5d7-107">**View volume clippingApplication-specific clipping.**</span></span> <span data-ttu-id="ea5d7-108">Imediatamente após os primitivos serem montados, eles são recortados em coordenadas de olho, conforme necessário, para todos os planos de recorte que você definiu com [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="ea5d7-108">Immediately after primitives are assembled, they're clipped in eye coordinates as necessary for any clipping planes you've defined with [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="ea5d7-109">(O OpenGL requer suporte para pelo menos seis planos de recorte específicos do aplicativo.)</span><span class="sxs-lookup"><span data-stu-id="ea5d7-109">(OpenGL requires support for at least six such application-specific clipping planes.)</span></span>
2.  <span data-ttu-id="ea5d7-110">Os primitivos são transformados pela matriz de projeção em coordenadas de clipes e recortados pelo volume de exibição correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-110">Primitives are transformed by the projection matrix into clip coordinates and clipped by the corresponding view volume.</span></span> <span data-ttu-id="ea5d7-111">Essa matriz pode ser controlada pelas funções de transformação de matriz (consulte [transformações de matriz](matrix-transformations.md)), mas normalmente é especificada por [**glFrustum**](glfrustum.md) ou [**glOrtho**](glortho.md).</span><span class="sxs-lookup"><span data-stu-id="ea5d7-111">This matrix can be controlled by the matrix transformation functions (see [Matrix Transformations](matrix-transformations.md)) but is typically specified by [**glFrustum**](glfrustum.md) or [**glOrtho**](glortho.md).</span></span>

<span data-ttu-id="ea5d7-112">Pontos, segmentos de linha e polígonos são tratados de forma diferente durante o recorte:</span><span class="sxs-lookup"><span data-stu-id="ea5d7-112">Points, line segments, and polygons are handled differently during clipping:</span></span>

-   <span data-ttu-id="ea5d7-113">Os pontos são retidos em seu estado original (se estiverem dentro do volume do clipe) ou descartados (se estiverem fora do volume do clipe).</span><span class="sxs-lookup"><span data-stu-id="ea5d7-113">Points are either retained in their original state (if they're inside the clip volume) or discarded (if they're outside the clip volume).</span></span>
-   <span data-ttu-id="ea5d7-114">Se partes de segmentos de linha ou polígonos estiverem fora do volume do clipe, novos vértices serão gerados nos pontos de corte.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-114">If portions of line segments or polygons are outside the clip volume, new vertices are generated at the clip points.</span></span>
-   <span data-ttu-id="ea5d7-115">Para polígonos, talvez seja necessário construir uma borda inteira entre os novos vértices gerados nos pontos de corte.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-115">For polygons, an entire edge may need to be constructed between new vertices generated at the clip points.</span></span>
-   <span data-ttu-id="ea5d7-116">Para os segmentos de linha e polígonos recortados, as informações de sinalizador de borda, cor e textura são atribuídas a todos os novos vértices.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-116">For line segments and polygons that are clipped, the edge flag, color, and texture information is assigned to all new vertices.</span></span>

 

 




