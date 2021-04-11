---
title: Gerando coordenadas de textura
description: Em vez de fornecer explicitamente coordenadas de textura, você pode fazer com que o OpenGL as gere como uma função de outros dados de vértice usando glTexGen \.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Pipeline de processamento OpenGL, coordenadas de textura
- coordenadas de textura OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d3f5b807f25aee2783ff8dab3a4930a9c797ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160036"
---
# <a name="generating-texture-coordinates"></a><span data-ttu-id="fc3ea-105">Gerando coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="fc3ea-105">Generating Texture Coordinates</span></span>

<span data-ttu-id="fc3ea-106">Em vez de fornecer explicitamente coordenadas de textura, você pode fazer com que o OpenGL as gere como uma função de outros dados de vértice usando [glTexGen \* ](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fc3ea-106">Rather than explicitly supplying texture coordinates, you can have OpenGL generate them as a function of other vertex data using [glTexGen\*](gltexgen-functions.md).</span></span> <span data-ttu-id="fc3ea-107">Depois que as coordenadas de textura tiverem sido especificadas ou geradas, elas serão transformadas pela matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="fc3ea-107">After the texture coordinates have been specified or generated, they are transformed by the texture matrix.</span></span> <span data-ttu-id="fc3ea-108">Essa matriz é controlada com as mesmas funções que são usadas para transformações de matriz (consulte [transformações de matriz](matrix-transformations.md)).</span><span class="sxs-lookup"><span data-stu-id="fc3ea-108">This matrix is controlled with the same functions that are used for matrix transformations (see [Matrix Transformations](matrix-transformations.md)).</span></span>

 

 




