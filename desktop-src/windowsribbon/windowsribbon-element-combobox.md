---
title: Elemento ComboBox
description: Representa um controle de caixa de combinação.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Faixa de combinação do elemento ComboBox do Windows
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60ad8866b655be587e0c3d0f123d8bc59b6b8a21
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443577"
---
# <a name="combobox-element"></a><span data-ttu-id="8f6e2-104">Elemento ComboBox</span><span class="sxs-lookup"><span data-stu-id="8f6e2-104">ComboBox element</span></span>

<span data-ttu-id="8f6e2-105">Representa um controle de [caixa de combinação](windowsribbon-controls-combobox.md) .</span><span class="sxs-lookup"><span data-stu-id="8f6e2-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="8f6e2-106">Uso</span><span class="sxs-lookup"><span data-stu-id="8f6e2-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="8f6e2-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f6e2-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f6e2-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="8f6e2-108">Attribute</span></span></th>
<th><span data-ttu-id="8f6e2-109">Type</span><span class="sxs-lookup"><span data-stu-id="8f6e2-109">Type</span></span></th>
<th><span data-ttu-id="8f6e2-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8f6e2-110">Required</span></span></th>
<th><span data-ttu-id="8f6e2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f6e2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f6e2-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="8f6e2-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="8f6e2-113">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="8f6e2-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="8f6e2-114">Não</span><span class="sxs-lookup"><span data-stu-id="8f6e2-114">No</span></span><br/></td>
<td><span data-ttu-id="8f6e2-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="8f6e2-116">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="8f6e2-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8f6e2-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="8f6e2-118">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="8f6e2-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f6e2-120"><strong>IsAutoCompleteEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="8f6e2-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="8f6e2-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="8f6e2-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="8f6e2-122">Não</span><span class="sxs-lookup"><span data-stu-id="8f6e2-122">No</span></span><br/></td>
<td><span data-ttu-id="8f6e2-123">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="8f6e2-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="8f6e2-124">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="8f6e2-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8f6e2-125">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-125">Default.</span></span> <br/> </dd> <span data-ttu-id="8f6e2-126"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="8f6e2-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f6e2-127"><strong>Iseditável</strong></span><span class="sxs-lookup"><span data-stu-id="8f6e2-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="8f6e2-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="8f6e2-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="8f6e2-129">Não</span><span class="sxs-lookup"><span data-stu-id="8f6e2-129">No</span></span><br/></td>
<td><span data-ttu-id="8f6e2-130">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="8f6e2-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="8f6e2-131">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="8f6e2-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8f6e2-132">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-132">Default.</span></span> <br/> </dd> <span data-ttu-id="8f6e2-133"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="8f6e2-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f6e2-134"><strong>Redimensionartype</strong></span><span class="sxs-lookup"><span data-stu-id="8f6e2-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="8f6e2-135">ComboBoxResizeType</span><span class="sxs-lookup"><span data-stu-id="8f6e2-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="8f6e2-136">Não</span><span class="sxs-lookup"><span data-stu-id="8f6e2-136">No</span></span><br/></td>
<td><span data-ttu-id="8f6e2-137"><dt><span></span><span></span><strong></strong> (NoResize)</span><span class="sxs-lookup"><span data-stu-id="8f6e2-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="8f6e2-138">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-138">Default.</span></span> <br/> </dd> <span data-ttu-id="8f6e2-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span><span class="sxs-lookup"><span data-stu-id="8f6e2-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8f6e2-140">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8f6e2-140">Child elements</span></span>

<span data-ttu-id="8f6e2-141">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8f6e2-142">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8f6e2-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f6e2-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f6e2-143">Element</span></span></th>
<th><span data-ttu-id="8f6e2-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f6e2-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f6e2-145"><a href="windowsribbon-element-controlgroup.md"><strong>Controlador de controle</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f6e2-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8f6e2-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f6e2-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8f6e2-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f6e2-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8f6e2-148"><a href="windowsribbon-element-group.md"><strong>Grupo</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f6e2-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8f6e2-149"><a href="windowsribbon-element-menugroup.md"><strong>Grupo Backstage</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f6e2-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8f6e2-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f6e2-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="8f6e2-151">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f6e2-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="8f6e2-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="8f6e2-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f6e2-153">Remarks</span></span>

<span data-ttu-id="8f6e2-154">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-154">Optional.</span></span>

<span data-ttu-id="8f6e2-155">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="8f6e2-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="8f6e2-156">Como a **ComboBox** é exclusivamente uma galeria de itens, ela não oferece suporte a itens de comando.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="8f6e2-157">Também é o único controle de galeria que não oferece suporte a um espaço de comando (uma coleção de comandos declarados em marcação e listados na parte inferior de uma galeria de itens ou galeria de comandos).</span><span class="sxs-lookup"><span data-stu-id="8f6e2-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="8f6e2-158">Para obter mais informações, consulte [trabalhando com galerias](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="8f6e2-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="8f6e2-159">A captura de tela a seguir ilustra um controle de [caixa de combinação](windowsribbon-controls-combobox.md) da faixa de opções do Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![captura de tela de um controle ComboBox na faixa de faixas do Microsoft Paint.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="8f6e2-161">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f6e2-161">Examples</span></span>

<span data-ttu-id="8f6e2-162">Os exemplos a seguir demonstram a marcação básica para a **ComboBox**.</span><span class="sxs-lookup"><span data-stu-id="8f6e2-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="8f6e2-163">Esta seção de código mostra as declarações de comando **ComboBox** , com um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai do elemento **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="8f6e2-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



<span data-ttu-id="8f6e2-164">Esta seção de código mostra as declarações de controle de **ComboBox** .</span><span class="sxs-lookup"><span data-stu-id="8f6e2-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="8f6e2-165">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8f6e2-165">Element information</span></span>

* <span data-ttu-id="8f6e2-166">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f6e2-166">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="8f6e2-167">**Pode estar vazio**: Sim</span><span class="sxs-lookup"><span data-stu-id="8f6e2-167">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="8f6e2-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f6e2-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6e2-169">Controle de caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="8f6e2-169">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="8f6e2-170">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="8f6e2-170">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





