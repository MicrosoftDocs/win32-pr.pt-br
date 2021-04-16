---
title: Portando viewports, Screenmasks e Scrboxes
description: As seguintes funções do visor do íris GL não têm nenhum equivalente em OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Portabilidade do íris GL, funções do visor
- portando do íris GL, funções do visor
- portando para OpenGL do íris GL, funções do visor
- Portabilidade do OpenGL do íris GL, funções do visor
- funções do visor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757497"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Portando viewports, Screenmasks e Scrboxes

As seguintes funções do visor do íris GL não têm nenhum equivalente em OpenGL:

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Com a função **viewport** GL do íris, você especifica as coordenadas x (em pixels) à esquerda e à direita de um retângulo do visor e as coordenadas y para as partes superior e inferior. No entanto, com a função OpenGL [**glViewport**](glviewport.md) , você especifica as coordenadas x e y (em pixels) do canto inferior esquerdo do retângulo do visor, juntamente com sua largura e altura.

A tabela a seguir lista as funções do viewport GL do íris e suas funções OpenGL equivalentes.



| Função GL de íris                          | Função OpenGL                                                                                         | Significado                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **visor** (esquerda, direita, inferior, superior) | [**glViewport**](glviewport.md) (x, y, largura, altura)                                                | Define o visor.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( \_ bit GL \_ viewport)<br/> | Envia e exibe a pilha.   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ viewport)               | Retorna dimensões do visor. |



 

??

 

 





