---
title: Elemento SplitButtonGallery
description: Representa um controle da Galeria de botões de divisão com um menu suspenso baseado na galeria.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Faixa de SplitButtonGallery do elemento do Windows
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68e90137325c16af6942f9f3929f8abfdf795660
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454231"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="deeb3-104">Elemento SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="deeb3-104">SplitButtonGallery element</span></span>

<span data-ttu-id="deeb3-105">Representa um controle da [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) com um menu suspenso baseado na galeria.</span><span class="sxs-lookup"><span data-stu-id="deeb3-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="deeb3-106">Uso</span><span class="sxs-lookup"><span data-stu-id="deeb3-106">Usage</span></span>

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a><span data-ttu-id="deeb3-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="deeb3-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="deeb3-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="deeb3-108">Attribute</span></span></th>
<th><span data-ttu-id="deeb3-109">Type</span><span class="sxs-lookup"><span data-stu-id="deeb3-109">Type</span></span></th>
<th><span data-ttu-id="deeb3-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="deeb3-110">Required</span></span></th>
<th><span data-ttu-id="deeb3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="deeb3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="deeb3-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="deeb3-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="deeb3-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="deeb3-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="deeb3-114">No</span><span class="sxs-lookup"><span data-stu-id="deeb3-114">No</span></span><br/></td>
<td><span data-ttu-id="deeb3-115">Válido somente se o <a href="windowsribbon-element-menugroup.md"><strong>MyMenu</strong></a> for o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="deeb3-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="deeb3-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="deeb3-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="deeb3-117">Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="deeb3-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="deeb3-118">O espaço em branco é válido e ignorado.</span><span class="sxs-lookup"><span data-stu-id="deeb3-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="deeb3-119">Comprimento máximo: 250 caracteres.</span><span class="sxs-lookup"><span data-stu-id="deeb3-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="deeb3-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="deeb3-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="deeb3-121">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="deeb3-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="deeb3-122">No</span><span class="sxs-lookup"><span data-stu-id="deeb3-122">No</span></span><br/></td>
<td><span data-ttu-id="deeb3-123">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="deeb3-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="deeb3-124">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="deeb3-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="deeb3-125">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="deeb3-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="deeb3-126">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="deeb3-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="deeb3-127">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="deeb3-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="deeb3-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="deeb3-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="deeb3-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="deeb3-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="deeb3-130">No</span><span class="sxs-lookup"><span data-stu-id="deeb3-130">No</span></span><br/></td>
<td><span data-ttu-id="deeb3-131">Determina se o recurso de imagem grande ou pequena do comando é exibido no controle galeria.</span><span class="sxs-lookup"><span data-stu-id="deeb3-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="deeb3-132">Aplica-se somente a galerias em que o valor do atributo <em>Type</em> é igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="deeb3-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="deeb3-133">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="deeb3-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="deeb3-134">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="deeb3-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="deeb3-135">Padrão.</span><span class="sxs-lookup"><span data-stu-id="deeb3-135">Default.</span></span> <br/> </dd> <span data-ttu-id="deeb3-136"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="deeb3-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="deeb3-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="deeb3-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="deeb3-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="deeb3-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="deeb3-139">No</span><span class="sxs-lookup"><span data-stu-id="deeb3-139">No</span></span><br/></td>
<td><span data-ttu-id="deeb3-140"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="deeb3-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="deeb3-141">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="deeb3-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="deeb3-142"><strong>@ Width</strong></span><span class="sxs-lookup"><span data-stu-id="deeb3-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="deeb3-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="deeb3-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="deeb3-144">No</span><span class="sxs-lookup"><span data-stu-id="deeb3-144">No</span></span><br/></td>
<td><span data-ttu-id="deeb3-145"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="deeb3-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="deeb3-146">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="deeb3-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="deeb3-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="deeb3-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="deeb3-148">Textpositiontype</span><span class="sxs-lookup"><span data-stu-id="deeb3-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="deeb3-149">No</span><span class="sxs-lookup"><span data-stu-id="deeb3-149">No</span></span><br/></td>
<td><span data-ttu-id="deeb3-150">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="deeb3-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="deeb3-151">
<dt><span></span><span></span><strong></strong> Resultado</span><span class="sxs-lookup"><span data-stu-id="deeb3-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="deeb3-152"><dt><span></span><span></span><strong></strong> Exibe</span><span class="sxs-lookup"><span data-stu-id="deeb3-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="deeb3-153"><dt><span></span><span></span><strong></strong> Mantida</span><span class="sxs-lookup"><span data-stu-id="deeb3-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="deeb3-154"><dt><span></span><span></span><strong></strong> Post</span><span class="sxs-lookup"><span data-stu-id="deeb3-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="deeb3-155"><dt><span></span><span></span><strong></strong> Adequada</span><span class="sxs-lookup"><span data-stu-id="deeb3-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="deeb3-156"><dt><span></span><span></span><strong></strong> Melhor</span><span class="sxs-lookup"><span data-stu-id="deeb3-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="deeb3-157"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="deeb3-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="deeb3-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="deeb3-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="deeb3-159">No</span><span class="sxs-lookup"><span data-stu-id="deeb3-159">No</span></span><br/></td>
<td><span data-ttu-id="deeb3-160">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="deeb3-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="deeb3-161">
<dt><span></span><span></span><strong></strong> Los</span><span class="sxs-lookup"><span data-stu-id="deeb3-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="deeb3-162"><dt><span></span><span></span><strong></strong> Comandos</span><span class="sxs-lookup"><span data-stu-id="deeb3-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="deeb3-163">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="deeb3-163">Child elements</span></span>



| <span data-ttu-id="deeb3-164">Elemento</span><span class="sxs-lookup"><span data-stu-id="deeb3-164">Element</span></span>                                                                                                 | <span data-ttu-id="deeb3-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="deeb3-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="deeb3-166">**Botão**</span><span class="sxs-lookup"><span data-stu-id="deeb3-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="deeb3-167">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="deeb3-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="deeb3-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="deeb3-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="deeb3-169">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="deeb3-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="deeb3-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="deeb3-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="deeb3-171">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="deeb3-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="deeb3-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="deeb3-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="deeb3-173">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="deeb3-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="deeb3-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="deeb3-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="deeb3-175">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="deeb3-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="deeb3-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="deeb3-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="deeb3-177">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="deeb3-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="deeb3-178">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="deeb3-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="deeb3-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="deeb3-179">Element</span></span></th>
<th><span data-ttu-id="deeb3-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="deeb3-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="deeb3-181"><a href="windowsribbon-element-controlgroup.md"><strong>Controlador de controle</strong></a></span><span class="sxs-lookup"><span data-stu-id="deeb3-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="deeb3-182"><a href="windowsribbon-element-group.md"><strong>Grupo</strong></a></span><span class="sxs-lookup"><span data-stu-id="deeb3-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="deeb3-183"><a href="windowsribbon-element-menugroup.md"><strong>Grupo Backstage</strong></a></span><span class="sxs-lookup"><span data-stu-id="deeb3-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="deeb3-184">Quando contido em um <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="deeb3-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="deeb3-185">Esse elemento só tem suporte no primeiro nível e não deve ter nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="deeb3-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="deeb3-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="deeb3-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="deeb3-187">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="deeb3-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="deeb3-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="deeb3-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="deeb3-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="deeb3-189">Remarks</span></span>

<span data-ttu-id="deeb3-190">Opcional.</span><span class="sxs-lookup"><span data-stu-id="deeb3-190">Optional.</span></span>

<span data-ttu-id="deeb3-191">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md)ou [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="deeb3-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="deeb3-192">O **SplitButtonGallery** dá suporte a [modos de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="deeb3-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="deeb3-193">[Interface do usuário \_ PKEY \_ boolianvalue](windowsribbon-reference-properties-uipkey-booleanvalue.md) é usado por um aplicativo para consultar o estado de alternância para o controle de botão de um **SplitButtonGallery**.</span><span class="sxs-lookup"><span data-stu-id="deeb3-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="deeb3-194">A captura de tela a seguir ilustra o controle da [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) da faixa de opções no Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="deeb3-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de tela de um controle de galeria de botões de divisão no Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="deeb3-196">Exemplos</span><span class="sxs-lookup"><span data-stu-id="deeb3-196">Examples</span></span>

<span data-ttu-id="deeb3-197">O exemplo a seguir demonstra a marcação básica para a [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="deeb3-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="deeb3-198">Esta seção de código mostra as declarações de comando **SplitButtonGallery** , com um [**grupo**](windowsribbon-element-group.md) associado que funciona como o contêiner pai para o elemento **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="deeb3-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



<span data-ttu-id="deeb3-199">Esta seção de código mostra as declarações de controle **SplitButtonGallery** .</span><span class="sxs-lookup"><span data-stu-id="deeb3-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="deeb3-200">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="deeb3-200">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="deeb3-201">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="deeb3-201">Minimum supported system</span></span><br/> | <span data-ttu-id="deeb3-202">Windows 7</span><span class="sxs-lookup"><span data-stu-id="deeb3-202">Windows 7</span></span> |
| <span data-ttu-id="deeb3-203">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="deeb3-203">Can be empty</span></span>                        | <span data-ttu-id="deeb3-204">Não</span><span class="sxs-lookup"><span data-stu-id="deeb3-204">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="deeb3-205">Confira também</span><span class="sxs-lookup"><span data-stu-id="deeb3-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deeb3-206">Controle da Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="deeb3-206">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="deeb3-207">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="deeb3-207">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="deeb3-208">**Setmodos**</span><span class="sxs-lookup"><span data-stu-id="deeb3-208">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="deeb3-209">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="deeb3-209">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

