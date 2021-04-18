---
title: Pontos de porta
description: O OpenGL não tem nenhum comando para desenhar um único ponto. Caso contrário, as funções de ponto de porta são simples. A tabela a seguir lista as funções do íris GL para pontos de desenho e suas funções OpenGL equivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Portabilidade do íris GL, pontos
- portando do íris GL, pontos
- portando para OpenGL do íris GL, pontos
- Portabilidade OpenGL do íris GL, pontos
- funções de desenho, pontos
- pontos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756709"
---
# <a name="porting-points"></a>Pontos de porta

O OpenGL não tem nenhum comando para desenhar um único ponto. Caso contrário, as funções de ponto de porta são simples. A tabela a seguir lista as funções do íris GL para pontos de desenho e suas funções OpenGL equivalentes.



| Função GL de íris           | Função OpenGL                                                   | Significado                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PNT**                    |                                                                   | Desenha um único ponto.                                                                                                                                |
| **bgnpoint**, **ponto de extremidade** | [**glBegin**](glbegin.md) ( \_ pontos GL), [ **glEnd**](glend.md) | Interpreta vértices como pontos.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Define o tamanho do ponto em pixels.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( \_ sem ajuste de ponto GL \_ )                | Ativa a suavização de ponto. (Para obter mais informações sobre a suavização de ponto, consulte [portando funções de anti-aliasing](porting-antialiasing-functions.md).) |



 

Para obter informações sobre as funções Get relacionadas, consulte [**glPointSize**](glpointsize.md).

??

 

 




