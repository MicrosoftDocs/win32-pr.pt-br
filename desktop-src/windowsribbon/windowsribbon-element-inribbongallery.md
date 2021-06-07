---
title: Elemento InRibbonGallery
description: Representa a In-Ribbon, um controle baseado em galeria que expõe um subconjunto padrão de itens diretamente na Faixa de Opções. Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Faixa de Opções do Windows do elemento InRibbonGallery
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443367"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="3ca3b-105">Elemento InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="3ca3b-105">InRibbonGallery element</span></span>

<span data-ttu-id="3ca3b-106">Representa a [Galeria na Faixa de Opções](windowsribbon-controls-inribbongallery.md), um controle baseado em galeria que expõe um subconjunto padrão de itens diretamente na Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="3ca3b-107">Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="3ca3b-108">Uso</span><span class="sxs-lookup"><span data-stu-id="3ca3b-108">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="3ca3b-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ca3b-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ca3b-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="3ca3b-110">Attribute</span></span></th>
<th><span data-ttu-id="3ca3b-111">Type</span><span class="sxs-lookup"><span data-stu-id="3ca3b-111">Type</span></span></th>
<th><span data-ttu-id="3ca3b-112">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3ca3b-112">Required</span></span></th>
<th><span data-ttu-id="3ca3b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ca3b-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ca3b-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-115">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="3ca3b-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3ca3b-116">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-116">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-117">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="3ca3b-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3ca3b-119">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3ca3b-120">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3ca3b-121">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca3b-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="3ca3b-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="3ca3b-124">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-124">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-125">Determina se o recurso de imagem grande ou pequeno do Comando é exibido no controle da galeria.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3ca3b-126">Aplica-se somente a galerias em que o valor do <em>atributo Type</em> é igual a <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="3ca3b-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="3ca3b-127">Restrito a um dos seguintes valores (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="3ca3b-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="3ca3b-128">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="3ca3b-129">Padrão.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-129">Default.</span></span> <br/> </dd> <span data-ttu-id="3ca3b-130"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca3b-131"><strong>Itemheight</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3ca3b-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3ca3b-133">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-133">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-134">Junto com <em>ItemWidth</em>, determina o tamanho da imagem do item que é exibida no controle da galeria.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3ca3b-135">Aplica-se somente a galerias em que o valor do <em>atributo Type</em> é igual a</span><span class="sxs-lookup"><span data-stu-id="3ca3b-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="3ca3b-136">.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="3ca3b-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3ca3b-138">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca3b-139"><strong>Itemwidth</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3ca3b-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3ca3b-141">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-141">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-142">Junto com <em>ItemHeight</em>, determina o tamanho da imagem do item que é exibida no controle da galeria.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3ca3b-143">Aplica-se somente a galerias em que o valor do <em>atributo Type</em> é igual a</span><span class="sxs-lookup"><span data-stu-id="3ca3b-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="3ca3b-144">.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="3ca3b-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3ca3b-146">O padrão é -1.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca3b-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3ca3b-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3ca3b-149">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-149">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-150">Especifica o número máximo de colunas que a <strong>InRibbonGallery</strong> <em></em> exibe, por exemplo, na lista de layouts de grupo grande.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="3ca3b-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca3b-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3ca3b-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3ca3b-154">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-154">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-155">Especifica o número máximo de colunas que a <strong>InRibbonGallery</strong> exibe no layout do grupo Médio, antes de alternar para <em>Layout Grande.</em> <em></em></span><span class="sxs-lookup"><span data-stu-id="3ca3b-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="3ca3b-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca3b-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3ca3b-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3ca3b-159">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-159">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-160">Especifica o número máximo de linhas para o layout de <strong>itens InRibbonGallery.</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="3ca3b-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3ca3b-162">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca3b-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3ca3b-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3ca3b-165">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-165">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-166">Especifica o número mínimo de colunas que a <strong>InRibbonGallery</strong> exibe no layout <em>do</em> grupo Grande, antes de alternar para <em>Médio.</em></span><span class="sxs-lookup"><span data-stu-id="3ca3b-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="3ca3b-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca3b-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3ca3b-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3ca3b-170">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-170">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-171">Especifica o número mínimo de colunas que a <strong>InRibbonGallery</strong> exibe no layout <em>do</em> grupo Médio, antes de alternar para <em>Pequeno.</em></span><span class="sxs-lookup"><span data-stu-id="3ca3b-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="3ca3b-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca3b-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="3ca3b-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="3ca3b-175">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-175">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-176">Especifica onde o rótulo do item é exibido, em relação à imagem.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="3ca3b-177">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3ca3b-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3ca3b-178">
<dt><span></span><span></span><strong></strong> (Inferior)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3ca3b-179"><dt><span></span><span></span><strong></strong> (Ocultar)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3ca3b-180"><dt><span></span><span></span><strong></strong> (Esquerda)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3ca3b-181"><dt><span></span><span></span><strong></strong> (Sobreposição)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3ca3b-182"><dt><span></span><span></span><strong></strong> (Direita)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3ca3b-183"><dt><span></span><span></span><strong></strong> (Superior)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca3b-184"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="3ca3b-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="3ca3b-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ca3b-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="3ca3b-186">Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-186">No</span></span><br/></td>
<td><span data-ttu-id="3ca3b-187">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3ca3b-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3ca3b-188">
<dt><span></span><span></span><strong></strong> (Itens)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3ca3b-189"><dt><span></span><span></span><strong></strong> (Comandos)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3ca3b-190">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3ca3b-190">Child elements</span></span>



| <span data-ttu-id="3ca3b-191">Elemento</span><span class="sxs-lookup"><span data-stu-id="3ca3b-191">Element</span></span>                                                                                           | <span data-ttu-id="3ca3b-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ca3b-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="3ca3b-193">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="3ca3b-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="3ca3b-194">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="3ca3b-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3ca3b-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3ca3b-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="3ca3b-196">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="3ca3b-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="3ca3b-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="3ca3b-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="3ca3b-198">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="3ca3b-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="3ca3b-199">**Botão**</span><span class="sxs-lookup"><span data-stu-id="3ca3b-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="3ca3b-200">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="3ca3b-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3ca3b-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3ca3b-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="3ca3b-202">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="3ca3b-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3ca3b-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3ca3b-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="3ca3b-204">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="3ca3b-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3ca3b-205">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="3ca3b-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ca3b-206">Elemento</span><span class="sxs-lookup"><span data-stu-id="3ca3b-206">Element</span></span></th>
<th><span data-ttu-id="3ca3b-207">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ca3b-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ca3b-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ca3b-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3ca3b-209"><a href="windowsribbon-element-group.md"><strong>Grupo</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ca3b-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3ca3b-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ca3b-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="3ca3b-211">Windows 8 e mais novos.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3ca3b-212">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ca3b-212">Remarks</span></span>

<span data-ttu-id="3ca3b-213">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-213">Optional.</span></span>

<span data-ttu-id="3ca3b-214">Pode ocorrer no máximo uma vez para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**ou Group.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="3ca3b-215">A captura de tela a seguir ilustra o controle [Galeria](windowsribbon-controls-inribbongallery.md) na Faixa de Opções na Faixa de Opções Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3ca3b-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de tela de um controle na galeria na faixa de opções na faixa de opções do Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="3ca3b-217">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ca3b-217">Examples</span></span>

<span data-ttu-id="3ca3b-218">O exemplo a seguir demonstra a marcação básica para uma [Galeria na Faixa de Opções](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="3ca3b-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="3ca3b-219">Esta seção de código mostra as declarações de Comando **InRibbonGallery,** com um Grupo associado que atua como o contêiner pai para o elemento **InRibbonGallery.** [](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="3ca3b-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


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



<span data-ttu-id="3ca3b-220">Esta seção de código mostra as **declarações de controle InRibbonGallery.**</span><span class="sxs-lookup"><span data-stu-id="3ca3b-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="3ca3b-221">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3ca3b-221">Element information</span></span>


* <span data-ttu-id="3ca3b-222">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ca3b-222">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="3ca3b-223">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="3ca3b-223">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="3ca3b-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ca3b-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca3b-225">Controle na Galeria na Faixa de Opções</span><span class="sxs-lookup"><span data-stu-id="3ca3b-225">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="3ca3b-226">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="3ca3b-226">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="3ca3b-227">Exemplo da Galeria</span><span class="sxs-lookup"><span data-stu-id="3ca3b-227">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





