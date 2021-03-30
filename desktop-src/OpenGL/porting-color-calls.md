---
title: Portando chamadas de cores
description: A tabela a seguir lista as funções de cor do íris GL e suas funções OpenGL equivalentes.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Portabilidade do íris GL, cor
- portando do íris GL, cor
- portando para OpenGL do íris GL, cor
- Portabilidade do OpenGL do íris GL, cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635223"
---
# <a name="porting-color-calls"></a>Portando chamadas de cores

A tabela a seguir lista as funções de cor do íris GL e suas funções OpenGL equivalentes.



| Função GL de íris                  | Função OpenGL                                                                                                                               | Significado                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | Define a cor RGB.                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | Define o índice de cores.                                |
| **GetColor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ índice atual do GL \_ )                                               | Retorna o índice de cores atual.                     |
| **getmcolor**                     |                                                                                                                                               | Obtém uma cópia dos valores RGB para uma entrada de mapa de cores. |
| **gRGBcolor**                     | **glGet**( \_ cor atual do GL \_ )                                                                                                               | Obtém os valores de cor RGB atuais.                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **RGBcolor**                      | **glColor**                                                                                                                                   | Define a cor RGB.                                      |
| **writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | Define a máscara de cor do modo de índice de cor.                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | Define a máscara do modo de cor RGB.                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Color \_ WRITEMASK)**glGet**( \_ índice GL \_ WRITEMASK)<br/> | Obtém a máscara de cor.                                 |
| **gRGBmask**                      | **glGet**(GL de \_ cor \_ WRITEMASK)                                                                                                             | Obtém a máscara de cor.                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> Tenha cuidado ao substituir **zwritemask** por [**glDepthMask**](gldepthmask.md); **glDepthMask** usa um argumento booliano, enquanto **zwritemask** usa um campo de bits.

 

Se você quiser usar vários mapas de cores, precisará usar as funções apropriadas do mapa de cores do Windows. Portanto, **Multimap**, **onemap**, **getcmmode**, **Setmap** e **GetMap** não têm equivalentes OpenGL.

 

 





