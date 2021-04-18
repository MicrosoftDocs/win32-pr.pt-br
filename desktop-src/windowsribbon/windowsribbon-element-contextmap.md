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
ms.openlocfilehash: e2ddcc8bdea16f5e00974b2b2e58934941e44c68
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "105764513"
---
# <a name="contextmap-element"></a><span data-ttu-id="79636-104">Elemento ContextMap</span><span class="sxs-lookup"><span data-stu-id="79636-104">ContextMap element</span></span>

<span data-ttu-id="79636-105">Representa um mapeamento de par [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**Minibarra**](windowsribbon-element-minitoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="79636-105">Represents a [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) pair mapping.</span></span>

## <a name="usage"></a><span data-ttu-id="79636-106">Uso</span><span class="sxs-lookup"><span data-stu-id="79636-106">Usage</span></span>

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="79636-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="79636-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79636-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="79636-108">Attribute</span></span></th>
<th><span data-ttu-id="79636-109">Type</span><span class="sxs-lookup"><span data-stu-id="79636-109">Type</span></span></th>
<th><span data-ttu-id="79636-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="79636-110">Required</span></span></th>
<th><span data-ttu-id="79636-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="79636-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79636-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="79636-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="79636-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="79636-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="79636-114">Não</span><span class="sxs-lookup"><span data-stu-id="79636-114">No</span></span><br/></td>
<td><span data-ttu-id="79636-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79636-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="79636-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="79636-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="79636-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79636-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="79636-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="79636-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="79636-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="79636-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79636-120"><strong>ContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="79636-120"><strong>ContextMenu</strong></span></span><br/></td>
<td><span data-ttu-id="79636-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="79636-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="79636-122">Não</span><span class="sxs-lookup"><span data-stu-id="79636-122">No</span></span><br/></td>
<td><span data-ttu-id="79636-123">Deve corresponder a um <em>nome</em>de <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> existente.</span><span class="sxs-lookup"><span data-stu-id="79636-123">Must correspond to an existing <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="79636-124">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="79636-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="79636-125">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="79636-125">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79636-126"><strong>Minibarra</strong></span><span class="sxs-lookup"><span data-stu-id="79636-126"><strong>MiniToolbar</strong></span></span><br/></td>
<td><span data-ttu-id="79636-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="79636-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="79636-128">Não</span><span class="sxs-lookup"><span data-stu-id="79636-128">No</span></span><br/></td>
<td><span data-ttu-id="79636-129">Deve corresponder a um <em>nome</em>de <a href="windowsribbon-element-minitoolbar.md"><strong>Minibarra</strong></a> existente.</span><span class="sxs-lookup"><span data-stu-id="79636-129">Must correspond to an existing <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> <em>Name</em>.</span></span><br/> <br/><span data-ttu-id="79636-130">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="79636-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="79636-131">Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="79636-131">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="79636-132">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="79636-132">Child elements</span></span>

<span data-ttu-id="79636-133">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="79636-133">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="79636-134">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="79636-134">Parent elements</span></span>



| <span data-ttu-id="79636-135">Elemento</span><span class="sxs-lookup"><span data-stu-id="79636-135">Element</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79636-136">**ContextPopup.ContextMaps**</span><span class="sxs-lookup"><span data-stu-id="79636-136">**ContextPopup.ContextMaps**</span></span>](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="79636-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="79636-137">Remarks</span></span>

<span data-ttu-id="79636-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="79636-138">Optional.</span></span>

<span data-ttu-id="79636-139">Pode ocorrer uma ou mais vezes para cada [**ContextPopup. ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span><span class="sxs-lookup"><span data-stu-id="79636-139">May occur one or more times for each [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md).</span></span>

## <a name="examples"></a><span data-ttu-id="79636-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="79636-140">Examples</span></span>

<span data-ttu-id="79636-141">O exemplo a seguir demonstra a marcação básica para uma exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="79636-141">The following example demonstrates the basic markup for a [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span>

<span data-ttu-id="79636-142">Esta seção de código mostra um conjunto de declarações de controle **ContextMap** .</span><span class="sxs-lookup"><span data-stu-id="79636-142">This section of code shows a set of **ContextMap** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="79636-143">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="79636-143">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="79636-144">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79636-144">Minimum supported system</span></span><br/> | <span data-ttu-id="79636-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79636-145">Windows 7</span></span> |
| <span data-ttu-id="79636-146">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="79636-146">Can be empty</span></span>                        | <span data-ttu-id="79636-147">Sim</span><span class="sxs-lookup"><span data-stu-id="79636-147">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="79636-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="79636-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79636-149">Controle Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="79636-149">Context Popup control</span></span>](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





