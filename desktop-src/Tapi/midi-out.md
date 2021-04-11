---
description: A classe de dispositivo MIDI/out consiste em seqüenciais MIDI que são usados para saída. Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164246"
---
# <a name="midiout"></a>MIDI/out

A classe de dispositivo MIDI/out consiste em seqüenciais MIDI que são usados para saída. Você acessa esses dispositivos usando as funções de MIDI, que são descritas no kit de desenvolvimento de software de plataforma (SDK).

As funções [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , definindo o membro **dwStringFormat** como o \_ valor binário StringFormat e acrescentando esse membro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

O membro **DeviceID** é o identificador de um dispositivo MIDI fechado. Você usa esse identificador em uma chamada para a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) para abrir o dispositivo para saída. Você pode usar o identificador de dispositivo resultante para reproduzir dados MIDI no dispositivo de linha ou telefone.

Para obter mais informações sobre as funções de MIDI, consulte [**funções de multimídia**](../multimedia/multimedia-functions.md).

 

 
