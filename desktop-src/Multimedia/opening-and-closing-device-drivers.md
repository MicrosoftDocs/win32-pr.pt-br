---
title: Abrindo e fechando drivers de dispositivo
description: Abrindo e fechando drivers de dispositivo
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- MIDI (interface digital de instrumento musical), abertura de dispositivos
- MIDI (interface digital de instrumentos musicais), abrindo dispositivos
- Serviços de MIDI, abrindo dispositivos
- abrindo dispositivos MIDI
- MIDI (interface digital de instrumento musical), dispositivos de fechamento
- MIDI (interface digital de instrumentos musicais), fechando dispositivos
- Serviços de MIDI, fechando dispositivos
- fechando dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640544"
---
# <a name="opening-and-closing-device-drivers"></a>Abrindo e fechando drivers de dispositivo

Você deve abrir um dispositivo MIDI antes de usá-lo e fechar o dispositivo assim que terminar de usá-lo. O Windows fornece as seguintes funções para abrir e fechar diferentes tipos de dispositivos MIDI.



| Valor                                | Significado                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Fecha um dispositivo de entrada MIDI especificado.              |
| [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Abre um dispositivo de entrada MIDI especificado para gravação. |
| [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Fecha um dispositivo de saída MIDI especificado.             |
| [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Abre um dispositivo de saída de MIDI para reprodução.           |



 

Cada função que abre um dispositivo MIDI usa como parâmetros um identificador de dispositivo, um endereço de um local de memória e alguns parâmetros exclusivos de dispositivos MIDI. O local da memória é preenchido com um identificador de dispositivo, que é usado para identificar o dispositivo de áudio aberto em chamadas a outras funções de áudio.

Muitas funções MIDI podem aceitar um identificador de dispositivo ou um dispositivo. Embora seja possível usar um identificador de dispositivo onde quer que você use uma identificação de dispositivo, nem sempre é possível usar um identificador de dispositivo quando um identificador é chamado para.

> [!Note]  
> Os dispositivos MIDI não são necessariamente compartilháveis, portanto, um dispositivo específico pode não estar disponível quando um usuário solicitá-lo. Se isso acontecer, o aplicativo deve notificar o usuário e permitir que o usuário tente abrir o dispositivo novamente.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços MIDI](midi-services.md)
</dt> </dl>

 

 