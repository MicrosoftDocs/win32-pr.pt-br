---
title: Grupo de menus
description: O grupo de menus organiza comandos e controles relacionados em um menu ou barra de ferramentas.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917571"
---
# <a name="menu-group"></a><span data-ttu-id="4f15d-103">Grupo de menus</span><span class="sxs-lookup"><span data-stu-id="4f15d-103">Menu Group</span></span>

<span data-ttu-id="4f15d-104">O grupo de menus organiza comandos e controles relacionados em um menu ou barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="4f15d-104">The Menu Group organizes related Commands and controls within a menu or toolbar.</span></span>

-   [<span data-ttu-id="4f15d-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="4f15d-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="4f15d-106">Propriedades do grupo de menus</span><span class="sxs-lookup"><span data-stu-id="4f15d-106">Menu Group Properties</span></span>](#menu-group-properties)
-   [<span data-ttu-id="4f15d-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f15d-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="4f15d-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="4f15d-108">Introduction</span></span>

<span data-ttu-id="4f15d-109">O controle de grupo de menu, exposto por meio do elemento de marcação de [**menu**](windowsribbon-element-menugroup.md) , é um contêiner lógico para grupos de itens ou comandos em controles baseados em menus, incluindo a mini-barra de ferramentas [Popup de contexto](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="4f15d-109">The Menu Group control, exposed through the [**MenuGroup**](windowsribbon-element-menugroup.md) markup element, is a logical container for groups of items or Commands in menu-based controls, including the [Context Popup](windowsribbon-controls-contextpopup.md) Mini-Toolbar.</span></span>

<span data-ttu-id="4f15d-110">Um rótulo pode ser especificado para um grupo de menus por meio do atributo *LabelTitle* ou da propriedade [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) de uma declaração de comando associada.</span><span class="sxs-lookup"><span data-stu-id="4f15d-110">A label can be specified for a Menu Group through the *LabelTitle* attribute or [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) property of an associated Command declaration.</span></span> <span data-ttu-id="4f15d-111">O valor atribuído a *LabelTitle* é renderizado como um cabeçalho de categoria.</span><span class="sxs-lookup"><span data-stu-id="4f15d-111">The value assigned to *LabelTitle* is rendered as a category header.</span></span>

<span data-ttu-id="4f15d-112">O exemplo a seguir demonstra a marcação de comando para um controle de [botão de divisão](windowsribbon-controls-splitbutton.md) que inclui duas declarações de comando de grupo de menus.</span><span class="sxs-lookup"><span data-stu-id="4f15d-112">The following example demonstrates the Command markup for a [Split Button](windowsribbon-controls-splitbutton.md) control that includes two Menu Group Command declarations.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="4f15d-113">O exemplo a seguir demonstra a marcação necessária para um elemento [**SplitButton**](windowsribbon-element-splitbutton.md) com três declarações de elemento de [**menu**](windowsribbon-element-menugroup.md) , duas das quais são associadas aos comandos de grupo de menus do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="4f15d-113">The following example demonstrates the markup required for a [**SplitButton**](windowsribbon-element-splitbutton.md) element with three [**MenuGroup**](windowsribbon-element-menugroup.md) element declarations, two of which are associated with the Menu Group Commands from the previous example.</span></span> <span data-ttu-id="4f15d-114">O atributo de *classe* do elemento de **menu** é usado para especificar o tamanho dos itens de menu.</span><span class="sxs-lookup"><span data-stu-id="4f15d-114">The *Class* attribute of the **MenuGroup** element is used to specify the size of the menu items.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



<span data-ttu-id="4f15d-115">A captura de tela a seguir ilustra o menu (com três controles de grupo de menus) que é gerado a partir da marcação nos exemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="4f15d-115">The following screen shot illustrates the menu (with three Menu Group controls) that is generated from the markup in the previous examples.</span></span>

![captura de tela de um menu com três controles de grupo de menus.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a><span data-ttu-id="4f15d-117">Propriedades do grupo de menus</span><span class="sxs-lookup"><span data-stu-id="4f15d-117">Menu Group Properties</span></span>

<span data-ttu-id="4f15d-118">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de grupo de menus.</span><span class="sxs-lookup"><span data-stu-id="4f15d-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Menu Group control.</span></span>

<span data-ttu-id="4f15d-119">Normalmente, uma propriedade de grupo de menus é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="4f15d-119">Typically, a Menu Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="4f15d-120">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="4f15d-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="4f15d-121">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="4f15d-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="4f15d-122">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="4f15d-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="4f15d-123">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="4f15d-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="4f15d-124">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de grupo de menu.</span><span class="sxs-lookup"><span data-stu-id="4f15d-124">The following table lists the property keys that are associated with the Menu Group control.</span></span>



| <span data-ttu-id="4f15d-125">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="4f15d-125">Property Key</span></span>                                                                                     | <span data-ttu-id="4f15d-126">Observações</span><span class="sxs-lookup"><span data-stu-id="4f15d-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f15d-127">Interface do usuário \_ PKEY \_ habilitada</span><span class="sxs-lookup"><span data-stu-id="4f15d-127">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                       | <span data-ttu-id="4f15d-128">Dá suporte a [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="4f15d-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="4f15d-129">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="4f15d-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="4f15d-130">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="4f15d-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="4f15d-131">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="4f15d-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="4f15d-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="4f15d-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="4f15d-133">\_TooltipDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="4f15d-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="4f15d-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="4f15d-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="4f15d-135">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="4f15d-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="4f15d-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="4f15d-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="4f15d-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f15d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f15d-138">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="4f15d-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="4f15d-139">**Elemento de marcação de menu**</span><span class="sxs-lookup"><span data-stu-id="4f15d-139">**MenuGroup markup element**</span></span>](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 