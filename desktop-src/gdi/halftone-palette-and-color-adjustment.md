---
description: Paletas de meio tom devem ser usadas sempre que o modo de alongamento de um contexto de dispositivo for definido como HALFTONE.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Paleta de meio tom e ajuste de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be13f780dc5496173ffb4ddb990a96f7dbe462223e41e8a48d4a58329451277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761000"
---
# <a name="halftone-palette-and-color-adjustment"></a>Paleta de meio tom e ajuste de cor

Paletas de meio tom devem ser usadas sempre que o modo de alongamento de um contexto de dispositivo for definido como HALFTONE. Um aplicativo cria uma paleta de meio-tom usando a [**função CreateHalftonePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) O aplicativo deve selecionar e realizar essa paleta no contexto do dispositivo antes de chamar a [**função StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ou [**StretchDIBits.**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

O sistema ajusta automaticamente a cor de entrada dos bitmaps de origem sempre que os aplicativos chamam as funções [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e o modo de alongamento de um contexto de dispositivo é definido como HALFTONE. Esses ajustes de cor afetam determinados atributos da imagem, como contraste e brilho. Um aplicativo pode definir os valores de ajuste de cor usando a [**função SetColorAdjustment.**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) O aplicativo pode recuperar os valores de ajuste de cor para o contexto do dispositivo especificado usando a [**função GetColorAdjustment.**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment)

 

 



