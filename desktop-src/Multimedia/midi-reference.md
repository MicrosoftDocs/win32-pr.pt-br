---
title: Referência de MIDI
description: Referência de MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Multimídia do Windows, MIDI (interface digital de instrumentos musicais)
- multimídia, MIDI (interface digital de instrumentos musicais)
- áudio multimídia, MIDI (interface digital de instrumentos musicais)
- áudio, MIDI (interface digital de instrumento musical)
- Multimídia do Windows, referência de MIDI
- referência de multimídia, MIDI
- áudio de multimídia, referência de MIDI
- áudio, referência de MIDI
- MIDI (interface digital de instrumento musical), referência
- MIDI (interface digital de instrumentos musicais), referência
- referência para MIDI, sobre
- Referência de MIDI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365960"
---
# <a name="midi-reference"></a>Referência de MIDI

Esta seção descreve as funções, macros, mensagens e estruturas associadas à MIDI (interface digital de instrumento musical). Esses elementos são agrupados da seguinte maneira.

## <a name="allocating-and-managing-buffers"></a>Alocando e gerenciando buffers

-   [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a>Funções de retorno de chamada

-   [**MidiInProc**](/previous-versions//dd798460(v=vs.85))
-   [**MidiOutProc**](/previous-versions//dd798478(v=vs.85))

## <a name="device-capabilities"></a>Funcionalidades do dispositivo

-   [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [**midiInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [**midiOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [**MIDISTRMBUFFVER**](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a>Processamento de erro

-   [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**erro do MIM \_**](mim-error.md)
-   [**\_LONGERROR mim**](mim-longerror.md)
-   [**\_erro do mim mm \_**](mm-mim-error.md)
-   [**\_LONGERROR do mim mm \_**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Gerenciando fluxos de MIDI

-   [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a>Abrindo e fechando dispositivos

-   [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [**próximo a MIM \_**](mim-close.md)
-   [**MIM \_ aberto**](mim-open.md)
-   [**Eu \_ fechar do mim \_**](mm-mim-close.md)
-   [**MIM de MM \_ \_ aberto**](mm-mim-open.md)
-   [**\_fechamento do MOM mm \_**](mm-mom-close.md)
-   [**\_Mom mm \_ aberto**](mm-mom-open.md)
-   [**fechamento do MOM \_**](mom-close.md)
-   [**MOM \_ aberto**](mom-open.md)

## <a name="output-devices"></a>Dispositivos de saída

-   [Keyarray](keyarray.md)
-   [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [PATCHARRAY](patcharray.md)

## <a name="playing-a-message-or-messages"></a>Reproduzir uma mensagem ou mensagens

-   [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**\_EVENTTYPE MEVT**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**\_Mom mm \_ concluído**](mm-mom-done.md)
-   [**MM \_ Mom \_ POSITIONCB**](mm-mom-positioncb.md)
-   [**MOM \_ concluído**](mom-done.md)
-   [**POSITIONCB do MOM \_**](mom-positioncb.md)

## <a name="recording"></a>Gravação

-   [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**midiDisconnect**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**MIDIPROPTEMPO**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**MIDIPROPTIMEDIV**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**dados do MIM \_**](mim-data.md)
-   [**\_LONGDATA mim**](mim-longdata.md)
-   [**\_MOREDATA mim**](mim-moredata.md)
-   [**\_dados do mim mm \_**](mm-mim-data.md)
-   [**\_MOREDATA do mim mm \_**](mm-mim-moredata.md)
-   [**\_LONGDATA do mim mm \_**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Enviando mensagens para dispositivos

-   [**midiInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**midiOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MIDI (interface digital de instrumento musical)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 