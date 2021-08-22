---
title: Recuperando a posição de reprodução atual
description: Recuperando a posição de reprodução atual
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- waveform audio, posição de reprodução atual
- interface waveform-audio, posição de reprodução atual
- reproduzindo arquivos waveform-audio, posição de reprodução atual
- Função waveOutGetPosition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85bc46e476786625ccae51802e0b720379a935110eb37d941c4c76d69d94783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689046"
---
# <a name="retrieving-the-current-playback-position"></a>Recuperando a posição de reprodução atual

Você pode monitorar a posição de reprodução atual dentro do arquivo enquanto o áudio waveform está sendo reproduzida usando a [**função waveOutGetPosition.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

Para dispositivos waveform-audio, os exemplos são o formato de tempo preferencial no qual representar a posição atual. Portanto, a posição atual de um dispositivo waveform-audio é especificada como o número de amostras de um canal desde o início do arquivo waveform-audio. Para consultar a posição atual de um dispositivo waveform-audio, de definido o membro **wType** da estrutura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) como TIME SAMPLES e passe essa estrutura para \_ **waveOutGetPosition**.

A estrutura **MMTIME** pode representar o tempo em um ou mais formatos diferentes, incluindo milissegundos, exemplos, SMPTE (Society of Motion Picture e Engenheiros de Tv) e formatos de ponteiro de música MIDI. O **membro wType** especifica o formato usado para representar a hora. Antes de chamar uma função que usa a **estrutura MMTIME,** você deve definir **wType** para indicar o formato de hora solicitado. Verifique **wType** após a chamada para ver se há suporte para o formato de tempo solicitado. Se não há suporte para o formato de hora solicitado, o driver de dispositivo especifica a hora em um formato de hora alternativo e altera o membro **wType** para o formato de hora selecionado.

Para obter mais informações sobre a **estrutura MMTIME,** consulte [Temporizadores multimídia](multimedia-timers.md).

 

 