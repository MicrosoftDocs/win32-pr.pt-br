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
# <a name="customizing-ribbon-colors"></a>Personalizando cores da faixa de das

A estrutura da faixa de faixas do Windows expõe um conjunto de propriedades de cor que permite que um aplicativo Personalize a aparência de vários elementos da interface do usuário da faixa de para-tempo de execução.

-   [Introdução](#introduction)
-   [Especificar cores da faixa de medida](#specify-ribbon-colors)
-   [Converter RGB em HSB](#convert-rgb-to-hsb)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

As [chaves de propriedade da estrutura](windowsribbon-reference-properties-framework.md) listadas na tabela a seguir são usadas para definir a cor de vários elementos da interface do usuário em um aplicativo da faixa de opções. Essas propriedades permitem que a estrutura da faixa de Ribbon dê suporte a personalização, requisitos de identidade e especificações de identidade visual entre aplicativos.

| Cor da faixa de da                     | Chave de propriedade da estrutura                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cor da tela de fundo                 | [\_GlobalBackgroundColor PKEY \_ UI](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Cor de realce (somente Windows 7) | [Interface do usuário \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)* * * * introduzido no Windows 8 * *: * * [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) não pode ser definido independentemente da [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).<br/> <br/>                                                              |
| Cor do texto                       | [Interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)* * * * introduzido no Windows 8 **:** as alterações no valor padrão da [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) no Windows 8 podem exigir um ajuste para a [interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) em aplicativos da faixa de faixas projetados para o Windows 7.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Especificar cores da faixa de medida

A estrutura da faixa de faixas usa um modelo de cores de matiz, saturação, brilho (HSB), que difere dos espaços de cores de matiz, saturação, luminosidade (HSL) ou matiz, saturação, valor (HSV) mais comuns. Em particular, B representa um nível de brilho ou luminosidade geral em vez da claridade de uma cor específica.

Para especificar a cor dos elementos da interface do usuário na estrutura da faixa de faixas, um aplicativo atribui valores HSB a cada uma das propriedades de cores globais. Esses valores são aplicados universalmente em todos os elementos da faixa de faixas, conforme exigido pelo aplicativo da faixa de faixas (a estrutura não dá suporte à atribuição de valores HSB a elementos individuais e controles).

Introduzido no Windows 8 * *: * *[UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) recebe o mesmo valor que a [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

A tabela a seguir descreve os parâmetros HSB da estrutura da faixa de opções.



Componente

Descrição

Valores ajustados\*

Matiz (H)

A cor Pigment, ou real, normalmente é identificada como um valor de um intervalo de circlular de 0 a 359 graus.

0 (vermelho) a 255 (vermelho)

Saturação (ões)

A pureza, ou saturação, da cor medida como uma porcentagem de 0 a 100%.

0 (cinza) a 255 (totalmente saturado)

Brilho (B)

O brilho geral ou a escuridão da cor medida como uma porcentagem de 0 a 100%.

0 (escuro) a 255 (claro)

\* O intervalo original para cada valor de parâmetro é convertido em um intervalo de 0 a 255 para a estrutura.



 

Os valores HSB não identificam cores específicas. Em vez disso, a combinação de valores de propriedade HSB influencia a forma como gradientes de cores em toda a interface do usuário são ajustados em relação uns aos outros.

Ao atribuir valores HSB personalizados à [interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) e à [interface do usuário do \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), é recomendável que esses valores sejam de contraste alto o suficiente para garantir a legibilidade. Especificamente, a cor do texto deve ser mais escura do que a tonalidade mais clara da interface do usuário da faixa de uma. Quando necessário, a estrutura ajusta automaticamente o valor HSB da interface do usuário \_ PKEY \_ GlobalTextColor para fornecer contraste suficiente em relação a qualquer sombra de plano de fundo ou gradiente derivado da interface do usuário \_ PKEY \_ GlobalBackgroundColor.

> [!Note]  
> No Windows 7, a [interface do usuário \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) pode ser definida independentemente da [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

 

O exemplo a seguir demonstra como especificar uma cor personalizada para a [interface do usuário \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)e propriedades [da interface do usuário \_ PKEY \_ ](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) GlobalHighlightColor.


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



## <a name="convert-rgb-to-hsb"></a>Converter RGB em HSB

Esta seção descreve a fórmula que é necessária para corresponder dinamicamente a um valor HSB da estrutura da faixa de forma, a [interface do usuário \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) neste exemplo, para uma cor RGB específica em tempo de execução.

O plano de fundo da linha de guia é usado como um ponto de referência porque é renderizado como uma superfície de cor simples em comparação com o gradiente de brilho da tela de fundo da faixa de medida.

Uma conversão preliminar é necessária para obter um valor HSL intermediário. Esse valor HSL pode então ser convertido em um valor HSB.

> [!Note]  
> A conversão de RGB em HSL é facilmente realizada com a maioria dos softwares de edição de fotos.

 

A conversão de HSL (com cada componente no intervalo de 0,0 a 1,0) para uma configuração HSB de faixa de opções é realizada por meio das seguintes fórmulas:

-   <sub>Plano de fundo</sub> H = Round (255.0 H)
-   <sub>Segundo plano</sub> = redondo (255.0 S)
-   B<sub>plano de fundo</sub> = redondo (257.7 + 149,9 LN (L)) se 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes de cores](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Propriedades da estrutura](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





