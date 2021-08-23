---
title: Recorte (OpenGL)
description: O recorte ocorre em duas etapas
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Pipeline de processamento de OpenGL, recorte
- OpenGL de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb518b9208b73dad2071531f6a30cdff6cab2ec5dcbe937fa3e66fea8bb0a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289036"
---
# <a name="clipping-opengl"></a>Recorte (OpenGL)

O recorte ocorre em duas etapas:

1.  **Exiba o recorte específico do volume clippingApplication.** Imediatamente após os primitivos serem montados, eles são recortados em coordenadas de olho, conforme necessário, para todos os planos de recorte que você definiu com [**glClipPlane**](glclipplane.md). (O OpenGL requer suporte para pelo menos seis planos de recorte específicos do aplicativo.)
2.  Os primitivos são transformados pela matriz de projeção em coordenadas de clipes e recortados pelo volume de exibição correspondente. Essa matriz pode ser controlada pelas funções de transformação de matriz (consulte [transformações de matriz](matrix-transformations.md)), mas normalmente é especificada por [**glFrustum**](glfrustum.md) ou [**glOrtho**](glortho.md).

Pontos, segmentos de linha e polígonos são tratados de forma diferente durante o recorte:

-   Os pontos são retidos em seu estado original (se estiverem dentro do volume do clipe) ou descartados (se estiverem fora do volume do clipe).
-   Se partes de segmentos de linha ou polígonos estiverem fora do volume do clipe, novos vértices serão gerados nos pontos de corte.
-   Para polígonos, talvez seja necessário construir uma borda inteira entre os novos vértices gerados nos pontos de corte.
-   Para os segmentos de linha e polígonos recortados, as informações de sinalizador de borda, cor e textura são atribuídas a todos os novos vértices.

 

 




