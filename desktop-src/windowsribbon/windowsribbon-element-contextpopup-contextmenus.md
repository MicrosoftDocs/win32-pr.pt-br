---
title: Propriedade ContextPopup. ContextMenus
description: Representa um contêiner para elementos ContextMenu.
ms.assetid: 92633689-a892-421e-a5fb-e494f4cd1ea8
keywords:
- Faixa de ContextPopup. ContextMenus da propriedade Windows
topic_type:
- apiref
api_name:
- ContextPopup.ContextMenus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ef8ab053b9912f545c2aad931eb8ad9583ff62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760666"
---
# <a name="contextpopupcontextmenus-property"></a><span data-ttu-id="60593-104">Propriedade ContextPopup. ContextMenus</span><span class="sxs-lookup"><span data-stu-id="60593-104">ContextPopup.ContextMenus property</span></span>

<span data-ttu-id="60593-105">Representa um contêiner para elementos [**ContextMenu**](windowsribbon-element-contextmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="60593-105">Represents a container for [**ContextMenu**](windowsribbon-element-contextmenu.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="60593-106">Uso</span><span class="sxs-lookup"><span data-stu-id="60593-106">Usage</span></span>

``` syntax
<ContextPopup.ContextMenus>
  child elements
</ContextPopup.ContextMenus>
```

## <a name="attributes"></a><span data-ttu-id="60593-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="60593-107">Attributes</span></span>

<span data-ttu-id="60593-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="60593-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="60593-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="60593-109">Child elements</span></span>



| <span data-ttu-id="60593-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="60593-110">Element</span></span>                                                             | <span data-ttu-id="60593-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="60593-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="60593-112">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="60593-112">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/> | <span data-ttu-id="60593-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="60593-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="60593-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="60593-114">Parent elements</span></span>



| <span data-ttu-id="60593-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="60593-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="60593-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="60593-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="60593-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="60593-117">Remarks</span></span>

<span data-ttu-id="60593-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="60593-118">Optional.</span></span>

<span data-ttu-id="60593-119">Pode ocorrer no máximo uma vez para cada [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="60593-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="examples"></a><span data-ttu-id="60593-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60593-120">Examples</span></span>

<span data-ttu-id="60593-121">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="60593-121">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="60593-122">Esta seção de código mostra uma declaração de controle **ContextPopup. ContextMenus** .</span><span class="sxs-lookup"><span data-stu-id="60593-122">This section of code shows a **ContextPopup.ContextMenus** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="60593-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60593-123">Requirements</span></span>



| <span data-ttu-id="60593-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="60593-124">Requirement</span></span> | <span data-ttu-id="60593-125">Valor</span><span class="sxs-lookup"><span data-stu-id="60593-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="60593-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60593-126">Minimum supported client</span></span><br/> | <span data-ttu-id="60593-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="60593-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="60593-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60593-128">Minimum supported server</span></span><br/> | <span data-ttu-id="60593-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="60593-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60593-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="60593-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60593-131">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="60593-131">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





