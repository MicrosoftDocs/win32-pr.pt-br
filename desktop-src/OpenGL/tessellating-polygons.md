---
title: Polígonos de mosaico
description: Polígonos de mosaico
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilitário OpenGL (GLU), mosaico
- GLU (Utilitário OpenGL), mosaico
- Utilitário OpenGL (GLU), polígonos simples
- GLU (Utilitário OpenGL), polígonos simples
- OpenGL de polígonos simples
- Utilitário OpenGL (GLU), polígonos complexos
- GLU (Utilitário OpenGL), polígonos complexos
- polígonos complexos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948e0669348404af763883f7ff713212d52f6f0d79312812552c0e5053041627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034507"
---
# <a name="tessellating-polygons"></a>Polígonos de mosaico

O OpenGL pode exibir diretamente apenas polígonos convexos simples. Um polígono será simples se:

-   As bordas intersecção somente em vértices.
-   Não há vértices duplicados.
-   Exatamente duas bordas se encontram em qualquer vértice.

Para exibir polígonos simples não convexos ou polígonos simples que contêm orifícios, primeiro você deve subdividir os polígonos (subdividi-los em polígonos convexos). Essa subdivisão é chamada *de mosaico*. GLU fornece uma coleção de funções que executam mosaico. Observe que as funções de mosaico GLU não podem lidar com polígonos não simples; não há nenhum método OpenGL padrão para lidar com esses polígonos.

Como o mosaico geralmente é necessário e pode ser bastante complicado, esta seção descreve as funções de mosaico GLU em detalhes. Essas funções são usadas como polígonos simples arbitrários de entrada que podem incluir orifícios e retornam alguma combinação de triângulos, malhas de triângulo e ventiladores de triângulo. Se você não quiser lidar com malhas ou ventiladores, poderá especificar que as funções de mosaico retornem apenas triângulos. No entanto, as informações de malha e ventilador melhoram o desempenho. As funções de mosaico de polígono moldam um polígono concave com um ou mais contornos.

**Para usar o mosaico de polígono**

1.  Crie um objeto de mosaico [**com gluNewTess**](glunewtess.md).
2.  Use [*gluTessCallBack*](glutess.md) para definir funções de retorno de chamada que você usará para processar os triângulos gerados pelo mosaico.
3.  Com [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), especifique o polígono com orifícios ou o polígono concave a ser mosaico.

    Quando a descrição do polígono for concluída, o recurso de mosaico invocará suas funções de retorno de chamada conforme necessário.

    Você pode destruir objetos de mosaico indeneados com [**gluDeleteTess**](gludeletetess.md).

Para obter mais informações sobre como salvar os dados de mosaico, consulte [Usando funções de retorno de chamada](using-callback-functions.md).

 

 




