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
ms.openlocfilehash: 5485365a6c846556a1037f55a0b211755ce0f93162bc6720c7241353fc8625b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037096"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Parando, pausando e retomando um dispositivo

O [**comando stop**](stop.md) ([**MCI \_ STOP**](mci-stop.md)) suspende a reprodução ou a gravação de um dispositivo. Muitos dispositivos também são compatíveis [**com o comando pause**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)). A diferença entre **parar** **e pausar** depende do dispositivo. Geralmente, **pausar** suspende a operação, mas deixa o dispositivo pronto para retomar a reprodução ou a gravação imediatamente.

Usar o comando [**play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) ou [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) para reiniciar um dispositivo redefine os locais especificados com os sinalizadores "to" (MCI TO) e \_ "from" (MCI FROM) antes que o dispositivo seja pausado ou \_ interrompido. Sem o sinalizador "from", esses comandos redefinem o local inicial para a posição atual. Sem o sinalizador "para", eles redefinem o local final para o final da mídia. Para continuar reproduzindo ou gravando sem redefinir  uma posição de parada especificada anteriormente, use o sinalizador "to" do comando play ou **record** para especificar uma posição final.

Alguns dispositivos são [**compatíveis com o comando resume**](resume.md) ([**MCI \_ RESUME**](mci-resume.md)) para reiniciar um dispositivo em pausa. Esse comando não altera os locais "para" e "de" especificados com o comando **play** ou **record** que precedeu o [**comando pause.**](pause.md)

 

 




