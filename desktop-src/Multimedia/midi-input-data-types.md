---
title: Tipos de dados de entrada de MIDI
description: Tipos de dados de entrada de MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- MIDI (interface digital de instrumento musical), tipos de dados de entrada
- MIDI (interface digital de instrumentos musicais), tipos de dados de entrada
- gravando áudio MIDI, tipos de dados de entrada
- Tipos de dados de entrada de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105757367"
---
# <a name="midi-input-data-types"></a>Tipos de dados de entrada de MIDI

O Windows define os seguintes tipos de dados para as funções de entrada de MIDI.



| Valor                            | Significado                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | Identificador de um dispositivo de entrada MIDI.                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | Cabeçalho de um buffer de fluxo ou de um bloco de dados exclusivos do sistema MIDI. Para aplicativos de entrada, essa estrutura registra somente dados exclusivos do sistema (não há suporte para streaming para entrada MIDI). |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Estrutura usada para consultar os recursos de um dispositivo de entrada MIDI.                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 