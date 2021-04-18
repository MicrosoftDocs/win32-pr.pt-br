---
title: Estilos de controle de cabeçalho (CommCtrl. h)
description: Os controles de cabeçalho têm um número de estilos, descritos nesta seção, que determinam a aparência e o comportamento do controle. Você define os estilos iniciais ao criar o controle de cabeçalho.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752195"
---
# <a name="header-control-styles"></a><span data-ttu-id="45178-104">Estilos de controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45178-104">Header Control Styles</span></span>

<span data-ttu-id="45178-105">Os controles de cabeçalho têm um número de estilos, descritos nesta seção, que determinam a aparência e o comportamento do controle.</span><span class="sxs-lookup"><span data-stu-id="45178-105">Header controls have a number of styles, described in this section, that determine the control's appearance and behavior.</span></span> <span data-ttu-id="45178-106">Você define os estilos iniciais ao criar o controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="45178-106">You set the initial styles when you create the header control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="45178-107">Constante</span><span class="sxs-lookup"><span data-stu-id="45178-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="45178-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="45178-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <span data-ttu-id="45178-109"><dt><strong>HDS_BUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-109"><dt><strong>HDS_BUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-110">Cada item do controle tem aparência e se comporta como um botão de ação.</span><span class="sxs-lookup"><span data-stu-id="45178-110">Each item in the control looks and behaves like a push button.</span></span> <span data-ttu-id="45178-111">Esse estilo será útil se um aplicativo executar uma tarefa quando o usuário clicar em um item no controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="45178-111">This style is useful if an application carries out a task when the user clicks an item in the header control.</span></span> <span data-ttu-id="45178-112">Por exemplo, um aplicativo pode classificar informações nas colunas de forma diferente, dependendo de qual item o usuário clica.</span><span class="sxs-lookup"><span data-stu-id="45178-112">For example, an application could sort information in the columns differently depending on which item the user clicks.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <span data-ttu-id="45178-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-113"><dt><strong>HDS_DRAGDROP</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-114">Permite reordenação do tipo "arrastar e soltar" de itens de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="45178-114">Allows drag-and-drop reordering of header items.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <span data-ttu-id="45178-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-115"><dt><strong>HDS_FILTERBAR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-116">Inclua uma barra de filtro como parte do controle de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="45178-116">Include a filter bar as part of the standard header control.</span></span> <span data-ttu-id="45178-117">Essa barra permite que os usuários apliquem convenientemente um filtro à exibição.</span><span class="sxs-lookup"><span data-stu-id="45178-117">This bar allows users to conveniently apply a filter to the display.</span></span> <span data-ttu-id="45178-118">Chamadas para <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> resultarão em um novo tamanho para o controle e farão com que a exibição de lista seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="45178-118">Calls to <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> will yield a new size for the control and cause the list view to update.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <span data-ttu-id="45178-119"><dt><strong>HDS_FLAT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-119"><dt><strong>HDS_FLAT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-120"><a href="common-control-versions.md">Versão 6,0 e posterior</a>.</span><span class="sxs-lookup"><span data-stu-id="45178-120"><a href="common-control-versions.md">Version 6.0 and later</a>.</span></span> <span data-ttu-id="45178-121">Faz com que o controle de cabeçalho seja desenhado simples quando o sistema operacional está em execução no modo clássico.</span><span class="sxs-lookup"><span data-stu-id="45178-121">Causes the header control to be drawn flat when the operating system is running in classic mode.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="45178-122">O Comctl32.dll versão 6 não é redistribuível, mas está incluído no Windows.</span><span class="sxs-lookup"><span data-stu-id="45178-122">Comctl32.dll version 6 is not redistributable but it is included in Windows.</span></span> <span data-ttu-id="45178-123">Para usar Comctl32.dll versão 6, especifique-o em um manifesto.</span><span class="sxs-lookup"><span data-stu-id="45178-123">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="45178-124">Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</span><span class="sxs-lookup"><span data-stu-id="45178-124">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <span data-ttu-id="45178-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-125"><dt><strong>HDS_FULLDRAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-126">Faz com que o controle de cabeçalho exiba o conteúdo da coluna mesmo quando o usuário redimensiona uma coluna.</span><span class="sxs-lookup"><span data-stu-id="45178-126">Causes the header control to display column contents even while the user resizes a column.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <span data-ttu-id="45178-127"><dt><strong>HDS_HIDDEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-127"><dt><strong>HDS_HIDDEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-128">Indica um controle de cabeçalho que deve ser ocultado.</span><span class="sxs-lookup"><span data-stu-id="45178-128">Indicates a header control that is intended to be hidden.</span></span> <span data-ttu-id="45178-129">Esse estilo não oculta o controle.</span><span class="sxs-lookup"><span data-stu-id="45178-129">This style does not hide the control.</span></span> <span data-ttu-id="45178-130">Em vez disso, quando você envia a mensagem de <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> para um controle de cabeçalho com o estilo de HDS_HIDDEN, o controle retorna zero no membro <strong>CY</strong> da estrutura <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="45178-130">Instead, when you send the <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> message to a header control with the HDS_HIDDEN style, the control returns zero in the <strong>cy</strong> member of the <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> structure.</span></span> <span data-ttu-id="45178-131">Em seguida, você ocultaria o controle definindo sua altura como zero.</span><span class="sxs-lookup"><span data-stu-id="45178-131">You would then hide the control by setting its height to zero.</span></span> <span data-ttu-id="45178-132">Isso pode ser útil quando você deseja usar o controle como um contêiner de informações em vez de um controle visual.</span><span class="sxs-lookup"><span data-stu-id="45178-132">This can be useful when you want to use the control as an information container instead of a visual control.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <span data-ttu-id="45178-133"><dt><strong>HDS_HORZ</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-133"><dt><strong>HDS_HORZ</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-134">Cria um controle de cabeçalho com uma orientação horizontal.</span><span class="sxs-lookup"><span data-stu-id="45178-134">Creates a header control with a horizontal orientation.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <span data-ttu-id="45178-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-135"><dt><strong>HDS_HOTTRACK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-136">Habilita o rastreamento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="45178-136">Enables hot tracking.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <span data-ttu-id="45178-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-137"><dt><strong>HDS_CHECKBOXES</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-138"><a href="common-control-versions.md">Versão 6, 0 e posterior</a>.</span><span class="sxs-lookup"><span data-stu-id="45178-138"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="45178-139">Permite a colocação de caixas de seleção em itens de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="45178-139">Allows the placing of checkboxes on header items.</span></span> <span data-ttu-id="45178-140">Para obter mais informações, consulte o membro <strong>fmt</strong> de <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="45178-140">For more information, see the <strong>fmt</strong> member of <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <span data-ttu-id="45178-141"><dt><strong>HDS_NOSIZING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-141"><dt><strong>HDS_NOSIZING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-142"><a href="common-control-versions.md">Versão 6, 0 e posterior</a>.</span><span class="sxs-lookup"><span data-stu-id="45178-142"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="45178-143">O usuário não pode arrastar o divisor no controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="45178-143">The user cannot drag the divider on the header control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <span data-ttu-id="45178-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="45178-144"><dt><strong>HDS_OVERFLOW</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="45178-145"><a href="common-control-versions.md">Versão 6, 0 e posterior</a>.</span><span class="sxs-lookup"><span data-stu-id="45178-145"><a href="common-control-versions.md">Version 6.00 and later</a>.</span></span> <span data-ttu-id="45178-146">Um botão é exibido quando nem todos os itens podem ser exibidos dentro do retângulo do controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="45178-146">A button is displayed when not all items can be displayed within the header control's rectangle.</span></span> <span data-ttu-id="45178-147">Quando clicado, esse botão envia uma notificação de <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .</span><span class="sxs-lookup"><span data-stu-id="45178-147">When clicked, this button sends an <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notification.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="45178-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="45178-148">Remarks</span></span>

<span data-ttu-id="45178-149">Para recuperar e alterar os estilos depois de criar o controle, use as funções [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="45178-149">To retrieve and change the styles after creating the control, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="45178-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45178-150">Requirements</span></span>



| <span data-ttu-id="45178-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="45178-151">Requirement</span></span> | <span data-ttu-id="45178-152">Valor</span><span class="sxs-lookup"><span data-stu-id="45178-152">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45178-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45178-153">Header</span></span><br/> | <dl> <span data-ttu-id="45178-154"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="45178-154"><dt>CommCtrl.h</dt></span></span> </dl> |



