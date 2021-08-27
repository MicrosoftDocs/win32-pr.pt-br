---
description: Este tópico discute os temporizadores. Um temporizador é uma rotina interna que mede repetidamente um intervalo especificado, em milissegundos.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd8eced20e7d8b1eca5ec8a952f10798f92f1650db3c77bca76aca756cdd569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110686"
---
# <a name="timers"></a>Temporizadores

Um temporizador é uma rotina interna que mede repetidamente um intervalo especificado, em milissegundos.

### <a name="in-this-section"></a>Nesta seção



| Nome                                   | Descrição                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Sobre temporizadores](about-timers.md)       | Descreve como criar, identificar, definir e excluir temporizadores.<br/>                                                     |
| [Usando temporizadores](using-timers.md)       | Discute como criar e destruir temporizadores e como usar um temporizador para interceptar a entrada do mouse em intervalos especificados.<br/> |
| [Referência do temporizador](timer-reference.md) | Contém a referência de API.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Funções de temporizador



| Nome                           | Descrição                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | Destrói o temporizador especificado. <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | Cria um temporizador com o valor de tempo limite especificado.<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Uma função de retorno de chamada definida pelo aplicativo que processa mensagens de [**\_ temporizador do WM**](wm-timer.md) . O tipo **TIMERPROC** define um ponteiro para essa função de retorno de chamada. [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) é um espaço reservado para o nome da função definida pelo aplicativo. <br/> |



 

### <a name="timer-notifications"></a>Notificações de timer



| Nome                          | Descrição                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_temporizador do WM**](wm-timer.md) | Postado na fila de mensagens do thread de instalação quando um temporizador expira. A mensagem é postada pela função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . <br/> |



 

 

 
