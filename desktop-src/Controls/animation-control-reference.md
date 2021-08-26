---
title: Controle de animação
description: Esta seção contém informações sobre os elementos de programação usados com controles de animação.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7241199dc92004f9b3616e2666dd96eadbf43fc6c4dfe9081369e13cca26e082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921776"
---
# <a name="animation-control"></a>Controle de animação

Esta seção contém informações sobre os elementos de programação usados com controles de animação.

### <a name="overviews"></a>Visões gerais



| Tópico                                                      | Sumário                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre controles de animação](animation-control-overview.md) | Um *controle de* animação é uma janela que exibe Audio-Video clipe INTERcalado (AVI). Um clipe AVI é uma série de quadros de bitmap como um filme. Os controles de animação só podem exibir clipes AVI que não contêm áudio.<br/> |
| [Usando controles de animação](using-animation-control.md)    | Esta seção fornece detalhes de implementação e código de exemplo para controles de animação.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Macros



| Tópico                                           | Sumário                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Animar \_ Fechar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Fecha um clipe AVI. Você pode usar essa macro ou enviar a mensagem [**\_ OPEN do ACM**](acm-open.md) explicitamente, passando parâmetros **NULL.** <br/>                                                                                                              |
| [**Animar \_ Criar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Cria um controle de animação. [**Animar \_ Criar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) chama a [**função CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para criar o controle de animação. <br/>                                                                                   |
| [**Animar \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Verifica se um clipe AVI está sendo gravado. Você pode usar essa macro ou enviar uma mensagem [**\_ ISPLAYING do ACM.**](acm-isplaying.md)<br/>                                                                                                                            |
| [**Animar \_ Aberto**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação. Você pode usar essa macro ou enviar a [**mensagem \_ OPEN do ACM**](acm-open.md) explicitamente. <br/>                                                                                          |
| [**Animar \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Abre um clipe AVI de um recurso em um módulo especificado e exibe seu primeiro quadro em um controle de animação. Você pode usar essa macro ou enviar a [**mensagem \_ OPEN do ACM**](acm-open.md) explicitamente. <br/>                                                    |
| [**Animar \_ a reprodução**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Reproduz um clipe AVI em um controle de animação. O controle reproduz o clipe em segundo plano enquanto o thread continua em execução. Você pode usar essa macro ou enviar a mensagem PLAY do [**ACM \_**](acm-play.md) explicitamente. <br/>                                    |
| [**Animar \_ a busca**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Direciona um controle de animação para exibir um quadro específico de um clipe AVI. O controle exibe o clipe em segundo plano enquanto o thread continua em execução. Você pode usar essa macro ou enviar a mensagem PLAY do [**ACM \_**](acm-play.md) explicitamente. <br/> |
| [**Animar \_ Parar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Interrompe a reprodução de um clipe AVI em um controle de animação. Você pode usar essa macro ou enviar a [**mensagem \_ STOP do ACM**](acm-stop.md) explicitamente. <br/>                                                                                                               |



 

### <a name="messages"></a>Mensagens



| Tópico                                   | Sumário                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACM \_ ISPLAYING**](acm-isplaying.md) | Verifica se um clipe AVI está sendo gravado. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ Animate IsPlaying.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying)<br/>                                                                                   |
| [**ACM \_ OPEN**](acm-open.md)           | Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação. Você pode enviar essa mensagem explicitamente ou usar a [**macro Animar \_ Abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ou [**Animar \_ OpenEx.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) <br/>              |
| [**ACM \_ PLAY**](acm-play.md)           | Reproduz um clipe AVI em um controle de animação. O controle reproduz o clipe em segundo plano enquanto o thread continua em execução. Você pode enviar essa mensagem explicitamente ou usando a [**macro Animar \_ Reproduzir.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)<br/> |
| [**PARADA \_ DO ACM**](acm-stop.md)           | Interrompe a reprodução de um clipe AVI em um controle de animação. Você pode enviar essa mensagem explicitamente ou usando a [**macro Animar \_ Parar.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)<br/>                                                                            |



 

### <a name="notifications"></a>Notificações



| Tópico                           | Sumário                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INÍCIO \_ DO ACN**](acn-start.md) | Notifica a janela pai de um controle de animação de que o clipe AVI associado começou a ser a reprodução. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) <br/>      |
| [**ACN \_ STOP**](acn-stop.md)   | Notifica a janela pai de um controle de animação de que o clipe AVI associado parou de ser gravado. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) <br/> |



 

### <a name="constants"></a>Constantes



| Tópico                                                        | Sumário                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Estilos de controle de animação**](animation-control-styles.md) | Esta seção lista os estilos de janela usados com controles de animação.<br/> |



 

 

