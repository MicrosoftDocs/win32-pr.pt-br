---
title: Dica de ferramenta
description: Esta seção contém informações sobre os elementos de programação usados com controles de dica de ferramenta.
ms.assetid: vs|controls|~\controls\tooltip\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228f7a0b40e934342081d73a24a612c9631e39bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159778"
---
# <a name="tooltip"></a>Dica de ferramenta

Esta seção contém informações sobre os elementos de programação usados com controles de dica de ferramenta.

### <a name="overviews"></a>Visões gerais



| Tópico                                              | Sumário                                                                                                                          |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Sobre os controles de dica de ferramenta](tooltip-controls.md)     | As dicas de ferramentas são exibidas automaticamente ou aparecem quando o usuário pausa o ponteiro do mouse sobre uma ferramenta ou algum outro elemento da interface do usuário.<br/> |
| [Usando controles de dica de ferramenta](using-tooltip-contro.md) | Esta seção contém exemplos que demonstram como criar diferentes tipos de dicas de ferramenta.<br/>                             |



 

### <a name="messages"></a>Mensagens



| Tópico                                               | Sumário                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TTM \_ Ativar**](ttm-activate.md)               | Ativa ou desativa um controle ToolTip. <br/>                                                                                                                                                           |
| [**addferramenta TTM \_**](ttm-addtool.md)                 | Registra uma ferramenta com um controle ToolTip. <br/>                                                                                                                                                              |
| [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)           | Calcula o retângulo de exibição de texto de um controle de dica de ferramenta de seu retângulo de janela ou o retângulo da janela de dica de ferramenta necessário para exibir um retângulo de exibição de texto especificado. <br/>                                |
| [**TTM \_ DELTOOL**](ttm-deltool.md)                 | Remove uma ferramenta de um controle ToolTip. <br/>                                                                                                                                                                |
| [**TTM \_ ENUMTOOLS**](ttm-enumtools.md)             | Recupera as informações que um controle ToolTip mantém sobre a ferramenta atual, que é a ferramenta para a qual a dica de ferramentas está exibindo texto no momento. <br/>                                               |
| [**TTM \_ GETbubbleize**](ttm-getbubblesize.md)     | Retorna a largura e a altura de um controle ToolTip.<br/>                                                                                                                                                     |
| [**TTM \_ GETCURRENTTOOL**](ttm-getcurrenttool.md)   | Recupera as informações da ferramenta atual em um controle ToolTip. <br/>                                                                                                                                  |
| [**TTM \_ GETdelaytime**](ttm-getdelaytime.md)       | Recupera as durações inicial, pop-up e Reexibir atualmente definidas para um controle ToolTip.<br/>                                                                                                               |
| [**GetMargin TTM \_**](ttm-getmargin.md)             | Recupera as margens superior, esquerda, inferior e direita definidas para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta. <br/> |
| [**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)   | Recupera a largura máxima de uma janela de dica de ferramenta. <br/>                                                                                                                                                     |
| [**TTM \_ GETtext**](ttm-gettext.md)                 | Recupera as informações que um controle ToolTip mantém sobre uma ferramenta. <br/>                                                                                                                                   |
| [**TTM \_ GETTIPBKCOLOR**](ttm-gettipbkcolor.md)     | Recupera a cor do plano de fundo em uma janela de dica de ferramenta. <br/>                                                                                                                                                   |
| [**TTM \_ GETTIPTEXTCOLOR**](ttm-gettiptextcolor.md) | Recupera a cor do texto em uma janela de dica de ferramenta. <br/>                                                                                                                                                         |
| [**TTM \_ GETtitle**](ttm-gettitle.md)               | Recupere informações relativas ao título de um controle ToolTip.<br/>                                                                                                                                        |
| [**TTM \_ GETTOOLCOUNT**](ttm-gettoolcount.md)       | Recupera uma contagem das ferramentas mantidas por um controle ToolTip. <br/>                                                                                                                                       |
| [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md)         | Recupera as informações que um controle ToolTip mantém sobre uma ferramenta. <br/>                                                                                                                              |
| [**TTM \_ HITTEST**](ttm-hittest.md)                 | Testa um ponto para determinar se ele está dentro do retângulo delimitador da ferramenta especificada e, se for, recupera informações sobre a ferramenta. <br/>                                                     |
| [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md)         | Define um novo retângulo delimitador para uma ferramenta. <br/>                                                                                                                                                             |
| [**TTM \_ pop**](ttm-pop.md)                         | Remove uma janela de dica de ferramenta exibida do modo de exibição. <br/>                                                                                                                                                         |
| [**\_pop-up TTM**](ttm-popup.md)                     | Faz com que a dica de ferramenta seja exibida nas coordenadas da última mensagem do mouse.<br/>                                                                                                                            |
| [**TTM \_ RELAYEVENT**](ttm-relayevent.md)           | Passa uma mensagem do mouse para um controle ToolTip para processamento. <br/>                                                                                                                                           |
| [**TTM \_ SETatrasartime**](ttm-setdelaytime.md)       | Define as durações inicial, pop-up e Reexibir para um controle ToolTip.<br/>                                                                                                                                  |
| [**TTM \_ SETmargin**](ttm-setmargin.md)             | Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta. <br/>          |
| [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)   | Define a largura máxima para uma janela de dica de ferramenta. <br/>                                                                                                                                                          |
| [**TTM \_ SETTIPBKCOLOR**](ttm-settipbkcolor.md)     | Define a cor do plano de fundo em uma janela de dica de ferramenta. <br/>                                                                                                                                                        |
| [**TTM \_ SETTIPTEXTCOLOR**](ttm-settiptextcolor.md) | Define a cor do texto em uma janela de dica de ferramenta. <br/>                                                                                                                                                              |
| [**TTM \_ SETtitle**](ttm-settitle.md)               | Adiciona um ícone padrão e uma cadeia de título a uma dica de ferramenta.<br/>                                                                                                                                                    |
| [**TTM \_ SETTOOLINFO**](ttm-settoolinfo.md)         | Define as informações que um controle ToolTip mantém para uma ferramenta. <br/>                                                                                                                                     |
| [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   | Define o estilo visual de um controle ToolTip.<br/>                                                                                                                                                            |
| [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)     | Ativa ou desativa uma dica de ferramenta de rastreamento.<br/>                                                                                                                                                           |
| [**TTM \_ TRACKPOSITION**](ttm-trackposition.md)     | Define a posição de uma dica de ferramenta de rastreamento.<br/>                                                                                                                                                               |
| [**atualização do TTM \_**](ttm-update.md)                   | Força a redesenho da dica de ferramenta atual. <br/>                                                                                                                                                             |
| [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md)     | Define o texto de ToolTip para uma ferramenta. <br/>                                                                                                                                                                     |
| [**TTM \_ WINDOWFROMPOINT**](ttm-windowfrompoint.md) | Permite que um procedimento de subclasse faça com que uma dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse. <br/>                                                                              |



 

### <a name="notifications"></a>Notificações



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                              |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (dica de ferramenta)](nm-customdraw-tooltip.md) | Enviado por um controle ToolTip para notificar suas janelas pai sobre as operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                 |
| [TTN \_ GETDISPINFO](ttn-getdispinfo.md)               | Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                            |
| [TTN \_ LINKCLICK](ttn-linkclick.md)                   | Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado. <br/>                                                                                                                                                                                                |
| [TTN \_ NEEDTEXT](ttn-needtext.md)                     | Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Essa notificação é idêntica a [TTN \_ GETDISPINFO](ttn-getdispinfo.md). Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/> |
| [TTN \_ pop](ttn-pop.md)                               | Notifica a janela do proprietário de que uma dica de ferramenta está prestes a ser ocultada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                  |
| [TTN \_ Mostrar](ttn-show.md)                             | Notifica a janela do proprietário que um controle ToolTip está prestes a ser exibido. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                       |



 

### <a name="structures"></a>Estruturas



| Tópico                                    | Sumário                                                                                                                                                                                                                           |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Contém informações específicas para um código de notificação [nm \_ CUSTOMDRAW](nm-customdraw-tooltip.md) enviado por um controle ToolTip. <br/>                                                                                           |
| [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)     | Contém informações usadas na manipulação do código de notificação [TTN \_ GETDISPINFO](ttn-getdispinfo.md) . Essa estrutura substitui a estrutura **ToolTipText** . <br/>                                                          |
| [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)             | A estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contém informações sobre uma ferramenta em um controle ToolTip.<br/>                                                                                                                      |
| [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle)         | Fornece informações sobre o título de um controle ToolTip. <br/>                                                                                                                                                             |
| [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa)   | Contém informações que um controle ToolTip usa para determinar se um ponto está no retângulo delimitador da ferramenta especificada. Se o ponto estiver no retângulo, a estrutura receberá informações sobre a ferramenta. <br/> |



 

### <a name="constants"></a>Constantes



| Tópico                                | Sumário                                                                     |
|--------------------------------------|------------------------------------------------------------------------------|
| [Estilos de dica de ferramenta](tooltip-styles.md) | Esta seção lista os estilos de controle usados com controles de dica de ferramenta.<br/> |



 

 

 





