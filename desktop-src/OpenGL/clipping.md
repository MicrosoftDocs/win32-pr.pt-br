---
title: Recorte (OpenGL)
description: O recorte ocorre em duas etapas
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Pipeline de processamento de OpenGL, recorte
- OpenGL de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369123"
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

 

 




