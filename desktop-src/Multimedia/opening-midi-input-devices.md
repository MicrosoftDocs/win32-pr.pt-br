---
title: Abrindo dispositivos de entrada MIDI
description: Abrindo dispositivos de entrada MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- MIDI (interface digital de instrumento musical), dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), dispositivos de entrada
- gravando áudio MIDI, dispositivos de entrada
- Dispositivos de entrada MIDI
- MIDI (interface digital de instrumento musical), abrindo dispositivos de entrada
- MIDI (interface digital de instrumentos musicais), abrindo dispositivos de entrada
- gravando áudio MIDI, abrindo dispositivos de entrada
- abrindo dispositivos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d260674194e7f066e5095e30a78c94b241a60b32304888aceb8db9ae06ccfea6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806266"
---
# <a name="opening-midi-input-devices"></a>Abrindo dispositivos de entrada MIDI

Para abrir um dispositivo de entrada MIDI para gravação, use a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) . Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto gravando o identificador em um local de memória especificado.

se você usar o \_ sinalizador de STATUS de e/s MIDI \_ com **midiInOpen**, o sistema usará a mensagem [**MIM \_ MOREDATA**](mim-moredata.md) para alertar a função de retorno de chamada do aplicativo quando ele não estiver processando dados MIDI rápido o suficiente para acompanhar o driver de dispositivo de entrada. (a mensagem [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md) faz o mesmo trabalho com retornos de chamada de janela. No entanto, por motivos de desempenho, a maioria dos aplicativos usará funções de retorno de chamada em vez de retornos de chamada de janela. Se seu aplicativo processa dados MIDI em um thread separado, aumentar a prioridade do thread pode ter um impacto significativo na capacidade do aplicativo de acompanhar o fluxo de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 