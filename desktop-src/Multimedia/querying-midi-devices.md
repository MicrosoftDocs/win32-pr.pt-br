---
title: Consultando dispositivos MIDI
description: Consultando dispositivos MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- MIDI (Instrument Digital Interface Instrument), consultando dispositivos
- MIDI (Interface Digital do Instrument Instrument), consultando dispositivos
- Serviços MIDI, consultando dispositivos
- consultando dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3546971a17a5a8002f0e6d4205ceee5ca796babeb2b27df911cfca5a5911371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372311"
---
# <a name="querying-midi-devices"></a>Consultando dispositivos MIDI

Antes de tocar ou gravar dados MIDI, você deve determinar os recursos do hardware MIDI presente no sistema. A funcionalidade MIDI pode variar de um computador multimídia para o próximo; os aplicativos não devem fazer suposições sobre o hardware presente em um determinado sistema.

Windows fornece as funções a seguir para determinar quantos dispositivos MIDI estão disponíveis para entrada ou saída em um determinado sistema.



| Valor                                          | Significado                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Recupera o número de dispositivos de entrada MIDI presentes no sistema.  |
| [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Recupera o número de dispositivos de saída MIDI presentes no sistema. |



 

Assim como outros dispositivos de áudio, os dispositivos MIDI são identificados por um identificador de dispositivo, que é determinado implicitamente pelo número de dispositivos presentes em um determinado sistema. Os identificadores de dispositivo variam de zero ao número de dispositivos presentes, menos um. Por exemplo, se houver dois dispositivos de saída MIDI em um sistema, os identificadores de dispositivo válidos serão 0 e 1.

Depois de determinar quantos dispositivos de entrada ou saída MIDI estão presentes em um sistema, você pode perguntar sobre os recursos de cada dispositivo. Windows fornece as funções a seguir para determinar os recursos dos dispositivos de áudio.



| Valor                                          | Significado                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Recupera os recursos de um determinado dispositivo de entrada MIDI e coloca essas informações na [**estrutura MIDIINCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)    |
| [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Recupera os recursos de um determinado dispositivo de saída MIDI e coloca essas informações na [**estrutura MIDIOUTCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) |



 

Cada uma dessas funções tem um parâmetro que especifica o endereço de uma estrutura que a função preenche com informações sobre os recursos de um dispositivo especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços MIDI](midi-services.md)
</dt> </dl>

 

 