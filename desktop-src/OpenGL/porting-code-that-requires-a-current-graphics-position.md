---
title: Código de porta que precisa de uma posição de gráfico atual
description: O OpenGL não mantém uma posição gráfica atual. As funções da íris GL que dependem da posição de gráficos atual, como mover, desenhar e RMV, não têm equivalentes em OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Portabilidade do íris GL, posição de gráficos atual
- portando do íris GL, posição de gráficos atual
- portando para OpenGL do íris GL, posição de gráficos atual
- Portabilidade OpenGL do íris GL, posição de gráficos atual
- posição de gráficos atual
- posições de rasterização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2354264ed5ad022c0657c95a31007ad33df2882d3c9ab2c44cfafeea99b53d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485786"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>Código de porta que precisa de uma posição de gráfico atual

O OpenGL não mantém uma posição gráfica atual. As funções da íris GL que dependem da posição de gráficos atual, como **mover**, **desenhar** e **RMV**, não têm equivalentes em OpenGL.

Versões mais antigas do íris GL incluíam comandos de desenho que se basearam na posição de gráficos atual, embora seu uso tenha sido desencorajado. Você precisará reescrever seu código se tiver confiado na posição gráfica atual de qualquer forma ou usar uma das seguintes rotinas:

-   **desenhar** e **mover**
-   **PMV**, **Laos** e **PCLOS**
-   **rdr**, **RMV**, **rpdr** e **rpmv**
-   **getgpos**

O OpenGL tem um conceito de posição de rasterização que corresponde à posição de caractere atual do íris GL. Para obter mais informações sobre o posicionamento de rasterização, consulte [portando operações de pixel](porting-pixel-operations.md).

Este tópico inclui informações sobre o seguinte.

-   [Comandos de limpeza de tela e buffer de portabilidade](porting-screen-and-buffer-clearing-commands.md)
-   [Portando funções de matriz e transformação](porting-matrix-and-transformation-functions.md)
-   [Portando o código do modo MSINGLE](porting-msingle-mode-code.md)
-   [Funções de portabilidade que obtêm matrizes e transformações](porting-functions-that-get-matrices-and-transformations.md)
-   [Portando viewports, Screenmasks e Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [Portando planos de recorte](porting-clipping-planes.md)

 

 




