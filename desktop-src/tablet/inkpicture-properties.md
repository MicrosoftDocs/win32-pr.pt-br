---
description: Esta seção contém propriedades para o controle InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Propriedades de InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663164"
---
# <a name="inkpicture-properties"></a>Propriedades de InkPicture

Esta seção contém propriedades para o controle InkPicture.



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
<td>Obtém ou define um valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> redesenha quando a janela é invalidada (se o objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> atualmente associado ao controle InkPicture é redesenhado automaticamente quando a janela associada ao InkPicture recebe uma mensagem de WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Fundo</strong></a></td>
<td>Obtém ou define a cor do plano de fundo do controle <a href="inkpicture-control-reference.md">InkPicture</a> . A cor do plano de fundo padrão é a cor do plano de fundo da janela do sistema, que normalmente é branca.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propriedade CollectingInk</strong></a></td>
<td>Obtém o valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> está coletando tinta (somente tempo de execução).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></td>
<td>Obtém ou define o modo de coleta que determina se a tinta, os gestos ou a tinta e os gestos são reconhecidos conforme o usuário escreve.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Propriedade Cursors</strong></a></td>
<td>Obtém a coleção <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponível para uso na região de tinta do controle <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
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
<td>Obtém ou define a descrição do pacote do controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propriedade DynamicRendering</strong></a></td>
<td>Obtém ou define o valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> renderiza dinamicamente a tinta conforme ela é coletada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Obtém ou define um valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> está no modo de tinta, no modo de exclusão ou no modo de seleção/edição.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>habilitado</strong></a></td>
<td>Obtém ou define um valor que determina se o controle <a href="inkpicture-control-reference.md">InkPicture</a> pode responder a eventos gerados pelo usuário.<br/>
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
<td>Obtém o identificador de janela ao qual o controle <a href="inkpicture-control-reference.md">InkPicture</a> está associado. (somente tempo de execução)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Tinta</strong></a></td>
<td>Obtém ou define o objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associado ao controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Obtém ou define um valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> coleta entrada de caneta (pacotes no ar, cursor em eventos de intervalo e assim por diante).<br/></td>
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
<td>Obtém ou define um valor que indica o tipo de ponteiro do mouse que aparece quando o mouse está sobre uma parte específica do controle <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagem</strong></a></td>
<td>Obtém o arquivo de gráficos para aparecer no controle <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Propriedade do renderizador</strong></a></td>
<td>Obtém ou define o objeto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> usado para desenhar tinta no controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Seleção</strong></a></td>
<td>Obtém a coleção <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> selecionada no momento dentro do controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).<br/></td>
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
<td>Obtém o objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> que o controle <a href="inkpicture-control-reference.md">InkPicture</a> está usando atualmente para coletar a entrada.<br/></td>
</tr>
</tbody>
</table>



 

