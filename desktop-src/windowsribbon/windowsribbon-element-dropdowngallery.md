---
title: Elemento DropDownGallery
description: Representa um controle de galeria de Drop-Down com um menu baseado na galeria.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Faixa de DropDownGallery do elemento do Windows
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499062"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="b3045-104">Elemento DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="b3045-104">DropDownGallery element</span></span>

<span data-ttu-id="b3045-105">Representa um controle de [Galeria suspensa](windowsribbon-controls-dropdowngallery.md) com um menu baseado na galeria.</span><span class="sxs-lookup"><span data-stu-id="b3045-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="b3045-106">Uso</span><span class="sxs-lookup"><span data-stu-id="b3045-106">Usage</span></span>

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a><span data-ttu-id="b3045-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="b3045-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3045-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="b3045-108">Attribute</span></span></th>
<th><span data-ttu-id="b3045-109">Type</span><span class="sxs-lookup"><span data-stu-id="b3045-109">Type</span></span></th>
<th><span data-ttu-id="b3045-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b3045-110">Required</span></span></th>
<th><span data-ttu-id="b3045-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3045-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3045-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="b3045-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="b3045-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3045-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3045-114">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-114">No</span></span><br/></td>
<td><span data-ttu-id="b3045-115">Válido somente se o <a href="windowsribbon-element-menugroup.md"><strong>MyMenu</strong></a> for o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="b3045-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="b3045-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3045-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3045-117">Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="b3045-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="b3045-118">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="b3045-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="b3045-119">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b3045-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3045-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="b3045-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="b3045-121">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="b3045-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="b3045-122">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-122">No</span></span><br/></td>
<td><span data-ttu-id="b3045-123">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3045-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="b3045-124">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="b3045-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b3045-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b3045-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="b3045-126">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="b3045-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="b3045-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b3045-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3045-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="b3045-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="b3045-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="b3045-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="b3045-130">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-130">No</span></span><br/></td>
<td><span data-ttu-id="b3045-131">Determina se o recurso de imagem grande ou pequena do comando é exibido no controle galeria.</span><span class="sxs-lookup"><span data-stu-id="b3045-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b3045-132">Aplica-se somente a galerias em que o valor do atributo <em>Type</em> é igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="b3045-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="b3045-133">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="b3045-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="b3045-134">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="b3045-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="b3045-135">Padrão.</span><span class="sxs-lookup"><span data-stu-id="b3045-135">Default.</span></span> <br/> </dd> <span data-ttu-id="b3045-136"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="b3045-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3045-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="b3045-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="b3045-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b3045-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="b3045-139">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-139">No</span></span><br/></td>
<td><span data-ttu-id="b3045-140"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="b3045-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="b3045-141">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="b3045-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3045-142"><strong>@ Width</strong></span><span class="sxs-lookup"><span data-stu-id="b3045-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="b3045-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b3045-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="b3045-144">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-144">No</span></span><br/></td>
<td><span data-ttu-id="b3045-145"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="b3045-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="b3045-146">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="b3045-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3045-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="b3045-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="b3045-148">Textpositiontype</span><span class="sxs-lookup"><span data-stu-id="b3045-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="b3045-149">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-149">No</span></span><br/></td>
<td><span data-ttu-id="b3045-150">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b3045-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="b3045-151">
<dt><span></span><span></span><strong></strong> Resultado</span><span class="sxs-lookup"><span data-stu-id="b3045-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b3045-152"><dt><span></span><span></span><strong></strong> Exibe</span><span class="sxs-lookup"><span data-stu-id="b3045-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b3045-153"><dt><span></span><span></span><strong></strong> Mantida</span><span class="sxs-lookup"><span data-stu-id="b3045-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b3045-154"><dt><span></span><span></span><strong></strong> Post</span><span class="sxs-lookup"><span data-stu-id="b3045-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b3045-155"><dt><span></span><span></span><strong></strong> Adequada</span><span class="sxs-lookup"><span data-stu-id="b3045-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b3045-156"><dt><span></span><span></span><strong></strong> Melhor</span><span class="sxs-lookup"><span data-stu-id="b3045-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3045-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="b3045-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="b3045-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="b3045-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="b3045-159">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-159">No</span></span><br/></td>
<td><span data-ttu-id="b3045-160">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b3045-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="b3045-161">
<dt><span></span><span></span><strong></strong> Los</span><span class="sxs-lookup"><span data-stu-id="b3045-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b3045-162"><dt><span></span><span></span><strong></strong> Comandos</span><span class="sxs-lookup"><span data-stu-id="b3045-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b3045-163">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b3045-163">Child elements</span></span>



| <span data-ttu-id="b3045-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="b3045-164">Element</span></span>                                                                                           | <span data-ttu-id="b3045-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3045-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="b3045-166">**Botão**</span><span class="sxs-lookup"><span data-stu-id="b3045-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="b3045-167">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="b3045-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="b3045-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="b3045-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="b3045-169">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="b3045-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="b3045-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="b3045-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="b3045-171">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="b3045-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="b3045-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="b3045-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="b3045-173">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="b3045-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="b3045-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="b3045-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="b3045-175">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="b3045-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="b3045-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="b3045-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="b3045-177">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="b3045-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b3045-178">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b3045-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3045-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="b3045-179">Element</span></span></th>
<th><span data-ttu-id="b3045-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3045-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3045-181"><a href="windowsribbon-element-controlgroup.md"><strong>Controlador de controle</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3045-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b3045-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3045-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b3045-183"><a href="windowsribbon-element-menugroup.md"><strong>Grupo Backstage</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3045-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="b3045-184">Quando contido em um <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b3045-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="b3045-185">Esse elemento só tem suporte no primeiro nível e não deve ter nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="b3045-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3045-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3045-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="b3045-187">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="b3045-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3045-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3045-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="b3045-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3045-189">Remarks</span></span>

<span data-ttu-id="b3045-190">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b3045-190">Optional.</span></span>

<span data-ttu-id="b3045-191">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md)ou [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="b3045-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="b3045-192">O **DropDownGallery** dá suporte a [modos de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="b3045-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="b3045-193">A captura de tela a seguir ilustra o controle da [Galeria suspensa](windowsribbon-controls-dropdowngallery.md) da faixa de opções no Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b3045-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de tela de um controle de galeria suspensa no Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="b3045-195">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b3045-195">Examples</span></span>

<span data-ttu-id="b3045-196">O exemplo a seguir demonstra a marcação básica para o **DropDownGallery**.</span><span class="sxs-lookup"><span data-stu-id="b3045-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="b3045-197">Esta seção de código mostra as declarações de comando **DropDownGallery** , com um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai para o elemento **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="b3045-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



<span data-ttu-id="b3045-198">Esta seção de código mostra as declarações de controle **DropDownGallery** .</span><span class="sxs-lookup"><span data-stu-id="b3045-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="b3045-199">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b3045-199">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="b3045-200">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3045-200">Minimum supported system</span></span><br/> | <span data-ttu-id="b3045-201">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3045-201">Windows 7</span></span> |
| <span data-ttu-id="b3045-202">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="b3045-202">Can be empty</span></span>                        | <span data-ttu-id="b3045-203">Não</span><span class="sxs-lookup"><span data-stu-id="b3045-203">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="b3045-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3045-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3045-205">**Controle da Galeria suspensa**</span><span class="sxs-lookup"><span data-stu-id="b3045-205">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="b3045-206">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="b3045-206">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="b3045-207">**Setmodos**</span><span class="sxs-lookup"><span data-stu-id="b3045-207">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="b3045-208">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="b3045-208">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

