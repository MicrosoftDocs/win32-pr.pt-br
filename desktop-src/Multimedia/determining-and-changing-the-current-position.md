---
title: Determinando e alterando a posição atual
description: Determinando e alterando a posição atual
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- Macro MCIWndGetStart
- Macro MCIWndGetEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453635"
---
# <a name="determining-and-changing-the-current-position"></a>Determinando e alterando a posição atual

Quando um arquivo ou dispositivo está associado a uma janela MCIWnd, a posição de reprodução é inicialmente definida no início do conteúdo, independentemente do tipo de mídia. Durante a reprodução, a posição da reprodução se move linearmente por meio do conteúdo e, se a reprodução não for interrompida, chegará eventualmente ao final do conteúdo. Se ocorrer uma interrupção, a posição de reprodução atual será o local em que a reprodução foi interrompida ou pausada.

Você pode recuperar os locais para o início e o fim do conteúdo usando as macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) . Você pode determinar o comprimento do conteúdo subtraindo o valor retornado por **MCIWndGetStart** do valor retornado por **MCIWndGetEnd** ou usando a macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) . Você pode recuperar a posição de reprodução atual usando a macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) ou pode recuperar a posição de reprodução como uma cadeia de caracteres terminada em nulo usando a macro [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .

Para alterar a posição de reprodução atual, use as macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)e [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) . Você pode mover a posição de reprodução para o início do conteúdo usando **MCIWndHome** ou para o final do conteúdo usando **MCIWndEnd**. Use **MCIWndSeek** para mover a posição de reprodução para qualquer local no conteúdo.

Você também pode percorrer o conteúdo usando a macro [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) . A partir da posição de reprodução atual, essa macro move a posição de reprodução para frente ou para trás por um incremento especificado.

> [!Note]  
> As unidades usadas para especificar a posição variam entre os diferentes tipos de mídia e dispositivos. Por exemplo, a posição de reprodução para arquivos AVI usados pelo dispositivo MCIAVI é medida em quadros; a posição de reprodução para áudio de CD, wave-áudio e arquivos MIDI é medida em milissegundos.

 

Dispositivos para outros tipos de mídia e dispositivos de terceiros podem usar outras unidades. Para obter informações sobre como determinar essas unidades, consulte [aprimoramentos de reprodução](playback-enhancements.md).

 

 




