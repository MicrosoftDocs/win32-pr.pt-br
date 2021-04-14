---
title: Propriedade ContextPopup. MiniToolbars
description: Representa um contêiner para elementos Minibarra.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- Faixa de ContextPopup de propriedades do Windows. MiniToolbars
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e85e6b170b4b7408a17687bd26725e9183161
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455777"
---
# <a name="contextpopupminitoolbars-property"></a><span data-ttu-id="c9f05-104">Propriedade ContextPopup. MiniToolbars</span><span class="sxs-lookup"><span data-stu-id="c9f05-104">ContextPopup.MiniToolbars property</span></span>

<span data-ttu-id="c9f05-105">Representa um contêiner para elementos [**Minibarra**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f05-105">Represents a container for [**MiniToolbar**](windowsribbon-element-minitoolbar.md) elements.</span></span>

## <a name="usage"></a><span data-ttu-id="c9f05-106">Uso</span><span class="sxs-lookup"><span data-stu-id="c9f05-106">Usage</span></span>

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a><span data-ttu-id="c9f05-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9f05-107">Attributes</span></span>

<span data-ttu-id="c9f05-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="c9f05-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c9f05-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c9f05-109">Child elements</span></span>



| <span data-ttu-id="c9f05-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9f05-110">Element</span></span>                                                             | <span data-ttu-id="c9f05-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9f05-111">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c9f05-112">**Minibarra**</span><span class="sxs-lookup"><span data-stu-id="c9f05-112">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/> | <span data-ttu-id="c9f05-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="c9f05-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c9f05-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c9f05-114">Parent elements</span></span>



| <span data-ttu-id="c9f05-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="c9f05-115">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="c9f05-116">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="c9f05-116">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c9f05-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9f05-117">Remarks</span></span>

<span data-ttu-id="c9f05-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c9f05-118">Optional.</span></span>

<span data-ttu-id="c9f05-119">Pode ocorrer no máximo uma vez para cada [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="c9f05-119">May occur at most once for each [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="c9f05-120">Como os controles em [**Minibarra**](windowsribbon-element-minitoolbar.md) não são acessíveis por teclado, os comandos que eles expõem devem estar disponíveis em outro lugar na interface do usuário da faixa de da.</span><span class="sxs-lookup"><span data-stu-id="c9f05-120">Because controls in the [**MiniToolbar**](windowsribbon-element-minitoolbar.md) are not keyboard accessible, the Commands they expose should be available elsewhere in the Ribbon UI.</span></span>

## <a name="examples"></a><span data-ttu-id="c9f05-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9f05-121">Examples</span></span>

<span data-ttu-id="c9f05-122">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f05-122">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="c9f05-123">Esta seção de código mostra a declaração de controle **ContextPopup. MiniToolbars** .</span><span class="sxs-lookup"><span data-stu-id="c9f05-123">This section of code shows the **ContextPopup.MiniToolbars** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c9f05-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9f05-124">Requirements</span></span>



| <span data-ttu-id="c9f05-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9f05-125">Requirement</span></span> | <span data-ttu-id="c9f05-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f05-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c9f05-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9f05-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f05-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c9f05-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c9f05-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9f05-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f05-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="c9f05-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9f05-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9f05-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f05-132">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="c9f05-132">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





