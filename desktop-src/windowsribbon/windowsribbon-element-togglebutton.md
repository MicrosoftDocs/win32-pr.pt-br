---
title: Elemento ToggleButton
description: Representa um controle de botão de alternância.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Faixa de das janelas do elemento ToggleButton
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104293726"
---
# <a name="togglebutton-element"></a><span data-ttu-id="76234-104">Elemento ToggleButton</span><span class="sxs-lookup"><span data-stu-id="76234-104">ToggleButton element</span></span>

<span data-ttu-id="76234-105">Representa um controle de [botão de alternância](windowsribbon-controls-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="76234-105">Represents a [Toggle Button](windowsribbon-controls-togglebutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="76234-106">Uso</span><span class="sxs-lookup"><span data-stu-id="76234-106">Usage</span></span>

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="76234-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="76234-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76234-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="76234-108">Attribute</span></span></th>
<th><span data-ttu-id="76234-109">Type</span><span class="sxs-lookup"><span data-stu-id="76234-109">Type</span></span></th>
<th><span data-ttu-id="76234-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="76234-110">Required</span></span></th>
<th><span data-ttu-id="76234-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="76234-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76234-112"><strong>ApplicationDefaults. IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="76234-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="76234-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="76234-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="76234-114">Não</span><span class="sxs-lookup"><span data-stu-id="76234-114">No</span></span><br/></td>
<td><span data-ttu-id="76234-115">Esse atributo é válido somente quando o elemento <strong>ToggleButton</strong> é filho de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="76234-115">This attribute is valid only when the <strong>ToggleButton</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="76234-116">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="76234-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="76234-117">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="76234-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="76234-118">Padrão.</span><span class="sxs-lookup"><span data-stu-id="76234-118">Default.</span></span> <br/> </dd> <span data-ttu-id="76234-119"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="76234-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76234-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="76234-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="76234-121">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="76234-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="76234-122">Não</span><span class="sxs-lookup"><span data-stu-id="76234-122">No</span></span><br/></td>
<td><span data-ttu-id="76234-123">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="76234-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="76234-124">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="76234-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="76234-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="76234-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="76234-126">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="76234-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="76234-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="76234-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="76234-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="76234-128">Child elements</span></span>

<span data-ttu-id="76234-129">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="76234-129">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="76234-130">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="76234-130">Parent elements</span></span>



| <span data-ttu-id="76234-131">Elemento</span><span class="sxs-lookup"><span data-stu-id="76234-131">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76234-132">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="76234-132">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="76234-133">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="76234-133">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="76234-134">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="76234-134">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="76234-135">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="76234-135">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="76234-136">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="76234-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="76234-137">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="76234-137">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="76234-138">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="76234-138">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="76234-139">**SplitButton. ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="76234-139">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="76234-140">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="76234-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="76234-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="76234-141">Remarks</span></span>

<span data-ttu-id="76234-142">Opcional ou obrigatório, dependendo do elemento pai.</span><span class="sxs-lookup"><span data-stu-id="76234-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="76234-143">Pode ocorrer no máximo uma vez para cada elemento [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="76234-143">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="76234-144">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**menu**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="76234-144">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="76234-145">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76234-145">Examples</span></span>

<span data-ttu-id="76234-146">O exemplo a seguir demonstra a marcação básica para o elemento **ToggleButton** .</span><span class="sxs-lookup"><span data-stu-id="76234-146">The following example demonstrates the basic markup for the **ToggleButton** element.</span></span>

<span data-ttu-id="76234-147">Esta seção de código mostra uma declaração de elemento **ToggleButton** dentro do elemento [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .</span><span class="sxs-lookup"><span data-stu-id="76234-147">This section of code shows a **ToggleButton** element declaration within the [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="76234-148">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="76234-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="76234-149">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76234-149">Minimum supported system</span></span><br/> | <span data-ttu-id="76234-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76234-150">Windows 7</span></span> |
| <span data-ttu-id="76234-151">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="76234-151">Can be empty</span></span>                        | <span data-ttu-id="76234-152">Sim</span><span class="sxs-lookup"><span data-stu-id="76234-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="76234-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="76234-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76234-154">Controle de botão de alternância</span><span class="sxs-lookup"><span data-stu-id="76234-154">Toggle Button control</span></span>](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





