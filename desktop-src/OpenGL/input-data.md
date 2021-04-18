---
title: Dados de entrada
description: O pipeline OpenGL exige que você insira vários tipos de dados
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline de processamento OpenGL, dados de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769204"
---
# <a name="input-data"></a><span data-ttu-id="a9eac-104">Dados de entrada</span><span class="sxs-lookup"><span data-stu-id="a9eac-104">Input Data</span></span>

<span data-ttu-id="a9eac-105">O pipeline OpenGL exige que você insira vários tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="a9eac-105">The OpenGL pipeline requires you to input several types of data:</span></span>

-   <span data-ttu-id="a9eac-106">**Vértices**.</span><span class="sxs-lookup"><span data-stu-id="a9eac-106">**Vertices**.</span></span> <span data-ttu-id="a9eac-107">Os vértices descrevem a forma do objeto geométrico desejado.</span><span class="sxs-lookup"><span data-stu-id="a9eac-107">Vertices describe the shape of the desired geometric object.</span></span> <span data-ttu-id="a9eac-108">Para especificar vértices, use as funções [**\* glVertex**](glvertex-functions.md) em conjunto com [**glBegin**](glbegin.md) e [**glEnd**](glend.md) para criar um ponto, uma linha ou um polígono.</span><span class="sxs-lookup"><span data-stu-id="a9eac-108">To specify vertices, use [**glVertex\***](glvertex-functions.md) functions in conjunction with [**glBegin**](glbegin.md) and [**glEnd**](glend.md) to create a point, line, or polygon.</span></span> <span data-ttu-id="a9eac-109">Você também pode usar [**glRect**](glrect-functions.md) para descrever um retângulo inteiro ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a9eac-109">You can also use [**glRect**](glrect-functions.md) to describe an entire rectangle at one time.</span></span>
-   <span data-ttu-id="a9eac-110">**Sinalizador de borda**.</span><span class="sxs-lookup"><span data-stu-id="a9eac-110">**Edge flag**.</span></span> <span data-ttu-id="a9eac-111">Por padrão, todas as bordas de polígonos são bordas de limite.</span><span class="sxs-lookup"><span data-stu-id="a9eac-111">By default, all edges of polygons are boundary edges.</span></span> <span data-ttu-id="a9eac-112">Use [**glEdgeFlag \***](gledgeflag-functions.md) para definir explicitamente o sinalizador de borda.</span><span class="sxs-lookup"><span data-stu-id="a9eac-112">Use [**glEdgeFlag\***](gledgeflag-functions.md) to explicitly set the edge flag.</span></span>
-   <span data-ttu-id="a9eac-113">**Posição atual da rasterização**.</span><span class="sxs-lookup"><span data-stu-id="a9eac-113">**Current raster position**.</span></span> <span data-ttu-id="a9eac-114">Especificado com [**glRasterPos \***](glrasterpos-functions.md), a posição de varredura atual é usada para determinar as coordenadas rasterizadas para operações de desenho de bitmap e pixel.</span><span class="sxs-lookup"><span data-stu-id="a9eac-114">Specified with [**glRasterPos\***](glrasterpos-functions.md), the current raster position is used to determine raster coordinates for pixel- and bitmap-drawing operations.</span></span>
-   <span data-ttu-id="a9eac-115">**Normal atual**.</span><span class="sxs-lookup"><span data-stu-id="a9eac-115">**Current normal**.</span></span> <span data-ttu-id="a9eac-116">Um vetor normal associado a um vértice específico determina como uma superfície nesse vértice é orientada em espaço tridimensional; isso, por sua vez, afeta a quantidade de luz que um vértice específico recebe.</span><span class="sxs-lookup"><span data-stu-id="a9eac-116">A normal vector associated with a particular vertex determines how a surface at that vertex is oriented in three-dimensional space; this in turn affects how much light that particular vertex receives.</span></span> <span data-ttu-id="a9eac-117">Use [**glNormal \***](glnormal-functions.md) para especificar um vetor normal.</span><span class="sxs-lookup"><span data-stu-id="a9eac-117">Use [**glNormal\***](glnormal-functions.md) to specify a normal vector.</span></span>
-   <span data-ttu-id="a9eac-118">**Cor atual**.</span><span class="sxs-lookup"><span data-stu-id="a9eac-118">**Current color**.</span></span> <span data-ttu-id="a9eac-119">A cor de um vértice, junto com as condições de iluminação, determinam a cor final e definitiva.</span><span class="sxs-lookup"><span data-stu-id="a9eac-119">The color of a vertex, together with the lighting conditions, determine the final, lit color.</span></span> <span data-ttu-id="a9eac-120">A cor é especificada [**com \* glColor**](glcolor-functions.md) se estiver no modo RGBA ou [**com \* glIndex**](glindex-functions.md) se estiver no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="a9eac-120">Color is specified with [**glColor\***](glcolor-functions.md) if in RGBA mode, or with [**glIndex\***](glindex-functions.md) if in color-index mode.</span></span>
-   <span data-ttu-id="a9eac-121">**Coordenadas de textura atuais**.</span><span class="sxs-lookup"><span data-stu-id="a9eac-121">**Current texture coordinates**.</span></span> <span data-ttu-id="a9eac-122">Especificado com [**glTexCoord \***](gltexcoord-functions.md), as coordenadas de textura determinam o local em um mapa de textura para associar a um vértice de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a9eac-122">Specified with [**glTexCoord\***](gltexcoord-functions.md), texture coordinates determine the location in a texture map to associate with a vertex of an object.</span></span>

> [!Note]  
> <span data-ttu-id="a9eac-123">Quando **glVertex \*** é chamado, o vértice resultante herda o sinalizador de borda atual, as coordenadas normal, Color e Texture.</span><span class="sxs-lookup"><span data-stu-id="a9eac-123">When **glVertex\*** is called, the resulting vertex inherits the current edge flag, normal, color, and texture coordinates.</span></span> <span data-ttu-id="a9eac-124">Portanto, **glEdgeFlag \***, **glNormal \***, **glColor \*** e **\* glTexCoord** devem ser chamados antes de **glVertex \***, se eles forem afetar o vértice resultante.</span><span class="sxs-lookup"><span data-stu-id="a9eac-124">Therefore, **glEdgeFlag\***, **glNormal\***, **glColor\***, and **glTexCoord\*** must be called before **glVertex\***, if they are to affect the resulting vertex.</span></span>

 

 

 




