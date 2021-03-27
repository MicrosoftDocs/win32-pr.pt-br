---
description: O sistema manipula cores em bitmaps de forma diferente das cores em canetas, pincéis e texto.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Cor em bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091205"
---
# <a name="color-in-bitmaps"></a>Cor em bitmaps

O sistema manipula cores em bitmaps de forma diferente das cores em canetas, pincéis e texto. Os bitmaps compatíveis, criados usando a função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , são específicos do dispositivo e retêm informações de cores em um formato dependente de dispositivo. Nenhum valor de cor é usado e as cores não estão sujeitas a aproximações e pontilhamento.

Os bitmaps independentes de dispositivo (DIBs) retêm informações de cores como valores de cor ou índices de paleta de cores. Se forem usados valores de cor, as cores estarão sujeitas à aproximação, mas não ao pontilhamento. Os índices de paleta de cores só podem ser usados com dispositivos que dão suporte a paletas de cores. Embora o sistema não tenha cores aproximadas ou pontilhadas identificadas por índices, a cor resultante pode ser diferente daquela desejada, pois os índices geram resultados válidos apenas no contexto da paleta de cores que era atual no momento em que o bitmap foi criado. Se a paleta for alterada, faça as cores no bitmap. Para obter mais informações sobre índices de paleta, consulte [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).

Além de referenciar a paleta lógica, um aplicativo também pode fazer referência a um valor em uma tabela de cores DIB. Para selecionar uma cor em uma tabela de cores DIB, chame [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex). Observe que isso só é possível para um contexto de dispositivo que tenha um DIB selecionado para ele.

 

 



