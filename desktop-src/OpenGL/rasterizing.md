---
title: Rasterização
description: A rasterização é o processo pelo qual um primitivo é convertido em uma imagem bidimensional.
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- Pipeline de processamento OpenGL, rasterização
- rasterização do OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0d8e7ece3bead408b8d056356593879edc638c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498662"
---
# <a name="rasterizing"></a>Rasterização

A *rasterização* é o processo pelo qual um primitivo é convertido em uma imagem bidimensional. Cada ponto dessa imagem contém informações como cor, profundidade e dados de textura. Um ponto e suas informações associadas são chamados de *fragmento*. A posição atual da varredura, conforme especificado [**com \* glRasterPos**](glrasterpos-functions.md), é usada de várias maneiras durante esse estágio para desenhar pixels e bitmaps. Problemas diferentes surgem ao rasterizar pontos, segmentos de linha e polígonos. Além disso, os retângulos e bitmaps de pixel precisam ser rasterizados.

Com o OpenGL, você controla a rasterização usando as seguintes funções:

-   Primitivos. Controle como os primitivos são rasterizados usando funções que determinam dimensões e padrões Stipple: [**glPointSize**](glpointsize.md), [**glLineWidth**](gllinewidth.md), [**glLineStipple**](gllinestipple.md)e [**glPolygonStipple**](glpolygonstipple.md). Controle como as faces dianteira e traseira dos polígonos são rasterizadas com [**glCullFace**](glcullface.md), [**glFrontFace**](glfrontface.md)e [**glPolygonMode**](glpolygonmode.md).
-   Pixels. Várias funções controlam o armazenamento de pixel e os modos de transferência. A função [**glPixelStore \***](glpixelstore-functions.md) controla a codificação de pixels na memória do cliente, [**e \* glPixelTransfer**](glpixeltransfer.md) e [**glPixelMap \***](glpixelmap.md) controlam como os pixels são processados antes de serem colocados no framebuffer. Especifique um retângulo de pixel com [**glDrawPixels**](gldrawpixels.md); controle sua rasterização com [**glPixelZoom**](glpixelzoom.md).
-   Bitmaps. Os bitmaps são retângulos de zeros e aqueles que especificam um padrão específico de fragmentos a serem produzidos. Cada um desses fragmentos tem os mesmos dados associados. A função [**glBitmap**](glbitmap.md) especifica um bitmap.
-   Memória de textura. Quando texturing está habilitado, o texturing mapeia uma parte de uma imagem de textura especificada em cada primitiva. Esse mapeamento é realizado usando a cor da imagem de textura no local indicado pelas coordenadas de textura de um fragmento para modificar a cor RGBA do fragmento. Especifique uma imagem de textura com [**glTexImage2D**](glteximage2d.md) ou [**glTexImage1D**](glteximage1d.md). As [**funções \* GlTexParameter**](gltexparameter-functions.md) e [**glTexEnv \***](gltexenv-functions.md) controlam como os valores de textura são interpretados e aplicados a um fragmento.
-   Neblina. Para misturar uma cor de neblina com uma cor texturing de um fragmento rasterizado, use um fator de mesclagem que dependa da distância entre o eyepoint e o fragmento. Use [**glFog \***](glfog.md) para especificar a cor de neblina e o fator de mesclagem.

 

 




