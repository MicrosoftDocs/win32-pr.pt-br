---
title: Barra de ferramentas
description: Esta seção contém informações sobre os elementos de programação usados com controles da barra de ferramentas.
ms.assetid: vs|controls|~\controls\toolbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0cadd2eb1560d3486073810e86a143b7fccca5
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642298"
---
# <a name="toolbar"></a>Barra de ferramentas

Esta seção contém informações sobre os elementos de programação usados com controles da barra de ferramentas.

### <a name="overviews"></a>Visões gerais



| Tópico                                                   | Sumário                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre os controles da barra de ferramentas](toolbar-controls-overview.md) | Uma barra de ferramentas é um controle que contém um ou mais botões. Cada botão, quando clicado por um usuário, envia uma mensagem de comando para a janela pai. Normalmente, os botões em uma barra de ferramentas correspondem aos itens no menu do aplicativo, fornecendo uma maneira adicional e mais direta para que o usuário acesse os comandos de um aplicativo.<br/> |
| [Usando controles da barra de ferramentas](using-toolbar-controls.md)    | Este tópico contém detalhes de implementação e código de exemplo para usar controles de barra de ferramentas em seus aplicativos.<br/>                                                                                                                                                                                                                  |



 

### <a name="functions"></a>Funções



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Sumário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap"><strong>CreateMappedBitmap</strong></a></td>
<td>Cria um bitmap para uso em uma barra de ferramentas. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex"><strong>CreateToolbarEx</strong></a></td>
<td>Cria uma janela de barra de ferramentas e adiciona os botões especificados à barra de ferramentas.
<blockquote>
[!Note]<br />
Essa função foi preterida, pois não oferece suporte a todos os recursos de barras de ferramentas. Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> em vez disso. Para obter exemplos, consulte <a href="using-toolbar-controls.md">usando controles da barra de ferramentas</a>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Mensagens



| Tópico                                                         | Sumário                                                                                                                                                                                                |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**rebitmap de TB \_**](tb-addbitmap.md)                         | Adiciona uma ou mais imagens à lista de imagens de botão disponíveis para uma barra de ferramentas. <br/>                                                                                                               |
| [**hiperbotãos de TB \_**](tb-addbuttons.md)                       | Adiciona um ou mais botões a uma barra de ferramentas.<br/>                                                                                                                                                       |
| [**\_caracteres ADDstring de TB**](tb-addstring.md)                         | Adiciona uma nova cadeia de caracteres ao pool de cadeias da barra de ferramentas.<br/>                                                                                                                                              |
| [**\_dimensionamento de TB**](tb-autosize.md)                           | Faz com que uma barra de ferramentas seja redimensionada. <br/>                                                                                                                                                             |
| [**TB de \_ BUTTONCOUNT**](tb-buttoncount.md)                     | Recupera uma contagem dos botões atualmente na barra de ferramentas. <br/>                                                                                                                                  |
| [**TB de \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md)           | Especifica o tamanho da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) . <br/>                                                                                                                           |
| [**TB de \_ CHANGEBITMAP**](tb-changebitmap.md)                   | Altera o bitmap de um botão em uma barra de ferramentas.<br/>                                                                                                                                                |
| [**TB de \_ CHECKBUTTON**](tb-checkbutton.md)                     | Verifica ou desmarca um determinado botão em uma barra de ferramentas.<br/>                                                                                                                                              |
| [**TB de \_ COMMANDTOINDEX**](tb-commandtoindex.md)               | Recupera o índice de base zero para o botão associado ao identificador de comando especificado. <br/>                                                                                             |
| [**personalização de TB \_**](tb-customize.md)                         | Exibe a caixa de diálogo **Personalizar barra de ferramentas** .<br/>                                                                                                                                               |
| [**TB de \_ DELETEBUTTON**](tb-deletebutton.md)                   | Exclui um botão da barra de ferramentas. <br/>                                                                                                                                                          |
| [**TB de \_ ENABLEBUTTON**](tb-enablebutton.md)                   | Habilita ou desabilita o botão especificado em uma barra de ferramentas.<br/>                                                                                                                                       |
| [**TB de \_ GETANCHORHIGHLIGHT**](tb-getanchorhighlight.md)       | Recupera a configuração de realce de âncora para uma barra de ferramentas. <br/>                                                                                                                                       |
| [**TB \_ GETbitmap**](tb-getbitmap.md)                         | Recupera o índice do bitmap associado a um botão em uma barra de ferramentas. <br/>                                                                                                                    |
| [**TB de \_ GETBITMAPFLAGS**](tb-getbitmapflags.md)               | Recupera os sinalizadores que descrevem o tipo de bitmap a ser usado.<br/>                                                                                                                             |
| [**TB \_ GETbutton**](tb-getbutton.md)                         | Recupera informações sobre o botão especificado em uma barra de ferramentas.<br/>                                                                                                                               |
| [**TB de \_ GETBUTTONINFO**](tb-getbuttoninfo.md)                 | Recupera informações estendidas para um botão em uma barra de ferramentas. <br/>                                                                                                                                   |
| [**TB \_ GETbuttons**](tb-getbuttonsize.md)                 | Recupera a largura e a altura atuais dos botões da barra de ferramentas, em pixels. <br/>                                                                                                                       |
| [**TB de \_ GETBUTTONTEXT**](tb-getbuttontext.md)                 | Recupera o texto de exibição de um botão em uma barra de ferramentas.<br/>                                                                                                                                         |
| [**TB de \_ GETCOLORSCHEME**](tb-getcolorscheme.md)               | Recupera as informações do esquema de cores do controle ToolBar. <br/>                                                                                                                            |
| [**TB de \_ GETDISABLEDIMAGELIST**](tb-getdisabledimagelist.md)   | Recupera a lista de imagens que um controle Toolbar usa para exibir botões inativos. <br/>                                                                                                           |
| [**TB \_ Extended**](tb-getextendedstyle.md)           | Recupera os estilos estendidos para um controle ToolBar. <br/>                                                                                                                                        |
| [**TB de \_ GETHOTIMAGELIST**](tb-gethotimagelist.md)             | Recupera a lista de imagens que um controle Toolbar usa para exibir botões de atalho.<br/>                                                                                                                 |
| [**TB de \_ GETHOTITEM**](tb-gethotitem.md)                       | Recupera o índice do item ativo em uma barra de ferramentas. <br/>                                                                                                                                           |
| [**TB de \_ GETIDEALSIZE**](tb-getidealsize.md)                   | Obtém o tamanho ideal da barra de ferramentas.<br/>                                                                                                                                                          |
| [**TB \_ GETimagelist**](tb-getimagelist.md)                   | Recupera a lista de imagens que um controle Toolbar usa para exibir botões em seu estado padrão. Um controle Toolbar usa essa lista de imagens para exibir botões quando eles não estão ativos ou desabilitados.<br/> |
| [**TB de \_ GETIMAGELISTCOUNT**](tb-getimagelistcount.md)         | Obtém o número de listas de imagens associadas à barra de ferramentas.<br/>                                                                                                                                  |
| [**TB de \_ GETINSERTMARK**](tb-getinsertmark.md)                 | Recupera a marca de inserção atual para a barra de ferramentas. <br/>                                                                                                                                       |
| [**TB de \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)       | Recupera a cor usada para desenhar a marca de inserção para a barra de ferramentas. <br/>                                                                                                                        |
| [**TB de \_ GETITEMDROPDOWNRECT**](tb-getitemdropdownrect.md)     | Obtém o retângulo delimitador da janela suspensa para um item da barra de ferramentas com a [**\_ lista suspensa estilo BTNS**](toolbar-control-and-button-styles.md).<br/>                                  |
| [**TB de \_ GETITEMRECT**](tb-getitemrect.md)                     | Recupera o retângulo delimitador de um botão em uma barra de ferramentas. <br/>                                                                                                                                  |
| [**TB \_ GETmaxsize**](tb-getmaxsize.md)                       | Recupera o tamanho total de todos os botões e separadores visíveis na barra de ferramentas. <br/>                                                                                                       |
| [**até TB de \_ métricas**](tb-getmetrics.md)                       | Recupera as métricas de um controle ToolBar.<br/>                                                                                                                                                  |
| [**TB \_ GETobject**](tb-getobject.md)                         | Recupera o [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para um controle ToolBar. <br/>                                                                                                                     |
| [**autopadding TB \_**](tb-getpadding.md)                       | Recupera o preenchimento de um controle ToolBar. <br/>                                                                                                                                                |
| [**TB de \_ GETPRESSEDIMAGELIST**](tb-getpressedimagelist.md)     | Obtém a lista de imagens que um controle Toolbar usa para exibir botões em um estado pressionado.<br/>                                                                                                       |
| [**TB \_ GETrect**](tb-getrect.md)                             | Recupera o retângulo delimitador para um botão de barra de ferramentas especificado. <br/>                                                                                                                            |
| [**TB \_ GETrows**](tb-getrows.md)                             | Recupera o número de linhas de botões em uma barra de ferramentas com o estilo [**TBSTYLE \_ Wrap**](toolbar-control-and-button-styles.md) . <br/>                                        |
| [**TB \_ GETstate**](tb-getstate.md)                           | Recupera informações sobre o estado do botão especificado em uma barra de ferramentas, como se ele está habilitado, pressionado ou marcado. <br/>                                                             |
| [**TB \_ GETstring**](tb-getstring.md)                         | Recupera uma cadeia de caracteres do pool de cadeias de caracteres de uma barra de ferramentas.<br/>                                                                                                                                             |
| [**um $ STYLE de TB \_**](tb-getstyle.md)                           | Recupera os estilos atualmente em uso para um controle ToolBar. <br/>                                                                                                                                |
| [**TB de \_ GETTEXTROWS**](tb-gettextrows.md)                     | Recupera o número máximo de linhas de texto que podem ser exibidas em um botão da barra de ferramentas. <br/>                                                                                                        |
| [**TB \_ GETtooltips**](tb-gettooltips.md)                     | Recupera o identificador para o controle ToolTip, se houver, associado à barra de ferramentas. <br/>                                                                                                           |
| [**TB de \_ GETUNICODEFORMAT**](tb-getunicodeformat.md)           | Recupera o sinalizador de formato de caractere Unicode para o controle. <br/>                                                                                                                                |
| [**TB de \_ HASACCELERATOR**](tb-hasaccelerator.md)               | **Destinado ao uso interno; Não recomendado para uso em aplicativos.**<br/> Recupera uma contagem de botões da barra de ferramentas que têm o caractere de acelerador especificado. <br/>                      |
| [**TB de \_ HIDEBUTTON**](tb-hidebutton.md)                       | Oculta ou mostra o botão especificado em uma barra de ferramentas.<br/>                                                                                                                                            |
| [**\_HITTEST TB**](tb-hittest.md)                             | Determina onde um ponto reside em um controle ToolBar. <br/>                                                                                                                                         |
| [**TB \_ indeterminado**](tb-indeterminate.md)                 | Define ou limpa o estado indeterminado do botão especificado em uma barra de ferramentas.<br/>                                                                                                                 |
| [**TB de \_ INSERTBUTTON**](tb-insertbutton.md)                   | Insere um botão em uma barra de ferramentas.<br/>                                                                                                                                                               |
| [**TB de \_ INSERTMARKHITTEST**](tb-insertmarkhittest.md)         | Recupera as informações de marca de inserção de um ponto em uma barra de ferramentas. <br/>                                                                                                                          |
| [**TB de \_ ISBUTTONCHECKED**](tb-isbuttonchecked.md)             | Determina se o botão especificado em uma barra de ferramentas está marcado. <br/>                                                                                                                            |
| [**TB de \_ ISBUTTONENABLED**](tb-isbuttonenabled.md)             | Determina se o botão especificado em uma barra de ferramentas está habilitado. <br/>                                                                                                                            |
| [**TB de \_ ISBUTTONHIDDEN**](tb-isbuttonhidden.md)               | Determina se o botão especificado em uma barra de ferramentas está oculto. <br/>                                                                                                                             |
| [**TB de \_ ISBUTTONHIGHLIGHTED**](tb-isbuttonhighlighted.md)     | Verifica o estado de realce de um botão da barra de ferramentas. <br/>                                                                                                                                             |
| [**TB de \_ ISBUTTONINDETERMINATE**](tb-isbuttonindeterminate.md) | Determina se o botão especificado em uma barra de ferramentas é indeterminado. <br/>                                                                                                                      |
| [**TB de \_ ISBUTTONPRESSED**](tb-isbuttonpressed.md)             | Determina se o botão especificado em uma barra de ferramentas é pressionado. <br/>                                                                                                                            |
| [**TB de \_ imagens**](tb-loadimages.md)                       | Carrega imagens de botão definidas pelo sistema em uma lista de imagens de controle da barra de ferramentas.<br/>                                                                                                                      |
| [**TB de \_ MAPACCELERATOR**](tb-mapaccelerator.md)               | Determina a ID do botão que corresponde ao caractere de acelerador especificado.<br/>                                                                                                     |
| [**TB de \_ MARKBUTTON**](tb-markbutton.md)                       | Define o estado de realce de um determinado botão em um controle ToolBar.<br/>                                                                                                                             |
| [**TB de \_ MOVEBUTTON**](tb-movebutton.md)                       | Move um botão de um índice para outro. <br/>                                                                                                                                                   |
| [**TB de \_ PRESSBUTTON**](tb-pressbutton.md)                     | Pressiona ou libera o botão especificado em uma barra de ferramentas.<br/>                                                                                                                                       |
| [**TB de \_ REPLACEBITMAP**](tb-replacebitmap.md)                 | Substitui um bitmap existente por um novo bitmap.<br/>                                                                                                                                               |
| [**TB de \_ SAVERESTORE**](tb-saverestore.md)                     | Envie esta mensagem para iniciar o salvamento ou a restauração de um estado da barra de ferramentas.<br/>                                                                                                                           |
| [**TB de \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)       | Define a configuração de realce de âncora para uma barra de ferramentas. <br/>                                                                                                                                            |
| [**TB de \_ SETBITMAPSIZE**](tb-setbitmapsize.md)                 | Define o tamanho das imagens de bitmap a serem adicionadas a uma barra de ferramentas. <br/>                                                                                                                             |
| [**TB de \_ SETBOUNDINGSIZE**](tb-setboundingsize.md)             | **Destinado ao uso interno; Não recomendado para uso em aplicativos.**<br/> Define o tamanho delimitador para um controle de barra de ferramentas de várias colunas. <br/>                                               |
| [**TB de \_ SETBUTTONINFO**](tb-setbuttoninfo.md)                 | Define as informações de um botão existente em uma barra de ferramentas.<br/>                                                                                                                                    |
| [**TB \_ SETbuttonse**](tb-setbuttonsize.md)                 | Define o tamanho dos botões em uma barra de ferramentas.<br/>                                                                                                                                                       |
| [**TB de \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md)               | Define as larguras mínima e máxima do botão no controle da barra de ferramentas.<br/>                                                                                                                           |
| [**TB de \_ SETCMDID**](tb-setcmdid.md)                           | Define o identificador de comando de um botão da barra de ferramentas. <br/>                                                                                                                                            |
| [**TB de \_ SETCOLORSCHEME**](tb-setcolorscheme.md)               | Define as informações do esquema de cores para o controle ToolBar. <br/>                                                                                                                                  |
| [**TB de \_ SETDISABLEDIMAGELIST**](tb-setdisabledimagelist.md)   | Define a lista de imagens que o controle Toolbar usará para exibir botões desabilitados. <br/>                                                                                                          |
| [**TB de \_ SETDRAWTEXTFLAGS**](tb-setdrawtextflags.md)           | Define os sinalizadores de desenho de texto para a barra de ferramentas. <br/>                                                                                                                                                |
| [**TB \_ SETextendedattribute**](tb-setextendedstyle.md)           | Define os estilos estendidos para um controle ToolBar. <br/>                                                                                                                                             |
| [**TB de \_ SETHOTIMAGELIST**](tb-sethotimagelist.md)             | Define a lista de imagens que o controle Toolbar usará para exibir botões quentes.<br/>                                                                                                                |
| [**TB de \_ SETHOTITEM**](tb-sethotitem.md)                       | Define o item ativo em uma barra de ferramentas.<br/>                                                                                                                                                              |
| [**TB de \_ SETHOTITEM2**](tb-sethotitem2.md)                     | Define o item ativo em uma barra de ferramentas.<br/>                                                                                                                                                              |
| [**TB \_ SETimagelist**](tb-setimagelist.md)                   | Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em seu estado padrão.<br/>                                                                                                |
| [**Recortar TB \_**](tb-setindent.md)                         | Define o recuo para o primeiro botão em um controle ToolBar. <br/>                                                                                                                             |
| [**TB de \_ SETINSERTMARK**](tb-setinsertmark.md)                 | Define a marca de inserção atual para a barra de ferramentas. <br/>                                                                                                                                            |
| [**TB de \_ SETINSERTMARKCOLOR**](tb-setinsertmarkcolor.md)       | Define a cor usada para desenhar a marca de inserção para a barra de ferramentas. <br/>                                                                                                                             |
| [**TB de \_ SETLISTGAP**](tb-setlistgap.md)                       | Define a distância entre os botões da barra de ferramentas em uma barra de ferramentas específica.<br/>                                                                                                                         |
| [**TB de \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md)               | Define o número máximo de linhas de texto exibidas em um botão da barra de ferramentas. <br/>                                                                                                                         |
| [**TB de \_ métricas**](tb-setmetrics.md)                       | Define as métricas de um controle ToolBar.<br/>                                                                                                                                                       |
| [**TB \_ SETpadding**](tb-setpadding.md)                       | Define o preenchimento de um controle ToolBar.<br/>                                                                                                                                                      |
| [**TB \_ SETpai**](tb-setparent.md)                         | Define a janela à qual o controle Toolbar envia códigos de notificação. <br/>                                                                                                                      |
| [**TB de \_ SETPRESSEDIMAGELIST**](tb-setpressedimagelist.md)     | Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em um estado pressionado.<br/>                                                                                                    |
| [**SetRows de TB \_**](tb-setrows.md)                             | Define o número de linhas de botões em uma barra de ferramentas.<br/>                                                                                                                                             |
| [**TB \_ SETstate**](tb-setstate.md)                           | Define o estado do botão especificado em uma barra de ferramentas.<br/>                                                                                                                                        |
| [**TB \_ SETstyle**](tb-setstyle.md)                           | Define o estilo de um controle ToolBar. <br/>                                                                                                                                                       |
| [**TB \_ SETtooltips**](tb-settooltips.md)                     | Associa um controle ToolTip a uma barra de ferramentas. <br/>                                                                                                                                                |
| [**TB de \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)           | Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle. <br/>    |
| [**TB de \_ SETWINDOWTHEME**](tb-setwindowtheme.md)               | Define o estilo visual de um controle ToolBar.<br/>                                                                                                                                                  |
| [**de TB \_ TRANSLATEACCELERATOR**](tb-translateaccelerator.md)   | Passa uma mensagem de teclado para a barra de ferramentas.<br/>                                                                                                                                                    |



 

### <a name="notifications"></a>Notificações



| Tópico                                                            | Sumário                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ Char (barra de ferramentas)](nm-char-toolbar.md)                        | Enviado pela barra de ferramentas quando recebe uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                       |
| [Clique no NM \_ (barra de ferramentas)](nm-click-toolbar.md)                      | Enviado por um controle Toolbar quando o usuário clica em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                     |
| [NM \_ CUSTOMDRAW (barra de ferramentas)](nm-customdraw-toolbar.md)            | Enviado pela barra de ferramentas para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                              |
| [NM \_ DBLCLK (barra de ferramentas)](nm-dblclk-toolbar.md)                    | Notifica a janela pai de um controle ToolBar que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                             |
| [NM \_ KEYDOWN (barra de ferramentas)](nm-keydown-toolbar.md)                  | Enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                 |
| [\_LDOWN nm](nm-ldown-toolbar.md)                                | Notifica uma janela pai da barra de ferramentas que o botão esquerdo do mouse foi pressionado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                        |
| [NM \_ RCLICK (barra de ferramentas)](nm-rclick-toolbar.md)                    | Enviado por um controle Toolbar quando o usuário clica na barra de ferramentas com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                |
| [NM \_ RDBLCLK (barra de ferramentas)](nm-rdblclk-toolbar.md)                  | Notifica uma janela pai do controle que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                         |
| [NM \_ RELEASEDCAPTURE (barra de ferramentas)](nm-releasedcapture-toolbar-.md) | Notifica uma janela pai do controle da barra de ferramentas que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                               |
| [NM \_ TOOLTIPSCREATED (barra de ferramentas)](nm-tooltipscreated-toolbar-.md) | Notifica uma janela pai da barra de ferramentas que a barra de ferramentas criou um controle ToolTip. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                    |
| [TBN \_ BEGINADJUST](tbn-beginadjust.md)                          | Notifica uma janela pai da barra de ferramentas que o usuário iniciou a personalização de uma barra de ferramentas. Esse código de mensagem é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                          |
| [TBN \_ BEGINDRAG](tbn-begindrag.md)                              | Notifica uma janela pai da barra de ferramentas que o usuário começou a arrastar um botão em uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                            |
| [TBN \_ CUSTHELP](tbn-custhelp.md)                                | Notifica uma janela pai da barra de ferramentas de que o usuário escolheu o botão ajuda na caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                       |
| [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md)                    | Enviado por um controle Toolbar quando um botão está prestes a ser excluído. <br/>                                                                                                                                                                                                                                                |
| [arrastar e TBN \_](tbn-dragout.md)                                  | Enviado por um controle Toolbar quando o usuário clica em um botão e, em seguida, move o cursor para fora do botão. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                     |
| [TBN \_ DRAGOVER](tbn-dragover.md)                                | Asseguro se uma mensagem [**\_ MARKBUTTON TB**](tb-markbutton.md) deve ser enviada para um botão que está sendo arrastado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                           |
| [\_lista suspensa tbn](tbn-dropdown.md)                                | Enviado por um controle Toolbar quando o usuário clica em um botão suspenso. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                                     |
| [TBN \_ DUPACCELERATOR](tbn-dupaccelerator.md)                    | Asseguro se uma tecla aceleradora pode ser usada em duas ou mais barras de ferramentas ativas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                      |
| [TBN \_ ENDajuste](tbn-endadjust.md)                              | Notifica uma janela pai da barra de ferramentas de que o usuário parou de personalizar uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                   |
| [TBN \_ ENDarrastar](tbn-enddrag.md)                                  | Notifica a janela pai da barra de ferramentas que o usuário parou de arrastar um botão em uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                        |
| [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)                      | Recupera informações de personalização da barra de ferramentas e notifica a janela pai da barra de ferramentas sobre quaisquer alterações feitas na barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                        |
| [TBN \_ GETDISPINFO](tbn-getdispinfo.md)                          | Recupera informações de exibição de um item da barra de ferramentas. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                                                           |
| [TBN \_ GETINFOTIP](tbn-getinfotip.md)                            | Recupera informações de InfoTip para um item da barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                                                      |
| [GetObject TBN \_](tbn-getobject.md)                              | Enviado por um controle ToolBar que usa o estilo [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) para solicitar um objeto de destino drop quando o ponteiro passa sobre um de seus botões. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/> |
| [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)                      | Enviado por um controle Toolbar quando o item quente (realçado) é alterado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                                    |
| [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md)                      | Notifica uma janela pai da barra de ferramentas que a personalização foi iniciada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                                       |
| [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md)                    | Solicita o índice do botão na barra de ferramentas correspondente ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                  |
| [TBN \_ QUERYDELETE](tbn-querydelete.md)                          | Notifica a janela pai da barra de ferramentas se um botão pode ser excluído de uma barra de ferramentas enquanto o usuário estiver personalizando a barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                        |
| [TBN \_ QUERYINSERT](tbn-queryinsert.md)                          | Notifica a janela pai da barra de ferramentas se um botão pode ser inserido à esquerda do botão especificado enquanto o usuário estiver personalizando uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                     |
| [redefinição de TBN \_](tbn-reset.md)                                      | Notifica a janela pai da barra de ferramentas que o usuário redefiniu o conteúdo da caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                          |
| [TBN \_ restauração](tbn-restore.md)                                  | Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está em processo de restauração. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                 |
| [TBN \_ salvar](tbn-save.md)                                        | Notifica uma janela pai da barra de ferramentas que uma barra de ferramentas está sendo salva. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                    |
| [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md)                      | Notifica a janela pai da barra de ferramentas que o usuário personalizou uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) . <br/>                                                                                                                                          |
| [TBN \_ WRAPACCELERATOR](tbn-wrapaccelerator.md)                  | Solicita o índice do botão em uma ou mais barras de ferramentas correspondentes ao caractere de acelerador especificado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                         |
| [TBN \_ WRAPHOTITEM](tbn-wraphotitem.md)                          | Notifica um aplicativo com duas ou mais barras de ferramentas que o item ativo está prestes a alterar. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .<br/>                                                                                                                                |



 

### <a name="structures"></a>Estruturas



| Tópico                                      | Sumário                                                                                                                                                                                                                                                                |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLORMAP**](/windows/desktop/api/Commctrl/ns-commctrl-colormap)               | Contém informações usadas pela função [**CreateMappedBitmap**](/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap) para mapear as cores do bitmap. <br/>                                                                                                                                 |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)   | Contém informações específicas para um código de notificação [nm \_ CUSTOMDRAW](nm-customdraw-toolbar.md) enviado por um controle ToolBar. <br/>                                                                                                                                |
| [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)       | Contém e recebe informações de exibição de um item da barra de ferramentas. Essa estrutura é usada com o código de notificação [tbn \_ GETDISPINFO](tbn-getdispinfo.md) . <br/>                                                                                                    |
| [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa)   | Contém e recebe informações de InfoTip para um item da barra de ferramentas. Essa estrutura é usada com o código de notificação [tbn \_ GETINFOTIP](tbn-getdispinfo.md) . <br/>                                                                                                     |
| [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)         | Contém informações usadas com o código de notificação [tbn \_ HOTITEMCHANGE](tbn-hotitemchange.md) . <br/>                                                                                                                                                           |
| [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)         | Permite que os aplicativos extraiam as informações que foram colocadas em [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) quando o estado da barra de ferramentas foi salvo. Essa estrutura é passada para aplicativos quando eles recebem um código de notificação de [ \_ restauração tbn](tbn-restore.md) .<br/>             |
| [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)               | Essa estrutura é passada para aplicativos quando eles recebem um código de notificação de [ \_ salvamento de tbn](tbn-save.md) . Ele contém informações sobre o botão que está sendo salvo no momento. Os aplicativos podem modificar os valores dos membros para salvar informações adicionais. <br/> |
| [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)             | Contém informações usadas para processar códigos de notificação da barra de ferramentas. Essa estrutura substitui a estrutura **TBNOTIFY** . <br/>                                                                                                                                      |
| [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)         | Adiciona um bitmap que contém imagens de botão a uma barra de ferramentas.<br/>                                                                                                                                                                                                      |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)               | Contém informações sobre um botão em uma barra de ferramentas.<br/>                                                                                                                                                                                                            |
| [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)       | Contém ou recebe informações de um botão específico em uma barra de ferramentas.<br/>                                                                                                                                                                                         |
| [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)       | Contém informações sobre a marca de inserção em um controle ToolBar. <br/>                                                                                                                                                                                            |
| [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics)             | Define as métricas de uma barra de ferramentas que são usadas para reduzir ou expandir itens da barra de ferramentas.<br/>                                                                                                                                                                            |
| [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) | Usado com a mensagem [**TB \_ REPLACEBITMAP**](tb-replacebitmap.md) para substituir um bitmap de barra de ferramentas por outro.<br/>                                                                                                                                              |
| [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)       | Especifica o local no registro em que a mensagem [**TB \_ SAVERESTORE**](tb-saverestore.md) armazena e recupera informações sobre o estado de uma barra de ferramentas. <br/>                                                                                           |



 

### <a name="constants"></a>Constantes



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Sumário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="toolbar-button-states.md">Estados de botão da barra de ferramentas</a></td>
<td>Esta seção lista os Estados que um botão de barra de ferramentas pode ter. <br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-control-and-button-styles.md">Controle da barra de ferramentas e estilos de botão</a></td>
<td>Os estilos de janela a seguir são específicos para barras de ferramentas. Eles são combinados com outros estilos de janela quando a barra de ferramentas é criada.<br/> <strong>Observação</strong> Para os controles comuns <a href="common-control-versions.md">versão 6, 0</a>, se um <a href="themes-overview.md">estilo visual</a> estiver sendo usado com a barra de ferramentas, os botões sempre serão transparentes, independentemente da configuração de estilo. Caso contrário, o comportamento de transparência é normal, conforme indicado pelo uso do <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_FLAT</strong></a> ou do estilo de <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_TRANSPARENT</strong></a> .
<blockquote>
[!Note]<br />
O Comctl32.dll versão 6 não é redistribuível, mas está incluído no Windows ou posterior. Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="toolbar-extended-styles.md">Estilos estendidos da barra de ferramentas</a></td>
<td>Esta seção lista os estilos estendidos com suporte pelos controles da barra de ferramentas.<br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-standard-button-image-index-values.md">Valores de índice da imagem do botão padrão da barra de ferramentas</a></td>
<td>Esta seção especifica valores de índice de imagens em bitmaps padrão.<br/></td>
</tr>
</tbody>
</table>



 

