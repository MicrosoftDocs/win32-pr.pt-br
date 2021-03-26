---
description: As paletas de meio-tom devem ser usadas sempre que o modo de alongamento de um contexto de dispositivo for definido como meio-tom.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Paleta de retícula e ajuste de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502418"
---
# <a name="halftone-palette-and-color-adjustment"></a>Paleta de retícula e ajuste de cor

As paletas de meio-tom devem ser usadas sempre que o modo de alongamento de um contexto de dispositivo for definido como meio-tom. Um aplicativo cria uma paleta de meio-tom usando a função [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) . O aplicativo deve selecionar e perceber essa paleta no contexto do dispositivo antes de chamar a função [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ou [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .

O sistema ajusta automaticamente a cor de entrada dos bitmaps de origem sempre que os aplicativos chamam as funções [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e o modo de alongamento de um contexto de dispositivo é definido como meio-tom. Esses ajustes de cor afetam determinados atributos da imagem, como contraste e brilho. Um aplicativo pode definir os valores de ajuste de cor usando a função [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) . O aplicativo pode recuperar os valores de ajuste de cor para o contexto de dispositivo especificado usando a função [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .

 

 



