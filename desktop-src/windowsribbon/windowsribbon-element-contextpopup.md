---
title: Elemento ContextPopup
description: Representa o controle Popup de contexto na exibição ContextPopup.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- Faixa de ContextPopup do elemento do Windows
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4feb7c4fbd2ca538fe4d0c2b2584163ee8c9fcea
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006590"
---
# <a name="contextpopup-element"></a><span data-ttu-id="9b6f1-104">Elemento ContextPopup</span><span class="sxs-lookup"><span data-stu-id="9b6f1-104">ContextPopup element</span></span>

<span data-ttu-id="9b6f1-105">Representa o controle [Popup de contexto](windowsribbon-controls-contextpopup.md) na exibição ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="9b6f1-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="9b6f1-106">Uso</span><span class="sxs-lookup"><span data-stu-id="9b6f1-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="9b6f1-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="9b6f1-107">Attributes</span></span>

<span data-ttu-id="9b6f1-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="9b6f1-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9b6f1-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9b6f1-109">Child elements</span></span>



| <span data-ttu-id="9b6f1-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="9b6f1-110">Element</span></span>                                                                                         | <span data-ttu-id="9b6f1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b6f1-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="9b6f1-112">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="9b6f1-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="9b6f1-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="9b6f1-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="9b6f1-114">**ContextPopup. ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="9b6f1-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="9b6f1-115">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="9b6f1-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="9b6f1-116">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="9b6f1-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="9b6f1-117">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="9b6f1-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="9b6f1-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9b6f1-118">Parent elements</span></span>



| <span data-ttu-id="9b6f1-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="9b6f1-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="9b6f1-120">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="9b6f1-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="9b6f1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b6f1-121">Remarks</span></span>

<span data-ttu-id="9b6f1-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9b6f1-122">Optional.</span></span>

<span data-ttu-id="9b6f1-123">Pode ocorrer no máximo uma vez para cada [**Application. views**](windowsribbon-element-application-views.md).</span><span class="sxs-lookup"><span data-stu-id="9b6f1-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9b6f1-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9b6f1-124">Examples</span></span>

<span data-ttu-id="9b6f1-125">O exemplo a seguir demonstra a marcação básica para uma exibição **ContextPopup** .</span><span class="sxs-lookup"><span data-stu-id="9b6f1-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="9b6f1-126">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9b6f1-126">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="9b6f1-127">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b6f1-127">Minimum supported system</span></span><br/> | <span data-ttu-id="9b6f1-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b6f1-128">Windows 7</span></span> |
| <span data-ttu-id="9b6f1-129">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="9b6f1-129">Can be empty</span></span>                        | <span data-ttu-id="9b6f1-130">Não</span><span class="sxs-lookup"><span data-stu-id="9b6f1-130">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="9b6f1-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b6f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6f1-132">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="9b6f1-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





