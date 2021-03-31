---
title: Usando paletas do MCIWnd
description: Usando paletas do MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- Macro MCIWndGetPalette
- Macro MCIWndSetPalette
- Macro MCIWndRealize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917272"
---
# <a name="using-mciwnd-palettes"></a>Usando paletas do MCIWnd

A reprodução de clipes de vídeo com intensidade de cor de 8 bits (256-capacidade de cor) requer uma paleta para definir as cores que estão sendo usadas. Às vezes, a paleta incluída com um videoclipe não é a paleta mais apropriada a ser usada durante a reprodução. Nesse caso, o MCIWnd fornece três maneiras de gerenciar paletas para reprodução:

-   Recupere um identificador para a paleta associada a uma janela MCIWnd usando a macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) . A paleta não está necessariamente associada exclusivamente à janela MCIWnd. Outros aplicativos podem acessar, e até mesmo invalidar, o identificador da paleta. Consequentemente, seu aplicativo deve antecipar o uso global da paleta e, quando terminar com a paleta, não deve liberá-la.
-   Especifique uma nova paleta a ser usada com o clipe de vídeo associado a uma janela MCIWnd usando a macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .
-   Perceba a paleta associada a uma janela do MCIWnd para a paleta do sistema usando a macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) . Essa macro chama a função [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) com a paleta associada à janela MCIWnd. Se os manipuladores de mensagens do aplicativo para o [**WM \_ PaletteChanged**](/windows/desktop/gdi/wm-palettechanged) e o [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) chamarem somente **RealizePalette** ou **MCIWndRealize**, você deverá encaminhar essas mensagens para MCIWnd se não as tratar.

> [!Note]  
> Quando um clipe de vídeo com profundidade de cor de 8 bits é carregado na janela MCIWnd, a paleta incluída nesse clipe substitui a paleta associada à janela MCIWnd.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimoramentos de reprodução](playback-enhancements.md)
</dt> </dl>

 

 