---
title: Transportando a cor, o sombreamento e o código Writemask
description: Transportando a cor, o sombreamento e o código Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Portabilidade do íris GL, cor
- portando do íris GL, cor
- portando para OpenGL do íris GL, cor
- Portabilidade do OpenGL do íris GL, cor
- Portabilidade do íris GL, sombreamento
- portando do íris GL, sombreamento
- portando para OpenGL do íris GL, sombreamento
- Portabilidade do OpenGL do íris GL, sombreamento
- Portabilidade do íris GL, writemask
- portando do íris GL, writemask
- portando para OpenGL do íris GL, writemask
- Portabilidade OpenGL do íris GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635224"
---
# <a name="porting-color-shading-and-writemask-code"></a>Transportando a cor, o sombreamento e o código Writemask

Ao portar a cor, o sombreamento e o código writemask para OpenGL, tenha em mente os seguintes pontos:

-   Embora você possa definir índices de mapa de cores com a função OpenGL [glIndex](glindex-functions.md) , o OpenGL não tem uma função para carregar índices de mapa de cores.
-   Os valores de cor são normalizados para seu tipo de dados. (Para obter informações sobre valores de cor, consulte [glColor](glcolor-functions.md)).
-   Não há um equivalente simples para **cpack**.
-   Talvez seja necessário converter o código que inclui as funções **c** ou **Color** para [**glClearColor**](glclearcolor.md) ou [**glClearIndex**](glclearindex.md) em vez de **glColor** ou **glIndex**.
-   O writemask RGBA se aplica a cada componente, mas não a cada bit.
-   A íris GL fornece constantes de cores definidas: preto, azul, vermelho, verde, MAGENTA, ciano, amarelo e branco. O OpenGL não fornece essas constantes.

Este tópico inclui informações sobre o seguinte.

-   [Portando chamadas de cores](porting-color-calls.md)
-   [Modelos de sombreamento de portador](porting-shading-models.md)

 

 




