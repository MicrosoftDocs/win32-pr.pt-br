---
title: Drop-Down Seletor de Cor
description: A estrutura da Faixa de Opções do Windows fornece um controle de Drop-Down Seletor de Cor especializado que expõe uma variedade de configurações de cores por meio de um botão de divisão e do seletor de cores de lista listada personalizável.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443657"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="f80ca-103">Drop-Down Seletor de Cor</span><span class="sxs-lookup"><span data-stu-id="f80ca-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="f80ca-104">A estrutura da Faixa de Opções do Windows fornece um controle de Drop-Down Seletor de Cor especializado que expõe uma variedade de configurações de cores por meio de um botão de divisão e do seletor de cores de lista listada personalizável.</span><span class="sxs-lookup"><span data-stu-id="f80ca-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="f80ca-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="f80ca-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f80ca-106">Marcação</span><span class="sxs-lookup"><span data-stu-id="f80ca-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="f80ca-107">Código</span><span class="sxs-lookup"><span data-stu-id="f80ca-107">Code</span></span>](#code)
    -   [<span data-ttu-id="f80ca-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f80ca-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="f80ca-109">Manipuladores de comandos</span><span class="sxs-lookup"><span data-stu-id="f80ca-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="f80ca-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f80ca-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="f80ca-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="f80ca-111">Introduction</span></span>

<span data-ttu-id="f80ca-112">Ao emular a aparência e a funcionalidade do selador de cores Microsoft Office, a estrutura da Faixa de Opções é capaz de se beneficiar e contribuir com a consistência e a familiaridade em uma ampla variedade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f80ca-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="f80ca-113">Marcação</span><span class="sxs-lookup"><span data-stu-id="f80ca-113">Markup</span></span>

<span data-ttu-id="f80ca-114">Como todos os controles de Faixa de Opções, Drop-Down Seletor de Cor é facilmente implementado e personalizado por meio da marcação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="f80ca-115">A estrutura fornece vários atributos de elemento para o Drop-Down Seletor de Cor expor vários níveis de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="f80ca-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="f80ca-116">A tabela a seguir lista os Drop-Down Seletor de Cor atributos.</span><span class="sxs-lookup"><span data-stu-id="f80ca-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f80ca-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="f80ca-117">Attribute</span></span></th>
<th><span data-ttu-id="f80ca-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f80ca-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f80ca-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="f80ca-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="f80ca-120">Modelos de layout que especificam o tipo de Drop-Down Seletor de Cor.</span><span class="sxs-lookup"><span data-stu-id="f80ca-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="f80ca-121">Há três modelos, cada um especificando um layout de controle e valores padrão para atributos associados e chaves de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f80ca-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-122">ChipSize</span><span class="sxs-lookup"><span data-stu-id="f80ca-122">ChipSize</span></span></td>
<td><span data-ttu-id="f80ca-123">O tamanho de cada chip de cor (ou amostra).</span><span class="sxs-lookup"><span data-stu-id="f80ca-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-124">Colunas</span><span class="sxs-lookup"><span data-stu-id="f80ca-124">Columns</span></span></td>
<td><span data-ttu-id="f80ca-125">O número de colunas de chip de cores (ou swatch).</span><span class="sxs-lookup"><span data-stu-id="f80ca-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="f80ca-126">CommandName</span></span></td>
<td><span data-ttu-id="f80ca-127">O nome da declaração command associada.</span><span class="sxs-lookup"><span data-stu-id="f80ca-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="f80ca-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="f80ca-129">Exibe (ou oculta) o <strong>botão</strong> Automático.</span><span class="sxs-lookup"><span data-stu-id="f80ca-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="f80ca-130">Válido somente quando <em>ColorTemplate</em> tem um valor <code>ThemeColors</code> de ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="f80ca-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="f80ca-132">Exibe (ou oculta) o <strong>botão Sem</strong> cor.</span><span class="sxs-lookup"><span data-stu-id="f80ca-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="f80ca-133">Válido para todos os <em>valores colorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="f80ca-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="f80ca-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="f80ca-135">O número de linhas de chip de cores (ou amostra) na <strong>área Cores</strong> recentes.</span><span class="sxs-lookup"><span data-stu-id="f80ca-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="f80ca-136">Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="f80ca-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="f80ca-138">O número de linhas de chip de cores (ou swatch) na <strong>área Cores</strong> padrão.</span><span class="sxs-lookup"><span data-stu-id="f80ca-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="f80ca-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="f80ca-140">O número de linhas de chip de cores (ou swatch) na área <strong>Cores do</strong> tema.</span><span class="sxs-lookup"><span data-stu-id="f80ca-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="f80ca-141">Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f80ca-142">As capturas de tela a seguir ilustram os layouts Drop-Down Seletor de Cor padrão para os três modelos de cores.</span><span class="sxs-lookup"><span data-stu-id="f80ca-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f80ca-143">`ThemeColors`: \[ captura de tela de nova linha do elemento \] ![ dropdowncolorpicker com o atributo colortemplate definido como 'themecolors'. ](images/markup/colortemplate.themedcolors.1.png) \[ Newline\]</span><span class="sxs-lookup"><span data-stu-id="f80ca-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="f80ca-144">`standardcolors`: \[ captura de tela de nova linha do elemento \] ![ dropdowncolorpicker com o atributo colortemplate definido como 'standardcolors'. ](images/markup/colortemplate.standardcolors.3.png) \[ Newline\]</span><span class="sxs-lookup"><span data-stu-id="f80ca-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="f80ca-145">`highlightcolors`: \[ captura de tela de nova linha do elemento \] ![ dropdowncolorpicker com o atributo colortemplate definido como 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="f80ca-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="f80ca-146">A marcação básica necessária para cada tipo Drop-Down Seletor de Cor é demonstrada nos exemplos a seguir:</span><span class="sxs-lookup"><span data-stu-id="f80ca-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="f80ca-147">O Drop-Down Seletor de Cor é um controle [Button](windowsribbon-controls-button.md) válido em um [**modelo SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="f80ca-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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





## <a name="code"></a><span data-ttu-id="f80ca-148">Código</span><span class="sxs-lookup"><span data-stu-id="f80ca-148">Code</span></span>

<span data-ttu-id="f80ca-149">Como um controle especializado que dá suporte à personalização, qualquer implementação do Drop-Down Seletor de Cor que aproveita essas funcionalidades requer um código de aplicativo especializado para gerenciar propriedades e manipular todos os Comandos emitidos pelo controle.</span><span class="sxs-lookup"><span data-stu-id="f80ca-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="f80ca-150">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f80ca-150">Properties</span></span>

<span data-ttu-id="f80ca-151">A estrutura ribbon define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle Drop-Down Seletor de Cor de opções.</span><span class="sxs-lookup"><span data-stu-id="f80ca-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="f80ca-152">Normalmente, uma propriedade Drop-Down Seletor de Cor é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)</span><span class="sxs-lookup"><span data-stu-id="f80ca-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="f80ca-153">O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)</span><span class="sxs-lookup"><span data-stu-id="f80ca-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="f80ca-154">O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="f80ca-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="f80ca-155">Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="f80ca-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="f80ca-156">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)</span><span class="sxs-lookup"><span data-stu-id="f80ca-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="f80ca-157">A tabela a seguir lista as chaves de propriedade associadas ao controle Drop-Down Seletor de Cor dados.</span><span class="sxs-lookup"><span data-stu-id="f80ca-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f80ca-158">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="f80ca-158">Property Key</span></span></th>
<th><span data-ttu-id="f80ca-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="f80ca-159">Description</span></span></th>
<th><span data-ttu-id="f80ca-160">Observações</span><span class="sxs-lookup"><span data-stu-id="f80ca-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f80ca-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="f80ca-162">Define o rótulo para o <strong>botão Cor</strong> automática.</span><span class="sxs-lookup"><span data-stu-id="f80ca-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="f80ca-163">Válido somente quando <em>ColorTemplate</em> tem um valor <code>ThemeColors</code> de ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="f80ca-164">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="f80ca-166">Define o valor de cor selecionado como <a href="/windows/win32/gdi/colorref">um COLORREF.</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="f80ca-167">Válido somente quando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> tem um valor de <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="f80ca-168">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="f80ca-170">Define o tipo de cor selecionado.</span><span class="sxs-lookup"><span data-stu-id="f80ca-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="f80ca-171">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="f80ca-173">Define a capacidade de um controle responder à interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f80ca-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="f80ca-174">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="f80ca-176">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="f80ca-178">Define a cadeia de caracteres para um rótulo de controle.</span><span class="sxs-lookup"><span data-stu-id="f80ca-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="f80ca-179">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="f80ca-181">Define a imagem de alto contraste grande a ser exibida para um controle .</span><span class="sxs-lookup"><span data-stu-id="f80ca-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="f80ca-182">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="f80ca-183">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">Especificando recursos de</a>imagem da faixa de opções .</span><span class="sxs-lookup"><span data-stu-id="f80ca-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="f80ca-185">Define a imagem grande a ser exibida para um controle .</span><span class="sxs-lookup"><span data-stu-id="f80ca-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="f80ca-186">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="f80ca-187">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">Especificando recursos de</a>imagem da faixa de opções .</span><span class="sxs-lookup"><span data-stu-id="f80ca-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="f80ca-189">Define o rótulo para o <strong>botão Mais cores....</strong></span><span class="sxs-lookup"><span data-stu-id="f80ca-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="f80ca-190">Válido somente quando <em>ColorTemplate</em> tem um valor <code>ThemeColors</code> de ou <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="f80ca-191">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="f80ca-193">Define o rótulo para o <strong>botão Sem</strong> cor.</span><span class="sxs-lookup"><span data-stu-id="f80ca-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="f80ca-194">Válido para todos os <em>valores colorTemplate.</em></span><span class="sxs-lookup"><span data-stu-id="f80ca-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="f80ca-195">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="f80ca-197">Define o rótulo para a <strong>categoria Cores recentes.</strong></span><span class="sxs-lookup"><span data-stu-id="f80ca-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="f80ca-198">Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="f80ca-199">Esse é o único modelo que contém categorias rotuladas.</span><span class="sxs-lookup"><span data-stu-id="f80ca-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="f80ca-200">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="f80ca-202">Define a pequena imagem de alto contraste a ser exibida para um controle .</span><span class="sxs-lookup"><span data-stu-id="f80ca-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="f80ca-203">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="f80ca-204">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">Especificando recursos de</a>imagem da faixa de opções .</span><span class="sxs-lookup"><span data-stu-id="f80ca-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="f80ca-206">Define a imagem pequena a ser exibida para um controle .</span><span class="sxs-lookup"><span data-stu-id="f80ca-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="f80ca-207">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="f80ca-208">Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">Especificando recursos de</a>imagem da faixa de opções .</span><span class="sxs-lookup"><span data-stu-id="f80ca-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="f80ca-210">Define uma matriz de <a href="/windows/win32/gdi/colorref">valores COLORREF</a> para as travas de um Drop-Down Seletor de Cor.</span><span class="sxs-lookup"><span data-stu-id="f80ca-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="f80ca-211">Cada Drop-Down Seletor de Cor <em>ColorTemplate contém</em> uma <code>StandardColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="f80ca-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f80ca-212">Os <a href="/windows/win32/gdi/colorref">valores COLORREF</a> das Colunas <em>StandardColorGridRows</em> x <em>iniciais</em> da matriz são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f80ca-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="f80ca-213">Se a matriz definir menos cores do que o número de travas declaradas na marcação, espaços vazios serão exibidos <code>StandardColors</code> para os chips ausentes.</span><span class="sxs-lookup"><span data-stu-id="f80ca-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="f80ca-214">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="f80ca-216">Define o rótulo para a <strong>categoria Cores</strong> padrão.</span><span class="sxs-lookup"><span data-stu-id="f80ca-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="f80ca-217">Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="f80ca-218">Esse é o único modelo que contém categorias rotuladas.</span><span class="sxs-lookup"><span data-stu-id="f80ca-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="f80ca-219">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="f80ca-221">Define uma matriz de cadeia de caracteres de dicas de ferramenta de amostra de cor para a <code>StandardColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="f80ca-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="f80ca-222">Cada Drop-Down Seletor de Cor <em>ColorTemplate contém</em> uma <code>StandardColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="f80ca-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f80ca-223">Somente as dicas de ferramenta necessárias para rotular as travas de cores exibidas na <code>StandardColors</code> grade são usadas.</span><span class="sxs-lookup"><span data-stu-id="f80ca-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="f80ca-224">Se menos rótulos são fornecidos do que o número de travas na grade, um padrão é fornecido para as <code>StandardColors</code> travas que permanecem.</span><span class="sxs-lookup"><span data-stu-id="f80ca-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="f80ca-225">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="f80ca-227">Define uma matriz de <a href="/windows/win32/gdi/colorref">valores COLORREF</a> para as travas de um Drop-Down Seletor de Cor.</span><span class="sxs-lookup"><span data-stu-id="f80ca-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="f80ca-228">Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f80ca-229">Os <a href="/windows/win32/gdi/colorref">valores COLORREF</a> das <em>colunas</em> <em>ThemeColorGridRows</em> x iniciais da matriz são exibidos.</span><span class="sxs-lookup"><span data-stu-id="f80ca-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="f80ca-230">Se a matriz definir menos cores do que o número de travas declaradas na marcação, espaços vazios serão exibidos <code>ThemeColors</code> para os chips ausentes.</span><span class="sxs-lookup"><span data-stu-id="f80ca-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="f80ca-231">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="f80ca-233">Define a matriz de cadeia de caracteres de dicas de ferramenta de amostra de cor para a <code>ThemeColors</code> grade.</span><span class="sxs-lookup"><span data-stu-id="f80ca-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="f80ca-234">Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f80ca-235">Somente as dicas de ferramenta necessárias para rotular as travas de cores exibidas na <code>ThemeColors</code> grade são usadas.</span><span class="sxs-lookup"><span data-stu-id="f80ca-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="f80ca-236">Se menos rótulos são fornecidos do que o número de travas na grade, um padrão é fornecido para as <code>ThemeColors</code> travas que permanecem.</span><span class="sxs-lookup"><span data-stu-id="f80ca-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="f80ca-237">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="f80ca-239">Define o rótulo para a <strong>categoria Cores do</strong> tema.</span><span class="sxs-lookup"><span data-stu-id="f80ca-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="f80ca-240">Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="f80ca-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="f80ca-241">Esse é o único modelo que contém categorias rotuladas.</span><span class="sxs-lookup"><span data-stu-id="f80ca-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="f80ca-242">Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f80ca-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f80ca-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="f80ca-244">Define a cadeia de caracteres para uma descrição de dica de ferramenta associada a um <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span><span class="sxs-lookup"><span data-stu-id="f80ca-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="f80ca-245">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f80ca-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="f80ca-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="f80ca-247">Define a cadeia de caracteres para uma dica de ferramenta Command.</span><span class="sxs-lookup"><span data-stu-id="f80ca-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="f80ca-248">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="f80ca-249">Manipuladores de comandos</span><span class="sxs-lookup"><span data-stu-id="f80ca-249">Command handlers</span></span>

<span data-ttu-id="f80ca-250">O [**método IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) é usado para personalizar um Drop-Down Seletor de Cor por meio das chaves de propriedade listadas acima.</span><span class="sxs-lookup"><span data-stu-id="f80ca-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="f80ca-251">O exemplo a seguir demonstra como definir as travas de cores de um Drop-Down Seletor de Cor, com base em uma preferência de estilo personalizado ou em uma grade de amostra personalizada declarada na marcação.</span><span class="sxs-lookup"><span data-stu-id="f80ca-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


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



<span data-ttu-id="f80ca-252">O exemplo a seguir demonstra uma implementação do método [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) que expõe as cores Drop-Down Seletor de Cor swatch ao aplicativo ribbon.</span><span class="sxs-lookup"><span data-stu-id="f80ca-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f80ca-253">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f80ca-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f80ca-254">Biblioteca de controle da Estrutura de Faixa de Opções do Windows</span><span class="sxs-lookup"><span data-stu-id="f80ca-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="f80ca-255">**Elemento de marcação DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="f80ca-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="f80ca-256">Seletor de Cor propriedades</span><span class="sxs-lookup"><span data-stu-id="f80ca-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="f80ca-257">Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="f80ca-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="f80ca-258">Exemplo de DropDownColorPicker</span><span class="sxs-lookup"><span data-stu-id="f80ca-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

