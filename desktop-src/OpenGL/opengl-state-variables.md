---
title: Variáveis de estado OpenGL
description: Os tópicos a seguir listam os nomes das variáveis de estado que podem ser consultadas
ms.assetid: f4bc4ec1-a529-4b9e-84af-94caa0ef7131
keywords:
- Variáveis de estado OpenGL
- variáveis de estado, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36dee51ba7726277832d94eaf336d03d3c579189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753730"
---
# <a name="opengl-state-variables"></a>Variáveis de estado OpenGL

Os tópicos a seguir listam os nomes das variáveis de estado que podem ser consultadas:

-   [**Variáveis de estado para valores atuais e dados associados**](state-variables-for-current-values-and-associated-data.md)
-   [**Variáveis de estado de transformação**](transformation-state-variables.md)
-   [**Variáveis de estado de coloração**](coloring-state-variables.md)
-   [**Variáveis de estado de iluminação**](lighting-state-variables.md)
-   [**Variáveis de estado de rasterização**](rasterization-state-variables.md)
-   [**Variáveis de estado texturing**](texturing-state-variables.md)
-   [**Operações de pixel**](pixel-operations.md)
-   [**Variáveis de estado de controle framebuffer**](framebuffer-control-state-variables.md)
-   [**Variáveis de estado de pixel**](pixel-state-variables.md)
-   [**Variáveis de estado do avaliador**](evaluator-state-variables.md)
-   [**Variáveis de estado de dica**](hint-state-variables.md)
-   [**Variáveis de estado dependentes da implementação**](implementation-dependent-state-variables.md)
-   [**Variáveis de estado de Pixel-Depth dependentes da implementação**](implementation-dependent-pixel-depth-state-variables.md)
-   [**Variáveis de estado diversas**](miscellaneous-state-variables.md)

Para cada variável, o tópico lista uma descrição, um grupo de atributos, um valor inicial ou mínimo e a função [**glGet \***](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) sugerida a ser usada para obtê-lo.

As variáveis de estado que você pode obter usando [**glGetBooleanv**](glgetbooleanv.md), [**glGetIntegerv**](glgetintegerv.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetDoublev**](glgetdoublev.md) são listadas com apenas um desses functionsthe, que é mais apropriado para o tipo de dados a ser retornado. Você não pode obter essas variáveis de estado usando [**glIsEnabled**](glisenabled.md). No entanto, você pode obter variáveis de estado para as quais **glIsEnabled** está listado como a função de consulta com **glGetBooleanv**, **glGetIntegerv**, **glGetFloatv** e **glGetDoublev**. Você pode obter variáveis de estado para as quais qualquer outra função está listada como a função de consulta somente usando essa função. Se nenhum grupo de atributos estiver listado, a variável não pertence a nenhum grupo. Todas as variáveis de estado que você pode consultar, exceto aquelas que são dependentes de implementação, têm valores iniciais. Para determinar o valor inicial de uma variável para a qual nenhum valor inicial está listado, consulte a referência da variável ou a

*Manual de referência OpenGL*.

 

 




