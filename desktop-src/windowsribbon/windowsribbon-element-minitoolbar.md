---
title: Elemento Minibarra
description: Representa uma barra de ferramentas contextual.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Faixa de Minibarra do elemento do Windows
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb5e4a27d10fe5233f8e7059bc9da8ecfd2fa383
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084143"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="fbe9e-104">Elemento Minibarra</span><span class="sxs-lookup"><span data-stu-id="fbe9e-104">MiniToolbar element</span></span>

<span data-ttu-id="fbe9e-105">Representa uma barra de ferramentas contextual.</span><span class="sxs-lookup"><span data-stu-id="fbe9e-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="fbe9e-106">Uso</span><span class="sxs-lookup"><span data-stu-id="fbe9e-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="fbe9e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbe9e-107">Attributes</span></span>



| <span data-ttu-id="fbe9e-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="fbe9e-108">Attribute</span></span>           | <span data-ttu-id="fbe9e-109">Type</span><span class="sxs-lookup"><span data-stu-id="fbe9e-109">Type</span></span>                 | <span data-ttu-id="fbe9e-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbe9e-110">Required</span></span>       | <span data-ttu-id="fbe9e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbe9e-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe9e-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fbe9e-112">**Name**</span></span><br/> | <span data-ttu-id="fbe9e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="fbe9e-113">xs:string</span></span><br/> | <span data-ttu-id="fbe9e-114">Yes</span><span class="sxs-lookup"><span data-stu-id="fbe9e-114">Yes</span></span><br/> | <span data-ttu-id="fbe9e-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fbe9e-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fbe9e-116">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="fbe9e-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="fbe9e-117">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fbe9e-117">Child elements</span></span>



| <span data-ttu-id="fbe9e-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="fbe9e-118">Element</span></span>                                                         | <span data-ttu-id="fbe9e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbe9e-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="fbe9e-120">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="fbe9e-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="fbe9e-121">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="fbe9e-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fbe9e-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fbe9e-122">Parent elements</span></span>



| <span data-ttu-id="fbe9e-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="fbe9e-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbe9e-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="fbe9e-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fbe9e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbe9e-125">Remarks</span></span>

<span data-ttu-id="fbe9e-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fbe9e-126">Optional.</span></span>

<span data-ttu-id="fbe9e-127">Pode ocorrer uma ou mais vezes para cada [**ContextPopup. MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="fbe9e-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="fbe9e-128">Ao contrário do elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , o **Minibarra** permanece visível quando um item na barra de ferramentas é clicado.</span><span class="sxs-lookup"><span data-stu-id="fbe9e-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="fbe9e-129">Se exibido sem um [**ContextMenu**](windowsribbon-element-contextmenu.md), o **Minibarra** esmaece à medida que o ponteiro do mouse é movido para fora.</span><span class="sxs-lookup"><span data-stu-id="fbe9e-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="fbe9e-130">Devido a esse comportamento de esmaecimento, um [**ContextMenu**](windowsribbon-element-contextmenu.md) deve ser exibido em proximidade com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="fbe9e-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="fbe9e-131">Como os controles em **Minibarra** não são acessíveis por teclado, os comandos que eles expõem devem estar disponíveis em outro lugar na interface do usuário da faixa de da.</span><span class="sxs-lookup"><span data-stu-id="fbe9e-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="fbe9e-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fbe9e-132">Examples</span></span>

<span data-ttu-id="fbe9e-133">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="fbe9e-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="fbe9e-134">Esta seção de código mostra um conjunto de declarações de controle **Minibarra** .</span><span class="sxs-lookup"><span data-stu-id="fbe9e-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a><span data-ttu-id="fbe9e-135">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="fbe9e-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="fbe9e-136">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbe9e-136">Minimum supported system</span></span><br/> | <span data-ttu-id="fbe9e-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbe9e-137">Windows 7</span></span> |
| <span data-ttu-id="fbe9e-138">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="fbe9e-138">Can be empty</span></span>                        | <span data-ttu-id="fbe9e-139">Não</span><span class="sxs-lookup"><span data-stu-id="fbe9e-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="fbe9e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbe9e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe9e-141">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="fbe9e-141">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





