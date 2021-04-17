---
title: Estilos estendidos da barra de ferramentas (CommCtrl. h)
description: Esta seção lista os estilos estendidos com suporte pelos controles da barra de ferramentas.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752603"
---
# <a name="toolbar-extended-styles"></a><span data-ttu-id="a50e5-103">Estilos estendidos da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a50e5-103">Toolbar Extended Styles</span></span>

<span data-ttu-id="a50e5-104">Esta seção lista os estilos estendidos com suporte pelos controles da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a50e5-104">This section lists the extended styles supported by toolbar controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a50e5-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a50e5-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a50e5-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a50e5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <span data-ttu-id="a50e5-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a50e5-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a50e5-108"><a href="common-control-versions.md">Versão 4,71</a>.</span><span class="sxs-lookup"><span data-stu-id="a50e5-108"><a href="common-control-versions.md">Version 4.71</a>.</span></span> <span data-ttu-id="a50e5-109">Esse estilo permite que os botões tenham uma seta suspensa separada.</span><span class="sxs-lookup"><span data-stu-id="a50e5-109">This style allows buttons to have a separate dropdown arrow.</span></span> <span data-ttu-id="a50e5-110">Os botões que têm o estilo de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> serão desenhados com uma seta suspensa em uma seção separada, à direita do botão.</span><span class="sxs-lookup"><span data-stu-id="a50e5-110">Buttons that have the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> style will be drawn with a dropdown arrow in a separate section, to the right of the button.</span></span> <span data-ttu-id="a50e5-111">Se a seta for clicada, somente a parte de seta do botão será pressionado e o controle Toolbar enviará um <a href="tbn-dropdown.md">TBN_DROPDOWN</a> código de notificação para solicitar que o aplicativo exiba o menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="a50e5-111">If the arrow is clicked, only the arrow portion of the button will depress, and the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code to prompt the application to display the dropdown menu.</span></span> <span data-ttu-id="a50e5-112">Se a parte principal do botão for clicada, o controle Toolbar enviará uma mensagem WM_COMMAND com a ID do botão.</span><span class="sxs-lookup"><span data-stu-id="a50e5-112">If the main part of the button is clicked, the toolbar control sends a WM_COMMAND message with the button's ID.</span></span> <span data-ttu-id="a50e5-113">Normalmente, o aplicativo responde iniciando o primeiro comando no menu.</span><span class="sxs-lookup"><span data-stu-id="a50e5-113">The application normally responds by launching the first command on the menu.</span></span><br/> <span data-ttu-id="a50e5-114">Há muitas situações em que você talvez queira ter apenas alguns dos botões suspensos em uma barra de ferramentas com setas separadas.</span><span class="sxs-lookup"><span data-stu-id="a50e5-114">There are many situations where you may want to have only some of the dropdown buttons on a toolbar with separated arrows.</span></span> <span data-ttu-id="a50e5-115">Para fazer isso, defina o TBSTYLE_EX_DRAWDDARROWS estilo estendido.</span><span class="sxs-lookup"><span data-stu-id="a50e5-115">To do so, set the TBSTYLE_EX_DRAWDDARROWS extended style.</span></span> <span data-ttu-id="a50e5-116">Dê a esses botões que não terão setas separadas <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> estilo.</span><span class="sxs-lookup"><span data-stu-id="a50e5-116">Give those buttons that will not have separated arrows the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> style.</span></span> <span data-ttu-id="a50e5-117">Os botões com esse estilo terão uma seta exibida ao lado da imagem.</span><span class="sxs-lookup"><span data-stu-id="a50e5-117">Buttons with this style will have an arrow displayed next to the image.</span></span> <span data-ttu-id="a50e5-118">No entanto, a seta não será separada e, quando qualquer parte do botão for clicada, o controle da barra de ferramentas enviará um <a href="tbn-dropdown.md">TBN_DROPDOWN</a> código de notificação.</span><span class="sxs-lookup"><span data-stu-id="a50e5-118">However, the arrow will not be separate and when any part of the button is clicked, the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code.</span></span> <span data-ttu-id="a50e5-119">Para evitar problemas de repintura, esse estilo deve ser definido antes que o controle da barra de ferramentas fique visível.</span><span class="sxs-lookup"><span data-stu-id="a50e5-119">To prevent repainting problems, this style should be set before the toolbar control becomes visible.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <span data-ttu-id="a50e5-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a50e5-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a50e5-121"><a href="common-control-versions.md">Versão 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="a50e5-121"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="a50e5-122">Esse estilo oculta os botões parcialmente recortados.</span><span class="sxs-lookup"><span data-stu-id="a50e5-122">This style hides partially clipped buttons.</span></span> <span data-ttu-id="a50e5-123">O uso mais comum desse estilo é para barras de ferramentas que fazem parte de um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="a50e5-123">The most common use of this style is for toolbars that are part of a rebar control.</span></span> <span data-ttu-id="a50e5-124">Se uma faixa adjacente abranger parte de um botão, o botão não será exibido.</span><span class="sxs-lookup"><span data-stu-id="a50e5-124">If an adjacent band covers part of a button, the button will not be displayed.</span></span> <span data-ttu-id="a50e5-125">No entanto, se a faixa Rebar tiver o estilo de <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , o botão será exibido no menu suspenso da divisa.</span><span class="sxs-lookup"><span data-stu-id="a50e5-125">However, if the rebar band has the <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> style, the button will be displayed on the chevron's dropdown menu.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <span data-ttu-id="a50e5-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a50e5-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a50e5-127"><a href="common-control-versions.md">Versão 6</a>.</span><span class="sxs-lookup"><span data-stu-id="a50e5-127"><a href="common-control-versions.md">Version 6</a>.</span></span> <span data-ttu-id="a50e5-128">Esse estilo requer que a barra de ferramentas seja duplamente armazenada em buffer.</span><span class="sxs-lookup"><span data-stu-id="a50e5-128">This style requires the toolbar to be double buffered.</span></span> <span data-ttu-id="a50e5-129">O buffer duplo é um mecanismo que detecta quando a barra de ferramentas foi alterada.</span><span class="sxs-lookup"><span data-stu-id="a50e5-129">Double buffering is a mechanism that detects when the toolbar has changed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a50e5-130">O Comctl32.dll versão 6 não é redistribuível, mas está incluído no Windows ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a50e5-130">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="a50e5-131">Para usar Comctl32.dll versão 6, especifique-o em um manifesto.</span><span class="sxs-lookup"><span data-stu-id="a50e5-131">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="a50e5-132">Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</span><span class="sxs-lookup"><span data-stu-id="a50e5-132">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <span data-ttu-id="a50e5-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a50e5-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a50e5-134"><a href="common-control-versions.md">Versão 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="a50e5-134"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="a50e5-135">Esse estilo permite que você defina o texto para todos os botões, mas só o exiba para esses botões com o estilo de botão <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a50e5-135">This style allows you to set text for all buttons, but only display it for those buttons with the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> button style.</span></span> <span data-ttu-id="a50e5-136">O estilo de <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> também deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="a50e5-136">The <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> style must also be set.</span></span> <span data-ttu-id="a50e5-137">Normalmente, quando um botão não exibe texto, seu aplicativo deve manipular <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> ou <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> para exibir uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a50e5-137">Normally, when a button does not display text, your application must handle <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> or <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> to display a tooltip.</span></span> <span data-ttu-id="a50e5-138">Com o TBSTYLE_EX_MIXEDBUTTONS estilo estendido, o texto definido, mas não exibido em um botão, será automaticamente usado como texto de dica de ferramenta do botão.</span><span class="sxs-lookup"><span data-stu-id="a50e5-138">With the TBSTYLE_EX_MIXEDBUTTONS extended style, text that is set but not displayed on a button will automatically be used as the button's tooltip text.</span></span> <span data-ttu-id="a50e5-139">Seu aplicativo só precisa manipular TBN_GETINFOTIP ou TTN_GETDISPINFO se precisar de mais flexibilidade para especificar o texto da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a50e5-139">Your application only needs to handle TBN_GETINFOTIP or or TTN_GETDISPINFO if it needs more flexibility in specifying the tooltip text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <span data-ttu-id="a50e5-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a50e5-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a50e5-141"><a href="common-control-versions.md">Versão 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="a50e5-141"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="a50e5-142"><strong>Destinado ao uso interno; Não recomendado para uso em aplicativos.</strong></span><span class="sxs-lookup"><span data-stu-id="a50e5-142"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="a50e5-143">Esse estilo dá à barra de ferramentas uma orientação vertical e organiza os botões da barra de ferramentas em colunas.</span><span class="sxs-lookup"><span data-stu-id="a50e5-143">This style gives the toolbar a vertical orientation and organizes the toolbar buttons into columns.</span></span> <span data-ttu-id="a50e5-144">Os botões fluem verticalmente até que um botão exceda a altura delimitadora da barra de ferramentas (consulte <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) e uma nova coluna seja criada.</span><span class="sxs-lookup"><span data-stu-id="a50e5-144">The buttons flow down vertically until a button has exceeded the bounding height of the toolbar (see <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), and then a new column is created.</span></span> <span data-ttu-id="a50e5-145">A barra de ferramentas flui os botões dessa maneira até que todos os botões sejam posicionados.</span><span class="sxs-lookup"><span data-stu-id="a50e5-145">The toolbar flows the buttons in this manner until all buttons are positioned.</span></span> <span data-ttu-id="a50e5-146">Para usar esse estilo, o estilo de TBSTYLE_EX_VERTICAL também deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="a50e5-146">To use this style, the TBSTYLE_EX_VERTICAL style must also be set.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a50e5-147">Esse estilo pode não ter suporte em versões futuras do Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="a50e5-147">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="a50e5-148">Além disso, esse estilo não é definido em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="a50e5-148">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="a50e5-149">Adicione a seguinte definição aos arquivos de origem do seu aplicativo para usar este estilo: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span><span class="sxs-lookup"><span data-stu-id="a50e5-149">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <span data-ttu-id="a50e5-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a50e5-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a50e5-151"><a href="common-control-versions.md">Versão 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="a50e5-151"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="a50e5-152"><strong>Destinado ao uso interno; Não recomendado para uso em aplicativos.</strong></span><span class="sxs-lookup"><span data-stu-id="a50e5-152"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="a50e5-153">Esse estilo dá à barra de ferramentas uma orientação vertical.</span><span class="sxs-lookup"><span data-stu-id="a50e5-153">This style gives the toolbar a vertical orientation.</span></span> <span data-ttu-id="a50e5-154">Os botões da barra de ferramentas fluem de cima para baixo em vez de horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="a50e5-154">Toolbar buttons flow from top to bottom instead of horizontally.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a50e5-155">Esse estilo pode não ter suporte em versões futuras do Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="a50e5-155">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="a50e5-156">Além disso, esse estilo não é definido em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="a50e5-156">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="a50e5-157">Adicione a seguinte definição aos arquivos de origem do seu aplicativo para usar este estilo: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span><span class="sxs-lookup"><span data-stu-id="a50e5-157">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span></span></blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="a50e5-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="a50e5-158">Remarks</span></span>

<span data-ttu-id="a50e5-159">Para definir um estilo estendido, envie o controle Toolbar a uma mensagem de [**TB \_ Extended**](tb-setextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a50e5-159">To set an extended style, send the toolbar control a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span> <span data-ttu-id="a50e5-160">Para determinar quais estilos estendidos estão atualmente definidos, envie uma mensagem de [**TB \_ Extended**](tb-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a50e5-160">To determine what extended styles are currently set, send a [**TB\_GETEXTENDEDSTYLE**](tb-getextendedstyle.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a50e5-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a50e5-161">Requirements</span></span>



| <span data-ttu-id="a50e5-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="a50e5-162">Requirement</span></span> | <span data-ttu-id="a50e5-163">Valor</span><span class="sxs-lookup"><span data-stu-id="a50e5-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a50e5-164">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a50e5-164">Header</span></span><br/> | <dl> <span data-ttu-id="a50e5-165"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a50e5-165"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





