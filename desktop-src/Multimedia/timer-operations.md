---
title: Operações de evento de timer
description: Operações de evento de timer
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- temporizadores de multimídia, eventos
- temporizadores, eventos
- função timeSetEvent
- função timeKillEvent
- Iniciando eventos de timer
- eventos de temporizador único
- eventos de timer periódicos
- Cancelando eventos de timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640474"
---
# <a name="timer-event-operations"></a>Operações de evento de timer

Depois de estabelecer a resolução do timer do aplicativo, você pode iniciar eventos de timer usando a função [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) . Essa função retorna um identificador de temporizador que pode ser usado para parar ou identificar eventos de timer. Um dos parâmetros da função é o endereço de uma função de retorno de chamada [**timeproc**](/previous-versions//dd757631(v=vs.85)) que é chamada quando o evento do temporizador ocorre.

Há dois tipos de eventos de temporizador: *único* e *periódico*. Um único evento de temporizador ocorre uma vez, após um número especificado de milissegundos. Um evento de timer periódico ocorre sempre que um número especificado de milissegundos é decorrido. O intervalo entre os eventos periódicos é chamado de *atraso de evento*. Eventos de timer periódicos com atraso de evento de 10 milissegundos ou menos consomem uma parte significativa dos recursos da CPU.

A relação entre a resolução de um evento de temporizador e o comprimento do atraso do evento é importante em eventos de temporizador. Por exemplo, se você especificar uma resolução de 5 e um atraso de evento de 100, os serviços de timer notificarão a função de retorno de chamada após um intervalo que varia de 95 a 105 milissegundos.

Você pode cancelar um evento de temporizador ativo a qualquer momento usando a função [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) . Lembre-se de cancelar todos os timers pendentes antes de liberar a memória que contém a função de retorno de chamada.

> [!Note]  
> O temporizador multimídia é executado em seu próprio thread.

 

 

 