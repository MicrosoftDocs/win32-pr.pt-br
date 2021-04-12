---
title: Suporte a tipos de controle de automação da interface do usuário
description: Esta seção contém informações detalhadas sobre a estrutura de árvore, propriedades, padrões de controle e eventos que cada tipo de controle de automação da interface do usuário da Microsoft precisa dar suporte.
ms.assetid: 35232907-6c54-47cd-b82a-0daee279ef17
keywords:
- Automação da interface do usuário, sobre tipos de controle
- Visão geral da automação da interface do usuário, tipo de controle
- suporte para tipo de controle
- tipos de controle, suporte
- tipos de controle, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac6f857da87691428c747cfe5dbff5102218f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366521"
---
# <a name="supporting-ui-automation-control-types"></a><span data-ttu-id="0296f-108">Suporte a tipos de controle de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0296f-108">Supporting UI Automation Control Types</span></span>

<span data-ttu-id="0296f-109">Esta seção contém informações detalhadas sobre a estrutura de árvore, propriedades, padrões de controle e eventos que cada tipo de controle de automação da interface do usuário da Microsoft precisa dar suporte.</span><span class="sxs-lookup"><span data-stu-id="0296f-109">This section contains detailed information about the tree structure, properties, control patterns, and events that each Microsoft UI Automation control type is required to support.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0296f-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0296f-110">In this section</span></span>

-   [<span data-ttu-id="0296f-111">Tipo de controle AppBar</span><span class="sxs-lookup"><span data-stu-id="0296f-111">AppBar Control Type</span></span>](uiauto-supportappbarcontroltype.md)
-   [<span data-ttu-id="0296f-112">Tipo de controle de botão</span><span class="sxs-lookup"><span data-stu-id="0296f-112">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="0296f-113">Tipo de controle de calendário</span><span class="sxs-lookup"><span data-stu-id="0296f-113">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="0296f-114">Tipo de controle de caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="0296f-114">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="0296f-115">Tipo de controle ComboBox</span><span class="sxs-lookup"><span data-stu-id="0296f-115">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="0296f-116">Tipo de controle DataGrid</span><span class="sxs-lookup"><span data-stu-id="0296f-116">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="0296f-117">Tipo de controle DataItem</span><span class="sxs-lookup"><span data-stu-id="0296f-117">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="0296f-118">Tipo de controle de documento</span><span class="sxs-lookup"><span data-stu-id="0296f-118">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="0296f-119">Editar tipo de controle</span><span class="sxs-lookup"><span data-stu-id="0296f-119">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="0296f-120">Tipo de controle de grupo</span><span class="sxs-lookup"><span data-stu-id="0296f-120">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="0296f-121">Tipo de controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0296f-121">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="0296f-122">Tipo de controle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="0296f-122">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="0296f-123">Tipo de controle de hiperlink</span><span class="sxs-lookup"><span data-stu-id="0296f-123">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="0296f-124">Tipo de controle de imagem</span><span class="sxs-lookup"><span data-stu-id="0296f-124">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="0296f-125">Tipo de controle de lista</span><span class="sxs-lookup"><span data-stu-id="0296f-125">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="0296f-126">Tipo de controle ListItem</span><span class="sxs-lookup"><span data-stu-id="0296f-126">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="0296f-127">Tipo de controle de menu</span><span class="sxs-lookup"><span data-stu-id="0296f-127">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="0296f-128">Tipo de controle MenuBar</span><span class="sxs-lookup"><span data-stu-id="0296f-128">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="0296f-129">Tipo de controle MenuItem</span><span class="sxs-lookup"><span data-stu-id="0296f-129">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="0296f-130">Tipo de controle de painel</span><span class="sxs-lookup"><span data-stu-id="0296f-130">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="0296f-131">Tipo de controle ProgressBar</span><span class="sxs-lookup"><span data-stu-id="0296f-131">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="0296f-132">Tipo de controle RadioButton</span><span class="sxs-lookup"><span data-stu-id="0296f-132">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="0296f-133">Tipo de controle ScrollBar</span><span class="sxs-lookup"><span data-stu-id="0296f-133">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="0296f-134">Tipo de controle SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="0296f-134">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="0296f-135">Tipo de controle Separator</span><span class="sxs-lookup"><span data-stu-id="0296f-135">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="0296f-136">Tipo de controle Slider</span><span class="sxs-lookup"><span data-stu-id="0296f-136">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="0296f-137">Tipo de controle Spinner</span><span class="sxs-lookup"><span data-stu-id="0296f-137">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="0296f-138">Tipo de controle SplitButton</span><span class="sxs-lookup"><span data-stu-id="0296f-138">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="0296f-139">Tipo de controle StatusBar</span><span class="sxs-lookup"><span data-stu-id="0296f-139">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="0296f-140">Tipo de controle da guia</span><span class="sxs-lookup"><span data-stu-id="0296f-140">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="0296f-141">Tipo de controle TabItem</span><span class="sxs-lookup"><span data-stu-id="0296f-141">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="0296f-142">Tipo de controle de tabela</span><span class="sxs-lookup"><span data-stu-id="0296f-142">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="0296f-143">Tipo de controle de texto</span><span class="sxs-lookup"><span data-stu-id="0296f-143">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="0296f-144">Tipo de controle Thumb</span><span class="sxs-lookup"><span data-stu-id="0296f-144">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="0296f-145">Tipo de controle TitleBar</span><span class="sxs-lookup"><span data-stu-id="0296f-145">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="0296f-146">Tipo de controle ToolBar</span><span class="sxs-lookup"><span data-stu-id="0296f-146">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="0296f-147">Tipo de controle ToolTip</span><span class="sxs-lookup"><span data-stu-id="0296f-147">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="0296f-148">Tipo de controle de árvore</span><span class="sxs-lookup"><span data-stu-id="0296f-148">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="0296f-149">Tipo de controle TreeItem</span><span class="sxs-lookup"><span data-stu-id="0296f-149">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="0296f-150">Tipo de controle de janela</span><span class="sxs-lookup"><span data-stu-id="0296f-150">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="0296f-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0296f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0296f-152">Guia do programador do provedor de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="0296f-152">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 