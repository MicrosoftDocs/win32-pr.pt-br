---
title: Implementando padrões de controle de automação da interface do usuário
description: Esta seção fornece informações detalhadas sobre como implementar as interfaces do provedor de automação da interface do usuário da Microsoft que dão suporte a padrões de controle.
ms.assetid: d1baa245-62a1-40b1-a671-e227dd3df60a
keywords:
- Automação da interface do usuário, implementação de padrões de controle
- Automação da interface do usuário, padrões de controle
- Implementando padrões de controle de automação da interface do usuário
- padrões de controle, implementação da automação da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfb75b6b275fee9230eb25d9a0b02e1da26ad4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105782529"
---
# <a name="implementing-ui-automation-control-patterns"></a><span data-ttu-id="19de5-107">Implementando padrões de controle de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="19de5-107">Implementing UI Automation Control Patterns</span></span>

<span data-ttu-id="19de5-108">Esta seção fornece informações detalhadas sobre como implementar as interfaces do provedor de automação da interface do usuário da Microsoft que dão suporte a padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="19de5-108">This section provides detailed information about implementing the Microsoft UI Automation provider interfaces that support control patterns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19de5-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="19de5-109">In this section</span></span>

-   [<span data-ttu-id="19de5-110">Padrão de controle de anotação</span><span class="sxs-lookup"><span data-stu-id="19de5-110">Annotation Control Pattern</span></span>](uiauto-implementingannotation.md)
-   [<span data-ttu-id="19de5-111">Padrão de controle CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="19de5-111">CustomNavigation Control Pattern</span></span>](uiauto-implementingcustomnavigation.md)
-   [<span data-ttu-id="19de5-112">Padrão de controle Dock</span><span class="sxs-lookup"><span data-stu-id="19de5-112">Dock Control Pattern</span></span>](uiauto-implementingdock.md)
-   [<span data-ttu-id="19de5-113">Arrastar padrão de controle</span><span class="sxs-lookup"><span data-stu-id="19de5-113">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
-   [<span data-ttu-id="19de5-114">Padrão de controle DropTarget</span><span class="sxs-lookup"><span data-stu-id="19de5-114">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
-   [<span data-ttu-id="19de5-115">Padrão de controle ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="19de5-115">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
-   [<span data-ttu-id="19de5-116">Padrão de controle de grade</span><span class="sxs-lookup"><span data-stu-id="19de5-116">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
-   [<span data-ttu-id="19de5-117">Padrão de controle GridItem</span><span class="sxs-lookup"><span data-stu-id="19de5-117">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
-   [<span data-ttu-id="19de5-118">Invocar padrão de controle</span><span class="sxs-lookup"><span data-stu-id="19de5-118">Invoke Control Pattern</span></span>](uiauto-implementinginvoke.md)
-   [<span data-ttu-id="19de5-119">Padrão de controle de IsContainer</span><span class="sxs-lookup"><span data-stu-id="19de5-119">ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
-   [<span data-ttu-id="19de5-120">Padrão de controle LegacyIAccessible</span><span class="sxs-lookup"><span data-stu-id="19de5-120">LegacyIAccessible Control Pattern</span></span>](uiauto-implementinglegacyiaccessible.md)
-   [<span data-ttu-id="19de5-121">Padrão de controle MultipleView</span><span class="sxs-lookup"><span data-stu-id="19de5-121">MultipleView Control Pattern</span></span>](uiauto-implementingmultipleview.md)
-   [<span data-ttu-id="19de5-122">Padrão de controle ObjectModel</span><span class="sxs-lookup"><span data-stu-id="19de5-122">ObjectModel Control Pattern</span></span>](uiauto-implementingobjectmodel.md)
-   [<span data-ttu-id="19de5-123">Padrão de controle RangeValue</span><span class="sxs-lookup"><span data-stu-id="19de5-123">RangeValue Control Pattern</span></span>](uiauto-implementingrangevalue.md)
-   [<span data-ttu-id="19de5-124">Padrão de controle Scroll</span><span class="sxs-lookup"><span data-stu-id="19de5-124">Scroll Control Pattern</span></span>](uiauto-implementingscroll.md)
-   [<span data-ttu-id="19de5-125">Padrão de controle ScrollItem</span><span class="sxs-lookup"><span data-stu-id="19de5-125">ScrollItem Control Pattern</span></span>](uiauto-implementingscrollitem.md)
-   [<span data-ttu-id="19de5-126">Padrão de controle de seleção</span><span class="sxs-lookup"><span data-stu-id="19de5-126">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
-   [<span data-ttu-id="19de5-127">Padrão de controle SelectionItem</span><span class="sxs-lookup"><span data-stu-id="19de5-127">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
-   [<span data-ttu-id="19de5-128">Padrão de controle de planilha</span><span class="sxs-lookup"><span data-stu-id="19de5-128">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
-   [<span data-ttu-id="19de5-129">Padrão de controle SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="19de5-129">SpreadsheetItem Control Pattern</span></span>](uiauto-implementingspreadsheetitem.md)
-   [<span data-ttu-id="19de5-130">Padrão de controle de estilos</span><span class="sxs-lookup"><span data-stu-id="19de5-130">Styles Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingstyles)
-   [<span data-ttu-id="19de5-131">Padrão de controle SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="19de5-131">SynchronizedInput Control Pattern</span></span>](uiauto-implementingsynchronizedinput.md)
-   [<span data-ttu-id="19de5-132">Padrão de controle de tabela</span><span class="sxs-lookup"><span data-stu-id="19de5-132">Table Control Pattern</span></span>](uiauto-implementingtable.md)
-   [<span data-ttu-id="19de5-133">Padrão de controle TableItem</span><span class="sxs-lookup"><span data-stu-id="19de5-133">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
-   [<span data-ttu-id="19de5-134">Padrões de controle Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="19de5-134">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
-   [<span data-ttu-id="19de5-135">Padrão de controle textchild</span><span class="sxs-lookup"><span data-stu-id="19de5-135">TextChild Control Pattern</span></span>](textchild-control-pattern.md)
-   [<span data-ttu-id="19de5-136">Padrão de controle editor</span><span class="sxs-lookup"><span data-stu-id="19de5-136">TextEdit Control Pattern</span></span>](textedit-control-pattern.md)
-   [<span data-ttu-id="19de5-137">Alternar padrão de controle</span><span class="sxs-lookup"><span data-stu-id="19de5-137">Toggle Control Pattern</span></span>](uiauto-implementingtoggle.md)
-   [<span data-ttu-id="19de5-138">Padrão de controle de transformação</span><span class="sxs-lookup"><span data-stu-id="19de5-138">Transform Control Pattern</span></span>](uiauto-implementingtransform.md)
-   [<span data-ttu-id="19de5-139">Padrão de controle de valor</span><span class="sxs-lookup"><span data-stu-id="19de5-139">Value Control Pattern</span></span>](uiauto-implementingvalue.md)
-   [<span data-ttu-id="19de5-140">Padrão de controle VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="19de5-140">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
-   [<span data-ttu-id="19de5-141">Padrão de controle de janela</span><span class="sxs-lookup"><span data-stu-id="19de5-141">Window Control Pattern</span></span>](uiauto-implementingwindow.md)

## <a name="related-topics"></a><span data-ttu-id="19de5-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19de5-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19de5-143">Guia do programador do provedor de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="19de5-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> <dt>

[<span data-ttu-id="19de5-144">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="19de5-144">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="19de5-145">Suporte a tipos de controle de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="19de5-145">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> </dl>

 

 