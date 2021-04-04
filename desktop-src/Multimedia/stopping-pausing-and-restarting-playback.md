---
title: Parando, pausando e reiniciando a reprodução
description: Parando, pausando e reiniciando a reprodução
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- áudio de onda, parando a reprodução
- Wave-interface de áudio, parando a reprodução
- executando a onda-arquivos de áudio, parando a reprodução
- áudio de onda, pausando reprodução
- Wave-interface de áudio, pausando reprodução
- executando a onda-arquivos de áudio, pausando a reprodução
- áudio de onda, reiniciando a reprodução
- Wave-interface de áudio, reiniciando a reprodução
- executando a onda-arquivos de áudio, reiniciando a reprodução
- função waveOutPause
- função waveOutReset
- função waveOutRestart
- parando a onda-reprodução de áudio
- Pausando a onda-reprodução de áudio
- Reiniciando a onda-reprodução de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084469"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Parando, pausando e reiniciando a reprodução

Você pode parar ou pausar a reprodução enquanto o áudio da onda está sendo tocado. Depois que a reprodução tiver sido pausada, você poderá reiniciá-la. O Windows fornece as seguintes funções para controlar a reprodução de formato wave-áudio.



| Função                                 | Descrição                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Pausa a reprodução em um dispositivo de saída de wave-áudio.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Interrompe a reprodução em um dispositivo de saída de wave-áudio e marca todos os blocos de dados pendentes como concluído. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Retoma a reprodução em um dispositivo de saída de wave-áudio em pausa.                                  |



 

Pausar uma wave-dispositivo de áudio usando [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) pode não ser instantâneo; o driver pode terminar de reproduzir o bloco atual antes de pausar a reprodução.

Em geral, assim que o primeiro bloco de dados de wave-áudio é enviado usando a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , o dispositivo de forma de onda-áudio começa a ser reproduzido. Se você não quiser que o som comece a ser reproduzido imediatamente, chame **waveOutPause** antes de chamar **waveOutWrite**. Em seguida, quando você quiser começar a reproduzir dados de formato de onda-áudio, chame [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

Não é possível usar **waveOutRestart** para reiniciar um dispositivo que foi interrompido com [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); Você deve usar **waveOutWrite** para enviar o primeiro bloco de dados para retomar a reprodução no dispositivo.

 

 