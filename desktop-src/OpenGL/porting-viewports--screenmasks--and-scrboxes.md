---
title: Portando Viewports, Screenmasks e Scrboxes
description: As seguintes funções do viewport IRIS GL não têm equivalente a OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Portação IRIS GL, funções de viewport
- portating from IRIS GL,viewport functions
- portando para OpenGL do IRIS GL, funções de viewport
- Portação openGL de IRIS GL, funções de viewport
- funções viewport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb1a01cfb038faf87e48381856fe281bf2c935d13fedb78b79266e2af4fe15e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776906"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Portando Viewports, Screenmasks e Scrboxes

As seguintes funções do viewport IRIS GL não têm equivalente a OpenGL:

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Com a função **de viewport** IRIS GL, você especifica as coordenadas x (em pixels) para a esquerda e a direita de um retângulo do viewport e as coordenadas y para as coordenadas superior e inferior. Com a função [**GlViewport**](glviewport.md) do OpenGL, no entanto, você especifica as coordenadas x e y (em pixels) do canto inferior esquerdo do retângulo do viewport junto com sua largura e altura.

A tabela a seguir lista as funções do viewport IRIS GL e suas funções equivalentes do OpenGL.



| Função IRIS GL                          | Função OpenGL                                                                                         | Significado                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **viewport** ( left, right, bottom, top ) | [**glViewport**](glviewport.md) ( x, y, width, height )                                                | Define o viewport.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL \_ VIEWPORT BIT \_ )<br/> | Es por push e a pilha é pop-pop.   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ VIEWPORT )               | Retorna dimensões do viewport. |



 

??

 

 





