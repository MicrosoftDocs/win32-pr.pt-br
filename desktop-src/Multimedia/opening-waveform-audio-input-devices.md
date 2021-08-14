---
title: Abrindo Waveform-Audio de entrada
description: Abrindo Waveform-Audio de entrada
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- waveform audio, abrindo dispositivos de entrada
- interface waveform-audio, abrindo dispositivos de entrada
- gravação de áudio de forma de onda, abrindo dispositivos de entrada
- abrindo dispositivos de entrada waveform-audio
- Função waveInOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6391ca5bfe0690d2235504057865fb588f08d0359417ccbcc04b6a7e5eb082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802303"
---
# <a name="opening-waveform-audio-input-devices"></a>Abrindo Waveform-Audio de entrada

Use a [**função waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir um dispositivo de entrada waveform-audio para gravação. Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto escrevendo o identificador de um local de memória especificado.

Alguns computadores multimídia têm vários dispositivos de entrada waveform-audio. A menos que você saiba que deseja abrir um dispositivo de entrada de áudio de forma de onda específico em um sistema, você deve usar a constante WAVE MAPPER para o identificador de dispositivo ao \_ abrir um dispositivo. A [**função waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) escolherá o dispositivo no sistema mais bem capaz de registrar no formato de dados especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravação de áudio waveform](recording-waveform-audio.md)
</dt> </dl>

 

 