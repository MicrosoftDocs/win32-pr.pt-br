---
title: Linhas de porta
description: Portar código GL do íris que desenha linhas é razoavelmente simples, embora você deva observar as diferenças no modo OpenGL stipples. A tabela a seguir lista as funções da íris GL para desenhar linhas e suas funções OpenGL equivalentes.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Portabilidade do íris GL, linhas
- portando do íris GL, linhas
- portando para OpenGL do íris GL, linhas
- Portabilidade OpenGL do íris GL, linhas
- funções de desenho, linhas
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160204"
---
# <a name="porting-lines"></a>Linhas de porta

Portar código GL do íris que desenha linhas é razoavelmente simples, embora você deva observar as diferenças no modo OpenGL stipples. A tabela a seguir lista as funções da íris GL para desenhar linhas e suas funções OpenGL equivalentes.



| Função GL de íris                               | Função OpenGL                                                                                         | Significado                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**preclosed**<br/> | [**glBegin**](glbegin.md) ( \_ loop de linha gl \_ )[**glEnd**](glend.md)<br/>                          | Desenha uma linha fechada.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) ( \_ faixa de linha gl \_ )                                                          | Desenha segmentos de linha.                                                                                                                         |
| **linewidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Define a largura da linha.                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ largura da linha gl \_ )            | Retorna a largura da linha atual.                                                                                                                  |
| **deflinestyle**,**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | Especifica um padrão de Stipple de linha.                                                                                                            |
| **lsrepeat**                                   | argumento de fator de **glLineStipple**                                                                    | Define um fator de repetição para o estilo de linha.                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ padrão de linha gl \_ STIPPLE \_ ) | Retorna o padrão de Stipple de linha.                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ STIPPLE de linha gl \_ \_ repetir)  | Retorna o fator de repetição.                                                                                                                       |
| **linesmooth**, **suavização**                 | [**glEnable**](glenable.md) ( \_ linha simples de GL \_ )                                                       | Ativa a suavização de linha (para obter mais informações sobre a anti-aliasing, consulte [portando funções de anti-aliasing](porting-antialiasing-functions.md)). |



 

O OpenGL não usa tabelas para a linha stipples; Ele mantém apenas um padrão Stipple de linha. Você pode usar [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) para alternar entre diferentes padrões de Stipple.

Funções de estilo de linha mais antigas do íris GL (como **draw**, **lsbackup**, **getlsbackup** e assim por diante) não são suportadas por OpenGL.

Para obter informações sobre como desenhar linhas AntiAlias, consulte [portando funções de anti-aliasing](porting-antialiasing-functions.md).

??

 

 





