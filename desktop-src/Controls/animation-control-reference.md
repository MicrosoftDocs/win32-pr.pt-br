---
title: Controle de animação
description: Esta seção contém informações sobre os elementos de programação usados com controles de animação.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454389"
---
# <a name="animation-control"></a>Controle de animação

Esta seção contém informações sobre os elementos de programação usados com controles de animação.

### <a name="overviews"></a>Visões gerais



| Tópico                                                      | Sumário                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre os controles de animação](animation-control-overview.md) | Um *controle de animação* é uma janela que exibe um clipe AVI (intercalado Audio-Video). Um clipe AVI é uma série de quadros de bitmap como um filme. Os controles de animação só podem exibir clipes AVI que não contenham áudio.<br/> |
| [Usando controles de animação](using-animation-control.md)    | Esta seção fornece detalhes de implementação e código de exemplo para controles de animação.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Macros



| Tópico                                           | Sumário                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Fechar animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Fecha um clipe AVI. Você pode usar essa macro ou enviar a [**mensagem \_ aberta do ACM**](acm-open.md) explicitamente, passando parâmetros **nulos** . <br/>                                                                                                              |
| [**\_Criar animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Cria um controle de animação. [**Animar \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) chama a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para criar o controle de animação. <br/>                                                                                   |
| [**Animar \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Verifica se um clipe AVI está sendo reproduzido. Você pode usar esta macro ou enviar uma mensagem de [**\_ IsPlaying do ACM**](acm-isplaying.md) .<br/>                                                                                                                            |
| [**Animação \_ aberta**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação. Você pode usar esta macro ou enviar a [**mensagem \_ aberta do ACM**](acm-open.md) explicitamente. <br/>                                                                                          |
| [**Animar \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Abre um clipe AVI de um recurso em um módulo especificado e exibe seu primeiro quadro em um controle de animação. Você pode usar esta macro ou enviar a [**mensagem \_ aberta do ACM**](acm-open.md) explicitamente. <br/>                                                    |
| [**Ação de animação \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Reproduz um clipe AVI em um controle de animação. O controle reproduz o clipe em segundo plano enquanto o thread continua em execução. Você pode usar esta macro ou enviar a mensagem de [**\_ reprodução do ACM**](acm-play.md) explicitamente. <br/>                                    |
| [**Animar \_ busca**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Direciona um controle de animação para exibir um quadro específico de um clipe AVI. O controle exibe o clipe em segundo plano enquanto o thread continua em execução. Você pode usar esta macro ou enviar a mensagem de [**\_ reprodução do ACM**](acm-play.md) explicitamente. <br/> |
| [**Parada de animação \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Interrompe a reprodução de um clipe AVI em um controle de animação. Você pode usar essa macro ou enviar a mensagem de [**\_ parada do ACM**](acm-stop.md) explicitamente. <br/>                                                                                                               |



 

### <a name="messages"></a>Mensagens



| Tópico                                   | Sumário                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsPlaying do ACM \_**](acm-isplaying.md) | Verifica se um clipe AVI está sendo reproduzido. Você pode enviar essa mensagem explicitamente ou usar a macro de [**\_ IsPlaying de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .<br/>                                                                                   |
| [**aberto no ACM \_**](acm-open.md)           | Abre um clipe AVI e exibe seu primeiro quadro em um controle de animação. Você pode enviar essa mensagem explicitamente ou usar a macro [**animado \_ abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ou [**animar \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . <br/>              |
| [**\_Play ACM**](acm-play.md)           | Reproduz um clipe AVI em um controle de animação. O controle reproduz o clipe em segundo plano enquanto o thread continua em execução. Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ reprodução de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .<br/> |
| [**parada do ACM \_**](acm-stop.md)           | Interrompe a reprodução de um clipe AVI em um controle de animação. Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ parada de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .<br/>                                                                            |



 

### <a name="notifications"></a>Notificações



| Tópico                           | Sumário                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACN \_ Iniciar**](acn-start.md) | Notifica uma janela pai do controle de animação que o clipe AVI associado começou a ser reproduzido. Esse código de notificação é enviado na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . <br/>      |
| [**ACN \_ parar**](acn-stop.md)   | Notifica a janela pai de um controle de animação que o clipe AVI associado parou de ser reproduzido. Esse código de notificação é enviado na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . <br/> |



 

### <a name="constants"></a>Constantes



| Tópico                                                        | Sumário                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Estilos de controle de animação**](animation-control-styles.md) | Esta seção lista os estilos de janela usados com controles de animação.<br/> |



 

 

