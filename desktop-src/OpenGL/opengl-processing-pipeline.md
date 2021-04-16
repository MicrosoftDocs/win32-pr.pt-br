---
title: Pipeline de processamento OpenGL
description: Pipeline de processamento OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline de processamento
- processando o pipeline OpenGL
- pipeline OpenGL
- framebuffers, pipeline de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556328"
---
# <a name="opengl-processing-pipeline"></a>Pipeline de processamento OpenGL

Muitas funções OpenGL são usadas especificamente para desenhar objetos, como pontos, linhas, polígonos e bitmaps. Algumas funções controlam a forma como parte desse desenho ocorre (como as que permitem a suavização ou texturing). Outras funções se preocupam especificamente com a manipulação de framebuffer. Os tópicos nesta seção descrevem como todas as funções OpenGL funcionam em conjunto para criar o pipeline de processamento OpenGL. Esta seção também examina mais detalhadamente os estágios em que os dados são realmente processados e vincula esses estágios às funções OpenGL.

O diagrama a seguir detalha o pipeline de processamento do OpenGL. Para a maior parte do pipeline, você pode ver três setas verticais entre os principais estágios. Essas setas representam vértices e os dois tipos principais de dados que podem ser associados a vértices: valores de cor e coordenadas de textura. Observe também que os vértices são montados em primitivos, em fragmentos e, finalmente, em pixels no framebuffer. Essa progressão é discutida em mais detalhes em [vértices](vertices.md), [primitivos](primitives.md), [fragmentos](fragments.md)e [pixels](pixels.md).

![Diagrama mostrando o pipeline de processamento OpenGL.](images/proc01.png)

 

 




