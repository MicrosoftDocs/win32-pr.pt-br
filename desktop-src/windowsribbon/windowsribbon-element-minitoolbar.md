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
ms.openlocfilehash: ceea8ba1a220674f177e740411bf98a13d7bfc2e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443257"
---
# <a name="minitoolbar-element"></a><span data-ttu-id="d7d25-104">Elemento Minibarra</span><span class="sxs-lookup"><span data-stu-id="d7d25-104">MiniToolbar element</span></span>

<span data-ttu-id="d7d25-105">Representa uma barra de ferramentas contextual.</span><span class="sxs-lookup"><span data-stu-id="d7d25-105">Represents a contextual toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="d7d25-106">Uso</span><span class="sxs-lookup"><span data-stu-id="d7d25-106">Usage</span></span>

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a><span data-ttu-id="d7d25-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7d25-107">Attributes</span></span>



| <span data-ttu-id="d7d25-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="d7d25-108">Attribute</span></span>           | <span data-ttu-id="d7d25-109">Type</span><span class="sxs-lookup"><span data-stu-id="d7d25-109">Type</span></span>                 | <span data-ttu-id="d7d25-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d7d25-110">Required</span></span>       | <span data-ttu-id="d7d25-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7d25-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d25-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d7d25-112">**Name**</span></span><br/> | <span data-ttu-id="d7d25-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d7d25-113">xs:string</span></span><br/> | <span data-ttu-id="d7d25-114">Sim</span><span class="sxs-lookup"><span data-stu-id="d7d25-114">Yes</span></span><br/> | <span data-ttu-id="d7d25-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="d7d25-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d7d25-116">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="d7d25-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="d7d25-117">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d7d25-117">Child elements</span></span>



| <span data-ttu-id="d7d25-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7d25-118">Element</span></span>                                                         | <span data-ttu-id="d7d25-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7d25-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="d7d25-120">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="d7d25-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="d7d25-121">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="d7d25-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d7d25-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d7d25-122">Parent elements</span></span>



| <span data-ttu-id="d7d25-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7d25-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7d25-124">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="d7d25-124">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d7d25-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7d25-125">Remarks</span></span>

<span data-ttu-id="d7d25-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d7d25-126">Optional.</span></span>

<span data-ttu-id="d7d25-127">Pode ocorrer uma ou mais vezes para cada [**ContextPopup. MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span><span class="sxs-lookup"><span data-stu-id="d7d25-127">May occur one or more times for each [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).</span></span>

<span data-ttu-id="d7d25-128">Ao contrário do elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , o **Minibarra** permanece visível quando um item na barra de ferramentas é clicado.</span><span class="sxs-lookup"><span data-stu-id="d7d25-128">Unlike the [**ContextMenu**](windowsribbon-element-contextmenu.md) element, the **MiniToolbar** remains visible when an item on the toolbar is clicked.</span></span>

<span data-ttu-id="d7d25-129">Se exibido sem um [**ContextMenu**](windowsribbon-element-contextmenu.md), o **Minibarra** esmaece à medida que o ponteiro do mouse é movido para fora.</span><span class="sxs-lookup"><span data-stu-id="d7d25-129">If displayed without a [**ContextMenu**](windowsribbon-element-contextmenu.md), the **MiniToolbar** fades as the mouse pointer is moved away.</span></span>

> [!Note]  
> <span data-ttu-id="d7d25-130">Devido a esse comportamento de esmaecimento, um [**ContextMenu**](windowsribbon-element-contextmenu.md) deve ser exibido em proximidade com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="d7d25-130">Due to this fading behavior, a [**ContextMenu**](windowsribbon-element-contextmenu.md) should be displayed in close proximity to the mouse pointer.</span></span>

 

<span data-ttu-id="d7d25-131">Como os controles em **Minibarra** não são acessíveis por teclado, os comandos que eles expõem devem estar disponíveis em outro lugar na interface do usuário da faixa de da.</span><span class="sxs-lookup"><span data-stu-id="d7d25-131">Because controls in the **MiniToolbar** are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="d7d25-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7d25-132">Examples</span></span>

<span data-ttu-id="d7d25-133">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d25-133">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="d7d25-134">Esta seção de código mostra um conjunto de declarações de controle **Minibarra** .</span><span class="sxs-lookup"><span data-stu-id="d7d25-134">This section of code shows a set of **MiniToolbar** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d7d25-135">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d7d25-135">Element information</span></span>

* <span data-ttu-id="d7d25-136">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7d25-136">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d7d25-137">**Pode estar vazio**: não</span><span class="sxs-lookup"><span data-stu-id="d7d25-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="d7d25-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7d25-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d25-139">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="d7d25-139">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





