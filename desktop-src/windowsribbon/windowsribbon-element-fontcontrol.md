---
title: Elemento FontControl
description: Representa um Controle de Fonte, que é um contêiner especializado de controles individuais dedicados à manipulação de fontes.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Faixa de Opções do Windows do elemento FontControl
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443397"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="7ec2c-104">Elemento FontControl</span><span class="sxs-lookup"><span data-stu-id="7ec2c-104">FontControl element</span></span>

<span data-ttu-id="7ec2c-105">Representa um [Controle de Fonte](windowsribbon-controls-fontcontrol.md), que é um contêiner especializado de controles individuais dedicados à manipulação de fontes.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="7ec2c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="7ec2c-106">Usage</span></span>

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
```

## <a name="attributes"></a><span data-ttu-id="7ec2c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ec2c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ec2c-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="7ec2c-108">Attribute</span></span></th>
<th><span data-ttu-id="7ec2c-109">Type</span><span class="sxs-lookup"><span data-stu-id="7ec2c-109">Type</span></span></th>
<th><span data-ttu-id="7ec2c-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7ec2c-110">Required</span></span></th>
<th><span data-ttu-id="7ec2c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ec2c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ec2c-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-113">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="7ec2c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="7ec2c-114">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-114">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="7ec2c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="7ec2c-118">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="7ec2c-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ec2c-120"><strong>FontType</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="7ec2c-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="7ec2c-122">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-122">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-123">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7ec2c-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="7ec2c-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-125">Padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="7ec2c-126">Definir o <em>atributo FontType</em> como <code>FontOnly</code> habilita a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="7ec2c-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="7ec2c-127"><strong>Caixa de combinação</strong> da família de fontes.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="7ec2c-128"><strong>Caixa de combinação</strong> Tamanho da Fonte.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="7ec2c-129"><strong>Botões</strong>de alternância Negrito, <strong>Itálico,</strong> <strong>Sublinhado</strong>e <strong>Tachado.</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-130">Os botões <strong></strong> <strong>de</strong> alternância Tachado e Sublinhado são exibidos por padrão, mas podem ser ocultos definindo os atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> como <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="7ec2c-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="7ec2c-132">Definir o <em>atributo FontType</em> como <code>FontWithColor</code> habilita a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="7ec2c-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="7ec2c-133"><strong>Caixa de combinação</strong> da família de fontes.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="7ec2c-134"><strong>Caixa de combinação</strong> tamanho da fonte.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="7ec2c-135"><strong>Aumentar a fonte</strong> e <strong>reduzir o incremento</strong> de tamanho da fonte e os botões de decremento.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="7ec2c-136"><strong>Botões</strong>de alternância Negrito, <strong>Itálico,</strong> <strong>Sublinhado</strong>e <strong>Tachado.</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-137">Os botões <strong></strong> <strong>de</strong> alternância Tachado e Sublinhado são exibidos por padrão, mas podem ser ocultos definindo os atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> como <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="7ec2c-138"><strong>Selador de cor</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="7ec2c-139"><strong>Selador de cor de realçada</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-140">Esse controle está oculto por padrão, mas pode ser exibido definindo o atributo <em>IsHighlightButtonVisible</em> como <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="7ec2c-141"><dt><span></span><span></span><strong></strong> (RichFont)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="7ec2c-142">Definir o <em>atributo FontType</em> como <code>RichFont</code> habilita a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="7ec2c-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="7ec2c-143"><strong>Caixa de combinação</strong> da família de fontes.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="7ec2c-144"><strong>Caixa de combinação</strong> tamanho da fonte.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="7ec2c-145"><strong>Aumentar a fonte</strong> e <strong>reduzir o incremento</strong> de tamanho da fonte e os botões de decremento.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="7ec2c-146"><strong>Botões</strong>de alternância Negrito, <strong>Itálico,</strong> <strong>Sublinhado</strong>e <strong>Tachado.</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-147">Os botões <strong></strong> <strong>de</strong> alternância Tachado e Sublinhado são exibidos por padrão e não podem ser ocultos definindo os atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> como <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="7ec2c-148"><strong>Selador de cor</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="7ec2c-149"><strong>Selador de cor de realçada</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-150">Esse controle é exibido por padrão e não pode ser ocultado definindo o atributo <em>IsHighlightButtonVisible</em> como <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="7ec2c-151"><strong>Botões de alternância</strong> <strong>de subscrito</strong> e Superscrito.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ec2c-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="7ec2c-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="7ec2c-154">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-154">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-155"><strong>Windows 8 e mais novos</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="7ec2c-156">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7ec2c-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-157">Os botões Aumentar/Reduzir nunca são exibidos na <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="7ec2c-158">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-159">Padrão quando o valor de <em>FontType</em> é igual <code>FontWithColor</code> ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="7ec2c-160"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-161">Padrão quando o valor de <em>FontType</em> é igual a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ec2c-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="7ec2c-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="7ec2c-164">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-164">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-165">Restrito a um dos seguintes valores (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="7ec2c-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-166">O realçamento de cores só está disponível em <strong>um FontControl</strong> quando o valor do atributo <em>FontType</em> é igual <code>FontWithColor</code> a ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="7ec2c-167">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-168">Padrão quando o valor de <em>FontType</em> é igual <code>FontWithColor</code> ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="7ec2c-169">Válido somente quando o valor de <em>FontType</em> for <code>FontWithColor</code> igual a ou <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="7ec2c-170"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-171">Padrão quando o valor de <em>FontType</em> é igual a <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="7ec2c-172">Válido somente quando o valor de <em>FontType</em> for <code>FontOnly</code> igual a ou <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ec2c-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="7ec2c-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="7ec2c-175">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-175">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-176">Restrito a um dos seguintes valores (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="7ec2c-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="7ec2c-177">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-178">Padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-178">Default.</span></span> <br/> </dd> <span data-ttu-id="7ec2c-179"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-180">Válido somente quando o valor de <em>FontType</em> for <code>FontOnly</code> igual a ou <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ec2c-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="7ec2c-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="7ec2c-183">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-183">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-184">Restrito a um dos seguintes valores (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="7ec2c-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="7ec2c-185">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-186">Padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-186">Default.</span></span> <br/> </dd> <span data-ttu-id="7ec2c-187"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-188">Válido somente quando o valor de <em>FontType</em> for <code>FontOnly</code> igual a ou <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ec2c-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="7ec2c-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="7ec2c-191">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-191">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-192">O tamanho máximo de ponto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="7ec2c-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-194">Um valor inteiro entre 1 e 9999, inclusive.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="7ec2c-195">O padrão é <strong>9999</strong>.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ec2c-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="7ec2c-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="7ec2c-198">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-198">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-199">O tamanho mínimo do ponto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="7ec2c-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="7ec2c-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-201">Um valor inteiro entre 1 e 9999, inclusive.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="7ec2c-202">O padrão é <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ec2c-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="7ec2c-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="7ec2c-205">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-205">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-206">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="7ec2c-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="7ec2c-207">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="7ec2c-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-208">Exibe somente as fontes TrueType e OpenType.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="7ec2c-209"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="7ec2c-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-210">Padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-210">Default.</span></span> <span data-ttu-id="7ec2c-211">Nenhuma restrição é colocada no tipo de fontes exibidas.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ec2c-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="7ec2c-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="7ec2c-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="7ec2c-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="7ec2c-214">Não</span><span class="sxs-lookup"><span data-stu-id="7ec2c-214">No</span></span><br/></td>
<td><span data-ttu-id="7ec2c-215">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="7ec2c-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-216">As fontes verticais são precedidas por um símbolo @ na lista <strong>família de fontes</strong> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="7ec2c-217">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="7ec2c-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-218">Padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-218">Default.</span></span> <span data-ttu-id="7ec2c-219">Exibe as fontes verticais que estão definidas para <strong>Mostrar</strong> no painel de controle <strong>fontes</strong> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="7ec2c-220"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="7ec2c-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="7ec2c-221">Permite que um aplicativo que não dá suporte a texto vertical oculte quaisquer fontes verticais definidas para <strong>Mostrar</strong> no painel de controle <strong>fontes</strong> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7ec2c-222">No Windows Vista, o painel de controle de <strong>fontes</strong> não oferece a funcionalidade de <strong>Mostrar</strong> ou <strong>ocultar</strong> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="7ec2c-223">Nesse caso, o atributo <em>ShowVerticalFonts</em> deve ser definido como <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="7ec2c-224">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7ec2c-224">Child elements</span></span>

<span data-ttu-id="7ec2c-225">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7ec2c-226">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7ec2c-226">Parent elements</span></span>



| <span data-ttu-id="7ec2c-227">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ec2c-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="7ec2c-228">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="7ec2c-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="7ec2c-229">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="7ec2c-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="7ec2c-230">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="7ec2c-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="7ec2c-231">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ec2c-231">Remarks</span></span>

<span data-ttu-id="7ec2c-232">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-232">Optional.</span></span>

<span data-ttu-id="7ec2c-233">Pode ocorrer no máximo uma vez para [](windowsribbon-element-controlgroup.md)cada elemento Control [**Group, grupo**](windowsribbon-element-group.md)ou [**menu**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="7ec2c-234">Quaisquer atributos de comando **FontControl** declarados na marcação, como [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), são substituídos pelos atributos dos controles individuais que compõem o **FontControl**.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="7ec2c-235">Qualquer tentativa de selecionar uma amostra de cor do seletor de cores de um [controle de fonte](windowsribbon-controls-fontcontrol.md) pode resultar em uma violação de acesso se nenhum manipulador de comando estiver associado ao controle.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="7ec2c-236">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ec2c-236">Examples</span></span>

<span data-ttu-id="7ec2c-237">O exemplo a seguir demonstra a marcação básica para os três tipos de [controle de fonte](windowsribbon-controls-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="7ec2c-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="7ec2c-238">Esta seção de código mostra as declarações de comando **FontControl** , cada uma com uma declaração de contêiner de [**grupo**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="7ec2c-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



<span data-ttu-id="7ec2c-239">Esta seção de código mostra as declarações de controle **FontControl** em que cada **FontControl** e [**grupo**](windowsribbon-element-group.md) é declarado em uma única guia.</span><span class="sxs-lookup"><span data-stu-id="7ec2c-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a><span data-ttu-id="7ec2c-240">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7ec2c-240">Element information</span></span>

* <span data-ttu-id="7ec2c-241">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ec2c-241">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="7ec2c-242">**Pode estar vazio**: Sim</span><span class="sxs-lookup"><span data-stu-id="7ec2c-242">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="7ec2c-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ec2c-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec2c-244">Controle de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="7ec2c-244">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="7ec2c-245">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="7ec2c-245">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="7ec2c-246">Exemplo de FontControl</span><span class="sxs-lookup"><span data-stu-id="7ec2c-246">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





