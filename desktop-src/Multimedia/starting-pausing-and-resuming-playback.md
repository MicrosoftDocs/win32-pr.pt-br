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
ms.openlocfilehash: 734a186b90b8d6701923d0ffa1f743cc8c5ae378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160441"
---
# <a name="starting-pausing-and-resuming-playback"></a>Iniciando, pausando e retomando a reprodução

[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) é a macro de reprodução mais geral. Essa macro permite que você reproduza um arquivo ou dispositivo da posição de reprodução atual. A reprodução continua até o final do conteúdo, a menos que seja interrompida.

Você pode interromper temporariamente um dispositivo que está sendo executado usando a macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) . Para retomar a reprodução da posição pausada, use a macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) . Alguns dispositivos não dão suporte aos comandos Pause e resume. Esses dispositivos geralmente mapeiam **MCIWndPause** para a macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , que interrompe a reprodução ou a gravação. Você pode reiniciar um dispositivo que não dá suporte a Pause ou resume usando **MCIWndPlay**, que inicia a reprodução a partir da posição de reprodução atual.

 

 




