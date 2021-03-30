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
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640854"
---
# <a name="opening-midi-input-devices"></a>Abrindo dispositivos de entrada MIDI

Para abrir um dispositivo de entrada MIDI para gravação, use a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) . Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto gravando o identificador em um local de memória especificado.

Se você usar o \_ sinalizador de status de e/s MIDI \_ com **midiInOpen**, o sistema usará a mensagem [**\_ MOREDATA do mim**](mim-moredata.md) para alertar a função de retorno de chamada do aplicativo quando não estiver processando dados MIDI rápido o suficiente para acompanhar o driver de dispositivo de entrada. (A mensagem [**mm \_ mim \_ MOREDATA**](mm-mim-moredata.md) faz o mesmo trabalho com retornos de chamada de janela. No entanto, por motivos de desempenho, a maioria dos aplicativos usará funções de retorno de chamada em vez de retornos de chamada de janela. Se seu aplicativo processa dados MIDI em um thread separado, aumentar a prioridade do thread pode ter um impacto significativo na capacidade do aplicativo de acompanhar o fluxo de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 