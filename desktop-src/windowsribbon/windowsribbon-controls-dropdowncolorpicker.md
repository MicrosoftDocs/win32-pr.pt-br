---
title: Drop-Down seletor de cores
description: A estrutura da faixa de opções do Windows fornece um controle de seletor de cores Drop-Down especializado que expõe uma variedade de configurações de cores por meio de um botão de divisão e seletor de cor de menu suspenso personalizável.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552cd05e619ba71653d0d72e8457f5d4c8c39624
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104366814"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="e89ed-103">Drop-Down seletor de cores</span><span class="sxs-lookup"><span data-stu-id="e89ed-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="e89ed-104">A estrutura da faixa de opções do Windows fornece um controle de seletor de cores Drop-Down especializado que expõe uma variedade de configurações de cores por meio de um botão de divisão e seletor de cor de menu suspenso personalizável.</span><span class="sxs-lookup"><span data-stu-id="e89ed-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="e89ed-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="e89ed-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="e89ed-106">Marcação</span><span class="sxs-lookup"><span data-stu-id="e89ed-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="e89ed-107">Código</span><span class="sxs-lookup"><span data-stu-id="e89ed-107">Code</span></span>](#code)
    -   [<span data-ttu-id="e89ed-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e89ed-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="e89ed-109">Manipuladores de comandos</span><span class="sxs-lookup"><span data-stu-id="e89ed-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="e89ed-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e89ed-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="e89ed-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="e89ed-111">Introduction</span></span>

<span data-ttu-id="e89ed-112">Ao emular a aparência e a funcionalidade do Microsoft Office seletor de cores, a estrutura da faixa de opções é capaz de se beneficiar e contribuir para, consistência e familiaridade em uma ampla gama de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e89ed-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="e89ed-113">Marcação</span><span class="sxs-lookup"><span data-stu-id="e89ed-113">Markup</span></span>

<span data-ttu-id="e89ed-114">Como todos os controles de faixa de faixas, o seletor de cor Drop-Down é facilmente implementado e personalizado por meio de marcação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="e89ed-115">A estrutura fornece vários atributos de elemento para o seletor de cor Drop-Down para expor vários níveis de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="e89ed-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="e89ed-116">A tabela a seguir lista os atributos do seletor de cor Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="e89ed-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e89ed-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="e89ed-117">Attribute</span></span></th>
<th><span data-ttu-id="e89ed-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="e89ed-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e89ed-119">Cortemplate</span><span class="sxs-lookup"><span data-stu-id="e89ed-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="e89ed-120">Modelos de layout que especificam o tipo de Drop-Down seletor de cor.</span><span class="sxs-lookup"><span data-stu-id="e89ed-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="e89ed-121">Há três modelos, cada um deles especifica um layout de controle e valores padrão para atributos associados e chaves de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e89ed-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-122">Chips</span><span class="sxs-lookup"><span data-stu-id="e89ed-122">ChipSize</span></span></td>
<td><span data-ttu-id="e89ed-123">O tamanho de cada chip de cor (ou amostra).</span><span class="sxs-lookup"><span data-stu-id="e89ed-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-124">Colunas</span><span class="sxs-lookup"><span data-stu-id="e89ed-124">Columns</span></span></td>
<td><span data-ttu-id="e89ed-125">O número de colunas de chip de cor (ou amostra).</span><span class="sxs-lookup"><span data-stu-id="e89ed-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="e89ed-126">CommandName</span></span></td>
<td><span data-ttu-id="e89ed-127">O nome da declaração de comando associada.</span><span class="sxs-lookup"><span data-stu-id="e89ed-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="e89ed-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="e89ed-129">Exibe (ou oculta) o botão <strong>automático</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="e89ed-130">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="e89ed-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="e89ed-132">Exibe (ou oculta) o botão <strong>sem cor</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="e89ed-133">Válido para todos os valores de <em>colortemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="e89ed-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="e89ed-135">O número de linhas de chip de cor (ou amostra) na área <strong>cores recentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="e89ed-136">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="e89ed-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="e89ed-138">O número de linhas de chip de cor (ou amostra) na área <strong>cores padrão</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="e89ed-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="e89ed-140">O número de linhas de chip de cor (ou amostra) na área <strong>cores do tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="e89ed-141">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e89ed-142">As capturas de tela a seguir ilustram os layouts padrão do seletor de cor Drop-Down para os três modelos de cor.</span><span class="sxs-lookup"><span data-stu-id="e89ed-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e89ed-143">`ThemeColors`: \[ \] ![ captura de tela de nova linha do elemento dropdowncolorpicker com o atributo colortemplate definido como ' themecolors '. ](images/markup/colortemplate.themedcolors.1.png) \[ separados\]</span><span class="sxs-lookup"><span data-stu-id="e89ed-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="e89ed-144">`standardcolors`: \[ \] ![ captura de tela de nova linha do elemento dropdowncolorpicker com o atributo colortemplate definido como ' standardcolors '. ](images/markup/colortemplate.standardcolors.3.png) \[ separados\]</span><span class="sxs-lookup"><span data-stu-id="e89ed-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="e89ed-145">`highlightcolors`: \[ \] ![ captura de tela de nova linha do elemento dropdowncolorpicker com o atributo colortemplate definido como ' highlightColors '.](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="e89ed-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="e89ed-146">A marcação básica necessária para cada tipo de seletor de cor Drop-Down é demonstrada nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="e89ed-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="e89ed-147">O seletor de cor Drop-Down é um controle de [botão](windowsribbon-controls-button.md) válido em um modelo [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="e89ed-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a><span data-ttu-id="e89ed-148">Código</span><span class="sxs-lookup"><span data-stu-id="e89ed-148">Code</span></span>

<span data-ttu-id="e89ed-149">Como um controle especializado que dá suporte à personalização, qualquer implementação do seletor de cores Drop-Down que aproveita esses recursos requer um código de aplicativo especializado para gerenciar Propriedades e manipular quaisquer comandos emitidos pelo controle.</span><span class="sxs-lookup"><span data-stu-id="e89ed-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="e89ed-150">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e89ed-150">Properties</span></span>

<span data-ttu-id="e89ed-151">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle do seletor de cor Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="e89ed-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="e89ed-152">Normalmente, uma propriedade Drop-Down seletor de cores é atualizada na interface do usuário da faixa de chamadas invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="e89ed-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="e89ed-153">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="e89ed-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="e89ed-154">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="e89ed-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="e89ed-155">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="e89ed-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="e89ed-156">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="e89ed-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="e89ed-157">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle do seletor de cor Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="e89ed-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e89ed-158">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="e89ed-158">Property Key</span></span></th>
<th><span data-ttu-id="e89ed-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="e89ed-159">Description</span></span></th>
<th><span data-ttu-id="e89ed-160">Observações</span><span class="sxs-lookup"><span data-stu-id="e89ed-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e89ed-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="e89ed-162">Define o rótulo para o botão de cor <strong>automático</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="e89ed-163">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="e89ed-164">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="e89ed-166">Define o valor de cor selecionado como um <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="e89ed-167">Válido somente quando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> tem um valor de <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="e89ed-168">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="e89ed-170">Define o tipo de cor selecionado.</span><span class="sxs-lookup"><span data-stu-id="e89ed-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="e89ed-171">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="e89ed-173">Define a capacidade de um controle de responder à interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e89ed-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="e89ed-174">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="e89ed-176">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="e89ed-178">Define a cadeia de caracteres para um rótulo de controle.</span><span class="sxs-lookup"><span data-stu-id="e89ed-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="e89ed-179">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="e89ed-181">Define a imagem grande de alto contraste a ser exibida para um controle.</span><span class="sxs-lookup"><span data-stu-id="e89ed-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="e89ed-182">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="e89ed-183">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">especificando recursos de imagem da faixa de Ribbon</a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="e89ed-185">Define a imagem grande a ser exibida para um controle.</span><span class="sxs-lookup"><span data-stu-id="e89ed-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="e89ed-186">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="e89ed-187">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">especificando recursos de imagem da faixa de Ribbon</a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="e89ed-189">Define o rótulo para o botão <strong>mais cores...</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="e89ed-190">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="e89ed-191">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="e89ed-193">Define o rótulo para o botão <strong>sem cor</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="e89ed-194">Válido para todos os valores de <em>colortemplate</em> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="e89ed-195">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="e89ed-197">Define o rótulo para a categoria de <strong>cores recentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="e89ed-198">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="e89ed-199">Esse é o único modelo que contém categorias rotuladas.</span><span class="sxs-lookup"><span data-stu-id="e89ed-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="e89ed-200">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="e89ed-202">Define a pequena imagem de alto contraste a ser exibida para um controle.</span><span class="sxs-lookup"><span data-stu-id="e89ed-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="e89ed-203">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="e89ed-204">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">especificando recursos de imagem da faixa de Ribbon</a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="e89ed-206">Define a imagem pequena a ser exibida para um controle.</span><span class="sxs-lookup"><span data-stu-id="e89ed-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="e89ed-207">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="e89ed-208">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">especificando recursos de imagem da faixa de Ribbon</a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="e89ed-210">Define uma matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para as amostras de um seletor de cor Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="e89ed-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="e89ed-211">Cada seletor de cor Drop-Down <em>colortemplate</em> contém uma <code>StandardColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="e89ed-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e89ed-212">Os valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> das colunas <em>StandardColorGridRows</em> x <em></em> iniciais da matriz são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e89ed-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="e89ed-213">Se a matriz definir menos cores do que o número de <code>StandardColors</code> amostras declaradas na marcação, espaços vazios serão exibidos para os chips ausentes.</span><span class="sxs-lookup"><span data-stu-id="e89ed-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="e89ed-214">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="e89ed-216">Define o rótulo para a categoria <strong>cores padrão</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="e89ed-217">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="e89ed-218">Esse é o único modelo que contém categorias rotuladas.</span><span class="sxs-lookup"><span data-stu-id="e89ed-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="e89ed-219">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="e89ed-221">Define uma matriz de cadeia de caracteres de dicas de ferramentas de amostra de cor para a <code>StandardColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="e89ed-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="e89ed-222">Cada seletor de cor Drop-Down <em>colortemplate</em> contém uma <code>StandardColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="e89ed-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e89ed-223">Somente as dicas de ferramenta necessárias para rotular as amostras de cor exibidas na <code>StandardColors</code> grade são usadas.</span><span class="sxs-lookup"><span data-stu-id="e89ed-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="e89ed-224">Se menos rótulos forem fornecidos do que o número de amostras na <code>StandardColors</code> grade, um padrão será fornecido para as amostras de remainining.</span><span class="sxs-lookup"><span data-stu-id="e89ed-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="e89ed-225">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="e89ed-227">Define uma matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para as amostras de um seletor de cor Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="e89ed-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="e89ed-228">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e89ed-229">Os valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> das colunas <em>ThemeColorGridRows</em> x <em></em> iniciais da matriz são exibidos.</span><span class="sxs-lookup"><span data-stu-id="e89ed-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="e89ed-230">Se a matriz definir menos cores do que o número de <code>ThemeColors</code> amostras declaradas na marcação, espaços vazios serão exibidos para os chips ausentes.</span><span class="sxs-lookup"><span data-stu-id="e89ed-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="e89ed-231">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="e89ed-233">Define a matriz de cadeia de caracteres das dicas de ferramentas de amostra de cor para a <code>ThemeColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="e89ed-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="e89ed-234">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e89ed-235">Somente as dicas de ferramenta necessárias para rotular as amostras de cor exibidas na <code>ThemeColors</code> grade são usadas.</span><span class="sxs-lookup"><span data-stu-id="e89ed-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="e89ed-236">Se menos rótulos forem fornecidos do que o número de amostras na <code>ThemeColors</code> grade, um padrão será fornecido para as amostras de remainining.</span><span class="sxs-lookup"><span data-stu-id="e89ed-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="e89ed-237">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="e89ed-239">Define o rótulo para a categoria <strong>cores do tema</strong> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="e89ed-240">Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="e89ed-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="e89ed-241">Esse é o único modelo que contém categorias rotuladas.</span><span class="sxs-lookup"><span data-stu-id="e89ed-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="e89ed-242">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e89ed-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="e89ed-244">Define a cadeia de caracteres para uma descrição da dica de ferramenta associada a um <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="e89ed-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="e89ed-245">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e89ed-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="e89ed-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="e89ed-247">Define a cadeia de caracteres para uma dica de ferramenta de comando.</span><span class="sxs-lookup"><span data-stu-id="e89ed-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="e89ed-248">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="e89ed-249">Manipuladores de comandos</span><span class="sxs-lookup"><span data-stu-id="e89ed-249">Command handlers</span></span>

<span data-ttu-id="e89ed-250">O método [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) é usado para personalizar um seletor de cores Drop-Down por meio das chaves de propriedade listadas acima.</span><span class="sxs-lookup"><span data-stu-id="e89ed-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="e89ed-251">O exemplo a seguir demonstra como definir as amostras de cor de um seletor de cor Drop-Down, com base em uma preferência de estilo personalizado ou em uma grade de amostra personalizada que é declarada na marcação.</span><span class="sxs-lookup"><span data-stu-id="e89ed-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



<span data-ttu-id="e89ed-252">O exemplo a seguir demonstra uma implementação do método [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) que expõe as cores de amostra do seletor de cor Drop-Down para o aplicativo da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="e89ed-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e89ed-253">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e89ed-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e89ed-254">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="e89ed-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="e89ed-255">**Elemento de marcação DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="e89ed-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="e89ed-256">Propriedades do seletor de cores</span><span class="sxs-lookup"><span data-stu-id="e89ed-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="e89ed-257">Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="e89ed-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="e89ed-258">Exemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="e89ed-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

