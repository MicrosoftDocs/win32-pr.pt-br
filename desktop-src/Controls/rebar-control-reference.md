---
title: Rebar
description: Esta seção contém informações sobre elementos de programação usados com controles Rebar.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef14343d33fb5ae45a2d93df74a9b915aca6d7b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454399"
---
# <a name="rebar"></a>Rebar

Esta seção contém informações sobre elementos de programação usados com controles Rebar.

### <a name="overviews"></a>Visões gerais



| Tópico                                            | Sumário                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Controles Rebar](rebar-controls.md)             | Os *controles Rebar* atuam como contêineres para janelas filhas.<br/>                       |
| [Usando controles Rebar](using-rebar-controls.md) | Esta seção contém um código de exemplo que mostra como implementar controles Rebar.<br/> |



 

### <a name="messages"></a>Mensagens



| Tópico                                               | Sumário                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BEGINDRAG RB**](rb-begindrag.md)               | Coloca o controle rebar no modo arrastar e soltar. Essa mensagem não faz com que uma notificação [RBN \_ BEGINDRAG](rbn-begindrag.md) seja enviada. <br/>                                                 |
| [**\_DELETEBAND RB**](rb-deleteband.md)             | Exclui uma faixa de um controle rebar. <br/>                                                                                                                                                     |
| [**\_DRAGMOVE RB**](rb-dragmove.md)                 | Atualiza a posição de arrastar no controle rebar após uma mensagem [**\_ BEGINDRAG de RB**](rb-begindrag.md) anterior. <br/>                                                                           |
| [**ARRASTAR para a RB \_**](rb-enddrag.md)                   | Encerra a operação de arrastar e soltar do controle rebar. Esta mensagem não faz com que uma notificação [RBN \_ endarraste](rbn-enddrag.md) seja enviada. <br/>                                          |
| [**\_GETBANDBORDERS RB**](rb-getbandborders.md)     | Recupera as bordas de uma banda. O resultado dessa mensagem pode ser usado para calcular a área utilizável em uma banda. <br/>                                                                          |
| [**\_GETBANDCOUNT RB**](rb-getbandcount.md)         | Recupera a contagem de faixas atualmente no controle rebar. <br/>                                                                                                                             |
| [**\_GETBANDINFO RB**](rb-getbandinfo.md)           | Recupera informações sobre uma faixa especificada em um controle rebar. <br/>                                                                                                                         |
| [**\_GETBANDMARGINS RB**](rb-getbandmargins.md)     | Recupera as margens de uma banda.<br/>                                                                                                                                                          |
| [**\_GETBARHEIGHT RB**](rb-getbarheight.md)         | Recupera a altura do controle rebar. <br/>                                                                                                                                               |
| [**\_GETBARINFO RB**](rb-getbarinfo.md)             | Recupera informações sobre o controle rebar e a lista de imagens que ele usa. <br/>                                                                                                                |
| [**\_GETBKCOLOR RB**](rb-getbkcolor.md)             | Recupera a cor do plano de fundo padrão de um controle rebar. <br/>                                                                                                                                    |
| [**\_GETCOLORSCHEME RB**](rb-getcolorscheme.md)     | Recupera as informações do esquema de cores do controle rebar. <br/>                                                                                                                           |
| [**\_GETDROPTARGET RB**](rb-getdroptarget.md)       | Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle rebar. <br/>                                                                                                        |
| [**RB \_ Extended**](rb-getextendedstyle.md) | Obtém o estilo estendido. <br/>                                                                                                                                                                 |
| [**GetPalette RB \_**](rb-getpalette.md)             | Recupera a paleta atual do controle rebar. <br/>                                                                                                                                           |
| [**GetRect de RB \_**](rb-getrect.md)                   | Recupera o retângulo delimitador para uma determinada faixa em um controle rebar. <br/>                                                                                                                    |
| [**GetRowCount de RB \_**](rb-getrowcount.md)           | Recupera o número de linhas de faixas em um controle rebar. <br/>                                                                                                                                |
| [**getalturadalinha de RB \_**](rb-getrowheight.md)         | Recupera a altura de uma linha especificada em um controle rebar. <br/>                                                                                                                              |
| [**\_GETTEXTCOLOR RB**](rb-gettextcolor.md)         | Recupera a cor de texto padrão de um controle rebar. <br/>                                                                                                                                          |
| [**\_GETtooltips RB**](rb-gettooltips.md)           | Recupera o identificador para qualquer controle ToolTip associado ao controle rebar. <br/>                                                                                                           |
| [**\_GETUNICODEFORMAT RB**](rb-getunicodeformat.md) | Recupera o sinalizador de formato de caractere Unicode para o controle. <br/>                                                                                                                             |
| [**HITTEST de RB \_**](rb-hittest.md)                   | Determina qual parte de uma banda de rebar está em um determinado ponto na tela, se existir uma banda de rebar nesse ponto. <br/>                                                                        |
| [**\_IDTOINDEX RB**](rb-idtoindex.md)               | Converte um identificador de banda em um índice de faixa em um controle rebar. <br/>                                                                                                                           |
| [**\_INSERTBAND RB**](rb-insertband.md)             | Insere uma nova faixa em um controle rebar. <br/>                                                                                                                                                   |
| [**\_MAXIMIZEBAND RB**](rb-maximizeband.md)         | Redimensiona uma faixa em um controle rebar para o tamanho ideal ou maior. <br/>                                                                                                                   |
| [**\_MINIMIZEBAND RB**](rb-minimizeband.md)         | Redimensiona uma faixa em um controle rebar para seu menor tamanho. <br/>                                                                                                                                  |
| [**\_MOVEBAND RB**](rb-moveband.md)                 | Move uma banda de um índice para outro. <br/>                                                                                                                                                  |
| [**\_PUSHCHEVRON RB**](rb-pushchevron.md)           | Enviado a um controle rebar para enviar por push programaticamente uma divisa.<br/>                                                                                                                               |
| [**\_SETBANDINFO RB**](rb-setbandinfo.md)           | Define características de uma banda existente em um controle rebar. <br/>                                                                                                                             |
| [**\_largura de banda RB**](rb-setbandwidth.md)         | Define a largura de uma faixa encaixada.<br/>                                                                                                                                                         |
| [**\_SETBARINFO RB**](rb-setbarinfo.md)             | Define as características de um controle rebar. <br/>                                                                                                                                             |
| [**\_SETBKCOLOR RB**](rb-setbkcolor.md)             | Define a cor do plano de fundo padrão de um controle rebar. <br/>                                                                                                                                         |
| [**\_SETCOLORSCHEME RB**](rb-setcolorscheme.md)     | Define as informações do esquema de cores para o controle rebar. <br/>                                                                                                                                 |
| [**RB \_ SETextendedattribute**](rb-setextendedstyle.md) | Define o estilo estendido. Esta mensagem não está implementada.<br/>                                                                                                                                 |
| [**SetPalette de RB \_**](rb-setpalette.md)             | Define a paleta atual do controle rebar. <br/>                                                                                                                                                |
| [**RB \_ SETpai**](rb-setparent.md)               | Define a janela pai do controle rebar. <br/>                                                                                                                                                    |
| [**\_SETTEXTCOLOR RB**](rb-settextcolor.md)         | Define a cor de texto padrão de um controle rebar. <br/>                                                                                                                                               |
| [**RB \_ SETtooltips**](rb-settooltips.md)           | Associa um controle ToolTip ao controle rebar. <br/>                                                                                                                                     |
| [**\_SETUNICODEFORMAT RB**](rb-setunicodeformat.md) | Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle. <br/> |
| [**\_SETWINDOWTHEME RB**](rb-setwindowtheme.md)     | Define o estilo visual de um controle rebar.<br/>                                                                                                                                                 |
| [**Não \_ Band de RB**](rb-showband.md)                 | Mostra ou oculta uma determinada faixa em um controle rebar. <br/>                                                                                                                                          |
| [**\_SIZETORECT RB**](rb-sizetorect.md)             | Tenta encontrar o melhor layout das faixas para o retângulo fornecido. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Notificações



| Tópico                                                        | Sumário                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (rebar)](nm-customdraw-rebar.md)            | Enviado pelo controle rebar para notificar sua janela pai sobre operações de desenho. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .<br/>                                                                                               |
| [NM \_ NCHITTEST (rebar)](nm-nchittest-rebar.md)              | Enviado por um controle rebar quando o controle recebe uma mensagem de [**\_ NCHITTEST do WM**](/windows/desktop/inputdev/wm-nchittest) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (rebar)](nm-releasedcapture-rebar-.md) | Notifica uma janela pai do controle rebar que o controle está liberando a captura do mouse. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) . <br/>                                                                                        |
| [\_quebra automática de RBN](rbn-autobreak.md)                          | Notifica o pai [de um rebar](rebar-controls.md) de que uma quebra aparecerá na barra. O pai determina se a interrupção deve ser feita. <br/>                                                                                                                            |
| [\_dimensionamento automático de RBN](rbn-autosize.md)                            | Enviado por um controle rebar criado com o estilo de [**\_ AUTOSIZE do RBS**](rebar-control-styles.md) quando o rebar é redimensionado automaticamente. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | Enviado por um controle rebar quando o usuário começa a arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | Enviado por um controle rebar quando uma divisa é enviada por push. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | Enviado por um controle rebar quando a janela filho de uma banda é redimensionada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | Enviado por um controle rebar após a exclusão de uma banda. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                  |
| [RBN \_ DELETINGBAND](rbn-deletingband.md)                    | Enviado por um controle rebar quando uma banda está prestes a ser excluída. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                             |
| [RBN \_ ENDarrastar](rbn-enddrag.md)                              | Enviado por um controle rebar quando o usuário para de arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                            |
| [GetObject RBN \_](rbn-getobject.md)                          | Enviado por um controle rebar criado com o estilo [**RBS \_ REGISTERDROP**](rebar-control-styles.md) quando um objeto é arrastado sobre uma banda no controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/> |
| [RBN \_ HEIGHTCHANGE](rbn-heightchange.md)                    | Enviado por um controle rebar quando sua altura é alterada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                    |
| [RBN \_ layoutchanged](rbn-layoutchanged.md)                  | Enviado por um controle rebar quando o usuário altera o layout das faixas do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                        |
| [RBN \_ por minMax](rbn-minmax.md)                                | Enviado por um controle rebar antes de maximizar ou minimizar uma banda. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | Enviado por um controle rebar quando o usuário arrasta um divisor. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                 |



 

### <a name="structures"></a>Estruturas



| Tópico                                        | Sumário                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Contém informações usadas para manipular os códigos de notificação de [ \_ dimensionamento de RBN](rbn-autosize.md) . <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Contém informações usadas na manipulação de vários códigos de notificação de rebar. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Contém informações usadas com a notificação de [ \_ quebra automática de RBN](rbn-autobreak.md) .<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Contém informações usadas na manipulação do código de notificação [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) . <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Contém informações usadas na manipulação do código de notificação [RBN \_ CHILDSIZE](rbn-childsize.md) . <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Contém informações usadas para manipular um código de notificação [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md) .<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Contém informações específicas para uma operação de teste de clique. Essa estrutura é usada com a mensagem de [**\_ HITTEST de RB**](rb-hittest.md) . <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Contém informações que definem uma faixa em um controle rebar. <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Contém informações que descrevem as características do controle rebar. <br/>                                                                |



 

### <a name="constants"></a>Constantes



| Tópico                                            | Sumário                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Estilos de controle rebar](rebar-control-styles.md) | Os controles Rebar dão suporte a uma variedade de estilos de controle, além dos estilos de janela padrão. <br/> |



 

 

