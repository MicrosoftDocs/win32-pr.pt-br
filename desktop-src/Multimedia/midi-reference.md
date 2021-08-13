---
title: Referência de MIDI
description: Referência de MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Windows multimídia, MIDI (Interface Digital do Instrument Instrument)
- multimídia, MIDI (Interface Digital do Instrument Instrument)
- audio multimídia, MIDI (Interface Digital do Instrument Instrument)
- audio,MIDI (Instrument Digital Interface)
- Windows multimídia, referência MIDI
- multimídia, referência MIDI
- áudio multimídia, referência MIDI
- audio, referência MIDI
- MIDI (Interface Digital do Instrument Instrument), referência
- MIDI (Interface Digital do Instrument Instrument), referência
- referência para MIDI, sobre
- Referência de MIDI, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da65f193bbdc6b67d317fac7546d4f5d7826d89307d1800c565febf0c7a8b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428346"
---
# <a name="midi-reference"></a>Referência de MIDI

Esta seção descreve as funções, macros, mensagens e estruturas associadas ao MIDI (Instrument Digital Interface Digital) do Instrument Instrument. Esses elementos são agrupados da seguinte forma.

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

## <a name="error-processing"></a>Processamento de erros

-   [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**\_MIM Erro**](mim-error.md)
-   [**\_MIM LONGERROR**](mim-longerror.md)
-   [**ERRO \_ MIM \_ MM**](mm-mim-error.md)
-   [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Gerenciando o MIDI Fluxos

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
-   [**\_MIM Perto**](mim-close.md)
-   [**\_MIM Aberto**](mim-open.md)
-   [**MM \_ MIM \_ CLOSE**](mm-mim-close.md)
-   [**MM \_ MIM \_ OPEN**](mm-mim-open.md)
-   [**MM \_ MOM \_ CLOSE**](mm-mom-close.md)
-   [**MM \_ MOM \_ OPEN**](mm-mom-open.md)
-   [**MOM \_ CLOSE**](mom-close.md)
-   [**MOM \_ OPEN**](mom-open.md)

## <a name="output-devices"></a>Dispositivos de saída

-   [KEYARRAY](keyarray.md)
-   [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [PATCHARRAY](patcharray.md)

## <a name="playing-a-message-or-messages"></a>Como tocar uma mensagem ou mensagens

-   [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**MEVT \_ EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**MM \_ MOM \_ DONE**](mm-mom-done.md)
-   [**MM \_ MOM \_ POSITIONCB**](mm-mom-positioncb.md)
-   [**MOM \_ DONE**](mom-done.md)
-   [**MOM \_ POSITIONCB**](mom-positioncb.md)

## <a name="recording"></a>Gravação

-   [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**midiDisconnect**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**MIDIPROPTEMPO**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**MIDIPROPTIMEDIV**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**\_MIM Dados**](mim-data.md)
-   [**\_MIM LONGDATA**](mim-longdata.md)
-   [**\_MIM Moredata**](mim-moredata.md)
-   [**MM \_ MIM \_ DADOS**](mm-mim-data.md)
-   [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)
-   [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Enviando mensagens para dispositivos

-   [**midiInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**midiOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MIDI (interface digital de instrumento musical)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 