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
# <a name="inkpicture-properties"></a><span data-ttu-id="06b73-103">Propriedades de InkPicture</span><span class="sxs-lookup"><span data-stu-id="06b73-103">InkPicture Properties</span></span>

<span data-ttu-id="06b73-104">Esta seção contém propriedades para o controle InkPicture.</span><span class="sxs-lookup"><span data-stu-id="06b73-104">This section contains Properties for the InkPicture Control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06b73-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="06b73-105">Property</span></span></th>
<th><span data-ttu-id="06b73-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="06b73-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06b73-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Propriedade de redesenhot</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-108">Obtém ou define um valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> redesenha quando a janela é invalidada (se o objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> atualmente associado ao controle InkPicture é redesenhado automaticamente quando a janela associada ao InkPicture recebe uma mensagem de WM_PAINT).</span><span class="sxs-lookup"><span data-stu-id="06b73-108">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control repaints when the window is invalidated (whether the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object currently associated with InkPicture control is automatically redrawn when the window associated with the InkPicture receives a WM_PAINT message).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Fundo</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span></span></td>
<td><span data-ttu-id="06b73-110">Obtém ou define a cor do plano de fundo do controle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="06b73-110">Gets or sets the background color for the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span> <span data-ttu-id="06b73-111">A cor do plano de fundo padrão é a cor do plano de fundo da janela do sistema, que normalmente é branca.</span><span class="sxs-lookup"><span data-stu-id="06b73-111">The default background color is the system window background color, which is typically white.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propriedade CollectingInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-113">Obtém o valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> está coletando tinta (somente tempo de execução).</span><span class="sxs-lookup"><span data-stu-id="06b73-113">Gets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is collecting ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span></span></td>
<td><span data-ttu-id="06b73-115">Obtém ou define o modo de coleta que determina se a tinta, os gestos ou a tinta e os gestos são reconhecidos conforme o usuário escreve.</span><span class="sxs-lookup"><span data-stu-id="06b73-115">Gets or sets the collection mode that determines whether ink, gestures, or ink and gestures are recognized as the user writes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Propriedade Cursors</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-117">Obtém a coleção <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponível para uso na região de tinta do controle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="06b73-117">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> collection available for use in the <a href="inkpicture-control-reference.md">InkPicture</a> control's inking region.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span></span></td>
<td><span data-ttu-id="06b73-119">Obtém a coleção <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> a ser persistida com a tinta (somente no tempo de Design).</span><span class="sxs-lookup"><span data-stu-id="06b73-119">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> collection to be persisted with the ink (design-time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propriedade DefaultDrawingAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-121">Obtém ou define a coleção de <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> padrão a ser usada ao desenhar e exibir tinta (somente tempo de execução).</span><span class="sxs-lookup"><span data-stu-id="06b73-121">Gets or sets the default <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> collection to use when drawing and displaying ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propriedade DesiredPacketDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-123">Obtém ou define a descrição do pacote do controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).</span><span class="sxs-lookup"><span data-stu-id="06b73-123">Gets or sets the packet description of the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propriedade DynamicRendering</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-125">Obtém ou define o valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> renderiza dinamicamente a tinta conforme ela é coletada.</span><span class="sxs-lookup"><span data-stu-id="06b73-125">Gets or sets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control dynamically renders the ink as it is collected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span></span></td>
<td><span data-ttu-id="06b73-127">Obtém ou define um valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> está no modo de tinta, no modo de exclusão ou no modo de seleção/edição.</span><span class="sxs-lookup"><span data-stu-id="06b73-127">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>habilitado</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span></span></td>
<td><span data-ttu-id="06b73-129">Obtém ou define um valor que determina se o controle <a href="inkpicture-control-reference.md">InkPicture</a> pode responder a eventos gerados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="06b73-129">Gets or sets a value that determines whether the <a href="inkpicture-control-reference.md">InkPicture</a> control can respond to user-generated events.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="06b73-130">Essa propriedade é equivalente à propriedade <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="06b73-130">This property is equivalent to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> property.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span></span></td>
<td><span data-ttu-id="06b73-132">Obtém ou define o valor que especifica se a tinta é apagada por traço ou por ponto.</span><span class="sxs-lookup"><span data-stu-id="06b73-132">Gets or sets the value that specifies whether ink is erased by stroke or by point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span></span></td>
<td><span data-ttu-id="06b73-134">Obtém ou define o valor que especifica a largura da dica de caneta do apagador.</span><span class="sxs-lookup"><span data-stu-id="06b73-134">Gets or sets the value that specifies the width of the eraser pen tip.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span></span></td>
<td><span data-ttu-id="06b73-136">Obtém o identificador de janela ao qual o controle <a href="inkpicture-control-reference.md">InkPicture</a> está associado.</span><span class="sxs-lookup"><span data-stu-id="06b73-136">Gets the window handle to which the <a href="inkpicture-control-reference.md">InkPicture</a> control is bound.</span></span> <span data-ttu-id="06b73-137">(somente tempo de execução)</span><span class="sxs-lookup"><span data-stu-id="06b73-137">(run time only)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Tinta</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Ink</strong></a></span></span></td>
<td><span data-ttu-id="06b73-139">Obtém ou define o objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associado ao controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).</span><span class="sxs-lookup"><span data-stu-id="06b73-139">Gets or sets the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object that is associated with the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span></span></td>
<td><span data-ttu-id="06b73-141">Obtém ou define um valor que especifica se o controle <a href="inkpicture-control-reference.md">InkPicture</a> coleta entrada de caneta (pacotes no ar, cursor em eventos de intervalo e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="06b73-141">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propriedade MarginX</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-143">Obtém ou define a margem do eixo x em volta do retângulo da janela em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="06b73-143">Gets or sets the x-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Propriedade MarginY</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-145">Obtém ou define a margem do eixo y em relação ao retângulo da janela em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="06b73-145">Gets or sets the y-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propriedade MouseIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-147">Obtém ou define o ícone de mouse personalizado atual.</span><span class="sxs-lookup"><span data-stu-id="06b73-147">Gets or sets the current custom mouse icon.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Propriedade MousePointer</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-149">Obtém ou define um valor que indica o tipo de ponteiro do mouse que aparece quando o mouse está sobre uma parte específica do controle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="06b73-149">Gets or sets a value that indicates the type of mouse pointer that appears when the mouse is over a particular part of the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagem</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span></span></td>
<td><span data-ttu-id="06b73-151">Obtém o arquivo de gráficos para aparecer no controle <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="06b73-151">Gets the graphics file to appear on the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Propriedade do renderizador</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-153">Obtém ou define o objeto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> usado para desenhar tinta no controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).</span><span class="sxs-lookup"><span data-stu-id="06b73-153">Gets or sets the <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> object that is used to draw ink on the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Seleção</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selection</strong></a></span></span></td>
<td><span data-ttu-id="06b73-155">Obtém a coleção <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> selecionada no momento dentro do controle <a href="inkpicture-control-reference.md">InkPicture</a> (somente tempo de execução).</span><span class="sxs-lookup"><span data-stu-id="06b73-155">Gets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection currently selected inside the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span></span></td>
<td><span data-ttu-id="06b73-157">Obtém ou define como o controle manipula o posicionamento e o dimensionamento da imagem.</span><span class="sxs-lookup"><span data-stu-id="06b73-157">Gets or sets how the control handles image placement and sizing.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propriedade SupportHighContrastInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-159">Obtém um valor que especifica se a tinta é renderizada como apenas uma cor, cor = COLOR_WINDOWTEXT (da chamada GetSystemMetrics) quando o sistema está no modo de Alto Contraste.</span><span class="sxs-lookup"><span data-stu-id="06b73-159">Gets a value that specifies whether ink is rendered as just one color, Color = COLOR_WINDOWTEXT (from the GetSystemMetrics call) when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06b73-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span></span></td>
<td><span data-ttu-id="06b73-161">Obtém ou define um valor que especifica se todas as interfaces de usuário de seleção (caixa delimitadora de seleção e identificadores de seleção) são desenhadas em alto contraste quando o sistema está no modo de Alto Contraste.</span><span class="sxs-lookup"><span data-stu-id="06b73-161">Gets or sets a value that specifies whether all selection user interfaces (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06b73-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propriedade do Tablet</strong></a></span><span class="sxs-lookup"><span data-stu-id="06b73-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet Property</strong></a></span></span></td>
<td><span data-ttu-id="06b73-163">Obtém o objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> que o controle <a href="inkpicture-control-reference.md">InkPicture</a> está usando atualmente para coletar a entrada.</span><span class="sxs-lookup"><span data-stu-id="06b73-163">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> object that the <a href="inkpicture-control-reference.md">InkPicture</a> control is currently using to collect input.</span></span><br/></td>
</tr>
</tbody>
</table>



 

