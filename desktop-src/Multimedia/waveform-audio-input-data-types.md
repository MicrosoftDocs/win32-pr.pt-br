---
title: Waveform-Audio de dados de entrada
description: Waveform-Audio de dados de entrada
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- áudio waveform, tipos de dados de entrada
- interface waveform-audio, tipos de dados de entrada
- gravação de áudio de forma de onda, tipos de dados de entrada
- Alça HWAVEIN
- Estrutura WAVEFORMATEX
- Estrutura WAVEHDR
- Estrutura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e131e55c404fe658a0c8f60a8f816ff231f9eb9492bcf8641a4e38781bfa78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892086"
---
# <a name="waveform-audio-input-data-types"></a>Waveform-Audio de dados de entrada

Os tipos de dados a seguir são definidos para funções de entrada waveform-audio.



| Tipo                                 | Descrição                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | Alça de um dispositivo de entrada de áudio de forma de onda aberta.                                                                                                                  |
| [**Waveformatex**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Estrutura que especifica os formatos de dados com suporte por um dispositivo de entrada waveform-audio específico. Essa estrutura também é usada para dispositivos de saída waveform-audio. |
| [**Wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Estrutura usada como um header para um bloco de dados de entrada waveform-audio. Essa estrutura também é usada para dispositivos de saída waveform-audio.                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Estrutura usada para perguntar sobre os recursos de um dispositivo de entrada de áudio de forma de onda específico.                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravação de áudio waveform](recording-waveform-audio.md)
</dt> </dl>

 

 