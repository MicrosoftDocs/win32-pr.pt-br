---
title: Usando funções de retorno de chamada
description: As funções de retorno de chamada GLU, gluBeginPolygon, gluTessVertex, gluNextContour e gluEndPolygon, são semelhantes às funções Polygon do OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilitário OpenGL (GLU), funções de retorno de chamada
- GLU (utilitário OpenGL), funções de retorno de chamada
- Utilitário OpenGL (GLU), mosaico
- GLU (utilitário OpenGL), mosaico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822469"
---
# <a name="using-callback-functions"></a><span data-ttu-id="09aa3-107">Usando funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="09aa3-107">Using Callback Functions</span></span>

<span data-ttu-id="09aa3-108">As funções de retorno de chamada GLU, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), são semelhantes às funções Polygon do OpenGL.</span><span class="sxs-lookup"><span data-stu-id="09aa3-108">The GLU callback functions, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), are similar to the OpenGL polygon functions.</span></span>

<span data-ttu-id="09aa3-109">Normalmente, eles salvam os dados dos triângulos, das malhas de triângulo e dos fãs de triângulo em estruturas de dados definidas pelo usuário ou em listas de exibição OpenGL.</span><span class="sxs-lookup"><span data-stu-id="09aa3-109">They typically save the data for the triangles, triangle meshes, and triangle fans in user-defined data structures or in OpenGL display lists.</span></span> <span data-ttu-id="09aa3-110">Para renderizar os polígonos, outro código percorre as estruturas de dados ou chama as listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="09aa3-110">To render the polygons, other code traverses the data structures or calls the display lists.</span></span> <span data-ttu-id="09aa3-111">Embora as funções de retorno de chamada pudessem chamar funções OpenGL para exibir polígonos diretamente, isso geralmente não é feito, pois o mosaico pode ser computacionalmente intensivo em recursos.</span><span class="sxs-lookup"><span data-stu-id="09aa3-111">Although the callback functions could call OpenGL functions to display polygons directly, this is usually not done, as tessellation can be computationally resource-intensive.</span></span> <span data-ttu-id="09aa3-112">É uma boa ideia salvar os dados se houver alguma chance de que você queira exibi-los novamente.</span><span class="sxs-lookup"><span data-stu-id="09aa3-112">It's a good idea to save the data if there is any chance that you want to display it again.</span></span> <span data-ttu-id="09aa3-113">As funções de mosaico GLU são garantidas nunca retornarão novos vértices, portanto, a interpolação de vértices, coordenadas de textura ou cores nunca é necessária.</span><span class="sxs-lookup"><span data-stu-id="09aa3-113">The GLU tessellation functions are guaranteed never to return any new vertices, so interpolation of vertices, texture coordinates, or colors is never required.</span></span>

 

 




