---
title: Elemento ContextMenu
description: Representa um controle de menu de contexto.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- Faixa de das janelas do elemento ContextMenu
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c824e87c063fb863e79f10cb9755b74df36023f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638528"
---
# <a name="contextmenu-element"></a><span data-ttu-id="2eb67-104">Elemento ContextMenu</span><span class="sxs-lookup"><span data-stu-id="2eb67-104">ContextMenu element</span></span>

<span data-ttu-id="2eb67-105">Representa um controle de menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="2eb67-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="2eb67-106">Uso</span><span class="sxs-lookup"><span data-stu-id="2eb67-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="2eb67-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2eb67-107">Attributes</span></span>



| <span data-ttu-id="2eb67-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="2eb67-108">Attribute</span></span>           | <span data-ttu-id="2eb67-109">Type</span><span class="sxs-lookup"><span data-stu-id="2eb67-109">Type</span></span>                 | <span data-ttu-id="2eb67-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2eb67-110">Required</span></span>       | <span data-ttu-id="2eb67-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2eb67-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb67-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2eb67-112">**Name**</span></span><br/> | <span data-ttu-id="2eb67-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="2eb67-113">xs:string</span></span><br/> | <span data-ttu-id="2eb67-114">Sim</span><span class="sxs-lookup"><span data-stu-id="2eb67-114">Yes</span></span><br/> | <span data-ttu-id="2eb67-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="2eb67-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2eb67-116">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="2eb67-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="2eb67-117">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2eb67-117">Child elements</span></span>



| <span data-ttu-id="2eb67-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="2eb67-118">Element</span></span>                                                         | <span data-ttu-id="2eb67-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="2eb67-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="2eb67-120">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="2eb67-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="2eb67-121">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="2eb67-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2eb67-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2eb67-122">Parent elements</span></span>



| <span data-ttu-id="2eb67-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="2eb67-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2eb67-124">**ContextPopup. ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="2eb67-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2eb67-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eb67-125">Remarks</span></span>

<span data-ttu-id="2eb67-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2eb67-126">Optional.</span></span>

<span data-ttu-id="2eb67-127">Pode ocorrer uma ou mais vezes para cada [**ContextPopup. ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="2eb67-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2eb67-128">Um **ContextMenu** não pode hospedar controles de [caixa de combinação](windowsribbon-controls-combobox.md) ou [controle giratório](windowsribbon-controls-spinner.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb67-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2eb67-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2eb67-129">Examples</span></span>

<span data-ttu-id="2eb67-130">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb67-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="2eb67-131">Esta seção de código mostra um conjunto de declarações de controle **ContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="2eb67-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2eb67-132">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2eb67-132">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2eb67-133">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eb67-133">Minimum supported system</span></span><br/> | <span data-ttu-id="2eb67-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2eb67-134">Windows 7</span></span> |
| <span data-ttu-id="2eb67-135">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="2eb67-135">Can be empty</span></span>                        | <span data-ttu-id="2eb67-136">Não</span><span class="sxs-lookup"><span data-stu-id="2eb67-136">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="2eb67-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2eb67-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb67-138">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="2eb67-138">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





