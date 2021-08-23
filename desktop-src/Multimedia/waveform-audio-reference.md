---
title: Referência de áudio de onda
description: Esta seção lista as funções, as estruturas e as mensagens associadas ao áudio de onda, que estão documentados em referência de multimídia. Esses elementos são agrupados da seguinte maneira.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows multimídia, referência de áudio de onda
- referência de áudio de multimídia, formato de onda
- áudio de multimídia, referência de Wave
- referência de áudio, de onda
- Windows multimídia, áudio de onda
- multimídia, áudio de onda
- áudio de multimídia, onda
- áudio, onda
- áudio de onda, referência
- referência de áudio de onda, sobre
- referência para áudio wavefore, sobre
- referência de áudio de onda, dispositivos auxiliares
- referência para áudio wavefore, dispositivos auxiliares
- referência de áudio de onda, reprodução
- referência para áudio wavefore, reprodução
- referência de áudio de onda, erros
- referência para áudio wavefore, erros
- referência de áudio de onda, abrindo
- referência para áudio wavefore, abrindo
- referência de áudio de onda, fechamento
- referência para áudio wavefore, fechamento
- referência de áudio de onda, pitch
- referência para áudio wavefore, pitch
- referência de áudio de onda, volume
- referência para áudio wavefore, volume
- referência de áudio de onda, mensagens
- referência para áudio wavefore, mensagens
- referência de áudio de onda, posição atual
- referência para áudio wavefore, posição atual
- referência de áudio de onda, gravação
- referência para áudio wavefore, gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd83f843de130d247749acfc87a67c60948871bb8cd878f9aa180fcd385fb13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687416"
---
# <a name="waveform-audio-reference"></a>Referência de áudio de onda

Esta seção lista as funções, as estruturas e as mensagens associadas ao áudio de onda, que estão documentados em [referência de multimídia](multimedia-reference.md). Esses elementos são agrupados da seguinte maneira.

## <a name="auxiliary-devices"></a>Dispositivos auxiliares

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Reprodução fácil

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Erros

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Abrindo e fechando

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**MM \_ de \_ fechamento de Wim**](mm-wim-close.md)
-   [**Wim de MM \_ \_ aberto**](mm-wim-open.md)
-   [**MM \_ wom \_ fechar**](mm-wom-close.md)
-   [**MM \_ wom \_ abertos**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**\_fechar wim**](wim-close.md)
-   [**WIM \_ aberto**](wim-open.md)
-   [**WOM \_ fechar**](wom-close.md)
-   [**WOM \_ abrir**](wom-open.md)

## <a name="pitch"></a>Densidade

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Taxa de reprodução

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Progresso da reprodução

-   [**MM \_ wom \_ concluído**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ concluído**](wom-done.md)

## <a name="playing"></a>Reproduzindo

-   [**MM \_ wom \_ concluído**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ concluído**](wom-done.md)

## <a name="querying-a-device"></a>Consultando um dispositivo

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Gravação

-   [**\_dados wim \_ mm**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**DADOS \_ DO WIM**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Recuperando identificadores de dispositivo

-   [**waveInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Recuperando a posição atual

-   [**waveInGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Enviando mensagens personalizadas

-   [**waveInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Volume

-   [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Waveform Audio](waveform-audio.md)
</dt> </dl>

 

 