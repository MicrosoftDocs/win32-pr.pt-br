---
title: Elemento ContextPopup
description: Representa o controle Pop-up de contexto na exibição ContextPopup.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- Elemento ContextPopup Da Faixa de Opções do Windows
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f779b0196d14fb42246c2a10d476352d835b6cf8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443457"
---
# <a name="contextpopup-element"></a><span data-ttu-id="ad243-104">Elemento ContextPopup</span><span class="sxs-lookup"><span data-stu-id="ad243-104">ContextPopup element</span></span>

<span data-ttu-id="ad243-105">Representa o [controle Pop-up de](windowsribbon-controls-contextpopup.md) contexto na exibição ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="ad243-105">Represents the [Context Popup](windowsribbon-controls-contextpopup.md) control in the ContextPopup View.</span></span>

## <a name="usage"></a><span data-ttu-id="ad243-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ad243-106">Usage</span></span>

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a><span data-ttu-id="ad243-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad243-107">Attributes</span></span>

<span data-ttu-id="ad243-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="ad243-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ad243-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ad243-109">Child elements</span></span>



| <span data-ttu-id="ad243-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ad243-110">Element</span></span>                                                                                         | <span data-ttu-id="ad243-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad243-111">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ad243-112">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="ad243-112">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | <span data-ttu-id="ad243-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="ad243-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="ad243-114">**ContextPopup.ContextMenus**</span><span class="sxs-lookup"><span data-stu-id="ad243-114">**ContextPopup.ContextMenus**</span></span>](windowsribbon-element-contextpopup-contextmenus.md)<br/> | <span data-ttu-id="ad243-115">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="ad243-115">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="ad243-116">**ContextPopup.MiniToolbars**</span><span class="sxs-lookup"><span data-stu-id="ad243-116">**ContextPopup.MiniToolbars**</span></span>](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | <span data-ttu-id="ad243-117">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="ad243-117">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ad243-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ad243-118">Parent elements</span></span>



| <span data-ttu-id="ad243-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="ad243-119">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="ad243-120">**Application.Views**</span><span class="sxs-lookup"><span data-stu-id="ad243-120">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ad243-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad243-121">Remarks</span></span>

<span data-ttu-id="ad243-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ad243-122">Optional.</span></span>

<span data-ttu-id="ad243-123">Pode ocorrer no máximo uma vez para cada [**Application.Views.**](windowsribbon-element-application-views.md)</span><span class="sxs-lookup"><span data-stu-id="ad243-123">May occur at most once for each [**Application.Views**](windowsribbon-element-application-views.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ad243-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad243-124">Examples</span></span>

<span data-ttu-id="ad243-125">O exemplo a seguir demonstra a marcação básica para uma **Exibição contextpopup.**</span><span class="sxs-lookup"><span data-stu-id="ad243-125">The following example demonstrates the basic markup for a **ContextPopup** View.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ad243-126">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ad243-126">Element information</span></span>

* <span data-ttu-id="ad243-127">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad243-127">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="ad243-128">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="ad243-128">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="ad243-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad243-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad243-130">Controle pop-up de contexto</span><span class="sxs-lookup"><span data-stu-id="ad243-130">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





