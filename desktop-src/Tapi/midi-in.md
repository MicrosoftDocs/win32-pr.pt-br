---
description: A classe de dispositivo midi/in consiste em sequenciadores MIDI usados para entrada. Você acessa esses dispositivos usando as funções MIDI, que são descritas no SDK (Kit de Desenvolvimento de Software de Plataforma).
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: midi/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d309fe510b08a1e86ef6a00b34a9e3d3282c993babe78eb45aeb6ebb0dab1eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659946"
---
# <a name="midiin"></a>midi/in

A classe de dispositivo midi/in consiste em sequenciadores MIDI usados para entrada. Você acessa esses dispositivos usando as funções MIDI, que são descritas no SDK (Kit de Desenvolvimento de Software de Plataforma).

As [**funções lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) preenchem uma estrutura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) definindo o membro **dwStringFormat** como o valor BINARY STRINGFORMAT e adicionando este \_ membro adicional:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

O **membro DeviceId** é o identificador de um dispositivo MIDI fechado. Use esse identificador em uma chamada para a [**função midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) para abrir o dispositivo para entrada. Você pode usar o alça do dispositivo resultante para registrar dados MIDI da linha ou do dispositivo de telefone.

Para obter mais informações sobre as funções MIDI, consulte [**Funções multimídia**](../multimedia/multimedia-functions.md).

 

 
