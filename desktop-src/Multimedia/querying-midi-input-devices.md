---
title: Consultando dispositivos de entrada MIDI
description: Consultando dispositivos de entrada MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- MIDI (interface digital de instrumento musical), dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), dispositivos de entrada
- gravando áudio MIDI, dispositivos de entrada
- Dispositivos de entrada MIDI
- MIDI (interface digital de instrumento musical), consultando dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), consultando dispositivos de entrada
- gravando áudio MIDI, consultando dispositivos de entrada
- consultando dispositivos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81340f767c1ef3acf3105f78d2cef000f7548361b387e6887ecc4136437dbe6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371928"
---
# <a name="querying-midi-input-devices"></a>Consultando dispositivos de entrada MIDI

Antes de gravar áudio MIDI, você deve usar a função [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) para determinar os recursos do dispositivo de entrada MIDI que está presente no sistema. Essa função usa um endereço de uma estrutura [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) , que preenche as informações sobre os recursos do determinado dispositivo. Essas informações incluem os identificadores de fabricante e produto, um nome de produto para o dispositivo e o número de versão do driver de dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 