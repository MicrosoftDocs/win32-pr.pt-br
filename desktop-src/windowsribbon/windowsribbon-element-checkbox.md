---
title: Elemento CheckBox
description: Representa um controle Check Box.
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- Faixa de Opções do Windows do elemento CheckBox
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9357337e569f43b14c34798c9c6e8da4b7b10b
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443037"
---
# <a name="checkbox-element"></a><span data-ttu-id="37cb1-104">Elemento CheckBox</span><span class="sxs-lookup"><span data-stu-id="37cb1-104">CheckBox element</span></span>

<span data-ttu-id="37cb1-105">Representa um [controle Check Box.](windowsribbon-controls-checkbox.md)</span><span class="sxs-lookup"><span data-stu-id="37cb1-105">Represents a [Check Box](windowsribbon-controls-checkbox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="37cb1-106">Uso</span><span class="sxs-lookup"><span data-stu-id="37cb1-106">Usage</span></span>

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="37cb1-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="37cb1-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37cb1-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="37cb1-108">Attribute</span></span></th>
<th><span data-ttu-id="37cb1-109">Type</span><span class="sxs-lookup"><span data-stu-id="37cb1-109">Type</span></span></th>
<th><span data-ttu-id="37cb1-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="37cb1-110">Required</span></span></th>
<th><span data-ttu-id="37cb1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="37cb1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37cb1-112"><strong>ApplicationDefaults.IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="37cb1-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="37cb1-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="37cb1-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="37cb1-114">Não</span><span class="sxs-lookup"><span data-stu-id="37cb1-114">No</span></span><br/></td>
<td><span data-ttu-id="37cb1-115">Esse atributo é válido somente quando o <strong>elemento CheckBox</strong> é um filho de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37cb1-115">This attribute is valid only when the <strong>CheckBox</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="37cb1-116">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="37cb1-116">Restricted to one of the following values:</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="37cb1-117">A <strong>CheckBox</strong> não dá suporte a um estado terciário ou indeterminado.</span><span class="sxs-lookup"><span data-stu-id="37cb1-117">The <strong>CheckBox</strong> does not support a tertiary, or indeterminate, state.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="37cb1-118">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="37cb1-118">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="37cb1-119">Padrão.</span><span class="sxs-lookup"><span data-stu-id="37cb1-119">Default.</span></span> <br/> </dd> <span data-ttu-id="37cb1-120"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="37cb1-120"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37cb1-121"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="37cb1-121"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="37cb1-122">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="37cb1-122">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="37cb1-123">Não</span><span class="sxs-lookup"><span data-stu-id="37cb1-123">No</span></span><br/></td>
<td><span data-ttu-id="37cb1-124">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37cb1-124">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="37cb1-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="37cb1-125">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="37cb1-126">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="37cb1-126">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="37cb1-127">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="37cb1-127">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="37cb1-128">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="37cb1-128">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="37cb1-129">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="37cb1-129">Child elements</span></span>

<span data-ttu-id="37cb1-130">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="37cb1-130">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="37cb1-131">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="37cb1-131">Parent elements</span></span>



| <span data-ttu-id="37cb1-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="37cb1-132">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37cb1-133">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="37cb1-133">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="37cb1-134">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="37cb1-134">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="37cb1-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="37cb1-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="37cb1-136">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="37cb1-136">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="37cb1-137">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="37cb1-137">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="37cb1-138">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="37cb1-138">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="37cb1-139">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="37cb1-139">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="37cb1-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="37cb1-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="37cb1-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="37cb1-141">Remarks</span></span>

<span data-ttu-id="37cb1-142">Opcional ou obrigatório, dependendo do elemento pai.</span><span class="sxs-lookup"><span data-stu-id="37cb1-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="37cb1-143">Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults,**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)</span><span class="sxs-lookup"><span data-stu-id="37cb1-143">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="37cb1-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37cb1-144">Examples</span></span>

<span data-ttu-id="37cb1-145">O exemplo a seguir demonstra a marcação básica para o **elemento CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="37cb1-145">The following example demonstrates the basic markup for the **CheckBox** element.</span></span>

<span data-ttu-id="37cb1-146">Esta seção de código mostra as declarações **do Comando CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="37cb1-146">This section of code shows the **CheckBox** Command declarations.</span></span>


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



<span data-ttu-id="37cb1-147">Esta seção de código mostra as declarações **de controle CheckBox.**</span><span class="sxs-lookup"><span data-stu-id="37cb1-147">This section of code shows the **CheckBox** control declarations.</span></span>


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="37cb1-148">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="37cb1-148">Element information</span></span>

* <span data-ttu-id="37cb1-149">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="37cb1-149">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="37cb1-150">**Pode estar vazio:** Sim</span><span class="sxs-lookup"><span data-stu-id="37cb1-150">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="37cb1-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="37cb1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cb1-152">Controle Check Box</span><span class="sxs-lookup"><span data-stu-id="37cb1-152">Check Box control</span></span>](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





