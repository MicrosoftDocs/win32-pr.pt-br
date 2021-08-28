---
title: Sobre timers de multimídia
description: Sobre timers de multimídia
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows multimídia, timers
- multimídia, Timers
- entrada de multimídia, temporizadores
- Timers de multimídia, sobre
- Timers, About
- temporizadores de multimídia, eventos de agendamento
- temporizadores, eventos de agendamento
- agendando eventos de timer
- tempo de alta resolução
- Função SetTimer
- Função CreateWaitableTimer
- WM_TIMER mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b5d899c93f0f292d7ef45e8584ae9e2b5e0e001037c456dcc4900f1c0d3f26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498206"
---
# <a name="about-multimedia-timers"></a>Sobre timers de multimídia

Os serviços de timer de multimídia permitem que os aplicativos agendem eventos de timer com a maior resolução (ou precisão) possível para a plataforma de hardware. Esses serviços de timer de multimídia permitem que você agende eventos de timer em uma resolução mais alta do que outros serviços de timer.

Esses serviços de timer são úteis para aplicativos que exigem tempo de alta resolução. Por exemplo, um sequenciador MIDI requer um temporizador de alta resolução porque ele deve manter o ritmo dos eventos MIDI dentro de uma resolução de 1 milissegundo.

Os aplicativos que não usam o tempo de alta resolução devem usar a função [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) em vez de serviços de timer de multimídia. Os serviços de temporizador fornecidos por mensagens de [ \_ temporizador do WM](../winmsg/wm-timer.md) do **webtimer** post para uma fila de mensagens, enquanto os serviços de timer de multimídia chamam uma função de retorno de chamada. Os aplicativos que desejam um temporizador que pode ser aguardado devem usar a função [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) .

 

 