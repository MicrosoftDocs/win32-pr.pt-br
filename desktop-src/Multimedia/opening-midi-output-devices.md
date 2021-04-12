---
title: Abrindo dispositivos de saída MIDI
description: Abrindo dispositivos de saída MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- MIDI (interface digital de instrumento musical), dispositivos de saída
- MIDI (interface digital de instrumentos musicais), dispositivos de saída
- executando arquivos MIDI, dispositivos de saída
- Dispositivos de saída MIDI
- MIDI (interface digital de instrumento musical), abrindo dispositivos de saída
- MIDI (interface digital de instrumentos musicais), abrindo dispositivos de saída
- executando arquivos MIDI, abrindo dispositivos de saída
- abrindo dispositivos de saída MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454026"
---
# <a name="opening-midi-output-devices"></a>Abrindo dispositivos de saída MIDI

Para abrir um dispositivo de saída de MIDI para reprodução, use a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . Essa função abre o dispositivo associado ao identificador de dispositivo especificado e retorna um identificador do dispositivo aberto gravando o identificador em um local de memória especificado.

Um dos parâmetros de **midiOutOpen** é um valor de doubleword. Esse valor especifica um identificador de janela ou thread, um identificador de evento ou o endereço de uma função de retorno de chamada que é usado para monitorar o progresso da reprodução de dados exclusivos do sistema MIDI e buffers de fluxo. O monitoramento permite que o aplicativo determine quando enviar blocos de dados adicionais e quando liberar os blocos de dados que foram enviados. Para obter mais informações sobre esses métodos, consulte [Managing MIDI data Blocks](managing-midi-data-blocks.md).

 

 