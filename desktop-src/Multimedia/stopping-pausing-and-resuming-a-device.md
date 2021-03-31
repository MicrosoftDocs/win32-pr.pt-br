---
title: Parando, pausando e retomando um dispositivo
description: Parando, pausando e retomando um dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- MCI_STOP comando
- MCI_PAUSE comando
- MCI_RESUME comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635969"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Parando, pausando e retomando um dispositivo

O comando [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) suspende a reprodução ou a gravação de um dispositivo. Muitos dispositivos também dão suporte ao comando [**Pause**](pause.md) ([**\_ pausa MCI**](mci-pause.md)). A diferença entre **parar** e **Pausar** depende do dispositivo. Geralmente, **Pause** suspende a operação, mas deixa o dispositivo pronto para retomar a reprodução ou a gravação imediatamente.

Usando o comando [**Play**](play.md) ([**\_ reprodução MCI**](mci-play.md)) ou [**gravar**](record.md) ([**\_ registro MCI**](mci-record.md)) para reiniciar um dispositivo, redefine os locais especificados com os sinalizadores "para" (MCI \_ para) e "de" (MCI \_ de) antes de o dispositivo ser pausado ou interrompido. Sem o sinalizador "from", esses comandos redefinem o local inicial para a posição atual. Sem o sinalizador "to", eles redefinem o local final para o final da mídia. Para continuar a reproduzir ou gravar sem redefinir uma posição de parada especificada anteriormente, use o sinalizador "para" do comando **Play** ou **Record** para especificar uma posição final.

Alguns dispositivos dão suporte ao comando [**resume**](resume.md) ([**\_ retomar MCI**](mci-resume.md)) para reiniciar um dispositivo em pausa. Esse comando não altera os locais "para" e "de" especificados com o comando **Play** ou **Record** que precede o comando [**Pause**](pause.md) .

 

 




