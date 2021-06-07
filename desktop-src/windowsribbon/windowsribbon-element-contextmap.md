---
title: Elemento ContextMap
description: Representa um mapeamento de par ContextMenu e Minibarra.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- Faixa de ContextMap do elemento do Windows
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4754fc75ca09e39cdc7eabbeae2a0a2d2630c31f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443007"
---
# <a name="contextmap-element"></a><span data-ttu-id="d3c9a-104">Elemento ContextMap</span><span class="sxs-lookup"><span data-stu-id="d3c9a-104">ContextMap element</span></span>

<span data-ttu-id="d3c9a-105">Representa um mapeamento de par [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**Minibarra**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="d3c9a-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="d3c9a-106">Uso</span><span class="sxs-lookup"><span data-stu-id="d3c9a-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="d3c9a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="d3c9a-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3c9a-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="d3c9a-108">Attribute</span></span></th>
<th><span data-ttu-id="d3c9a-109">Type</span><span class="sxs-lookup"><span data-stu-id="d3c9a-109">Type</span></span></th>
<th><span data-ttu-id="d3c9a-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d3c9a-110">Required</span></span></th>
<th><span data-ttu-id="d3c9a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3c9a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3c9a-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d3c9a-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d3c9a-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="d3c9a-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d3c9a-114">Não</span><span class="sxs-lookup"><span data-stu-id="d3c9a-114">No</span></span><br/></td>
<td><span data-ttu-id="d3c9a-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d3c9a-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="d3c9a-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d3c9a-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d3c9a-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d3c9a-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3c9a-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="d3c9a-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="d3c9a-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="d3c9a-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="d3c9a-122">Não</span><span class="sxs-lookup"><span data-stu-id="d3c9a-122">No</span></span><br/></td>
<td><span data-ttu-id="d3c9a-123">Deve corresponder a um <em>nome</em>de <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> existente.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="d3c9a-124">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="d3c9a-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d3c9a-125">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3c9a-126"><strong>Minibarra</strong></span><span class="sxs-lookup"><span data-stu-id="d3c9a-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="d3c9a-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="d3c9a-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="d3c9a-128">Não</span><span class="sxs-lookup"><span data-stu-id="d3c9a-128">No</span></span><br/></td>
<td><span data-ttu-id="d3c9a-129">Deve corresponder a um <em>nome</em>de <a href="windowsribbon-element-minitoolbar.md"><strong>Minibarra</strong></a> existente.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="d3c9a-130">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="d3c9a-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d3c9a-131">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d3c9a-132">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d3c9a-132">Child elements</span></span>

<span data-ttu-id="d3c9a-133">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d3c9a-134">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="d3c9a-134">Parent elements</span></span>



| <span data-ttu-id="d3c9a-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="d3c9a-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3c9a-136">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="d3c9a-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d3c9a-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3c9a-137">Remarks</span></span>

<span data-ttu-id="d3c9a-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d3c9a-138">Optional.</span></span>

<span data-ttu-id="d3c9a-139">Pode ocorrer uma ou mais vezes para cada [**ContextPopup. ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span><span class="sxs-lookup"><span data-stu-id="d3c9a-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d3c9a-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d3c9a-140">Examples</span></span>

<span data-ttu-id="d3c9a-141">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="d3c9a-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="d3c9a-142">Esta seção de código mostra um conjunto de declarações de controle **ContextMap** .</span><span class="sxs-lookup"><span data-stu-id="d3c9a-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d3c9a-143">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d3c9a-143">Element information</span></span>


* <span data-ttu-id="d3c9a-144">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3c9a-144">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d3c9a-145">**Pode estar vazio**: Sim</span><span class="sxs-lookup"><span data-stu-id="d3c9a-145">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="d3c9a-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3c9a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c9a-147">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="d3c9a-147">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





