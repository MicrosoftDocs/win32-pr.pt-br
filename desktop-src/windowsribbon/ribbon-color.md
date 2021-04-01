---
title: Personalizando cores da faixa de das
description: A estrutura da faixa de faixas do Windows expõe um conjunto de propriedades de cor que permite que um aplicativo Personalize a aparência de vários elementos da interface do usuário da faixa de para-tempo de execução.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Faixa de-se do Windows, personalizando cores
- Faixa de faixas, personalizando cores
- Personalizando as cores da faixa de das janelas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103640226"
---
# <a name="customizing-ribbon-colors"></a><span data-ttu-id="d259f-106">Personalizando cores da faixa de das</span><span class="sxs-lookup"><span data-stu-id="d259f-106">Customizing Ribbon Colors</span></span>

<span data-ttu-id="d259f-107">A estrutura da faixa de faixas do Windows expõe um conjunto de propriedades de cor que permite que um aplicativo Personalize a aparência de vários elementos da interface do usuário da faixa de para-tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d259f-107">The Windows Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon UI elements at run time.</span></span>

-   [<span data-ttu-id="d259f-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="d259f-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d259f-109">Especificar cores da faixa de medida</span><span class="sxs-lookup"><span data-stu-id="d259f-109">Specify Ribbon Colors</span></span>](#specify-ribbon-colors)
-   [<span data-ttu-id="d259f-110">Converter RGB em HSB</span><span class="sxs-lookup"><span data-stu-id="d259f-110">Convert RGB to HSB</span></span>](#convert-rgb-to-hsb)
-   [<span data-ttu-id="d259f-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d259f-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d259f-112">Introdução</span><span class="sxs-lookup"><span data-stu-id="d259f-112">Introduction</span></span>

<span data-ttu-id="d259f-113">As [chaves de propriedade da estrutura](windowsribbon-reference-properties-framework.md) listadas na tabela a seguir são usadas para definir a cor de vários elementos da interface do usuário em um aplicativo da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="d259f-113">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to set the color of various UI elements in a Ribbon application.</span></span> <span data-ttu-id="d259f-114">Essas propriedades permitem que a estrutura da faixa de Ribbon dê suporte a personalização, requisitos de identidade e especificações de identidade visual entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d259f-114">These properties allow the Ribbon framework to support personalization, identity requirements, and branding specifications across applications.</span></span>

| <span data-ttu-id="d259f-115">Cor da faixa de da</span><span class="sxs-lookup"><span data-stu-id="d259f-115">Ribbon Color</span></span>                     | <span data-ttu-id="d259f-116">Chave de propriedade da estrutura</span><span class="sxs-lookup"><span data-stu-id="d259f-116">Framework Property Key</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d259f-117">Cor da tela de fundo</span><span class="sxs-lookup"><span data-stu-id="d259f-117">Background color</span></span>                 | [<span data-ttu-id="d259f-118">\_GlobalBackgroundColor PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="d259f-118">UI\_PKEY\_GlobalBackgroundColor</span></span>](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d259f-119">Cor de realce (somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="d259f-119">Highlight color (Windows 7 only)</span></span> | <span data-ttu-id="d259f-120">[Interface do usuário \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\* \* \* \* introduzido no Windows 8 \* \*: \* \* [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) não pode ser definido independentemente da [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d259f-120">[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\*\*\*\*Introduced in Windows 8\*\*:  \*\* [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span><br/> <br/>                                                              |
| <span data-ttu-id="d259f-121">Cor do texto</span><span class="sxs-lookup"><span data-stu-id="d259f-121">Text color</span></span>                       | <span data-ttu-id="d259f-122">[Interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\* \* \* \* introduzido no Windows 8 **:** as alterações no valor padrão da [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) no Windows 8 podem exigir um ajuste para a [interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) em aplicativos da faixa de faixas projetados para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d259f-122">[UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\*\*\*\*Introduced in Windows 8 **:** Changes to the default value of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 might require an adjustment to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Ribbon apps designed for Windows 7.</span></span><br/> <br/> |



 

## <a name="specify-ribbon-colors"></a><span data-ttu-id="d259f-123">Especificar cores da faixa de medida</span><span class="sxs-lookup"><span data-stu-id="d259f-123">Specify Ribbon Colors</span></span>

<span data-ttu-id="d259f-124">A estrutura da faixa de faixas usa um modelo de cores de matiz, saturação, brilho (HSB), que difere dos espaços de cores de matiz, saturação, luminosidade (HSL) ou matiz, saturação, valor (HSV) mais comuns.</span><span class="sxs-lookup"><span data-stu-id="d259f-124">The Ribbon framework uses a Hue, Saturation, Brightness (HSB) color model, which differs from the more common hue, saturation, luminosity (HSL) or hue, saturation, value (HSV) color spaces.</span></span> <span data-ttu-id="d259f-125">Em particular, B representa um nível de brilho ou luminosidade geral em vez da claridade de uma cor específica.</span><span class="sxs-lookup"><span data-stu-id="d259f-125">In particular, B represents an overall brightness or luminosity level rather than the lightness of a particular color.</span></span>

<span data-ttu-id="d259f-126">Para especificar a cor dos elementos da interface do usuário na estrutura da faixa de faixas, um aplicativo atribui valores HSB a cada uma das propriedades de cores globais.</span><span class="sxs-lookup"><span data-stu-id="d259f-126">To specify the color of UI elements in the Ribbon framework, an application assigns HSB values to each of the global color properties.</span></span> <span data-ttu-id="d259f-127">Esses valores são aplicados universalmente em todos os elementos da faixa de faixas, conforme exigido pelo aplicativo da faixa de faixas (a estrutura não dá suporte à atribuição de valores HSB a elementos individuais e controles).</span><span class="sxs-lookup"><span data-stu-id="d259f-127">These values are then applied universally across all Ribbon elements as required by the Ribbon application (the framework does not support assigning HSB values to individual elements and controls).</span></span>

<span data-ttu-id="d259f-128">Introduzido no Windows 8 \* \*: \* \*[UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) recebe o mesmo valor que a [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d259f-128">\*\*\*\*Introduced in Windows 8\*\*:  \*\*[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

<span data-ttu-id="d259f-129">A tabela a seguir descreve os parâmetros HSB da estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="d259f-129">The following table describes the Ribbon framework HSB parameters.</span></span>



<span data-ttu-id="d259f-130">Componente</span><span class="sxs-lookup"><span data-stu-id="d259f-130">Component</span></span>

<span data-ttu-id="d259f-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="d259f-131">Description</span></span>

<span data-ttu-id="d259f-132">Valores ajustados\*</span><span class="sxs-lookup"><span data-stu-id="d259f-132">Adjusted Values\*</span></span>

<span data-ttu-id="d259f-133">Matiz (H)</span><span class="sxs-lookup"><span data-stu-id="d259f-133">Hue (H)</span></span>

<span data-ttu-id="d259f-134">A cor Pigment, ou real, normalmente é identificada como um valor de um intervalo de circlular de 0 a 359 graus.</span><span class="sxs-lookup"><span data-stu-id="d259f-134">The pigment, or actual, color is typically identified as a value from a circlular range of 0 to 359 degrees.</span></span>

<span data-ttu-id="d259f-135">0 (vermelho) a 255 (vermelho)</span><span class="sxs-lookup"><span data-stu-id="d259f-135">0 (red) to 255 (red)</span></span>

<span data-ttu-id="d259f-136">Saturação (ões)</span><span class="sxs-lookup"><span data-stu-id="d259f-136">Saturation (S)</span></span>

<span data-ttu-id="d259f-137">A pureza, ou saturação, da cor medida como uma porcentagem de 0 a 100%.</span><span class="sxs-lookup"><span data-stu-id="d259f-137">The purity, or saturation, of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="d259f-138">0 (cinza) a 255 (totalmente saturado)</span><span class="sxs-lookup"><span data-stu-id="d259f-138">0 (grey) to 255 (fully saturated)</span></span>

<span data-ttu-id="d259f-139">Brilho (B)</span><span class="sxs-lookup"><span data-stu-id="d259f-139">Brightness (B)</span></span>

<span data-ttu-id="d259f-140">O brilho geral ou a escuridão da cor medida como uma porcentagem de 0 a 100%.</span><span class="sxs-lookup"><span data-stu-id="d259f-140">The overall brightness or darkness of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="d259f-141">0 (escuro) a 255 (claro)</span><span class="sxs-lookup"><span data-stu-id="d259f-141">0 (dark) to 255 (light)</span></span>

<span data-ttu-id="d259f-142">\* O intervalo original para cada valor de parâmetro é convertido em um intervalo de 0 a 255 para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="d259f-142">\* The original range for each parameter value is translated into a range of 0 to 255 for the framework.</span></span>



 

<span data-ttu-id="d259f-143">Os valores HSB não identificam cores específicas.</span><span class="sxs-lookup"><span data-stu-id="d259f-143">HSB values do not identify specific colors.</span></span> <span data-ttu-id="d259f-144">Em vez disso, a combinação de valores de propriedade HSB influencia a forma como gradientes de cores em toda a interface do usuário são ajustados em relação uns aos outros.</span><span class="sxs-lookup"><span data-stu-id="d259f-144">Instead, the combination of HSB property values influences how color gradients throughout the UI are adjusted relative to each other.</span></span>

<span data-ttu-id="d259f-145">Ao atribuir valores HSB personalizados à [interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) e à [interface do usuário do \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), é recomendável que esses valores sejam de contraste alto o suficiente para garantir a legibilidade.</span><span class="sxs-lookup"><span data-stu-id="d259f-145">When assigning custom HSB values to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) and [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), it is recommended that these values be of high enough contrast to ensure readability.</span></span> <span data-ttu-id="d259f-146">Especificamente, a cor do texto deve ser mais escura do que a tonalidade mais clara da interface do usuário da faixa de uma.</span><span class="sxs-lookup"><span data-stu-id="d259f-146">Specifically, the text color should be darker than the lightest shade of the ribbon UI.</span></span> <span data-ttu-id="d259f-147">Quando necessário, a estrutura ajusta automaticamente o valor HSB da interface do usuário \_ PKEY \_ GlobalTextColor para fornecer contraste suficiente em relação a qualquer sombra de plano de fundo ou gradiente derivado da interface do usuário \_ PKEY \_ GlobalBackgroundColor.</span><span class="sxs-lookup"><span data-stu-id="d259f-147">Where necessary, the framework automatically adjusts the UI\_PKEY\_GlobalTextColor HSB value to provide sufficient contrast against any background shade or gradient derived from UI\_PKEY\_GlobalBackgroundColor.</span></span>

> [!Note]  
> <span data-ttu-id="d259f-148">No Windows 7, a [interface do usuário \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) pode ser definida independentemente da [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d259f-148">In Windows 7, [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) can be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

 

<span data-ttu-id="d259f-149">O exemplo a seguir demonstra como especificar uma cor personalizada para a [interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)e propriedades [da interface do usuário \_ PKEY \_ ](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) GlobalHighlightColor.</span><span class="sxs-lookup"><span data-stu-id="d259f-149">The following example demonstrates how to specify a custom color for the [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), and [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) properties.</span></span>


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a><span data-ttu-id="d259f-150">Converter RGB em HSB</span><span class="sxs-lookup"><span data-stu-id="d259f-150">Convert RGB to HSB</span></span>

<span data-ttu-id="d259f-151">Esta seção descreve a fórmula que é necessária para corresponder dinamicamente a um valor HSB da estrutura da faixa de forma, a [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) neste exemplo, para uma cor RGB específica em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d259f-151">This section describes the formula that is required for dynamically matching a Ribbon framework HSB value, the [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in this example, to a specific RGB color at run time.</span></span>

<span data-ttu-id="d259f-152">O plano de fundo da linha de guia é usado como um ponto de referência porque é renderizado como uma superfície de cor simples em comparação com o gradiente de brilho da tela de fundo da faixa de medida.</span><span class="sxs-lookup"><span data-stu-id="d259f-152">The tab row background is used as a reference point because it is rendered as a flat color surface compared to the brightness gradient of the ribbon background.</span></span>

<span data-ttu-id="d259f-153">Uma conversão preliminar é necessária para obter um valor HSL intermediário.</span><span class="sxs-lookup"><span data-stu-id="d259f-153">A preliminary conversion is necessary to obtain an intermediate HSL value.</span></span> <span data-ttu-id="d259f-154">Esse valor HSL pode então ser convertido em um valor HSB.</span><span class="sxs-lookup"><span data-stu-id="d259f-154">This HSL value can then be converted to an HSB value.</span></span>

> [!Note]  
> <span data-ttu-id="d259f-155">A conversão de RGB em HSL é facilmente realizada com a maioria dos softwares de edição de fotos.</span><span class="sxs-lookup"><span data-stu-id="d259f-155">The conversion from RGB to HSL is easily accomplished with most photo editing software.</span></span>

 

<span data-ttu-id="d259f-156">A conversão de HSL (com cada componente no intervalo de 0,0 a 1,0) para uma configuração HSB de faixa de opções é realizada por meio das seguintes fórmulas:</span><span class="sxs-lookup"><span data-stu-id="d259f-156">Conversion of HSL (with each component in the range of 0.0 to 1.0) to a Ribbon HSB setting is accomplished through the following formulas:</span></span>

-   <span data-ttu-id="d259f-157"><sub>Plano de fundo</sub> H = Round (255.0 H)</span><span class="sxs-lookup"><span data-stu-id="d259f-157">H<sub>background</sub> = Round(255.0 H)</span></span>
-   <span data-ttu-id="d259f-158"><sub>Segundo plano</sub> = redondo (255.0 S)</span><span class="sxs-lookup"><span data-stu-id="d259f-158">S<sub>background</sub> = Round(255.0 S)</span></span>
-   <span data-ttu-id="d259f-159">B<sub>plano de fundo</sub> = redondo (257.7 + 149,9 LN (L)) se 0,1793 <= L <= 0,9821</span><span class="sxs-lookup"><span data-stu-id="d259f-159">B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821</span></span>

## <a name="related-topics"></a><span data-ttu-id="d259f-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d259f-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d259f-161">Diretrizes de cores</span><span class="sxs-lookup"><span data-stu-id="d259f-161">Color Guidelines</span></span>](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[<span data-ttu-id="d259f-162">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d259f-162">Framework Properties</span></span>](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





