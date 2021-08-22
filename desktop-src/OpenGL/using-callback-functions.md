---
title: Usando funções de retorno de chamada
description: As funções de retorno de chamada GLU, gluBeginPolygon, gluTessVertex, gluNextContour e gluEndPolygon, são semelhantes às funções de polígono openGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilitário OpenGL (GLU), funções de retorno de chamada
- GLU (Utilitário OpenGL), funções de retorno de chamada
- Utilitário OpenGL (GLU), mosaico
- GLU (Utilitário OpenGL), mosaico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75556b8c366c83df5a5976c867e6fc5f68d520da65ed8f34609f312cbfebaa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932891"
---
# <a name="using-callback-functions"></a>Usando funções de retorno de chamada

As funções de retorno de chamada GLU, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), são semelhantes às funções de polígono OpenGL.

Normalmente, eles salvam os dados para triângulos, malhas de triângulo e ventiladores de triângulo em estruturas de dados definidas pelo usuário ou em listas de exibição do OpenGL. Para renderizar os polígonos, outro código atravessa as estruturas de dados ou chama as listas de exibição. Embora as funções de retorno de chamada possam chamar funções OpenGL para exibir polígonos diretamente, isso geralmente não é feito, pois o mosaico pode ser computacionalmente com uso intensivo de recursos. É uma boa ideia salvar os dados se houver alguma chance de você querer exibi-los novamente. As funções de mosaico GLU têm a garantia de nunca retornar novos vértices, portanto, a interpolação de vértices, coordenadas de textura ou cores nunca é necessária.

 

 




