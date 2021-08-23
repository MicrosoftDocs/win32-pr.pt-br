---
title: Iniciando, pausando e retomando a reprodução
description: Iniciando, pausando e retomando a reprodução
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- Macro MCIWndPlay
- Macro MCIWndPause
- Macro MCIWndResume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49977b9bc741c6b32ce0da0c0ae9f63bd875a24268a00bb4782cd71531a4ef31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688666"
---
# <a name="starting-pausing-and-resuming-playback"></a>Iniciando, pausando e retomando a reprodução

[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) é a macro de reprodução mais geral. Essa macro permite que você reproduza um arquivo ou dispositivo da posição de reprodução atual. A reprodução continua até o final do conteúdo, a menos que seja interrompida.

Você pode interromper temporariamente um dispositivo que está sendo executado usando a macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) . Para retomar a reprodução da posição pausada, use a macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) . Alguns dispositivos não dão suporte aos comandos Pause e resume. Esses dispositivos geralmente mapeiam **MCIWndPause** para a macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , que interrompe a reprodução ou a gravação. Você pode reiniciar um dispositivo que não dá suporte a Pause ou resume usando **MCIWndPlay**, que inicia a reprodução a partir da posição de reprodução atual.

 

 




