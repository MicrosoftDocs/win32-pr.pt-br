---
title: Elemento SplitButton
description: Representa um controle de botão de divisão padrão.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Faixa de das janelas do elemento SplitButton
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf03d85dd0402548d02f107dafb209b68c13bb72
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444397"
---
# <a name="splitbutton-element"></a><span data-ttu-id="a0089-104">Elemento SplitButton</span><span class="sxs-lookup"><span data-stu-id="a0089-104">SplitButton element</span></span>

<span data-ttu-id="a0089-105">Representa um controle de [botão de divisão](windowsribbon-controls-splitbutton.md) padrão.</span><span class="sxs-lookup"><span data-stu-id="a0089-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="a0089-106">Uso</span><span class="sxs-lookup"><span data-stu-id="a0089-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="a0089-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0089-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0089-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="a0089-108">Attribute</span></span></th>
<th><span data-ttu-id="a0089-109">Type</span><span class="sxs-lookup"><span data-stu-id="a0089-109">Type</span></span></th>
<th><span data-ttu-id="a0089-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a0089-110">Required</span></span></th>
<th><span data-ttu-id="a0089-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0089-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0089-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="a0089-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="a0089-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="a0089-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="a0089-114">Não</span><span class="sxs-lookup"><span data-stu-id="a0089-114">No</span></span><br/></td>
<td><span data-ttu-id="a0089-115">Válido somente se o <a href="windowsribbon-element-menugroup.md"><strong>MyMenu</strong></a> for o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="a0089-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="a0089-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="a0089-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0089-117">Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="a0089-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="a0089-118">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="a0089-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="a0089-119">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0089-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0089-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="a0089-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="a0089-121">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="a0089-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="a0089-122">Não</span><span class="sxs-lookup"><span data-stu-id="a0089-122">No</span></span><br/></td>
<td><span data-ttu-id="a0089-123">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a0089-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="a0089-124">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="a0089-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="a0089-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="a0089-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="a0089-126">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="a0089-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="a0089-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0089-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="a0089-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a0089-128">Child elements</span></span>



| <span data-ttu-id="a0089-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0089-129">Element</span></span>                                                                                   | <span data-ttu-id="a0089-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0089-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a0089-131">**Botão**</span><span class="sxs-lookup"><span data-stu-id="a0089-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="a0089-132">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0089-133">**Verificação**</span><span class="sxs-lookup"><span data-stu-id="a0089-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="a0089-134">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0089-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="a0089-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="a0089-136">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0089-137">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="a0089-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="a0089-138">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0089-139">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="a0089-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="a0089-140">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="a0089-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a0089-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="a0089-142">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0089-143">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="a0089-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="a0089-144">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="a0089-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="a0089-145">**SplitButton. MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="a0089-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="a0089-146">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="a0089-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="a0089-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="a0089-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="a0089-148">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="a0089-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="a0089-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="a0089-150">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="a0089-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a0089-151">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a0089-151">Parent elements</span></span>



| <span data-ttu-id="a0089-152">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0089-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a0089-153">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="a0089-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="a0089-154">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="a0089-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="a0089-155">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a0089-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="a0089-156">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="a0089-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="a0089-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a0089-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="a0089-158">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="a0089-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a0089-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0089-159">Remarks</span></span>

<span data-ttu-id="a0089-160">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a0089-160">Optional.</span></span>

<span data-ttu-id="a0089-161">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md), **SplitButton** ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="a0089-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="a0089-162">**SplitButton** dá suporte a [modos de aplicativo](ribbon-applicationmodes.md) quando ele está hospedado na coluna à esquerda do menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a0089-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="a0089-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) e [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) não são elementos filho válidos de [**DropDownButton**](windowsribbon-element-dropdownbutton.md) quando **DropDownButton** é um descendente de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="a0089-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="a0089-164">[**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) deve ocorrer uma vez se os seguintes não estiverem presentes como elementos filho de **SplitButton**:</span><span class="sxs-lookup"><span data-stu-id="a0089-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="a0089-165">**Botão**</span><span class="sxs-lookup"><span data-stu-id="a0089-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="a0089-166">**Verificação**</span><span class="sxs-lookup"><span data-stu-id="a0089-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="a0089-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="a0089-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="a0089-168">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="a0089-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="a0089-169">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="a0089-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="a0089-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a0089-170">**SplitButton**</span></span>
-   [<span data-ttu-id="a0089-171">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="a0089-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="a0089-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="a0089-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="a0089-173">Esses controles são tratados como elementos filho de um único elemento [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) padrão.</span><span class="sxs-lookup"><span data-stu-id="a0089-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a0089-174">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0089-174">Examples</span></span>

<span data-ttu-id="a0089-175">O exemplo a seguir demonstra a marcação básica para o [botão de divisão](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="a0089-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="a0089-176">Esta seção de código mostra as declarações de comando **SplitButton** , com um [**grupo**](windowsribbon-element-group.md) associado que funciona como o contêiner pai para o elemento **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="a0089-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="a0089-177">Esta seção de código mostra as declarações de controle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="a0089-177">This section of code shows the **SplitButton** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="a0089-178">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a0089-178">Element information</span></span>

- <span data-ttu-id="a0089-179">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0089-179">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="a0089-180">**Pode estar vazio**: não</span><span class="sxs-lookup"><span data-stu-id="a0089-180">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="a0089-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0089-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0089-182">Controle de botão de divisão</span><span class="sxs-lookup"><span data-stu-id="a0089-182">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="a0089-183">**Setmodos**</span><span class="sxs-lookup"><span data-stu-id="a0089-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

