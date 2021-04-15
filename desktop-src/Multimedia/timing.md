---
title: Tempo (multimídia do Windows)
description: Timing
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, tempo
- Função DrawDibTime
- DrawDib, depuração
- Depurando DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454528"
---
# <a name="timing-windows-multimedia"></a>Tempo (multimídia do Windows)

Como parte da depuração de um aplicativo, você pode obter informações sobre a quantidade de tempo necessária para concluir operações DrawDib repetitivas. A função [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) retorna informações de tempo para as seguintes operações:

-   Desenhando um bitmap
-   Descompactando um bitmap
-   Pontilhamento de um bitmap
-   Alongando um bitmap
-   Transferindo um bitmap usando a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Transferindo um bitmap usando a função [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Depois de recuperar um conjunto de valores, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) redefine a contagem e o valor de cada operação.

A função [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) está disponível apenas na versão de depuração das funções DrawDib.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de imagem](image-rendering.md)
</dt> </dl>

 

 
