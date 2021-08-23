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
ms.openlocfilehash: b04491a676a104e288d274da7dd70eb759e363adc6476805b261a9651444bf1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688486"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Parando, pausando e reiniciando a reprodução

Você pode parar ou pausar a reprodução enquanto o áudio da onda está sendo tocado. Depois que a reprodução tiver sido pausada, você poderá reiniciá-la. Windows fornece as seguintes funções para controlar a reprodução de formato wave-áudio.



| Função                                 | Descrição                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Pausa a reprodução em um dispositivo de saída de wave-áudio.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Interrompe a reprodução em um dispositivo de saída de wave-áudio e marca todos os blocos de dados pendentes como concluído. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Retoma a reprodução em um dispositivo de saída de wave-áudio em pausa.                                  |



 

Pausar uma wave-dispositivo de áudio usando [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) pode não ser instantâneo; o driver pode terminar de reproduzir o bloco atual antes de pausar a reprodução.

Em geral, assim que o primeiro bloco de dados de wave-áudio é enviado usando a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , o dispositivo de forma de onda-áudio começa a ser reproduzido. Se você não quiser que o som comece a ser reproduzido imediatamente, chame **waveOutPause** antes de chamar **waveOutWrite**. Em seguida, quando você quiser começar a reproduzir dados de formato de onda-áudio, chame [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).

Não é possível usar **waveOutRestart** para reiniciar um dispositivo que foi interrompido com [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); Você deve usar **waveOutWrite** para enviar o primeiro bloco de dados para retomar a reprodução no dispositivo.

 

 