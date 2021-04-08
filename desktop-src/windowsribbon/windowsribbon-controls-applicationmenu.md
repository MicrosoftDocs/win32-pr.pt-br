---
title: Menu do aplicativo
description: O menu aplicativo é o menu principal para um aplicativo que implementa a estrutura da faixa de dasgem do Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823775"
---
# <a name="application-menu"></a><span data-ttu-id="28514-103">Menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-103">Application Menu</span></span>

<span data-ttu-id="28514-104">O menu aplicativo é o menu principal para um aplicativo que implementa a estrutura da faixa de dasgem do Windows.</span><span class="sxs-lookup"><span data-stu-id="28514-104">The Application Menu is the main menu for an application that implements the Windows Ribbon framework.</span></span>

-   [<span data-ttu-id="28514-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="28514-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="28514-106">Componentes do menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-106">Components of the Application Menu</span></span>](#components-of-the-application-menu)
    -   [<span data-ttu-id="28514-107">Menu de menus do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-107">Application Menu MenuGroup</span></span>](#application-menu-menugroup)
-   [<span data-ttu-id="28514-108">Dimensionando o menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-108">Sizing the Application Menu</span></span>](#sizing-the-application-menu)
-   [<span data-ttu-id="28514-109">Propriedades do menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-109">Application Menu Properties</span></span>](#application-menu-properties)
-   [<span data-ttu-id="28514-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28514-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="28514-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="28514-111">Introduction</span></span>

<span data-ttu-id="28514-112">O menu do aplicativo é composto por um controle de botão suspenso que exibe um menu contendo comandos que expõem a funcionalidade relacionada a um projeto completo, como um documento, imagem ou filme inteiro.</span><span class="sxs-lookup"><span data-stu-id="28514-112">The Application Menu is composed of a drop-down button control that displays a menu containing Commands that expose functionality related to a complete project, such as an entire document, picture, or movie.</span></span> <span data-ttu-id="28514-113">Os exemplos incluem os comandos **novo**, **abrir**, **salvar** e **sair** .</span><span class="sxs-lookup"><span data-stu-id="28514-113">Examples include the **New**, **Open**, **Save**, and **Exit** Commands.</span></span>

<span data-ttu-id="28514-114">A captura de tela a seguir ilustra o menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28514-114">The following screen shot illustrates the Application Menu.</span></span>

![captura de tela da lista de menus do aplicativo e itens recentes da faixa de pintura do Paint para Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a><span data-ttu-id="28514-116">Componentes do menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-116">Components of the Application Menu</span></span>

<span data-ttu-id="28514-117">O menu aplicativo é um elemento obrigatório em qualquer aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="28514-117">The Application Menu is a mandatory element in any Ribbon application.</span></span> <span data-ttu-id="28514-118">O ponto de entrada no menu do aplicativo é um botão distintivo que aparece como o primeiro item na linha da [guia](windowsribbon-controls-tab.md) , conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="28514-118">The entry point into the Application Menu is a distinctive button that appears as the first item in the [Tab](windowsribbon-controls-tab.md) row, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="28514-119">Windows 8 e mais recente: imagem do botão de menu do aplicativo alterada para rótulo: **arquivo**.</span><span class="sxs-lookup"><span data-stu-id="28514-119">Windows 8 and newer: Application Menu button image changed to label: **File**.</span></span> <span data-ttu-id="28514-120">Recomendamos que você não use o arquivo como rótulo para qualquer uma das suas próprias guias.</span><span class="sxs-lookup"><span data-stu-id="28514-120">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

![captura de tela do botão de menu do aplicativo do WordPad para Windows 7.](images/overviews/applicationmenu-button.png)

<span data-ttu-id="28514-122">Quando clicado, esse botão exibe o menu avançado que é mostrado na captura de tela a seguir (o menu do aplicativo do WordPad para Windows 7).</span><span class="sxs-lookup"><span data-stu-id="28514-122">When clicked, this button displays the rich menu that is shown in the following screen shot (the Application Menu from WordPad for Windows 7).</span></span>

![captura de tela do menu de menu do aplicativo do WordPad para Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> <span data-ttu-id="28514-124">Não há nenhum impacto no conjunto de guias quando o botão de menu do aplicativo é clicado; em vez disso, o foco entra no menu.</span><span class="sxs-lookup"><span data-stu-id="28514-124">There is no impact on the tab set when the Application Menu button is clicked; instead, the focus enters the menu.</span></span>

 

<span data-ttu-id="28514-125">O menu aplicativo contém dois painéis: uma lista de comandos representados por um ou mais elementos do [**menu de menus**](windowsribbon-element-menugroup.md) e uma lista de [itens recentes](windowsribbon-controls-recentitems.md) representada por um elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="28514-125">The Application Menu contains two panes: a list of Commands represented by one or more [**MenuGroup**](windowsribbon-element-menugroup.md) elements, and a [Recent Items](windowsribbon-controls-recentitems.md) list represented by an [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

### <a name="application-menu-menugroup"></a><span data-ttu-id="28514-126">Menu de menus do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-126">Application Menu MenuGroup</span></span>

<span data-ttu-id="28514-127">O elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) deve conter pelo menos um elemento filho de um [**menu**](windowsribbon-element-menugroup.md) que expõe uma lista de comandos no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28514-127">The [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element must contain at least one [**MenuGroup**](windowsribbon-element-menugroup.md) child element that exposes a list of application-level commands.</span></span> <span data-ttu-id="28514-128">Se vários elementos do grupo de **menus** forem declarados, uma linha divisória será desenhada entre os grupos, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="28514-128">If multiple **MenuGroup** elements are declared, a divider line is drawn between the groups, as shown in the following screen shot.</span></span>

![captura de tela de um menu de menu do aplicativo.](images/overviews/applicationmenu-menugroup.png)

<span data-ttu-id="28514-130">Veja a seguir uma lista de restrições para um elemento do [**menu**](windowsribbon-element-menugroup.md) de um do menu do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="28514-130">The following is a list of constraints for a [**MenuGroup**](windowsribbon-element-menugroup.md) element of an Application Menu:</span></span>

-   <span data-ttu-id="28514-131">Todos os itens do [**menu de menus**](windowsribbon-element-menugroup.md) devem ser declarados com um valor de atributo de *classe* de `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="28514-131">All [**MenuGroup**](windowsribbon-element-menugroup.md) items must be declared with a *Class* attribute value of `MajorItems`.</span></span>
-   <span data-ttu-id="28514-132">Um  [**menu de aplicativo é compatível apenas**](windowsribbon-element-menugroup.md) com o [botão](windowsribbon-controls-button.md), [botão de alternância](windowsribbon-controls-togglebutton.md), botão [suspenso](windowsribbon-controls-dropdownbutton.md), [botão de divisão](windowsribbon-controls-splitbutton.md), [Galeria suspensa](windowsribbon-controls-dropdowngallery.md)e controles de [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="28514-132">An Application Menu  [**MenuGroup**](windowsribbon-element-menugroup.md) supports only the [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), and [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) controls.</span></span>
    > <span data-ttu-id="28514-133">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="28514-133">\[!Important\]</span></span>  
    > <span data-ttu-id="28514-134">As galerias de comandos são o único tipo de galeria com suporte no menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28514-134">Command galleries are the only type of gallery that are supported in the Application Menu.</span></span> <span data-ttu-id="28514-135">Consulte [trabalhando com galerias](./ribbon-controls-galleries.md)para obter mais informações sobre controles da galeria.</span><span class="sxs-lookup"><span data-stu-id="28514-135">See [Working with Galleries](./ribbon-controls-galleries.md), for more information on gallery controls.</span></span>

     

<span data-ttu-id="28514-136">Quando um [botão](windowsribbon-controls-button.md) ou [botão de alternância](windowsribbon-controls-togglebutton.md) é usado em um [**menu**](windowsribbon-element-menugroup.md), o valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) é exibido no menu e os valores de [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) e [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) são exibidos como a dica de ferramenta, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="28514-136">When a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) is used in a [**MenuGroup**](windowsribbon-element-menugroup.md), the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is displayed in the menu and the values of [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) and [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) are displayed as the tooltip, as shown in the following screen shot.</span></span>

![captura de tela de um controle de botão em um menu de aplicativo.](images/overviews/applicationmenu-menubutton.png)

<span data-ttu-id="28514-138">Quando um [botão suspenso](windowsribbon-controls-dropdownbutton.md), um [botão de divisão](windowsribbon-controls-splitbutton.md), uma [Galeria suspensa](windowsribbon-controls-dropdowngallery.md)ou uma [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) são usados no menu do aplicativo, a parte do menu é exibida como um submenu que cobre e oculta o painel **itens recentes** .</span><span class="sxs-lookup"><span data-stu-id="28514-138">When a [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), or [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) is used in the Application Menu, the menu portion is displayed as a flyout that covers and conceals the **Recent items** pane.</span></span>

<span data-ttu-id="28514-139">Para os controles botão de [divisão](windowsribbon-controls-splitbutton.md) e [botão suspenso](windowsribbon-controls-dropdownbutton.md) , o valor de [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) é mostrado embutido no menu do submenu para auxiliar visualmente os usuários com a descoberta da funcionalidade do comando.</span><span class="sxs-lookup"><span data-stu-id="28514-139">For [Split Button](windowsribbon-controls-splitbutton.md) and [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) controls, the value of [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) is shown inline in the flyout menu to visually assist users with discovering the Command functionality.</span></span> <span data-ttu-id="28514-140">O valor exibido de **Command. LabelDescription** é interrompido programaticamente em um intervalo de duas linhas e é feita uma tentativa de ajustar o valor exatamente acima do painel **itens recentes** abaixo.</span><span class="sxs-lookup"><span data-stu-id="28514-140">The displayed value of **Command.LabelDescription** is programmatically broken over a two-line span, and an attempt is made to fit the value exactly over the **Recent items** pane beneath.</span></span> <span data-ttu-id="28514-141">Se o valor de **Command. LabelDescription** não couber, o submenu será expandido para acomodar o valor de comando mais longo [**. Comment**](windowsribbon-element-command-comment.md) no [**menu**](windowsribbon-element-menugroup.md).</span><span class="sxs-lookup"><span data-stu-id="28514-141">If the **Command.LabelDescription** value does not fit, the flyout will expand to accommodate the longest [**Command.Comment**](windowsribbon-element-command-comment.md) value in the [**MenuGroup**](windowsribbon-element-menugroup.md).</span></span>

<span data-ttu-id="28514-142">A captura de tela a seguir ilustra esses comportamentos em um submenu de [botão de divisão](windowsribbon-controls-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="28514-142">The following screen shot illustrates these behaviors in a [Split Button](windowsribbon-controls-splitbutton.md) flyout.</span></span>

![captura de tela de um submenu de controle de lista em um menu de aplicativo.](images/overviews/applicationmenu-menuflyout.png)

<span data-ttu-id="28514-144">Com uma [Galeria suspensa](windowsribbon-controls-dropdowngallery.md) e uma galeria de [botões de divisão](windowsribbon-controls-splitbuttongallery.md), apenas um rótulo e uma imagem são mostrados.</span><span class="sxs-lookup"><span data-stu-id="28514-144">With a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) and a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md), only a label and an image are shown.</span></span>

## <a name="sizing-the-application-menu"></a><span data-ttu-id="28514-145">Dimensionando o menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-145">Sizing the Application Menu</span></span>

<span data-ttu-id="28514-146">O dimensionamento do menu do aplicativo é tratado pela estrutura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="28514-146">Sizing of the Application Menu is handled by the Ribbon framework.</span></span> <span data-ttu-id="28514-147">Se forem fornecidas cadeias de caracteres muito longas para o valor de [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md), ou se uma longa lista de comandos for usada, o menu ajustará seu tamanho para acomodar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="28514-147">If very long strings are supplied for the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), or a long list of Commands is used, the menu will adjust its size to accommodate the contents.</span></span> <span data-ttu-id="28514-148">Algumas formas de ajuste incluem expandir o tamanho de submenus ou painéis de menus e adicionar visualizadores de Pan quando a rolagem é necessária.</span><span class="sxs-lookup"><span data-stu-id="28514-148">Some forms of adjustment include expanding the size of flyouts or menu panes, and adding pan viewers when scrolling is required.</span></span>

## <a name="application-menu-properties"></a><span data-ttu-id="28514-149">Propriedades do menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="28514-149">Application Menu Properties</span></span>

<span data-ttu-id="28514-150">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="28514-150">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Application Menu control.</span></span>

<span data-ttu-id="28514-151">Normalmente, uma propriedade de menu de aplicativo é atualizada na interface do usuário da faixa de guia invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="28514-151">Typically, an Application Menu property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="28514-152">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="28514-152">The invalidation event is handled and the property updates are defined by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="28514-153">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo não é consultado quanto a um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="28514-153">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed and the application is not queried for an updated property value until the property is required by the framework.</span></span> <span data-ttu-id="28514-154">Por exemplo, a estrutura requer a propriedade quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de ferramentas ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="28514-154">For example, the framework requires the property when a tab is activated and a control is revealed in the ribbon UI, or when a tooltip is displayed.</span></span>



| <span data-ttu-id="28514-155">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="28514-155">Property key</span></span>                                                                                     | <span data-ttu-id="28514-156">Observações</span><span class="sxs-lookup"><span data-stu-id="28514-156">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="28514-157">\_TooltipDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="28514-157">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="28514-158">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="28514-158">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="28514-159">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="28514-159">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="28514-160">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="28514-160">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="28514-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28514-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28514-162">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="28514-162">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="28514-163">**Elemento de marcação ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="28514-163">**ApplicationMenu markup element**</span></span>](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 