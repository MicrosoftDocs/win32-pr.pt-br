---
title: Elemento DropDownColorPicker
description: Representa um Pickercontrol de cor de Drop-Down que, quando clicado, exibe uma paleta de amostras de cor.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Faixa de DropDownColorPicker do elemento do Windows
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442897"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="79638-104">Elemento DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="79638-104">DropDownColorPicker element</span></span>

<span data-ttu-id="79638-105">Representa um controle [seletor de cores suspensa](windowsribbon-controls-dropdowncolorpicker.md)que, quando clicado, exibe uma paleta de amostras de cor.</span><span class="sxs-lookup"><span data-stu-id="79638-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="79638-106">Uso</span><span class="sxs-lookup"><span data-stu-id="79638-106">Usage</span></span>

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="79638-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="79638-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79638-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="79638-108">Attribute</span></span></th>
<th><span data-ttu-id="79638-109">Type</span><span class="sxs-lookup"><span data-stu-id="79638-109">Type</span></span></th>
<th><span data-ttu-id="79638-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="79638-110">Required</span></span></th>
<th><span data-ttu-id="79638-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="79638-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79638-112"><strong>Chips</strong></span><span class="sxs-lookup"><span data-stu-id="79638-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="79638-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="79638-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="79638-114">Não</span><span class="sxs-lookup"><span data-stu-id="79638-114">No</span></span><br/></td>
<td><span data-ttu-id="79638-115">O tamanho de cada amostra ou chip de cor.</span><span class="sxs-lookup"><span data-stu-id="79638-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="79638-116">Restrito a um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="79638-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="79638-117">
<dt><span></span><span></span><strong></strong> Menores</span><span class="sxs-lookup"><span data-stu-id="79638-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-118">Cada chip de cor é um quadrado de pixel 11x11.</span><span class="sxs-lookup"><span data-stu-id="79638-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="79638-119"><dt><span></span><span></span><strong></strong> Médio</span><span class="sxs-lookup"><span data-stu-id="79638-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-120">Cada chip de cor é um quadrado de 16x16 pixels.</span><span class="sxs-lookup"><span data-stu-id="79638-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="79638-121"><dt><span></span><span></span><strong></strong> Vários</span><span class="sxs-lookup"><span data-stu-id="79638-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-122">Cada chip de cor é um quadrado de pixel 24x24.</span><span class="sxs-lookup"><span data-stu-id="79638-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79638-123"><strong>Cortemplate</strong></span><span class="sxs-lookup"><span data-stu-id="79638-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="79638-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="79638-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="79638-125">Não</span><span class="sxs-lookup"><span data-stu-id="79638-125">No</span></span><br/></td>
<td><span data-ttu-id="79638-126">Modelos de layout que especificam o tipo de <a href="windowsribbon-controls-dropdowncolorpicker.md">seletor de cores suspenso</a>.</span><span class="sxs-lookup"><span data-stu-id="79638-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="79638-127">Restrito a um dos valores a seguir (se nenhum atributo opcional relacionado a um <em>colortemplate</em> for declarado, a exibição padrão será mostrada):</span><span class="sxs-lookup"><span data-stu-id="79638-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="79638-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span><span class="sxs-lookup"><span data-stu-id="79638-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-129">Padrão.</span><span class="sxs-lookup"><span data-stu-id="79638-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="79638-130">Definir o atributo <em>colortemplate</em> para <code>ThemeColors</code> habilitar a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="79638-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="79638-131">Âncora de SplitButton.</span><span class="sxs-lookup"><span data-stu-id="79638-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="79638-132">O botão de cor <strong>automático</strong> é exibido por padrão.</span><span class="sxs-lookup"><span data-stu-id="79638-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="79638-133">Grade de amostras de <strong>cores de tema</strong> do Windows.</span><span class="sxs-lookup"><span data-stu-id="79638-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="79638-134">Grade de amostra de <strong>cores padrão</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="79638-135">A grade de amostras de <strong>cores recentes</strong> é opcional.</span><span class="sxs-lookup"><span data-stu-id="79638-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="79638-136">Iniciador da caixa de diálogo <strong>mais cores</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="79638-137"><strong>Nenhum</strong> botão de cor de cor é exibido por padrão.</span><span class="sxs-lookup"><span data-stu-id="79638-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="79638-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span><span class="sxs-lookup"><span data-stu-id="79638-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="79638-139">Definir o atributo <em>colortemplate</em> para <code>StandardColors</code> habilitar a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="79638-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="79638-140">Âncora de SplitButton.</span><span class="sxs-lookup"><span data-stu-id="79638-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="79638-141">O botão de cor <strong>automático</strong> é exibido por padrão.</span><span class="sxs-lookup"><span data-stu-id="79638-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="79638-142">Grade de amostra de <strong>cores padrão</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="79638-143">Iniciador da caixa de diálogo <strong>mais cores</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="79638-144"><strong>Nenhum</strong> botão de cor de cor é exibido por padrão.</span><span class="sxs-lookup"><span data-stu-id="79638-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="79638-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span><span class="sxs-lookup"><span data-stu-id="79638-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="79638-146">Definir o atributo <em>colortemplate</em> para <code>HighlightColors</code> habilitar a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="79638-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="79638-147">Âncora de SplitButton.</span><span class="sxs-lookup"><span data-stu-id="79638-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="79638-148">Grade de amostra de <strong>cores padrão</strong> sem cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="79638-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="79638-149"><strong>Nenhum</strong> botão de cor de cor é exibido por padrão.</span><span class="sxs-lookup"><span data-stu-id="79638-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79638-150"><strong>Colunas</strong></span><span class="sxs-lookup"><span data-stu-id="79638-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="79638-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="79638-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="79638-152">Não</span><span class="sxs-lookup"><span data-stu-id="79638-152">No</span></span><br/></td>
<td><span data-ttu-id="79638-153">O número de colunas de chip de cor (ou amostra).</span><span class="sxs-lookup"><span data-stu-id="79638-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="79638-154">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="79638-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-155">Qualquer valor inteiro positivo entre 1 e 256, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79638-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79638-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="79638-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="79638-157">xs: positiveInteger ou xs: String</span><span class="sxs-lookup"><span data-stu-id="79638-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="79638-158">Não</span><span class="sxs-lookup"><span data-stu-id="79638-158">No</span></span><br/></td>
<td><span data-ttu-id="79638-159">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79638-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="79638-160">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)</span><span class="sxs-lookup"><span data-stu-id="79638-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-161">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79638-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="79638-162">O valor deve ser exclusivo no documento XML da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="79638-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="79638-163">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="79638-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79638-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="79638-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="79638-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="79638-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="79638-166">Não</span><span class="sxs-lookup"><span data-stu-id="79638-166">No</span></span><br/></td>
<td><span data-ttu-id="79638-167">Exibe (ou oculta) o botão de cor <strong>automática</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="79638-168">Válido somente quando <code>StandardColors</code> ou <code>ThemeColors</code> é especificado para o atributo <em>colortemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="79638-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="79638-169">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="79638-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="79638-170">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="79638-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="79638-171"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="79638-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79638-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="79638-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="79638-173">Boolean</span><span class="sxs-lookup"><span data-stu-id="79638-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="79638-174">Não</span><span class="sxs-lookup"><span data-stu-id="79638-174">No</span></span><br/></td>
<td><span data-ttu-id="79638-175">Exibe (ou oculta) o botão <strong>sem cor</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="79638-176">Válido para todos os valores de <em>colortemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="79638-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="79638-177">Restrito a um dos valores a seguir (0 e 1 não são válidos):</span><span class="sxs-lookup"><span data-stu-id="79638-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="79638-178">
<dt><span></span><span></span><strong></strong> true</span><span class="sxs-lookup"><span data-stu-id="79638-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="79638-179"><dt><span></span><span></span><strong></strong> for</span><span class="sxs-lookup"><span data-stu-id="79638-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79638-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="79638-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="79638-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="79638-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="79638-182">Não</span><span class="sxs-lookup"><span data-stu-id="79638-182">No</span></span><br/></td>
<td><span data-ttu-id="79638-183">O número de linhas de chip de cor (ou amostra) na área <strong>cores recentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="79638-184">Válido somente quando <code>ThemeColors</code> é especificado para o atributo <em>colortemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="79638-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="79638-185">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="79638-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-186">Qualquer valor inteiro positivo entre 1 e 256, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79638-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79638-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="79638-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="79638-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="79638-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="79638-189">Não</span><span class="sxs-lookup"><span data-stu-id="79638-189">No</span></span><br/></td>
<td><span data-ttu-id="79638-190">O número de linhas de chip de cor (ou amostra) na área <strong>cores padrão</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="79638-191">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="79638-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-192">Qualquer valor inteiro positivo entre 1 e 256, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79638-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79638-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="79638-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="79638-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="79638-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="79638-195">Não</span><span class="sxs-lookup"><span data-stu-id="79638-195">No</span></span><br/></td>
<td><span data-ttu-id="79638-196">O número de linhas de chip de cor (ou amostra) na área <strong>cores do tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="79638-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="79638-197">Válido somente quando <code>ThemeColors</code> é especificado para o atributo <em>colortemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="79638-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="79638-198">
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="79638-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="79638-199">Qualquer valor inteiro positivo entre 1 e 256, inclusive.</span><span class="sxs-lookup"><span data-stu-id="79638-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="79638-200">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="79638-200">Child elements</span></span>

<span data-ttu-id="79638-201">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="79638-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="79638-202">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="79638-202">Parent elements</span></span>



| <span data-ttu-id="79638-203">Elemento</span><span class="sxs-lookup"><span data-stu-id="79638-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="79638-204">**Controlador de controle**</span><span class="sxs-lookup"><span data-stu-id="79638-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="79638-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="79638-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="79638-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="79638-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="79638-207">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="79638-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="79638-208">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="79638-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="79638-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="79638-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="79638-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="79638-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="79638-211">Comentários</span><span class="sxs-lookup"><span data-stu-id="79638-211">Remarks</span></span>

<span data-ttu-id="79638-212">Opcional.</span><span class="sxs-lookup"><span data-stu-id="79638-212">Optional.</span></span>

<span data-ttu-id="79638-213">Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md)Group [**, DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="79638-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="79638-214">Exemplos</span><span class="sxs-lookup"><span data-stu-id="79638-214">Examples</span></span>

<span data-ttu-id="79638-215">O exemplo a seguir demonstra a marcação básica para todos os três tipos de [seletor de cor suspenso](windowsribbon-controls-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="79638-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="79638-216">Esta seção de código mostra as declarações de comando para três elementos **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="79638-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



<span data-ttu-id="79638-217">Esta seção de código mostra os três tipos de declarações de controle **DropDownColorPicker** .</span><span class="sxs-lookup"><span data-stu-id="79638-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="79638-218">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="79638-218">Element information</span></span>

* <span data-ttu-id="79638-219">**Sistema mínimo com suporte**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="79638-219">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="79638-220">**Pode estar vazio**: Sim</span><span class="sxs-lookup"><span data-stu-id="79638-220">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="79638-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="79638-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79638-222">Controle seletor de cores suspensa</span><span class="sxs-lookup"><span data-stu-id="79638-222">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="79638-223">Exemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="79638-223">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





