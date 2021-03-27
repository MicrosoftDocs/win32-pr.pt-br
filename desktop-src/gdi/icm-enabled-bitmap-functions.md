---
description: O Microsoft Image Color Management (ICM) garante que uma imagem colorida, um objeto gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled funções de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827649"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled funções de bitmap

O Microsoft Image Color Management (ICM) garante que uma imagem colorida, um objeto gráfico ou um objeto de texto seja renderizado o mais próximo possível de sua intenção original em qualquer dispositivo, apesar das diferenças nas tecnologias de geração de imagens e funcionalidades de cores entre os dispositivos. Quer você esteja verificando uma imagem ou outro gráfico em um scanner de cor, baixando-o pela Internet, exibindo ou editando-o na tela ou imprimindo-o em papel, filme ou outra mídia, o ICM 2,0 ajuda a manter as cores consistentes e precisas. Para obter mais informações sobre o ICM, consulte [sistema de cores do Windows](/previous-versions//dd372446(v=vs.85)).

Há várias funções na interface gráfica de dispositivo (GDI) que usam ou operam em dados de cores. As seguintes funções de bitmap estão habilitadas para uso com o ICM:

-   [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
