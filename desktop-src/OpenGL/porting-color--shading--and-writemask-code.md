---
title: Cor de portação, sombreamento e código de máscara de gravação
description: Cor de portação, sombreamento e código de máscara de gravação
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Portação IRIS GL, cor
- portando de IRIS GL, cor
- portando para OpenGL de IRIS GL,color
- Portação openGL de IRIS GL, cor
- Portação IRIS GL, sombreamento
- portando de IRIS GL, sombreamento
- portando para OpenGL de IRIS GL, sombreamento
- Portação openGL de IRIS GL, sombreamento
- Portação IRIS GL, writemask
- portando de IRIS GL, writemask
- portando para OpenGL de IRIS GL, writemask
- Portação openGL de IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d3fcb9cf47b45b4b1174cb20e3259dbb883c2fd0414d255a418c52b50fa28e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485776"
---
# <a name="porting-color-shading-and-writemask-code"></a>Cor de portação, sombreamento e código de máscara de gravação

Ao portar cores, sombreamento e código de máscara de gravação para OpenGL, lembre-se dos seguintes pontos:

-   Embora você possa definir índices de mapa de cores com a função [GlIndex](glindex-functions.md) do OpenGL, o OpenGL não tem uma função para carregar índices de mapa de cores.
-   Os valores de cor são normalizados para seu tipo de dados. (Para obter informações sobre valores de cor, consulte [glColor](glcolor-functions.md)).
-   Não há nenhum equivalente simples para **cpack.**
-   Talvez seja preciso converter o código que inclui as funções **c** ou **color** para [**glClearColor**](glclearcolor.md) ou [**glClearIndex em**](glclearindex.md) vez de **glColor** ou **glIndex.**
-   A máscara de gravação RGBA se aplica a cada componente, mas não a cada bit.
-   IRIS GL fornece constantes de cores definidas: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW e WHITE. O OpenGL não fornece essas constantes.

Este tópico inclui informações sobre o seguinte.

-   [Portando chamadas de cor](porting-color-calls.md)
-   [Portando modelos de sombreamento](porting-shading-models.md)

 

 




