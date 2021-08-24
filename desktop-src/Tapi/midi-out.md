---
description: A classe de dispositivo midi/out consiste em sequenciadores MIDI usados para saída. Você acessa esses dispositivos usando as funções MIDI, que são descritas no SDK (Kit de Desenvolvimento de Software de Plataforma).
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: midi/out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c0199cc7918ab9aeacb3210b6f98d5ff03fc3bca90624bee00d864727ae0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518606"
---
# <a name="midiout"></a>midi/out

A classe de dispositivo midi/out consiste em sequenciadores MIDI usados para saída. Você acessa esses dispositivos usando as funções MIDI, que são descritas no SDK (Kit de Desenvolvimento de Software de Plataforma).

As [**funções lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) definindo o membro **dwStringFormat** como o valor BINARY STRINGFORMAT e adicionando este \_ membro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

O **membro DeviceId** é o identificador de um dispositivo MIDI fechado. Use esse identificador em uma chamada para a [**função midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) para abrir o dispositivo para saída. Você pode usar o alça do dispositivo resultante para reproduzir dados MIDI na linha ou no dispositivo de telefone.

Para obter mais informações sobre as funções MIDI, consulte [**Funções multimídia**](../multimedia/multimedia-functions.md).

 

 
