---
title: Especificando o polígono a ser Mosaicodo
description: Você especifica um polígono (possivelmente contendo buracos) para ser mosaico usando
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916589"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a>Especificando o polígono a ser Mosaicodo

Você especifica um polígono (possivelmente contendo buracos) para ser mosaico usando:

-   [**gluBeginPolygon**](glubeginpolygon.md)
-   [**gluTessVertex**](glutessvertex.md)
-   [**gluNextContour**](glunextcontour.md)
-   [**gluEndPolygon**](gluendpolygon.md)

Para polígonos sem buracos, o processo de especificação é exatamente como no OpenGL:

1.  Comece com [**gluBeginPolygon**](glubeginpolygon.md).
2.  Chame [**gluTessVertex**](glutessvertex.md) para cada vértice no limite.
3.  Finalize o polígono com uma chamada para [**gluEndPolygon**](gluendpolygon.md).

Se um polígono consistir em vários contornos, incluindo buracos e buracos dentro de buracos, você especificará os contornos um após o outro, precedendo cada um por [**gluNextContour**](glunextcontour.md). Quando você chama [**gluEndPolygon**](gluendpolygon.md), ele sinaliza o final da delimitação final e inicia o mosaico. Você pode omitir a chamada para **gluNextContour** antes da primeira delimitação. A função [**gluBeginPolygon**](glubeginpolygon.md) inicia a especificação de um polígono para ser mosaico e associa um objeto de mosaico, **tessobj**, a ele. As funções de retorno de chamada a serem usadas são aquelas que você associa ao objeto de mosaico com [*gluTessCallback*](glutess.md).

A função [**gluTessVertex**](glutessvertex.md) especifica um vértice no polígono a ser mosaico. Chame **gluTessVertex** para cada vértice no polígono. O parâmetro *tessobj* da função é o objeto de mosaico a ser usado, o *v* contém as coordenadas de vértice tridimensionais e os *dados* são um ponteiro arbitrário que é enviado para o retorno de chamada associado ao **\_ vértice Glu**. Normalmente, os *dados* contêm dados de vértice, coordenadas de textura, informações de cores ou qualquer outra coisa que o aplicativo possa exigir.

A função [**gluNextContour**](glunextcontour.md) marca o início da próxima delimitação quando várias contornos compõem o limite do polígono como mosaico. O parâmetro de *tipo* da função pode **ser Glu \_ exterior**, **Glu \_ interior**, **Glu \_ CCW**, **Glu \_ CW** ou **Glu \_ Unknown**. Essas constantes servem apenas como dicas para o mosaico. Se você os obtiver certo, o mosaico pode ir mais rápido. Se você os receber errado, eles serão ignorados e o mosaico ainda funcionará.

Para um polígono com buracos, uma delimitação é a delimitação exterior e as outras são interiores. Se você não chamar **gluNextContour** imediatamente após [**gluBeginPolygon**](glubeginpolygon.md), a primeira delimitação será considerada como **\_ exterior** do tipo Glu.

**Glu \_** O CCW e o **Glu \_ anti** -horário indicam polígonos e em sentido anti-horário. Escolher quais são no sentido horário e que são arbitrários em três dimensões, mas em qualquer plano, há duas orientações diferentes; Use os tipos **Glu \_ CW** e **Glu \_ CCW** de forma consistente. Use **Glu \_ desconhecido** se você não souber qual usar.

A função [**gluEndPolygon**](gluendpolygon.md) indica o fim da especificação do polígono. Ele também indica que o mosaico pode começar a usar o objeto de mosaico *tessobj*.

 

 




