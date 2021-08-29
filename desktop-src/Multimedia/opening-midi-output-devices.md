---
title: Abrindo dispositivos de saída MIDI
description: Abrindo dispositivos de saída MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Instrument Digital Interface (MIDI), dispositivos de saída
- MIDI (Interface Digital do Instrument Instrument), dispositivos de saída
- reprodução de arquivos MIDI, dispositivos de saída
- Dispositivos de saída MIDI
- MIDI (Instrument Digital Interface Instrument), abrindo dispositivos de saída
- MIDI (Interface Digital do Instrument Instrument), abrindo dispositivos de saída
- reprodução de arquivos MIDI, abertura de dispositivos de saída
- abrindo dispositivos de saída MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0976e265fe253d02bc9662e6ea9b376d5acc4b5fd9f62e56642b56df53ce135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136705"
---
# <a name="opening-midi-output-devices"></a>Abrindo dispositivos de saída MIDI

Para abrir um dispositivo de saída MIDI para reprodução, use a [**função midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto, escrevendo o identificador em um local de memória especificado.

Um dos parâmetros de **midiOutOpen** é um valor doubleword. Esse valor especifica uma janela ou um alça de thread, um handle de evento ou o endereço de uma função de retorno de chamada que é usada para monitorar o progresso da reprodução de dados exclusivos do sistema MIDI e buffers de fluxo. O monitoramento permite que o aplicativo determine quando enviar blocos de dados adicionais e quando liberar blocos de dados que foram enviados. Para obter mais informações sobre esses métodos, consulte [Gerenciando blocos de dados MIDI.](managing-midi-data-blocks.md)

 

 