---
title: Rasterização
description: Rasterização é o processo pelo qual um primitivo é convertido em uma imagem bidimensional.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- Pipeline de processamento openGL, rasterização
- rasterizando o OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192f8fdd919c14be4bd47688abf911b363e13f2e8ca9606f1943eb2956378ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776876"
---
# <a name="rasterizing"></a>Rasterização

*Rasterização* é o processo pelo qual um primitivo é convertido em uma imagem bidimensional. Cada ponto dessa imagem contém informações como dados de cor, profundidade e textura. Um ponto e suas informações associadas são chamados de *fragmento*. A posição atual do raster, conforme especificado com [**glRasterPos, \***](glrasterpos-functions.md)é usada de várias maneiras durante esse estágio para desenhar pixels e bitmaps. Diferentes problemas surgem ao rasterizar pontos, segmentos de linha e polígonos. Além disso, retângulos de pixel e bitmaps precisam ser rasterizados.

Com o OpenGL, você controla o rasterização usando as seguintes funções:

-   Primitives. Controle como os primitivos são rasterizados usando funções que determinam dimensões e padrões de apple: [**glPointSize**](glpointsize.md), [**glLineWidth,**](gllinewidth.md) [**glLineStipple**](gllinestipple.md)e [**glPolygonStipple**](glpolygonstipple.md). Controle como as faces frontal e traseira dos polígonos são rasterizadas com [**glCullFace,**](glcullface.md) [**glFrontFace**](glfrontface.md)e [**glPolygonMode.**](glpolygonmode.md)
-   Pixels. Várias funções controlam os modos de transferência e armazenamento de pixels. A função [ * *glPixelStore \** _](glpixelstore-functions.md) controla a codificação de pixels na memória do cliente e [_*glPixelTransfer \**_](glpixeltransfer.md) e [_*glPixelMap \**_](glpixelmap.md) controlam como os pixels são processados antes de serem colocados no framebuffer. Especifique um retângulo de pixel com [_ *glDrawPixels* *](gldrawpixels.md); controle sua rasterização com [**glPixelZoom**](glpixelzoom.md).
-   Bitmaps. Bitmaps são retângulos de zeros e aqueles que especificam um padrão específico de fragmentos a serem produzidos. Cada um desses fragmentos tem os mesmos dados associados. A [**função glBitmap**](glbitmap.md) especifica um bitmap.
-   Memória de textura. Quando a texturização está habilitada, a texturização mapeia uma parte de uma imagem de textura especificada para cada primitivo. Esse mapeamento é realizado usando a cor da imagem de textura no local indicado pelas coordenadas de textura de um fragmento para modificar a cor RGBA do fragmento. Especifique uma imagem de textura [**com glTexImage2D**](glteximage2d.md) [**ou glTexImage1D.**](glteximage1d.md) As [ * *funções glTexParameter \** _](gltexparameter-functions.md) e _ [*glTexEnv \** *](gltexenv-functions.md) controlam como os valores de textura são interpretados e aplicados a um fragmento.
-   Nevoeiro. Para combinar uma cor de cinza com a cor pós-texting de um fragmento rasterizado, use um fator de mesclagem que depende da distância entre o ponto de vista e o fragmento. Use [**glFog \* para**](glfog.md) especificar a cor da coloração e o fator de combinação.

 

 




