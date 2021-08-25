---
title: Alocando e preparando blocos de dados MIDI
description: Alocando e preparando blocos de dados MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- MIDI (Instrument Digital Interface), alocando blocos de dados
- MIDI (Interface Digital do Instrument Instrument), alocando blocos de dados
- Serviços MIDI, alocando blocos de dados
- alocando blocos de dados MIDI
- MIDI (Instrument Digital Interface Instrument), preparando blocos de dados
- MIDI (Interface Digital do Instrument Instrument), preparando blocos de dados
- Serviços MIDI, preparando blocos de dados
- preparando blocos de dados MIDI
- Instrument Digital Interface (MIDI), blocos de dados
- MIDI (Interface Digital Instrument Instrument), blocos de dados
- Serviços MIDI, blocos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137556c1344e6f2e8db8557d45a70c5981fa7bab99e7452cc1f756b4a8ee159b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808486"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Alocando e preparando blocos de dados MIDI

As funções [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)e [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) exigem que os aplicativos alocem blocos de dados para passar para os drivers de dispositivo para fins de reprodução ou gravação. Cada uma dessas funções usa uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) para descrever seu bloco de dados.

Antes de usar uma dessas funções para passar um bloco de dados para um driver de dispositivo, você deve alocar memória para o buffer e a estrutura de header que descreve o bloco de dados.

Windows fornece as seguintes funções para preparar e limpar blocos de dados MIDI.



| Valor                                                    | Significado                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prepara um bloco de dados de entrada MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Limpa a preparação de um bloco de dados de entrada MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prepara um bloco de dados de saída MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Limpa a preparação de um bloco de dados de saída MIDI. |



 

Antes de passar um bloco de dados MIDI para um driver de dispositivo, você deve preparar o buffer passando-o para a função [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) ou [**midiOutPrepareHeader.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) Quando o driver de dispositivo for concluído com o buffer e o retornar, você deverá limpar essa preparação passando o buffer para a função [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) ou [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) antes que qualquer memória alocada possa ser liberada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços MIDI](midi-services.md)
</dt> </dl>

 

 