---
title: Pager
description: Esta seção contém informações sobre os elementos de programação usados com controles de pager.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bf9860c9e1dd1d565b24c7bbfc02e46480198f5bdea03717288abc83591a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914766"
---
# <a name="pager"></a>Pager

Esta seção contém informações sobre os elementos de programação usados com controles de pager.

### <a name="overviews"></a>Visões gerais



| Tópico                                | Sumário                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controles de pager](pager-controls.md) | Um *controle de pager* é um contêiner de janela que é usado com uma janela que não tem área de exibição suficiente para mostrar todo o seu conteúdo.<br/> |



 

### <a name="macros"></a>Macros



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Paginar \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Habilita ou desabilita o encaminhamento do mouse para o controle de pager. Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha as mensagens [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) para a janela contida. Você pode usar essa macro ou enviar a [**mensagem \_ FORWARDMOUSE PGM**](pgm-forwardmouse.md) explicitamente. <br/>                                                                                                                     |
| [**Paginar \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Recupera a cor do plano de fundo atual para o controle de pager. Você pode usar essa macro ou enviar a [**mensagem \_ GETBKCOLOR PGM**](pgm-getbkcolor.md) explicitamente. <br/>                                                                                                                                                                                                                                                                 |
| [**Pager \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Recupera o tamanho da borda atual para o controle de pager. Você pode usar essa macro ou enviar a mensagem de [**\_ GetBorder do PGM**](pgm-getborder.md) explicitamente. <br/>                                                                                                                                                                                                                                                                        |
| [**Paginar \_ Getbuttons**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Recupera o tamanho do botão atual para o controle de pager. Você pode usar essa macro ou enviar explicitamente a mensagem [**PGM \_ getbuttons**](pgm-getbuttonsize.md) . <br/>                                                                                                                                                                                                                                                                |
| [**Pager \_ Getbuttonstate**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Recupera o estado do botão especificado em um controle de pager. Você pode usar essa macro ou enviar a mensagem [**PGM \_ getbuttonstate**](pgm-getbuttonstate.md) explicitamente. <br/>                                                                                                                                                                                                                                                       |
| [**Paginar \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle de pager. Você pode usar essa macro ou enviar a [**mensagem \_ GETDROPTARGET PGM**](pgm-getdroptarget.md) explicitamente. <br/>                                                                                                                                                                                                                                       |
| [**Paginar \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Recupera a posição de rolagem atual do controle de pager. Você pode usar essa macro ou enviar a [**mensagem \_ GETPOS PGM**](pgm-getpos.md) explicitamente. <br/>                                                                                                                                                                                                                                                                           |
| [**Paginar \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Força o controle de pager a recalcular o tamanho da janela contida. Usar essa macro resultará em uma notificação [PGN \_ CALCSIZE](pgn-calcsize.md) ser enviada. Você pode usar essa macro ou enviar a [**mensagem \_ RECALCSIZE PGM**](pgm-recalcsize.md) explicitamente. <br/>                                                                                                                                                        |
| [**Paginar \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Define a cor do plano de fundo atual para o controle de pager. Você pode usar essa macro ou enviar a [**mensagem \_ SETBKCOLOR PGM**](pgm-setbkcolor.md) explicitamente. <br/>                                                                                                                                                                                                                                                                      |
| [**Autoborder do pager \_**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Define o tamanho da borda atual para o controle de pager. Você pode usar essa macro ou enviar a mensagem do [**PGM \_ SetBorder**](pgm-setborder.md) explicitamente. <br/>                                                                                                                                                                                                                                                                             |
| [**Paginar \_ SetButtons**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Define o tamanho do botão atual para o controle de pager. Você pode usar essa macro ou enviar explicitamente a mensagem do [**PGM \_ SetButtons**](pgm-setbuttonsize.md) . <br/>                                                                                                                                                                                                                                                                     |
| [**Pager- \_ filho**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Define a janela contida para o controle de pager. Essa macro não alterará o pai da janela contida; Ele atribui apenas um identificador de janela ao controle de pager para rolagem. Na maioria dos casos, a janela contida será uma janela filho. Se esse for o caso, a janela contida deverá ser um filho do controle de pager. Você pode usar essa macro ou enviar explicitamente [**a \_ mensagem do PGM**](pgm-setchild.md) . <br/> |
| [**Paginar \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Define a posição de rolagem para o controle de pager. Você pode usar essa macro ou enviar a [**mensagem \_ SETPOS PGM**](pgm-setpos.md) explicitamente. <br/>                                                                                                                                                                                                                                                                                       |
| [**Paginar \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Destinado ao uso interno; Não recomendado para uso em aplicativos.**<br/> Define os parâmetros de rolagem do controle de pager, incluindo o valor de tempo limite, as linhas por tempo limite e os pixels por linha. Você pode usar essa macro ou enviar a [**mensagem \_ SETSETSCROLLINFO PGM**](pgm-setscrollinfo.md) explicitamente. <br/>                                                                                                  |



 

### <a name="messages"></a>Mensagens



| Tópico                                              | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_FORWARDMOUSE PGM**](pgm-forwardmouse.md)      | Habilita ou desabilita o encaminhamento do mouse para o controle de pager. Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha as mensagens [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) para a janela contida. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ForwardMouse do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) . <br/>                                                                                                                       |
| [**\_GETBKCOLOR PGM**](pgm-getbkcolor.md)          | Recupera a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBkColor do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) . <br/>                                                                                                                                                                                                                                                                   |
| [**GetBorder do PGM \_**](pgm-getborder.md)            | Recupera o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) . <br/>                                                                                                                                                                                                                                                                          |
| [**getbuttons do PGM \_**](pgm-getbuttonsize.md)    | Recupera o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getbuttons do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) . <br/>                                                                                                                                                                                                                                                                  |
| [**PGM \_ GETbuttonstate**](pgm-getbuttonstate.md)  | Recupera o estado do botão especificado em um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getbuttonstate do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) . <br/>                                                                                                                                                                                                                                                         |
| [**\_GETDROPTARGET PGM**](pgm-getdroptarget.md)    | Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetDropTarget do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) . <br/>                                                                                                                                                                                                                                         |
| [**\_GETPOS PGM**](pgm-getpos.md)                  | Recupera a posição de rolagem atual do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetPos do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) . <br/>                                                                                                                                                                                                                                                                             |
| [**\_RECALCSIZE PGM**](pgm-recalcsize.md)          | Força o controle de pager a recalcular o tamanho da janela contida. O envio dessa mensagem resultará na envio de uma notificação [PGN \_ CALCSIZE](pgn-calcsize.md) . Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ RecalcSize do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) . <br/>                                                                                                                                                      |
| [**\_SETBKCOLOR PGM**](pgm-setbkcolor.md)          | Define a cor do plano de fundo atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBkColor do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) . <br/>                                                                                                                                                                                                                                                                        |
| [**SetBorder do PGM \_**](pgm-setborder.md)            | Define o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) . <br/>                                                                                                                                                                                                                                                                               |
| [**SetButtons do PGM \_**](pgm-setbuttonsize.md)    | Define o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetButtons do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) . <br/>                                                                                                                                                                                                                                                                       |
| [**PGM \_ filho**](pgm-setchild.md)              | Define a janela contida para o controle de pager. Esta mensagem não vai alterar o pai da janela contida; Ele atribui apenas um identificador de janela ao controle de pager para rolagem. Na maioria dos casos, a janela contida será uma janela filho. Se esse for o caso, a janela contida deverá ser um filho do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetChild do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) . <br/> |
| [**\_SETPOS PGM**](pgm-setpos.md)                  | Define a posição de rolagem atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetPos do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) . <br/>                                                                                                                                                                                                                                                                                 |
| [**\_SETSETSCROLLINFO PGM**](pgm-setscrollinfo.md) | **Destinado ao uso interno; Não recomendado para uso em aplicativos.**<br/> Define os parâmetros de rolagem do controle de pager, incluindo o valor de tempo limite, as linhas por tempo limite e os pixels por linha. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetScrollInfo do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) . <br/>                                                                                                  |



 

### <a name="notifications"></a>Notificações



| Tópico                                                        | Sumário                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (pager)](nm-releasedcapture-pager-.md) | Notifica uma janela pai do controle de pager que o controle liberou a captura do mouse. \_O nm RELEASEDCAPTURE é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                |
| [PGN \_ CALCSIZE](pgn-calcsize.md)                            | Notificação enviada por um controle de pager para obter as dimensões roláveis da janela contida. Essas dimensões são usadas pelo controle de pager para determinar o tamanho rolável da janela contida. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) . <br/> |
| [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md)                  | Enviado por um controle de pager quando o item quente (realçado) é alterado. <br/>                                                                                                                                                                                                                               |
| [PGN \_ Scroll](pgn-scroll.md)                                | Notificação enviada por um controle de pager antes de a janela contida ser rolada. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                         |



 

### <a name="structures"></a>Estruturas



| Tópico                                | Sumário                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Contém e recebe informações que o controle de pager usa para calcular a área rolável da janela contida. Ele é usado com a notificação [PGN \_ CALCSIZE](pgn-calcsize.md) . <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Contém informações usadas com a notificação [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md) . <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Contém e recebe informações que o controle de pager usa ao rolar a janela contida. Ele é usado com a notificação de [ \_ rolagem de PGN](pgn-scroll.md) . <br/>                          |



 

### <a name="constants"></a>Constantes



| Tópico                                            | Sumário                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Estilos de controle de pager](pager-control-styles.md) | Esta seção lista os estilos de janela usados ao criar controles de pager. <br/> |



 

 

