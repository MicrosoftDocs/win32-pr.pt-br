---
title: Elemento InRibbonGallery
description: Representa a Galeria de In-Ribbon, um controle baseado na galeria que expõe um subconjunto padrão de itens diretamente na faixa de bits. Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Faixa de InRibbonGallery do elemento do Windows
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2020
ms.locfileid: "104007275"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="30553-105">Elemento InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="30553-105">InRibbonGallery element</span></span>

<span data-ttu-id="30553-106">Representa a [Galeria na faixa de faixas](windowsribbon-controls-inribbongallery.md), um controle baseado na galeria que expõe um subconjunto padrão de itens diretamente na faixa de bits.</span><span class="sxs-lookup"><span data-stu-id="30553-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="30553-107">Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.</span><span class="sxs-lookup"><span data-stu-id="30553-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="30553-108">Uso</span><span class="sxs-lookup"><span data-stu-id="30553-108">Usage</span></span>

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
```

## <a name="attributes"></a><span data-ttu-id="30553-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="30553-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30553-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="30553-110">Attribute</span></span></th>
<th><span data-ttu-id="30553-111">Type</span><span class="sxs-lookup"><span data-stu-id="30553-111">Type</span></span></th>
<th><span data-ttu-id="30553-112">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30553-112">Required</span></span></th>
<th><span data-ttu-id="30553-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="30553-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30553-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="30553-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="30553-115">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="30553-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="30553-116">Não</span><span class="sxs-lookup"><span data-stu-id="30553-116">No</span></span><br/></td>
<td><span data-ttu-id="30553-117">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="30553-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="30553-118">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="30553-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="30553-119">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="30553-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="30553-120">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="30553-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="30553-121">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="30553-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30553-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="30553-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="30553-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="30553-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="30553-124">Não</span><span class="sxs-lookup"><span data-stu-id="30553-124">No</span></span><br/></td>
<td><span data-ttu-id="30553-125">Determina se o recurso de imagem grande ou pequena do comando é exibido no controle galeria.</span><span class="sxs-lookup"><span data-stu-id="30553-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="30553-126">Aplica-se somente a galerias em que o valor do atributo <em>Type</em> é igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="30553-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="30553-127">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="30553-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="30553-128">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="30553-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="30553-129">Padrão.</span><span class="sxs-lookup"><span data-stu-id="30553-129">Default.</span></span> <br/> </dd> <span data-ttu-id="30553-130"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="30553-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30553-131"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="30553-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="30553-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30553-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="30553-133">Não</span><span class="sxs-lookup"><span data-stu-id="30553-133">No</span></span><br/></td>
<td><span data-ttu-id="30553-134">Junto com o @ <em>Width</em>, determina o tamanho da imagem do item que é exibido no controle da galeria.</span><span class="sxs-lookup"><span data-stu-id="30553-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="30553-135">Aplica-se somente a galerias em que o valor do atributo de <em>tipo</em> é igual a</span><span class="sxs-lookup"><span data-stu-id="30553-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="30553-136">.</span><span class="sxs-lookup"><span data-stu-id="30553-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="30553-137">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="30553-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="30553-138">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="30553-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30553-139"><strong>@ Width</strong></span><span class="sxs-lookup"><span data-stu-id="30553-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="30553-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30553-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="30553-141">Não</span><span class="sxs-lookup"><span data-stu-id="30553-141">No</span></span><br/></td>
<td><span data-ttu-id="30553-142">Junto com <em>ItemHeight</em>, determina o tamanho da imagem do item que é exibida no controle da galeria.</span><span class="sxs-lookup"><span data-stu-id="30553-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="30553-143">Aplica-se somente a galerias em que o valor do atributo de <em>tipo</em> é igual a</span><span class="sxs-lookup"><span data-stu-id="30553-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="30553-144">.</span><span class="sxs-lookup"><span data-stu-id="30553-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="30553-145">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="30553-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="30553-146">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="30553-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30553-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="30553-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="30553-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30553-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="30553-149">Não</span><span class="sxs-lookup"><span data-stu-id="30553-149">No</span></span><br/></td>
<td><span data-ttu-id="30553-150">Especifica o número máximo de colunas que o <strong>InRibbonGallery</strong> exibe, por exemplo, na lista suspensa layout de grupo <em>grande</em> .</span><span class="sxs-lookup"><span data-stu-id="30553-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="30553-151">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="30553-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30553-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="30553-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="30553-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30553-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="30553-154">Não</span><span class="sxs-lookup"><span data-stu-id="30553-154">No</span></span><br/></td>
<td><span data-ttu-id="30553-155">Especifica o número máximo de colunas que o <strong>InRibbonGallery</strong> exibe no layout de grupo <em>médio</em> , antes de alternar para o layout <em>grande</em> .</span><span class="sxs-lookup"><span data-stu-id="30553-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="30553-156">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="30553-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30553-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="30553-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="30553-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30553-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="30553-159">Não</span><span class="sxs-lookup"><span data-stu-id="30553-159">No</span></span><br/></td>
<td><span data-ttu-id="30553-160">Especifica o número máximo de linhas para o layout dos itens <strong>InRibbonGallery</strong> .</span><span class="sxs-lookup"><span data-stu-id="30553-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="30553-161">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="30553-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="30553-162">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="30553-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30553-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="30553-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="30553-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30553-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="30553-165">Não</span><span class="sxs-lookup"><span data-stu-id="30553-165">No</span></span><br/></td>
<td><span data-ttu-id="30553-166">Especifica o número mínimo de colunas que o <strong>InRibbonGallery</strong> exibe no layout de grupo <em>grande</em> , antes de passar para <em>médio</em>.</span><span class="sxs-lookup"><span data-stu-id="30553-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="30553-167">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="30553-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30553-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="30553-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="30553-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30553-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="30553-170">Não</span><span class="sxs-lookup"><span data-stu-id="30553-170">No</span></span><br/></td>
<td><span data-ttu-id="30553-171">Especifica o número mínimo de colunas que o <strong>InRibbonGallery</strong> exibe no layout de grupo <em>médio</em> , antes de mudar para <em>pequeno</em>.</span><span class="sxs-lookup"><span data-stu-id="30553-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="30553-172">
<dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="30553-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30553-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="30553-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="30553-174">Textpositiontype</span><span class="sxs-lookup"><span data-stu-id="30553-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="30553-175">Não</span><span class="sxs-lookup"><span data-stu-id="30553-175">No</span></span><br/></td>
<td><span data-ttu-id="30553-176">Especifica onde o rótulo do item é exibido, em relação à imagem.</span><span class="sxs-lookup"><span data-stu-id="30553-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="30553-177">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="30553-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="30553-178">
<dt><span></span><span></span><strong></strong> Resultado</span><span class="sxs-lookup"><span data-stu-id="30553-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="30553-179"><dt><span></span><span></span><strong></strong> Exibe</span><span class="sxs-lookup"><span data-stu-id="30553-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="30553-180"><dt><span></span><span></span><strong></strong> Mantida</span><span class="sxs-lookup"><span data-stu-id="30553-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="30553-181"><dt><span></span><span></span><strong></strong> Post</span><span class="sxs-lookup"><span data-stu-id="30553-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="30553-182"><dt><span></span><span></span><strong></strong> Adequada</span><span class="sxs-lookup"><span data-stu-id="30553-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="30553-183"><dt><span></span><span></span><strong></strong> Melhor</span><span class="sxs-lookup"><span data-stu-id="30553-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30553-184"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="30553-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="30553-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="30553-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="30553-186">Não</span><span class="sxs-lookup"><span data-stu-id="30553-186">No</span></span><br/></td>
<td><span data-ttu-id="30553-187">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="30553-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="30553-188">
<dt><span></span><span></span><strong></strong> Los</span><span class="sxs-lookup"><span data-stu-id="30553-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="30553-189"><dt><span></span><span></span><strong></strong> Comandos</span><span class="sxs-lookup"><span data-stu-id="30553-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="30553-190">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="30553-190">Child elements</span></span>



| <span data-ttu-id="30553-191">Elemento</span><span class="sxs-lookup"><span data-stu-id="30553-191">Element</span></span>                                                                                           | <span data-ttu-id="30553-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="30553-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="30553-193">**Verificação**</span><span class="sxs-lookup"><span data-stu-id="30553-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="30553-194">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="30553-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="30553-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="30553-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="30553-196">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="30553-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="30553-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="30553-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="30553-198">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="30553-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="30553-199">**Button**</span><span class="sxs-lookup"><span data-stu-id="30553-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="30553-200">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="30553-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="30553-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="30553-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="30553-202">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="30553-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="30553-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="30553-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="30553-204">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="30553-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="30553-205">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="30553-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30553-206">Elemento</span><span class="sxs-lookup"><span data-stu-id="30553-206">Element</span></span></th>
<th><span data-ttu-id="30553-207">Descrição</span><span class="sxs-lookup"><span data-stu-id="30553-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30553-208"><a href="windowsribbon-element-controlgroup.md"><strong>Controlador de controle</strong></a></span><span class="sxs-lookup"><span data-stu-id="30553-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="30553-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span><span class="sxs-lookup"><span data-stu-id="30553-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="30553-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="30553-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="30553-211">Windows 8 e mais recente.</span><span class="sxs-lookup"><span data-stu-id="30553-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="30553-212">Comentários</span><span class="sxs-lookup"><span data-stu-id="30553-212">Remarks</span></span>

<span data-ttu-id="30553-213">Opcional.</span><span class="sxs-lookup"><span data-stu-id="30553-213">Optional.</span></span>

<span data-ttu-id="30553-214">Pode ocorrer no máximo uma vez para cada elemento [**Control**](windowsribbon-element-controlgroup.md) ou [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="30553-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="30553-215">A captura de tela a seguir ilustra o controle da [Galeria de faixa de](windowsribbon-controls-inribbongallery.md) opções no Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30553-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de tela de um controle da galeria na faixa de faixas na faixa de bits do Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="30553-217">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30553-217">Examples</span></span>

<span data-ttu-id="30553-218">O exemplo a seguir demonstra a marcação básica para uma [Galeria na faixa de](windowsribbon-controls-inribbongallery.md)opções.</span><span class="sxs-lookup"><span data-stu-id="30553-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="30553-219">Esta seção de código mostra as declarações de comando **InRibbonGallery** , com um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai para o elemento **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="30553-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



<span data-ttu-id="30553-220">Esta seção de código mostra as declarações de controle **InRibbonGallery** .</span><span class="sxs-lookup"><span data-stu-id="30553-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="30553-221">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="30553-221">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="30553-222">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30553-222">Minimum supported system</span></span><br/> | <span data-ttu-id="30553-223">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30553-223">Windows 7</span></span> |
| <span data-ttu-id="30553-224">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="30553-224">Can be empty</span></span>                        | <span data-ttu-id="30553-225">Não</span><span class="sxs-lookup"><span data-stu-id="30553-225">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="30553-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="30553-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30553-227">Controle da Galeria de faixa de bits</span><span class="sxs-lookup"><span data-stu-id="30553-227">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="30553-228">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="30553-228">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="30553-229">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="30553-229">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





