---
title: Operações de evento de temporizador
description: Operações de evento de temporizador
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- temporizadores de multimídia, eventos
- temporizadores, eventos
- Função timeSetEvent
- Função timeKillEvent
- iniciando eventos de temporizador
- eventos de temporizador único
- eventos de temporizador periódicos
- cancelando eventos de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3869015cdde4afe5bd77bb65d39d5ee43aeb4eab65b1f54e7bfd3dadca1a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370816"
---
# <a name="timer-event-operations"></a>Operações de evento de temporizador

Depois de estabelecer a resolução de temporizador do aplicativo, você pode iniciar eventos de temporizador usando a [**função timeSetEvent.**](/previous-versions//dd757634(v=vs.85)) Essa função retorna um identificador de temporizador que pode ser usado para parar ou identificar eventos de temporizador. Um dos parâmetros da função é o endereço de uma função de retorno de chamada [**TimeProc**](/previous-versions//dd757631(v=vs.85)) que é chamada quando o evento de temporizador ocorre.

Há dois tipos de eventos de temporizador: *único* e *periódico.* Um único evento de temporizador ocorre uma vez, após um número especificado de milissegundos. Um evento de temporizador periódico ocorre sempre que um número especificado de milissegundos ocorre. O intervalo entre eventos periódicos é chamado de *atraso de evento*. Eventos periódicos de temporizador com um atraso de evento de 10 milissegundos ou menos consomem uma parte significativa dos recursos da CPU.

A relação entre a resolução de um evento de temporizador e o comprimento do atraso do evento é importante em eventos de temporizador. Por exemplo, se você especificar uma resolução de 5 e um atraso de evento de 100, os serviços de temporizador notificarão a função de retorno de chamada após um intervalo que varia de 95 a 105 milissegundos.

Você pode cancelar um evento de temporizador ativo a qualquer momento usando a [**função timeKillEvent.**](/previous-versions//dd757630(v=vs.85)) Cancele todos os temporizadores pendentes antes de liberar a memória que contém a função de retorno de chamada.

> [!Note]  
> O temporizador de multimídia é executado em seu próprio thread.

 

 

 