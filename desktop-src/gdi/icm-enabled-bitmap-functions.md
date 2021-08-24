---
description: O ICM (Gerenciamento de Cores de Imagem da Microsoft) garante que uma imagem de cor, objeto gráfico ou objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e nas funcionalidades de cores entre os dispositivos.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: funções ICM-Enabled Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38341851eb9ba2aed25cc93afbf7b869909430a30ecb626bf3a452883fdea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831966"
---
# <a name="icm-enabled-bitmap-functions"></a>funções ICM-Enabled Bitmap

O ICM (Gerenciamento de Cores de Imagem da Microsoft) garante que uma imagem de cor, objeto gráfico ou objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e nas funcionalidades de cores entre os dispositivos. Se você está digitalizando uma imagem ou outro gráfico em um verificador de cores, baixando-a pela Internet, exibindo ou editando-a na tela ou imprimindo-a em papel, filme ou outra mídia, o ICM 2.0 ajuda a manter as cores consistentes e precisas. Para obter mais informações sobre ICM, [consulte Windows Color System](/previous-versions//dd372446(v=vs.85)).

Há várias funções na GDI (interface de dispositivo gráfico) que usam ou operam em dados de cores. As seguintes funções de bitmap estão habilitadas para uso com ICM:

-   [**Bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**Createdibitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**Createdibsection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**Maskblt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**Stretchblt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**Setdibits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**Setdibitstodevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**Stretchdibits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
