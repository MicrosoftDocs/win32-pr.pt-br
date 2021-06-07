---
title: Elemento DropDownButton
description: Representa um controle de botão de Drop-Down padrão.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Faixa de DropDownButton do elemento do Windows
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a42b8ffb6d39c1da8993972c0b25995f778bdaca
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442957"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="4aea0-104">Elemento DropDownButton</span><span class="sxs-lookup"><span data-stu-id="4aea0-104">DropDownButton element</span></span>

<span data-ttu-id="4aea0-105">Representa um controle de [botão suspenso](windowsribbon-controls-dropdownbutton.md) padrão.</span><span class="sxs-lookup"><span data-stu-id="4aea0-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="4aea0-106">Uso</span><span class="sxs-lookup"><span data-stu-id="4aea0-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="4aea0-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="4aea0-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4aea0-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="4aea0-108">Attribute</span></span></th>
<th><span data-ttu-id="4aea0-109">Type</span><span class="sxs-lookup"><span data-stu-id="4aea0-109">Type</span></span></th>
<th><span data-ttu-id="4aea0-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4aea0-110">Required</span></span></th>
<th><span data-ttu-id="4aea0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4aea0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4aea0-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="4aea0-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="4aea0-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="4aea0-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="4aea0-114">Não</span><span class="sxs-lookup"><span data-stu-id="4aea0-114">No</span></span><br/></td>
<td><span data-ttu-id="4aea0-115">Válido somente se o <a href="windowsribbon-element-menugroup.md"><strong>MyMenu</strong></a> for o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="4aea0-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="4aea0-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="4aea0-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4aea0-117">Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="4aea0-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="4aea0-118">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="4aea0-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="4aea0-119">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4aea0-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4aea0-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="4aea0-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="4aea0-121">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="4aea0-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="4aea0-122">Não</span><span class="sxs-lookup"><span data-stu-id="4aea0-122">No</span></span><br/></td>
<td><span data-ttu-id="4aea0-123">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4aea0-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="4aea0-124">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="4aea0-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4aea0-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="4aea0-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="4aea0-126">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="4aea0-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="4aea0-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4aea0-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="4aea0-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4aea0-128">Child elements</span></span>



| <span data-ttu-id="4aea0-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="4aea0-129">Element</span></span>                                                                             | <span data-ttu-id="4aea0-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="4aea0-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="4aea0-131">**Botão**</span><span class="sxs-lookup"><span data-stu-id="4aea0-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="4aea0-132">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="4aea0-133">**Verificação**</span><span class="sxs-lookup"><span data-stu-id="4aea0-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="4aea0-134">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="4aea0-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="4aea0-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="4aea0-136">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="4aea0-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="4aea0-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="4aea0-138">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="4aea0-139">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="4aea0-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="4aea0-140">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="4aea0-141">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="4aea0-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="4aea0-142">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="4aea0-143">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="4aea0-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="4aea0-144">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="4aea0-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="4aea0-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="4aea0-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="4aea0-146">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="4aea0-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="4aea0-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="4aea0-148">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="4aea0-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="4aea0-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="4aea0-150">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="4aea0-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4aea0-151">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4aea0-151">Parent elements</span></span>



| <span data-ttu-id="4aea0-152">Elemento</span><span class="sxs-lookup"><span data-stu-id="4aea0-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="4aea0-153">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="4aea0-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="4aea0-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="4aea0-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="4aea0-155">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="4aea0-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="4aea0-156">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="4aea0-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="4aea0-157">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="4aea0-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="4aea0-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="4aea0-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="4aea0-159">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="4aea0-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4aea0-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="4aea0-160">Remarks</span></span>

<span data-ttu-id="4aea0-161">Opcional ou obrigatório, dependendo do elemento pai.</span><span class="sxs-lookup"><span data-stu-id="4aea0-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="4aea0-162">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md)Group **, DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="4aea0-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="4aea0-163">O **DropDownButton** dá suporte a [modos de aplicativo](ribbon-applicationmodes.md) quando ele está hospedado na coluna à esquerda do menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4aea0-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="4aea0-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) e [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) não são elementos filho válidos de **DropDownButton** quando **DropDownButton** é um descendente de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="4aea0-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4aea0-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4aea0-165">Examples</span></span>

<span data-ttu-id="4aea0-166">O exemplo a seguir demonstra a marcação básica para o **DropDownButton**.</span><span class="sxs-lookup"><span data-stu-id="4aea0-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="4aea0-167">Esta seção de código mostra as declarações de comando **DropDownButton** , com um [**grupo**](windowsribbon-element-group.md) associado que funciona como o contêiner pai para o elemento **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="4aea0-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



<span data-ttu-id="4aea0-168">Esta seção de código mostra as declarações de controle **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="4aea0-168">This section of code shows the **DropDownButton** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="4aea0-169">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4aea0-169">Element information</span></span>

* <span data-ttu-id="4aea0-170">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="4aea0-170">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="4aea0-171">**Pode estar vazio**: não</span><span class="sxs-lookup"><span data-stu-id="4aea0-171">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="4aea0-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="4aea0-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aea0-173">Controle do botão suspenso</span><span class="sxs-lookup"><span data-stu-id="4aea0-173">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="4aea0-174">**Setmodos**</span><span class="sxs-lookup"><span data-stu-id="4aea0-174">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

