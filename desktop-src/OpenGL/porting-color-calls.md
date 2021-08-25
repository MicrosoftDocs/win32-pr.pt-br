---
title: Portando chamadas de cor
description: A tabela a seguir lista as funções de cor IRIS GL e suas funções equivalentes do OpenGL.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Portação IRIS GL, cor
- portando de IRIS GL, cor
- portando para OpenGL de IRIS GL,color
- Portação openGL de IRIS GL, cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e15774f66964c11527955b57651e69db26f6f3d3704d114fdfa4de9a0d5b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777046"
---
# <a name="porting-color-calls"></a>Portando chamadas de cor

A tabela a seguir lista as funções de cor IRIS GL e suas funções equivalentes do OpenGL.



| Função IRIS GL                  | Função OpenGL                                                                                                                               | Significado                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Define a cor RGB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Define o índice de cores.                                |
| **Getcolor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ CURRENT \_ INDEX )                                               | Retorna o índice de cores atual.                     |
| **getmcolor**                     |                                                                                                                                               | Obtém uma cópia dos valores RGB para uma entrada de mapa de cores. |
| **gRGBcolor**                     | **glGet**( GL \_ CURRENT \_ COLOR )                                                                                                               | Obtém os valores de cor RGB atuais.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **Rgbcolor**                      | **glColor**                                                                                                                                   | Define a cor RGB.                                      |
| **writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Define a máscara de cor do modo de índice de cores.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Define a máscara de modo de cor RGB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ COLOR \_ WRITEMASK )**glGet**( GL \_ INDEX \_ WRITEMASK )<br/> | Obtém a máscara de cor.                                 |
| **gRGBmask**                      | **glGet**( GL \_ COLOR \_ WRITEMASK )                                                                                                             | Obtém a máscara de cor.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Tenha cuidado ao substituir **zwritemask** por [**glDepthMask**](gldepthmask.md); **glDepthMask** aceita um argumento booliana, enquanto **zwritemask** leva um campo de bits.

 

Se você quiser usar vários mapas de cores, precisará usar as funções Windows mapa de cores apropriadas. Portanto, **multimap**, **onemap**, **getcmmode,** **setmap** e **getmap** não têm equivalentes openGL.

 

 





