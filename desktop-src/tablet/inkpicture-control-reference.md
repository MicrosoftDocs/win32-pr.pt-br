---
description: O controle InkPicture fornece a capacidade de inserir uma imagem em um aplicativo e permitir que os usuários adicionem tinta sobre ela.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: Referência de controle InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8caaf1970394338f858cd0fdff0dab58153f53b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922840"
---
# <a name="inkpicture-control-reference"></a>Referência de controle InkPicture

O controle InkPicture fornece a capacidade de inserir uma imagem em um aplicativo e permitir que os usuários adicionem tinta sobre ela. Ele destina-se a cenários em que a tinta não é reconhecida como texto, mas é armazenada como tinta.

O controle InkPicture pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

> [!Note]  
> O controle InkPicture não está marcado como seguro para scripts. O controle InkPicture não deve ser usado em páginas HTML ou ASP.NET.

 

Criar o controle InkPicture por trás de um controle transparente (como uma GroupBox com o \_ conjunto de propriedades de WS ex \_ Transparent) impedirá o InkPicture de coletar tinta.

## <a name="members"></a>Membros



| Enumeração                                      | Descrição                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InkPictureSizeMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Define os valores que especificam como a imagem de plano de fundo se comporta dentro do controle InkPicture.<br/> |



 



| Evento                                                                              | Descrição                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | Preterido.<br/>                                                                                                                                                                                                                                                                                             |
| [**Clicar**](inkpicture-click.md)                                                  | Ocorre quando um usuário clica no controle InkPicture.<br/>                                                                                                                                                                                                                                                       |
| [**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)                      | Ocorre quando o controle [**InkCollector**](inkcollector-class.md) detecta um objeto [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) que está inativo.<br/>                                                                                                                                                         |
| [**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)                          | Ocorre quando o controle InkPicture detecta um [**IInkCursorButton**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) que está ativo.<br/>                                                                                                                                                                                                  |
| [**Evento CursorDown**](inkpicture-cursordown.md)                                  | Ocorre quando a dica de cursor entra na superfície do Tablet de digitalização.<br/>                                                                                                                                                                                                                                      |
| [**Evento CursorInRange**](inkpicture-cursorinrange.md)                            | Ocorre quando um cursor entra no intervalo de detecção física (proximidade) do contexto do Tablet.<br/>                                                                                                                                                                                                             |
| [**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)                      | Ocorre quando o cursor sai do intervalo de detecção física (proximidade) do contexto do Tablet.<br/>                                                                                                                                                                                                           |
| [**DblClick**](inkpicture-dblclick.md)                                            | Ocorre quando o controle InkPicture é clicado duas vezes.<br/> Esse método de evento é definido na interface **\_ IInkPictureEvents** . A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEDblClick DISPID.<br/> |
| [**Evento de gesto**](inkpicture-gesture.md)                                        | Ocorre quando um gesto de aplicativo é reconhecido.<br/>                                                                                                                                                                                                                                                       |
| [**Controle InkPicture de evento KeyDown \[\]**](inkpicture-keydown.md)                 | Ocorre quando uma tecla é pressionada e na posição para baixo enquanto o controle InkPicture tem foco.<br/>                                                                                                                                                                                                           |
| [**Controle InkPicture de evento KeyPress \[\]**](inkpicture-keypress.md)                | Ocorre quando uma tecla é pressionada enquanto o controle InkPicture tem foco.<br/>                                                                                                                                                                                                                                    |
| [**Controle InkPicture de evento KeyUp \[\]**](inkpicture-keyup.md)                     | Ocorre quando uma tecla é liberada enquanto o controle InkPicture tem foco.<br/>                                                                                                                                                                                                                                   |
| [**Controle InkPicture de evento MouseDown \[\]**](inkpicture-mousedown.md)             | Ocorre quando o ponteiro do mouse está sobre o controle InkPicture e um botão do mouse é pressionado.<br/>                                                                                                                                                                                                             |
| [**MouseEnter**](inkpicture-mouseenter.md)                                        | Ocorre quando o ponteiro do mouse entra no controle InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**MouseHover**](inkpicture-mousehover.md)                                        | Ocorre quando o ponteiro do mouse passa sobre o controle InkPicture.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Ocorre quando o ponteiro do mouse sai do controle InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**Controle InkPicture de evento MouseMove \[\]**](inkpicture-mousemove.md)             | Ocorre quando o ponteiro do mouse é movido sobre o controle InkPicture.<br/>                                                                                                                                                                                                                                     |
| [**Controle de evento InkPicture de MouseUp \[\]**](inkpicture-mouseup.md)                 | Ocorre quando o ponteiro do mouse está sobre o controle InkPicture e um botão do mouse é liberado.<br/>                                                                                                                                                                                                            |
| [**MouseWheel**](inkpicture-mousewheel.md)                                        | Ocorre quando a roda do mouse se move enquanto o controle InkPicture tem foco.<br/>                                                                                                                                                                                                                               |
| [**Evento NewInAirPackets**](inkpicture-newinairpackets.md)                        | Ocorre quando um pacote no ar é visto.<br/>                                                                                                                                                                                                                                                                   |
| [**Evento NewPackets**](inkpicture-newpackets.md)                                  | Ocorre quando o controle InkPicture recebe um pacote.<br/>                                                                                                                                                                                                                                                   |
| [**Pintado**](inkpicture-painted.md)                                              | Ocorre quando o controle InkPicture conclui a redesenho de si mesmo.<br/>                                                                                                                                                                                                                                      |
| [**Pintura**](inkpicture-painting.md)                                            | Ocorre antes de o controle InkPicture ser redesenhado.<br/>                                                                                                                                                                                                                                                    |
| [**Redimensionar**](inkpicture-resize.md)                                                | Ocorre quando o controle InkPicture é redimensionado.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Ocorre quando a seleção de texto dentro do controle InkPicture é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                    |
| [**SelectionChanging**](inkpicture-selectionchanging.md)                          | Ocorre quando a seleção de texto dentro do controle InkPicture está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                             |
| [**SelectionMoved**](inkpicture-selectionmoved.md)                                | Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                  |
| [**Controle InkPicture de evento SelectionMoving \[\]**](inkpicture-selectionmoving.md) | Ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                           |
| [**SelectionResized**](inkpicture-selectionresized.md)                            | Ocorre quando o tamanho da seleção atual é alterado, por exemplo, por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                      |
| [**SelectionResizing**](inkpicture-selectionresizing.md)                          | Ocorre quando o tamanho da seleção atual está prestes a ser alterado, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Ocorre depois que o controle InkPicture é redimensionado, especificamente, depois que o valor da propriedade [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) ou [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) é alterado.<br/>                                                                                                      |
| [**Modotamanhochanged**](inkpicture-sizemodechanged.md)                              | Ocorre depois que a propriedade [**ModoTamanho**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) do controle InkPicture é alterada.<br/>                                                                                                                                                                                           |
| **Estilochanged**                                                                   | Não implementado.<br/>                                                                                                                                                                                                                                                                                        |
| [**Pincel**](inkpicture-stroke.md)                                                | Ocorre quando o usuário desenha um novo traço em qualquer mesa digitalizadora.<br/>                                                                                                                                                                                                                                                  |
| [**StrokesDeleted**](inkpicture-strokesdeleted.md)                                | Ocorre após a exclusão dos objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                        |
| [**StrokesDeleting**](inkpicture-strokesdeleting.md)                              | Ocorre antes de os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                             |
| [**SystemColorsChanged**](inkpicture-systemcolorschanged.md)                      | Ocorre após a alteração das cores do sistema.<br/>                                                                                                                                                                                                                                                                  |
| [**SystemGesture**](inkpicture-systemgesture.md)                                  | Ocorre quando um gesto do sistema é reconhecido.<br/>                                                                                                                                                                                                                                                             |
| [**Evento TabletAdded**](inkpicture-tabletadded.md)                                | Ocorre quando um Tablet é adicionado ao sistema.<br/>                                                                                                                                                                                                                                                            |
| [**Evento TabletRemoved**](inkpicture-tabletremoved.md)                            | Ocorre quando um Tablet é removido do sistema.<br/>                                                                                                                                                                                                                                                        |



 



| Método                                                                                   | Descrição                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Método GetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Retorna um valor que indica se o controle InkPicture tem interesse em um evento específico.<br/>                                                                   |
| [**GetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Retorna um valor que indica se o controle InkPicture tem interesse em um gesto de aplicativo específico.<br/>                                                     |
| [**Método GetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Retorna o retângulo da janela, em pixels, no qual a tinta é desenhada.<br/>                                                                                                 |
| [**HitTestSelection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Retorna um membro da enumeração [**SelectionHitResult**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) , que especifica qual parte de uma seleção, se houver, foi atingida durante um teste de clique.<br/> |
| [**Método SetAllTabletsMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Permite que o controle InkPicture colete tinta de qualquer Tablet conectado ao Tablet PC.<br/>                                                                            |
| [**Método SetEventInterest**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Define um valor que indica se um controle InkPicture tem interesse em um evento especificado.<br/>                                                                        |
| SetFocus                                                                                 | Move o foco para o controle InkPicture.<br/>                                                                                                                          |
| [**Método SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Define o interesse do objeto InkPicture em um gesto de aplicativo especificado.<br/>                                                                                      |
| [**Método SetSingleTabletIntegratedMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Define o controle InkPicture para coletar tinta de apenas um Tablet anexado ao Tablet PC. A tinta de outros tablets é ignorada.<br/>                                       |
| [**Método SetWindowInputRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Especifica o retângulo da janela a ser definido, em coordenadas da janela, dentro da qual a tinta é desenhada.<br/>                                                                            |
| ShowWhatsThis                                                                            | Exibe um tópico selecionado em um arquivo de ajuda usando o pop-up "o que é isto" fornecido pela ajuda em sistemas operacionais Microsoft Windows de 32 bits (somente em tempo de Design).<br/>           |
| ZOrder                                                                                   | Coloca o controle na frente ou atrás da ordem z em seu nível gráfico (somente no tempo de Design).<br/>                                                               |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Propriedade de redesenhot</strong></a></td>
<td>Obtém ou define um valor que especifica se o controle InkPicture redesenha quando a janela é invalidada (se o objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> atualmente associado ao controle InkPicture é redesenhado automaticamente quando a janela associada ao InkPicture recebe uma mensagem de WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Fundo</strong></a></td>
<td>Obtém ou define a cor do plano de fundo do controle InkPicture. A cor do plano de fundo padrão é a cor do plano de fundo da janela do sistema, que normalmente é branca.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propriedade CollectingInk</strong></a></td>
<td>Obtém o valor que especifica se o controle InkPicture está coletando tinta (somente tempo de execução).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>Obtém ou define o modo de coleta que determina se a tinta, os gestos ou a tinta e os gestos são reconhecidos conforme o usuário escreve.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Propriedade Cursors</strong></a></td>
<td>Obtém a coleção <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponível para uso na região de tinta do controle InkPicture.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></td>
<td>Obtém a coleção <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> a ser persistida com a tinta (somente no tempo de Design).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propriedade DefaultDrawingAttributes</strong></a></td>
<td>Obtém ou define a coleção de <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> padrão a ser usada ao desenhar e exibir tinta (somente tempo de execução).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propriedade DesiredPacketDescription</strong></a></td>
<td>Obtém ou define a descrição do pacote do controle InkPicture (somente tempo de execução).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propriedade DynamicRendering</strong></a></td>
<td>Obtém ou define o valor que especifica se o controle InkPicture renderiza dinamicamente a tinta conforme ela é coletada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Obtém ou define um valor que especifica se o controle InkPicture está no modo de tinta, no modo de exclusão ou no modo de seleção/edição.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>habilitado</strong></a></td>
<td>Obtém ou define um valor que determina se o controle InkPicture pode responder a eventos gerados pelo usuário.<br/>
<blockquote>
[!Note]<br />
Essa propriedade é equivalente à propriedade <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>Obtém ou define o valor que especifica se a tinta é apagada por traço ou por ponto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>Obtém ou define o valor que especifica a largura da dica de caneta do apagador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></td>
<td>Obtém o identificador de janela ao qual o controle InkPicture está associado. (somente tempo de execução)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Tinta</strong></a></td>
<td>Obtém ou define o objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associado ao controle InkPicture (somente tempo de execução).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Obtém ou define um valor que especifica se o controle InkPicture coleta entrada de caneta (pacotes no ar, cursor em eventos de intervalo e assim por diante).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propriedade MarginX</strong></a></td>
<td>Obtém ou define a margem do eixo x em volta do retângulo da janela em coordenadas da tela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Propriedade MarginY</strong></a></td>
<td>Obtém ou define a margem do eixo y em relação ao retângulo da janela em coordenadas da tela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propriedade MouseIcon</strong></a></td>
<td>Obtém ou define o ícone de mouse personalizado atual.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Propriedade MousePointer</strong></a></td>
<td>Obtém ou define um valor que indica o tipo de ponteiro do mouse que aparece quando o mouse está sobre uma parte específica do controle InkPicture.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagem</strong></a></td>
<td>Obtém o arquivo de gráficos para aparecer no controle InkPicture.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Propriedade do renderizador</strong></a></td>
<td>Obtém ou define o objeto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> usado para desenhar tinta no controle InkPicture (somente tempo de execução).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Seleção</strong></a></td>
<td>Obtém a coleção <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> selecionada no momento dentro do controle InkPicture (somente tempo de execução).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></td>
<td>Obtém ou define como o controle manipula o posicionamento e o dimensionamento da imagem.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propriedade SupportHighContrastInk</strong></a></td>
<td>Obtém um valor que especifica se a tinta é renderizada como apenas uma cor, cor = COLOR_WINDOWTEXT (da chamada GetSystemMetrics) quando o sistema está no modo de Alto Contraste.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>Obtém ou define um valor que especifica se todas as interfaces de usuário de seleção (caixa delimitadora de seleção e identificadores de seleção) são desenhadas em alto contraste quando o sistema está no modo de Alto Contraste.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propriedade do Tablet</strong></a></td>
<td>Obtém o objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> que o controle InkPicture está usando atualmente para coletar a entrada.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

A interface do usuário de tempo de execução para o controle InkPicture é uma janela com um plano de fundo opaco (cor única, plano de fundo de imagem ou ambos) que contém tinta opaca.

Você pode usar o controle InkPicture para renderizar tinta no Microsoft Windows 2000, no Windows Server 2003, em qualquer edição do Windows XP que não seja o Windows XP Tablet PC Edition e qualquer versão do Windows Vista. No entanto, você pode inserir tinta, aceitar gestos ou reconhecer manuscrito somente sob as seguintes condições:

-   A tinta pode ser inserida e reconhecida se o Windows Vista ou o XP Tablet PC Edition 2005 estiver instalado.
-   Os gestos também podem ser reconhecidos.
-   O manuscrito poderá ser reconhecido como texto se o manuscrito tiver sido originado em computadores que executam versões anteriores do Windows, desde que os reconhecedores estejam presentes.

Se você usar o Windows 2000, o Windows Server 2003, qualquer edição do Windows XP que não seja o Windows XP Tablet PC Edition 2005, poderá atribuir valores às propriedades de ambiente do controle InkPicture e, em seguida, copiar e colar a tinta em outros aplicativos. No entanto, o valor de sua propriedade InkEnabled será sempre **false**.

Objetos [**InkDisp**](inkdisp-class.md) persistentes podem ser carregados e exibidos em todas as edições do Windows Vista e XP e em sistemas que têm apenas o SDK (Software Development Kit) do Windows XP Tablet PC Edition instalado. Os objetos **InkDisp** só podem ser convertidos em texto (reconhecido), se o Windows Vista ou o Windows XP Tablet PC Edition 2005 estiver instalado.

Se as operações nesse controle não tiverem sucesso, um HRESULT legal será retornado. Se as condições de erro resultarem, verifique o HRESULT retornado em relação ao erro.

Para obter mais informações sobre controles de tinta, consulte [Ink](ink-controls.md).

Para obter informações sobre quais threads geram eventos específicos, consulte [threads nos quais um evento pode ser acionado](threads-on-which-an-event-can-fire.md).

Para melhorar o desempenho do aplicativo, descarte manualmente um controle InkPicture quando ele não for mais necessário.

> [!Note]  
> Quando um controle InkPicture é sobreposto com outro controle, como uma **GroupBox** definida como transparente, o InkPicture não coletará tinta. O InkPicture deve ser o controle mais alto na ordem Z ou deve ser um filho da **GroupBox**.

 

## <a name="com-implementation"></a>Implementação COM

Esse objeto implementa a interface com do **IInkPicture** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Classe InkOverlay**](inkoverlay-class.md)
</dt> </dl>

