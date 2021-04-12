---
title: Ajustando a velocidade, o volume e o zoom
description: Ajustando a velocidade, o volume e o zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- Macro MCIWndSetSpeed
- Macro MCIWndGetSpeed
- Macro MCIWndSetVolume
- Macro MCIWndGetVolume
- Macro MCIWndSetZoom
- Macro MCIWndGetZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364041"
---
# <a name="adjusting-speed-volume-and-zoom"></a>Ajustando a velocidade, o volume e o zoom

A velocidade, o volume e as macros de zoom fornecem a funcionalidade dos comandos de **exibição**, **volume** e **velocidade** no menu MCIWnd. As macros descritas nesta seção geralmente são usadas com vídeo e outros dispositivos que exibem imagens durante a reprodução.

Alguns dispositivos dão suporte a várias alterações na velocidade de reprodução. Você pode definir a velocidade de reprodução para esses dispositivos usando a macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) . Essa macro define a velocidade de reprodução como 1000. Valores mais altos indicam velocidades mais rápidas. Valores mais baixos indicam velocidades mais lentas.

Você pode recuperar a velocidade de reprodução atual usando a macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) . Essa macro usa os mesmos valores e intervalos usados pelo **MCIWndSetSpeed**.

Alguns dispositivos dão suporte a alterações de volume. Você pode ajustar ou definir o volume usando a macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) . Essa macro define o nível de volume normal como 1000. Valores mais altos indicam volumes mais altos. Valores mais baixos indicam volumes mais silenciosos.

Você pode recuperar o nível de volume atual usando a macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) . Essa macro usa os mesmos valores numéricos e o intervalo usado pelo **MCIWndSetVolume**.

Para dispositivos que usam uma janela de reprodução, o MCIWnd dá suporte a um recurso de zoom que define o tamanho da imagem de reprodução. Você pode definir o tamanho da imagem de reprodução usando a macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) . A macro redefine o tamanho da imagem de reprodução enquanto mantém uma taxa de proporção constante para a imagem. O valor de zoom é definido como uma porcentagem do tamanho da imagem original. Assim, 100 representa o tamanho original da imagem, 50 indica que a imagem mostrada é metade do tamanho original e 200 indica que a imagem mostrada é duas vezes seu tamanho original.

Você pode recuperar o valor de zoom atual usando a macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) . Essa macro usa os mesmos valores e intervalos usados pelo **MCIWndSetZoom**.

> [!Note]  
> Os drivers áudio de CD MCI e Wave-audio padrão não dão suporte a alterações de volume ou velocidade.

 

 

 




