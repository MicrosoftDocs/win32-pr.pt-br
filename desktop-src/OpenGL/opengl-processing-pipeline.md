---
title: Pipeline de processamento do OpenGL
description: Pipeline de processamento do OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline de processamento
- pipeline de processamento OpenGL
- pipeline OpenGL
- framebuffers, pipeline de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b52568de344404e9bddbedbacc40beda064b09d3e3af96c2657f670e677c32a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936856"
---
# <a name="opengl-processing-pipeline"></a>Pipeline de processamento do OpenGL

Muitas funções OpenGL são usadas especificamente para desenhar objetos como pontos, linhas, polígonos e bitmaps. Algumas funções controlam a maneira como algumas desse desenho ocorrem (como aquelas que habilitam a ressalação ou a textagem). Outras funções se preocupam especificamente com a manipulação de framebuffer. Os tópicos nesta seção descrevem como todas as funções do OpenGL funcionam em conjunto para criar o pipeline de processamento do OpenGL. Esta seção também dá uma olhada mais de perto nos estágios em que os dados são realmente processados e vincula esses estágios às funções openGL.

O diagrama a seguir detalha o pipeline de processamento do OpenGL. Na maioria do pipeline, você pode ver três setas verticais entre os estágios principais. Essas setas representam vértices e os dois tipos principais de dados que podem ser associados a vértices: valores de cor e coordenadas de textura. Observe também que os vértices são montados em primitivos, em fragmentos e, por fim, em pixels no framebuffer. Essa progressão é discutida mais detalhadamente em [Vértices,](vertices.md) [Primitivos,](primitives.md) [Fragmentos](fragments.md)e [Pixels.](pixels.md)

![Diagrama mostrando o pipeline de processamento do OpenGL.](images/proc01.png)

 

 




