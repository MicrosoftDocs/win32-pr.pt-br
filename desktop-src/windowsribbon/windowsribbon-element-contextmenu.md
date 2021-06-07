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
ms.openlocfilehash: 916a031ed642a76fb22ecc58dbbe1ce29cbcd105
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443458"
---
# <a name="contextmenu-element"></a><span data-ttu-id="f2c8a-104">Elemento ContextMenu</span><span class="sxs-lookup"><span data-stu-id="f2c8a-104">ContextMenu element</span></span>

<span data-ttu-id="f2c8a-105">Representa um controle de menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="f2c8a-105">Represents a context menu control.</span></span>

## <a name="usage"></a><span data-ttu-id="f2c8a-106">Uso</span><span class="sxs-lookup"><span data-stu-id="f2c8a-106">Usage</span></span>

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a><span data-ttu-id="f2c8a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="f2c8a-107">Attributes</span></span>



| <span data-ttu-id="f2c8a-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="f2c8a-108">Attribute</span></span>           | <span data-ttu-id="f2c8a-109">Type</span><span class="sxs-lookup"><span data-stu-id="f2c8a-109">Type</span></span>                 | <span data-ttu-id="f2c8a-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f2c8a-110">Required</span></span>       | <span data-ttu-id="f2c8a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2c8a-111">Description</span></span>                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c8a-112">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f2c8a-112">**Name**</span></span><br/> | <span data-ttu-id="f2c8a-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="f2c8a-113">xs:string</span></span><br/> | <span data-ttu-id="f2c8a-114">Sim</span><span class="sxs-lookup"><span data-stu-id="f2c8a-114">Yes</span></span><br/> | <span data-ttu-id="f2c8a-115"><dt> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="f2c8a-115"><dt> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f2c8a-116">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="f2c8a-116">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="f2c8a-117">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f2c8a-117">Child elements</span></span>



| <span data-ttu-id="f2c8a-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="f2c8a-118">Element</span></span>                                                         | <span data-ttu-id="f2c8a-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2c8a-119">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="f2c8a-120">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="f2c8a-120">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="f2c8a-121">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="f2c8a-121">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f2c8a-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f2c8a-122">Parent elements</span></span>



| <span data-ttu-id="f2c8a-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="f2c8a-123">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2c8a-124">**ContextPopup. ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="f2c8a-124">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f2c8a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2c8a-125">Remarks</span></span>

<span data-ttu-id="f2c8a-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f2c8a-126">Optional.</span></span>

<span data-ttu-id="f2c8a-127">Pode ocorrer uma ou mais vezes para cada [**ContextPopup. ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span><span class="sxs-lookup"><span data-stu-id="f2c8a-127">May occur one or more times for each [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2c8a-128">Um **ContextMenu** não pode hospedar controles de [caixa de combinação](windowsribbon-controls-combobox.md) ou [controle giratório](windowsribbon-controls-spinner.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c8a-128">A **ContextMenu** cannot host [Combo Box](windowsribbon-controls-combobox.md) or [Spinner](windowsribbon-controls-spinner.md) controls.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f2c8a-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2c8a-129">Examples</span></span>

<span data-ttu-id="f2c8a-130">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c8a-130">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="f2c8a-131">Esta seção de código mostra um conjunto de declarações de controle **ContextMenu** .</span><span class="sxs-lookup"><span data-stu-id="f2c8a-131">This section of code shows a set of **ContextMenu** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="f2c8a-132">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f2c8a-132">Element information</span></span>

* <span data-ttu-id="f2c8a-133">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2c8a-133">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="f2c8a-134">**Pode estar vazio**: não</span><span class="sxs-lookup"><span data-stu-id="f2c8a-134">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="f2c8a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2c8a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c8a-136">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="f2c8a-136">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





