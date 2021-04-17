---
title: Polígonos inclusão
description: Polígonos inclusão
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilitário OpenGL (GLU), mosaico
- GLU (utilitário OpenGL), mosaico
- Utilitário OpenGL (GLU), polígonos simples
- GLU (utilitário OpenGL), polígonos simples
- polígonos simples OpenGL
- Utilitário OpenGL (GLU), polígonos complexos
- GLU (utilitário OpenGL), polígonos complexos
- polígonos complexos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783256"
---
# <a name="tessellating-polygons"></a>Polígonos inclusão

O OpenGL pode exibir diretamente apenas polígonos convexa simples. Um polígono é simples se:

-   As bordas se cruzam somente em vértices.
-   Não há vértices duplicados.
-   Exatamente duas bordas se encontram em qualquer vértice.

Para exibir polígonos nonconvex simples ou polígonos simples contendo buracos, você deve primeiro triangular os polígonos (subdividir-os em polígonos do convexa). Essa subdivisão é chamada de *mosaico*. O GLU fornece uma coleção de funções que executam mosaico. Observe que as funções de mosaico GLU não podem manipular polígonos não simples; Não há nenhum método OpenGL padrão para lidar com esses polígonos.

Como o mosaico geralmente é necessário e pode ser bastante complicado, esta seção descreve as funções de mosaico GLU em detalhes. Essas funções utilizam como entrada polígonos simples arbitrários que podem incluir buracos e retornam alguma combinação de triângulos, malhas de triângulo e ventiladores de triângulo. Se você não quiser lidar com malhas ou fãs, poderá especificar que as funções de mosaico retornem apenas triângulos. No entanto, as informações de malha e ventilador melhoram o desempenho. As funções de mosaico Polygon triangulam um polígono côncavo com um ou mais contornos.

**Para usar o mosaico Polygon**

1.  Crie um objeto de mosaico com [**gluNewTess**](glunewtess.md).
2.  Use [*gluTessCallBack*](glutess.md) para definir as funções de retorno de chamada que serão usadas para processar os triângulos gerados pelo Tessellator.
3.  Com [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), especifique o polígono com buracos ou o polígono côncavo para ser mosaico.

    Quando a descrição do polígono for concluída, o recurso de mosaico invocará suas funções de retorno de chamada conforme necessário.

    Você pode destruir objetos de mosaico desnecessários com [**gluDeleteTess**](gludeletetess.md).

Para obter mais informações sobre como salvar os dados de mosaico, consulte [usando funções de retorno de chamada](using-callback-functions.md).

 

 




