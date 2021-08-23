---
title: tempo (Windows multimídia)
description: Timing
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, tempo
- Função DrawDibTime
- DrawDib, depuração
- Depurando DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc4324de5336a00b246ad644794ce8d0b3491bb644f34e8fc22dc8a7e460ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688076"
---
# <a name="timing-windows-multimedia"></a>tempo (Windows multimídia)

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

 

 
