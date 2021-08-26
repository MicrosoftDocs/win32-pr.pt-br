---
title: Dica de ferramenta
description: Esta seção contém informações sobre os elementos de programação usados com controles de dica de ferramenta.
ms.assetid: vs|controls|~\controls\tooltip\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30ebe66569ede133c311168d3f3f2870dc3aeabe8eaeaa3e15d6584be2d6873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046036"
---
# <a name="tooltip"></a>Dica de ferramenta

Esta seção contém informações sobre os elementos de programação usados com controles de dica de ferramenta.

### <a name="overviews"></a>Visões gerais



| Tópico                                              | Sumário                                                                                                                          |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Sobre controles de dica de ferramenta](tooltip-controls.md)     | As dicas de ferramenta aparecem automaticamente ou aparecem quando o usuário pausa o ponteiro do mouse sobre uma ferramenta ou algum outro elemento de interface do usuário.<br/> |
| [Usando controles de dica de ferramenta](using-tooltip-contro.md) | Esta seção contém exemplos que demonstram como criar diferentes tipos de dicas de ferramenta.<br/>                             |



 

### <a name="messages"></a>Mensagens



| Tópico                                               | Sumário                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TTM \_ ACTIVATE**](ttm-activate.md)               | Ativa ou desativa um controle de dica de ferramenta. <br/>                                                                                                                                                           |
| [**TTM \_ ADDTOOL**](ttm-addtool.md)                 | Registra uma ferramenta com um controle de dica de ferramenta. <br/>                                                                                                                                                              |
| [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)           | Calcula o retângulo de exibição de texto de um controle de dica de ferramenta de seu retângulo de janela ou o retângulo da janela de dica de ferramenta necessário para exibir um retângulo de exibição de texto especificado. <br/>                                |
| [**TTM \_ DELTOOL**](ttm-deltool.md)                 | Remove uma ferramenta de um controle de dica de ferramenta. <br/>                                                                                                                                                                |
| [**TTM \_ ENUMTOOLS**](ttm-enumtools.md)             | Recupera as informações que um controle de dica de ferramenta mantém sobre a ferramenta atual, ou seja, a ferramenta para a qual a dica de ferramenta está exibindo texto no momento. <br/>                                               |
| [**TTM \_ GETBUBBLESIZE**](ttm-getbubblesize.md)     | Retorna a largura e a altura de um controle de dica de ferramenta.<br/>                                                                                                                                                     |
| [**TTM \_ GETCURRENTTOOL**](ttm-getcurrenttool.md)   | Recupera as informações da ferramenta atual em um controle de dica de ferramenta. <br/>                                                                                                                                  |
| [**TTM \_ GETDELAYTIME**](ttm-getdelaytime.md)       | Recupera as durações iniciais, pop-up e remostr atualmente definidas para um controle de dica de ferramenta.<br/>                                                                                                               |
| [**TTM \_ GETMARGIN**](ttm-getmargin.md)             | Recupera as margens superior, esquerda, inferior e direita definidas para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta. <br/> |
| [**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)   | Recupera a largura máxima de uma janela de dica de ferramenta. <br/>                                                                                                                                                     |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                 | Recupera as informações que um controle de dica de ferramenta mantém sobre uma ferramenta. <br/>                                                                                                                                   |
| [**TTM \_ GETTIPBKCOLOR**](ttm-gettipbkcolor.md)     | Recupera a cor da tela de fundo em uma janela de dica de ferramenta. <br/>                                                                                                                                                   |
| [**TTM \_ GETTIPTEXTCOLOR**](ttm-gettiptextcolor.md) | Recupera a cor do texto em uma janela de dica de ferramenta. <br/>                                                                                                                                                         |
| [**TTM \_ GETTITLE**](ttm-gettitle.md)               | Recuperar informações sobre o título de um controle de dica de ferramenta.<br/>                                                                                                                                        |
| [**TTM \_ GETTOOLCOUNT**](ttm-gettoolcount.md)       | Recupera uma contagem das ferramentas mantidas por um controle de dica de ferramenta. <br/>                                                                                                                                       |
| [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md)         | Recupera as informações que um controle de dica de ferramenta mantém sobre uma ferramenta. <br/>                                                                                                                              |
| [**TTM \_ HITTEST**](ttm-hittest.md)                 | Testa um ponto para determinar se ele está dentro do retângulo delimitante da ferramenta especificada e, se estiver, recupera informações sobre a ferramenta. <br/>                                                     |
| [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md)         | Define um novo retângulo delimitado para uma ferramenta. <br/>                                                                                                                                                             |
| [**TTM \_ POP**](ttm-pop.md)                         | Remove uma janela de dica de ferramenta exibida da exibição. <br/>                                                                                                                                                         |
| [**\_POP-UP TTM**](ttm-popup.md)                     | Faz com que a dica de ferramenta seja exibida nas coordenadas da última mensagem do mouse.<br/>                                                                                                                            |
| [**TTM \_ RELAYEVENT**](ttm-relayevent.md)           | Passa uma mensagem do mouse para um controle de dica de ferramenta para processamento. <br/>                                                                                                                                           |
| [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)       | Define as durações inicial, pop-up e remostr para um controle de dica de ferramenta.<br/>                                                                                                                                  |
| [**TTM \_ SETMARGIN**](ttm-setmargin.md)             | Define as margens superior, esquerda, inferior e direita para uma janela de dica de ferramenta. Uma margem é a distância, em pixels, entre a borda da janela de dica de ferramenta e o texto contido na janela de dica de ferramenta. <br/>          |
| [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)   | Define a largura máxima de uma janela de dica de ferramenta. <br/>                                                                                                                                                          |
| [**TTM \_ SETTIPBKCOLOR**](ttm-settipbkcolor.md)     | Define a cor da tela de fundo em uma janela de dica de ferramenta. <br/>                                                                                                                                                        |
| [**TTM \_ SETTIPTEXTCOLOR**](ttm-settiptextcolor.md) | Define a cor do texto em uma janela de dica de ferramenta. <br/>                                                                                                                                                              |
| [**TTM \_ SETTITLE**](ttm-settitle.md)               | Adiciona um ícone padrão e uma cadeia de caracteres de título a uma dica de ferramenta.<br/>                                                                                                                                                    |
| [**TTM \_ SETTOOLINFO**](ttm-settoolinfo.md)         | Define as informações que um controle de dica de ferramenta mantém para uma ferramenta. <br/>                                                                                                                                     |
| [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   | Define o estilo visual de um controle de dica de ferramenta.<br/>                                                                                                                                                            |
| [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)     | Ativa ou desativa uma dica de ferramenta de acompanhamento.<br/>                                                                                                                                                           |
| [**TTM \_ TRACKPOSITION**](ttm-trackposition.md)     | Define a posição de uma dica de ferramenta de acompanhamento.<br/>                                                                                                                                                               |
| [**ATUALIZAÇÃO \_ TTM**](ttm-update.md)                   | Força a dica de ferramenta atual a ser redesenhada. <br/>                                                                                                                                                             |
| [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md)     | Define o texto da dica de ferramenta para uma ferramenta. <br/>                                                                                                                                                                     |
| [**JANELA \_ TTMFROMPOINT**](ttm-windowfrompoint.md) | Permite que um procedimento de subclasse cause uma dica de ferramenta a exibir texto para uma janela diferente da que está abaixo do cursor do mouse. <br/>                                                                              |



 

### <a name="notifications"></a>Notificações



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                              |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (dica de ferramenta)](nm-customdraw-tooltip.md) | Enviado por um controle de dica de ferramenta para notificar suas janelas pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                 |
| [TTN \_ GETDISPINFO](ttn-getdispinfo.md)               | Enviado por um controle de dica de ferramenta para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                            |
| [TTN \_ LINKCLICK](ttn-linkclick.md)                   | Enviado quando um link de texto dentro de uma dica de ferramenta de balão é clicado. <br/>                                                                                                                                                                                                |
| [TTN \_ NEEDTEXT](ttn-needtext.md)                     | Enviado por um controle de dica de ferramenta para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Essa notificação é idêntica [a TTN \_ GETDISPINFO.](ttn-getdispinfo.md) Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [TTN \_ POP](ttn-pop.md)                               | Notifica a janela do proprietário de que uma dica de ferramenta está prestes a ser ocultada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                  |
| [TTN \_ SHOW](ttn-show.md)                             | Notifica a janela do proprietário de que um controle de dica de ferramenta está prestes a ser exibido. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                       |



 

### <a name="structures"></a>Estruturas



| Tópico                                    | Sumário                                                                                                                                                                                                                           |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | Contém informações específicas para um [código de notificação \_ CUSTOMDRAW NM](nm-customdraw-tooltip.md) enviado por um controle de dica de ferramenta. <br/>                                                                                           |
| [**Nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)     | Contém informações usadas para lidar com o código de notificação [ \_ GETDISPINFO do TTN.](ttn-getdispinfo.md) Essa estrutura sobressalva a **estrutura TOOLTIPTEXT.** <br/>                                                          |
| [**Toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)             | A [**estrutura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contém informações sobre uma ferramenta em um controle de dica de ferramenta.<br/>                                                                                                                      |
| [**TTGTLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle)         | Fornece informações sobre o título de um controle de dica de ferramenta. <br/>                                                                                                                                                             |
| [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa)   | Contém informações que um controle de dica de ferramenta usa para determinar se um ponto está no retângulo delimitar da ferramenta especificada. Se o ponto estiver no retângulo, a estrutura receberá informações sobre a ferramenta. <br/> |



 

### <a name="constants"></a>Constantes



| Tópico                                | Sumário                                                                     |
|--------------------------------------|------------------------------------------------------------------------------|
| [Estilos de dica de ferramenta](tooltip-styles.md) | Esta seção lista os estilos de controle usados com controles de dica de ferramenta.<br/> |



 

 

 





