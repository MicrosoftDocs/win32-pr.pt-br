---
title: Pontos de portação
description: O OpenGL não tem nenhum comando para desenhar um único ponto. Caso contrário, as funções de ponto de portação são simples. A tabela a seguir lista as funções IRIS GL para pontos de desenho e suas funções OpenGL equivalentes.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Portação IRIS GL, pontos
- portando de IRIS GL, pontos
- portando para OpenGL de IRIS GL, pontos
- Portação openGL de IRIS GL, pontos
- funções de desenho, pontos
- pontos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ef24ad81942681b3d70a303a22e89e9573aa609d3f08f52a92583ae88e0e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012064"
---
# <a name="porting-points"></a>Pontos de portação

O OpenGL não tem nenhum comando para desenhar um único ponto. Caso contrário, as funções de ponto de portação são simples. A tabela a seguir lista as funções IRIS GL para pontos de desenho e suas funções OpenGL equivalentes.



| Função IRIS GL           | Função OpenGL                                                   | Significado                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pnt**                    |                                                                   | Desenha um único ponto.                                                                                                                                |
| **bgnpoint**, **ponto de extremidade** | [**glBegin**](glbegin.md) ( GL \_ POINTS ), [ **glEnd**](glend.md) | Interpreta vértices como pontos.                                                                                                                       |
| **pntsize**                | [**glPointSize**](glpointsize.md)                                | Define o tamanho do ponto em pixels.                                                                                                                           |
| **pntsmooth**              | [**glEnable**](glenable.md) ( GL \_ POINT \_ SMOOTH )                | Liga a antialiação de ponto. (Para obter mais informações sobre a antialiação de ponto, consulte Portando funções [antialiasing](porting-antialiasing-functions.md).) |



 

Para obter informações sobre funções get relacionadas, [**consulte glPointSize**](glpointsize.md).

??

 

 




