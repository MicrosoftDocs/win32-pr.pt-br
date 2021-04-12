---
title: Revertendo a reprodução
description: Revertendo a reprodução
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- Macro MCIWndPlayReverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363965"
---
# <a name="reversing-playback"></a>Revertendo a reprodução

Alguns dispositivos dão suporte à reprodução na direção inversa. Você pode reproduzir o conteúdo desse dispositivo na direção inversa usando a macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) . Essa macro define o escopo de reprodução da posição de reprodução atual para o início do conteúdo. O dispositivo de vídeo digital, MCIAVI. DRV, pode reproduzir para trás. Dispositivos que não podem reproduzir, como áudio de CD, podem emitir uma mensagem de erro quando **MCIWndPlayReverse** é invocado.

 

 




