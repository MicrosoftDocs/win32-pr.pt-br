---
title: Waveform-Audio tipos de dados de entrada
description: Waveform-Audio tipos de dados de entrada
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- áudio de onda, tipos de dados de entrada
- Wave-interface de áudio, tipos de dados de entrada
- gravando áudio de onda, tipos de dados de entrada
- Identificador de HWAVEIN
- Estrutura WAVEFORMATEX
- Estrutura WAVEHDR
- Estrutura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007479"
---
# <a name="waveform-audio-input-data-types"></a>Waveform-Audio tipos de dados de entrada

Os tipos de dados a seguir são definidos para funções de entrada de formato wave-áudio.



| Tipo                                 | Descrição                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | Identificador de um dispositivo de entrada de wave-áudio aberto.                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Estrutura que especifica os formatos de dados com suporte por um dispositivo de entrada de wave-áudio específico. Essa estrutura também é usada para dispositivos de saída de wave-áudio. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Estrutura usada como um cabeçalho para um bloco de dados de entrada de forma de onda-áudio. Essa estrutura também é usada para dispositivos de saída de wave-áudio.                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Estrutura usada para consultar os recursos de um dispositivo de entrada de áudio de onda específico.                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 