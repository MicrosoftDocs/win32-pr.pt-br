---
title: Rebar
description: Esta seção contém informações sobre elementos de programação usados com controles de barra rebar.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ac71ea71b5e0b0bd1e222d46c070a62512f0f5ff3b885fe13b19fad10f7bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434836"
---
# <a name="rebar"></a>Rebar

Esta seção contém informações sobre elementos de programação usados com controles de barra rebar.

### <a name="overviews"></a>Visões gerais



| Tópico                                            | Sumário                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Rebar Controls](rebar-controls.md)             | *Os controles de barra* de rebar atuam como contêineres para janelas filho.<br/>                       |
| [Usando controles de barra de rebar](using-rebar-controls.md) | Esta seção contém um código de exemplo mostrando como implementar controles de barras rebar.<br/> |



 

### <a name="messages"></a>Mensagens



| Tópico                                               | Sumário                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RB \_ BEGINDRAG**](rb-begindrag.md)               | Coloca o controle de barra de rebar no modo do tipo "arrastar e soltar". Essa mensagem não faz com que uma [notificação \_ BEGINDRAG](rbn-begindrag.md) do RBN seja enviada. <br/>                                                 |
| [**RB \_ DELETEBAND**](rb-deleteband.md)             | Exclui uma faixa de um controle de barra de rebar. <br/>                                                                                                                                                     |
| [**RB \_ DRAGMOVE**](rb-dragmove.md)                 | Atualiza a posição de arrastar no controle de barra de rebar após uma mensagem [**\_ BEGINDRAG do RB**](rb-begindrag.md) anterior. <br/>                                                                           |
| [**RB \_ ENDDRAG**](rb-enddrag.md)                   | Encerra a operação do tipo "arrastar e soltar" do controle de barras. Essa mensagem não faz com que uma [notificação \_ RBN ENDDRAG](rbn-enddrag.md) seja enviada. <br/>                                          |
| [**RB \_ GETBANDBORDERS**](rb-getbandborders.md)     | Recupera as bordas de uma banda. O resultado dessa mensagem pode ser usado para calcular a área acessível em uma banda. <br/>                                                                          |
| [**RB \_ GETBANDCOUNT**](rb-getbandcount.md)         | Recupera a contagem de faixas atualmente no controle de barra de rebar. <br/>                                                                                                                             |
| [**RB \_ GETBANDINFO**](rb-getbandinfo.md)           | Recupera informações sobre uma faixa especificada em um controle de barra rebar. <br/>                                                                                                                         |
| [**RB \_ GETBANDMARGINS**](rb-getbandmargins.md)     | Recupera as margens de uma banda.<br/>                                                                                                                                                          |
| [**RB \_ GETBARHEIGHT**](rb-getbarheight.md)         | Recupera a altura do controle de barra de rebar. <br/>                                                                                                                                               |
| [**RB \_ GETBARINFO**](rb-getbarinfo.md)             | Recupera informações sobre o controle de barra de rebar e a lista de imagens que ele usa. <br/>                                                                                                                |
| [**RB \_ GETBKCOLOR**](rb-getbkcolor.md)             | Recupera a cor da tela de fundo padrão de um controle de barras. <br/>                                                                                                                                    |
| [**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)     | Recupera as informações do esquema de cores do controle de barra de rebar. <br/>                                                                                                                           |
| [**RB \_ GETDROPTARGET**](rb-getdroptarget.md)       | Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle de barra de rebar. <br/>                                                                                                        |
| [**RB \_ GETEXTENDEDSTYLE**](rb-getextendedstyle.md) | Obtém o estilo estendido. <br/>                                                                                                                                                                 |
| [**RB \_ GETPALETTE**](rb-getpalette.md)             | Recupera a paleta atual do controle de barra de rebar. <br/>                                                                                                                                           |
| [**GETRECT do RB \_**](rb-getrect.md)                   | Recupera o retângulo delimitado para uma determinada faixa em um controle de barra rebar. <br/>                                                                                                                    |
| [**RB \_ GETROWCOUNT**](rb-getrowcount.md)           | Recupera o número de linhas de faixas em um controle de barra rebar. <br/>                                                                                                                                |
| [**RB \_ GETROWHEIGHT**](rb-getrowheight.md)         | Recupera a altura de uma linha especificada em um controle de barra de rebar. <br/>                                                                                                                              |
| [**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)         | Recupera a cor de texto padrão de um controle de barra de rebar. <br/>                                                                                                                                          |
| [**RB \_ GETTOOLTIPS**](rb-gettooltips.md)           | Recupera o alça para qualquer controle de dica de ferramenta associado ao controle de barra de ferramentas. <br/>                                                                                                           |
| [**RB \_ GETUNICODEFORMAT**](rb-getunicodeformat.md) | Recupera o sinalizador de formato de caractere Unicode para o controle . <br/>                                                                                                                             |
| [**RB \_ HITTEST**](rb-hittest.md)                   | Determina qual parte de uma faixa de barra de rebar está em um determinado ponto na tela, se uma faixa de barra de rebar existir nesse ponto. <br/>                                                                        |
| [**RB \_ IDTOINDEX**](rb-idtoindex.md)               | Converte um identificador de banda em um índice de banda em um controle de barra rebar. <br/>                                                                                                                           |
| [**RB \_ INSERTBAND**](rb-insertband.md)             | Insere uma nova banda em um controle de barra de rebar. <br/>                                                                                                                                                   |
| [**RB \_ MAXIMIZEBAND**](rb-maximizeband.md)         | Resize uma banda em um controle de barra de rebar para seu tamanho ideal ou maior. <br/>                                                                                                                   |
| [**RB \_ MINIMIZEBAND**](rb-minimizeband.md)         | Resize uma banda em um controle de barra de rebar para seu menor tamanho. <br/>                                                                                                                                  |
| [**RB \_ MOVEBAND**](rb-moveband.md)                 | Move uma faixa de um índice para outro. <br/>                                                                                                                                                  |
| [**RB \_ PUSH LTDRON**](rb-pushchevron.md)           | Enviado para um controle de barra de rebar para enviar por push programaticamente uma divisa.<br/>                                                                                                                               |
| [**RB \_ SETBANDINFO**](rb-setbandinfo.md)           | Define características de uma banda existente em um controle de barra rebar. <br/>                                                                                                                             |
| [**RB \_ SETBANDWIDTH**](rb-setbandwidth.md)         | Define a largura de uma banda encaixada.<br/>                                                                                                                                                         |
| [**RB \_ SETBARINFO**](rb-setbarinfo.md)             | Define as características de um controle de barra de rebar. <br/>                                                                                                                                             |
| [**RB \_ SETBKCOLOR**](rb-setbkcolor.md)             | Define a cor padrão da tela de fundo de um controle de barra de rebar. <br/>                                                                                                                                         |
| [**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)     | Define as informações do esquema de cores para o controle de barra de rebar. <br/>                                                                                                                                 |
| [**RB \_ SETEXTENDEDSTYLE**](rb-setextendedstyle.md) | Define o estilo estendido. Essa mensagem não está implementada.<br/>                                                                                                                                 |
| [**RB \_ SETPALETTE**](rb-setpalette.md)             | Define a paleta atual do controle de barra de rebar. <br/>                                                                                                                                                |
| [**RB \_ SETPARENT**](rb-setparent.md)               | Define a janela pai de um controle de barra de rebar. <br/>                                                                                                                                                    |
| [**RB \_ SETTEXTCOLOR**](rb-settextcolor.md)         | Define a cor de texto padrão de um controle de barra de rebar. <br/>                                                                                                                                               |
| [**RB \_ SETTOOLTIPS**](rb-settooltips.md)           | Associa um controle de dica de ferramenta ao controle de barra de rebar. <br/>                                                                                                                                     |
| [**RB \_ SETUNICODEFORMAT**](rb-setunicodeformat.md) | Define o sinalizador de formato de caractere Unicode para o controle . Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de executar, em vez de precisar criar o controle. <br/> |
| [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     | Define o estilo visual de um controle de barra de rebar.<br/>                                                                                                                                                 |
| [**RB \_ SHOWBAND**](rb-showband.md)                 | Mostra ou oculta uma determinada banda em um controle de barra rebar. <br/>                                                                                                                                          |
| [**RB \_ SIZETORECT**](rb-sizetorect.md)             | Tenta encontrar o melhor layout das faixas para o retângulo determinado. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Notificações



| Tópico                                                        | Sumário                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (barra rebar)](nm-customdraw-rebar.md)            | Enviado pelo controle rebar para notificar sua janela pai sobre operações de desenho. Essa notificação é enviada na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                               |
| [NM \_ NCHITTEST (barra rebar)](nm-nchittest-rebar.md)              | Enviado por um controle de barra de rebar quando o controle recebe uma [**mensagem WM \_ NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (barra rebar)](nm-releasedcapture-rebar-.md) | Notifica a janela pai de um controle de barra de rebar de que o controle está liberando a captura do mouse. Essa notificação é enviada na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                        |
| [RBN \_ AUTOBREAK](rbn-autobreak.md)                          | Notifica o [pai de uma barra de rebar](rebar-controls.md) de que uma quebra será exibida na barra. O pai determina se deve fazer a quebra. <br/>                                                                                                                            |
| [RBN \_ AUTOSIZE](rbn-autosize.md)                            | Enviado por um controle de barra de rebar criado com o [**estilo \_ AUTOSIZE do RBS**](rebar-control-styles.md) quando a barra de rebar é automaticamente ressarçada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | Enviado por um controle de barra de rebar quando o usuário começa a arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | Enviado por um controle de barra de rebar quando uma divisa é enviada por pushed. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | Enviado por um controle de barra de rebar quando a janela filho de uma banda é resized. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | Enviado por um controle de barra de rebar após a exclusão de uma banda. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                  |
| [RBN \_ DELETINGBAND](rbn-deletingband.md)                    | Enviado por um controle de barra de rebar quando uma banda está prestes a ser excluída. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                             |
| [RBN \_ ENDDRAG](rbn-enddrag.md)                              | Enviado por um controle de barra de rebar quando o usuário para de arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                            |
| [RBN \_ GETOBJECT](rbn-getobject.md)                          | Enviado por um controle de barra de rebar criado com o [**estilo \_ REGISTERDROP do RBS**](rebar-control-styles.md) quando um objeto é arrastado sobre uma banda no controle . Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [RBN \_ HEIGHTCHANGE](rbn-heightchange.md)                    | Enviado por um controle de barra de rebar quando sua altura foi alterada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                    |
| [LAYOUT DO \_ RBNCHANGED](rbn-layoutchanged.md)                  | Enviado por um controle de barra de rebar quando o usuário altera o layout das faixas do controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                        |
| [RBN \_ MINMAX](rbn-minmax.md)                                | Enviado por um controle de barra de rebar antes de maximizar ou minimizar uma banda. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | Enviado por um controle de barra de rebar quando o usuário arrasta um divisor. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                 |



 

### <a name="structures"></a>Estruturas



| Tópico                                        | Sumário                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Contém informações usadas para lidar com os códigos [de \_ notificação AUTOSIZE do RBN.](rbn-autosize.md) <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Contém informações usadas para lidar com vários códigos de notificação de barra rebar. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Contém informações usadas com a [notificação \_ RBN AUTOBREAK.](rbn-autobreak.md)<br/>                                               |
| [**NMREBAR LTDRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Contém informações usadas para lidar com o [código de notificação \_ RBN CHEVRONPUSHED.](rbn-chevronpushed.md) <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Contém informações usadas para lidar com o [código de notificação \_ CHILDSIZE do RBN.](rbn-childsize.md) <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Contém informações usadas para lidar com um [código de notificação \_ RBN SPLITTERDRAG.](rbn-splitterdrag.md)<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Contém informações específicas de uma operação de teste de acerto. Essa estrutura é usada com a [**mensagem RB \_ HITTEST.**](rb-hittest.md) <br/> |
| [**Rebarbandinfo**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Contém informações que definem uma faixa em um controle de barra rebar. <br/>                                                                      |
| [**Rebarinfo**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Contém informações que descrevem as características de controle de barra rebar. <br/>                                                                |



 

### <a name="constants"></a>Constantes



| Tópico                                            | Sumário                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Rebar estilos de controle](rebar-control-styles.md) | Os controles de barra de rebar suportam uma variedade de estilos de controle, além dos estilos de janela padrão. <br/> |



 

 

