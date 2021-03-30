---
description: A classe de dispositivo MIDI/in consiste em seqüenciais MIDI que são usados para entrada. Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646659"
---
# <a name="midiin"></a>MIDI/in

A classe de dispositivo MIDI/in consiste em seqüenciais MIDI que são usados para entrada. Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).

As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esse membro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

O membro **DeviceID** é o identificador de um dispositivo MIDI fechado. Você usa esse identificador em uma chamada para a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) para abrir o dispositivo para entrada. Você pode usar o identificador de dispositivo resultante para registrar dados MIDI do dispositivo de linha ou telefone.

Para obter mais informações sobre as funções de MIDI, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).

 

 
