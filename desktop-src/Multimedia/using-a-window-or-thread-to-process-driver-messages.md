---
title: Usando uma janela ou thread para processar mensagens do driver
description: Usando uma janela ou thread para processar mensagens do driver
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- áudio de onda, retorno de chamada de janela
- blocos de dados de áudio, retorno de chamada de janela
- áudio de onda, retorno de chamada de thread
- blocos de dados de áudio, retorno de chamada de thread
- áudio de onda, mensagens de driver de processamento
- blocos de dados de áudio, processando mensagens de driver
- Processando mensagens do driver
- função waveInOpen
- função waveOutOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917298"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a>Usando uma janela ou thread para processar mensagens do driver

Para usar uma função de retorno de chamada de janela, especifique o sinalizador de janela de retorno de chamada \_ no parâmetro *fdwOpen* e um identificador de janela na palavra de ordem inferior do parâmetro *dwCallback* da função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) . As mensagens de driver serão enviadas para o procedimento de janela para a janela identificada pelo identificador em *dwCallback*.

Da mesma forma, para usar um retorno de chamada de thread, especifique o thread de retorno de chamada \_ e um identificador de thread na chamada para **WaveInOpen** ou **waveOutOpen**. Nesse caso, as mensagens são postadas no thread especificado em vez de em uma janela.

As mensagens enviadas para a janela ou retorno de chamada de thread são específicas para o tipo de dispositivo de áudio usado. Para obter mais informações sobre essas mensagens, consulte [reproduzindo arquivos de Waveform-Audio](playing-waveform-audio-files.md).

 

 