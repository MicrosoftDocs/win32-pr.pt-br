---
title: Elemento button (estrutura da faixa de medida do Windows)
description: Representa um controle de botão.
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Faixa de das janelas do elemento Button
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c037a598a4a853db3203162bcdbe6cd71afca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084576"
---
# <a name="button-element"></a><span data-ttu-id="1e8bc-104">Elemento Button</span><span class="sxs-lookup"><span data-stu-id="1e8bc-104">Button element</span></span>

<span data-ttu-id="1e8bc-105">Representa um controle de [botão](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="1e8bc-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="1e8bc-106">Uso</span><span class="sxs-lookup"><span data-stu-id="1e8bc-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="1e8bc-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="1e8bc-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e8bc-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="1e8bc-108">Attribute</span></span></th>
<th><span data-ttu-id="1e8bc-109">Type</span><span class="sxs-lookup"><span data-stu-id="1e8bc-109">Type</span></span></th>
<th><span data-ttu-id="1e8bc-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e8bc-110">Required</span></span></th>
<th><span data-ttu-id="1e8bc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e8bc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e8bc-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="1e8bc-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="1e8bc-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="1e8bc-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="1e8bc-114">Não</span><span class="sxs-lookup"><span data-stu-id="1e8bc-114">No</span></span><br/></td>
<td><span data-ttu-id="1e8bc-115">Esse atributo é válido somente quando o elemento <strong>Button</strong> é filho de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="1e8bc-116">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1e8bc-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="1e8bc-117">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="1e8bc-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="1e8bc-118">Padrão.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-118">Default.</span></span> <br/> </dd> <span data-ttu-id="1e8bc-119"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="1e8bc-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e8bc-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="1e8bc-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="1e8bc-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="1e8bc-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="1e8bc-122">Não</span><span class="sxs-lookup"><span data-stu-id="1e8bc-122">No</span></span><br/></td>
<td><span data-ttu-id="1e8bc-123">Válido somente se o <a href="windowsribbon-element-menugroup.md"><strong>MyMenu</strong></a> for o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="1e8bc-124">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="1e8bc-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e8bc-125">Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="1e8bc-126">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="1e8bc-127">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e8bc-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="1e8bc-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="1e8bc-129">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="1e8bc-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="1e8bc-130">Não</span><span class="sxs-lookup"><span data-stu-id="1e8bc-130">No</span></span><br/></td>
<td><span data-ttu-id="1e8bc-131">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="1e8bc-132">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="1e8bc-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1e8bc-133">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="1e8bc-134">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1e8bc-135">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1e8bc-136">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1e8bc-136">Child elements</span></span>

<span data-ttu-id="1e8bc-137">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="1e8bc-138">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1e8bc-138">Parent elements</span></span>



| <span data-ttu-id="1e8bc-139">Elemento</span><span class="sxs-lookup"><span data-stu-id="1e8bc-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e8bc-140">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="1e8bc-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="1e8bc-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="1e8bc-143">**Group**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="1e8bc-144">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="1e8bc-145">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="1e8bc-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="1e8bc-147">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="1e8bc-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="1e8bc-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e8bc-149">Remarks</span></span>

<span data-ttu-id="1e8bc-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-150">Optional.</span></span>

<span data-ttu-id="1e8bc-151">Pode ocorrer no máximo uma vez para cada elemento [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1e8bc-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="1e8bc-152">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="1e8bc-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="1e8bc-153">O **botão** dá suporte a [modos de aplicativo](ribbon-applicationmodes.md) quando ele está hospedado na coluna à esquerda do menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="1e8bc-154">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e8bc-154">Examples</span></span>

<span data-ttu-id="1e8bc-155">O exemplo a seguir demonstra a marcação básica para o **botão**.</span><span class="sxs-lookup"><span data-stu-id="1e8bc-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="1e8bc-156">Esta seção de código mostra as declarações de comando de **botão** , com um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai do elemento **Button** .</span><span class="sxs-lookup"><span data-stu-id="1e8bc-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="1e8bc-157">Esta seção de código mostra as declarações de controle de **botão** .</span><span class="sxs-lookup"><span data-stu-id="1e8bc-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="1e8bc-158">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1e8bc-158">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="1e8bc-159">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e8bc-159">Minimum supported system</span></span><br/> | <span data-ttu-id="1e8bc-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e8bc-160">Windows 7</span></span> |
| <span data-ttu-id="1e8bc-161">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="1e8bc-161">Can be empty</span></span>                        | <span data-ttu-id="1e8bc-162">Sim</span><span class="sxs-lookup"><span data-stu-id="1e8bc-162">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="1e8bc-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e8bc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e8bc-164">Controle de botão</span><span class="sxs-lookup"><span data-stu-id="1e8bc-164">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="1e8bc-165">**Setmodos**</span><span class="sxs-lookup"><span data-stu-id="1e8bc-165">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

