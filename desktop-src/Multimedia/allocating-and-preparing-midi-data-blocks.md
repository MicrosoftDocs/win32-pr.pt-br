---
title: Alocando e preparando blocos de dados MIDI
description: Alocando e preparando blocos de dados MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- MIDI (interface digital de instrumento musical), alocando blocos de dados
- MIDI (interface digital de instrumentos musicais), alocando blocos de dados
- Serviços de MIDI, alocando blocos de dados
- alocando blocos de dados MIDI
- MIDI (interface digital de instrumento musical), preparando blocos de dados
- MIDI (interface digital de instrumentos musicais), preparando blocos de dados
- Serviços de MIDI, preparando blocos de dados
- preparando blocos de dados MIDI
- MIDI (interface digital de instrumento musical), blocos de dados
- MIDI (interface digital de instrumentos musicais), blocos de dados
- Serviços de MIDI, blocos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105757774"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Alocando e preparando blocos de dados MIDI

As funções [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)e [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) exigem que os aplicativos aloquem blocos de dados para passar para os drivers de dispositivo para fins de reprodução ou gravação. Cada uma dessas funções usa uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) para descrever seu bloco de dados.

Antes de usar uma dessas funções para passar um bloco de dados para um driver de dispositivo, você deve alocar memória para o buffer e a estrutura de cabeçalho que descreve o bloco de dados.

O Windows fornece as seguintes funções para preparar e limpar os blocos de dados MIDI.



| Valor                                                    | Significado                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prepara um bloco de dados de entrada MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Limpa a preparação de um bloco de dados de entrada MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prepara um bloco de dados de saída MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Limpa a preparação de um bloco de dados de saída de MIDI. |



 

Antes de passar um bloco de dados MIDI para um driver de dispositivo, você deve preparar o buffer passando-o para a função [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) ou [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) . Quando o driver de dispositivo for concluído com o buffer e o retornar, você deverá limpar essa preparação passando o buffer para a função [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) ou [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) antes que qualquer memória alocada possa ser liberada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços MIDI](midi-services.md)
</dt> </dl>

 

 