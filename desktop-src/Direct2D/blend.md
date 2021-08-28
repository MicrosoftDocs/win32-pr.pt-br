---
title: Efeito de mesclagem
description: Use o efeito blend para combinar duas imagens. Esse efeito tem 26 modos de combinação.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- efeito blend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853043123c6eea9a87656a7450b1295236ed5d6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478192"
---
# <a name="blend-effect"></a>Efeito de mesclagem

Use o efeito blend para combinar duas imagens. Esse efeito tem 26 modos de combinação.

O CLSID para esse efeito é CLSID \_ D2D1Blend.

-   [Combinando exemplos](#blending-examples)
-   [Propriedades de efeito](#effect-properties)
-   [Modos do Blend](#blend-modes)
-   [Conversões de espaço de cor HSL](#hsl-color-space-conversions)
    -   [Convertendo de RGB para HSL](#converting-from-rgb-to-hsl)
    -   [Convertendo de HSL para RGB](#converting-from-hsl-to-rgb)
-   [Bitmap de saída](#output-bitmap)
-   [Código de exemplo](#sample-code)
-   [Requisitos](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="blending-examples"></a>Combinando exemplos

Aqui está uma imagem de exemplo de cada modo de combinação do efeito blend. Uma lista completa dos modos de combinação e as propriedades de modo correspondentes está na próxima seção

![captura de tela de exemplo de efeito de todos os modos de combinação disponíveis.](images/blend-modes.png)

Aqui está outro exemplo usando o modo de exclusão.



| Antes da imagem 1                                                             |
|----------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg)    |
| Antes da imagem 2                                                             |
| ![a segunda imagem antes do efeito.](images/4-arthimetic-composite2.jpg) |
| Depois                                                                      |
| ![a imagem após a transformação.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                 | Descrição                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> D2D1 \_ BLEND \_ PROP \_ MODE<br/> | O modo de combinação usado para o efeito. Confira [Modos do Blend para](#blend-modes) obter mais informações. O tipo é D2D1 \_ BLEND \_ MODE.<br/> O valor padrão é D2D1 \_ BLEND \_ MODE \_ MULTIPLY.<br/> |



 

## <a name="blend-modes"></a>Modos do Blend

A tabela aqui mostra todos os modos de mesclagem desse efeito. As funções auxiliares necessárias para calcular a saída do efeito estão na próxima seção.

Cor: O <sub>PRGB</sub>  =  *f*(F <sub>RGB,</sub>B <sub>RGB</sub>) \* F <sub>A</sub> \* B <sub>A</sub> + F <sub>RGB</sub> \* F <sub>A</sub> \* (1 - B <sub>A</sub>) + B <sub>RGB</sub> \* B <sub>A</sub> \* (1 - F <sub>A</sub>)

Alfa: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub>

Em que:

-   O<sub>PRGB</sub> é a cor de saída pré-multiplicada
-   O<sub>A</sub> é Alfa de Saída
-   B<sub>RGB</sub> é a cor de destino não multiplicada previamente
-   B<sub>A é</sub> alfa de destino
-   F<sub>RGB</sub> é a cor de origem não multiplicada previamente
-   F<sub>A é</sub> alfa de origem
-   *f*(S <sub>RGB</sub>, D <sub>RGB</sub>) é uma função blend que varia por modo de combinação

Alguns dos modos de combinação exigem a conversão de e para o espaço de cores matiz, saturação, luminosidade (HSL) para RGB.




| Enumeração | Equação | 
|-------------|----------|
| D2D1_BLEND_MODE_DARKEN | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /> | 
| D2D1_BLEND_MODE_MULTIPLY | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /> | 
| D2D1_BLEND_MODE_COLOR_BURN | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /> | 
| D2D1_BLEND_MODE_LINEAR_BURN | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /> | 
| D2D1_BLEND_MODE_DARKER_COLOR | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /> | 
| D2D1_BLEND_MODE_LIGHTEN | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /> | 
| D2D1_BLEND_MODE_SCREEN | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /> | 
| D2D1_BLEND_MODE_COLOR_DODGE | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /> | 
| D2D1_BLEND_MODE_LINEAR_DODGE | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /> | 
| D2D1_BLEND_MODE_LIGHTER_COLOR | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /> | 
| D2D1_BLEND_MODE_OVERLAY | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /> | 
| D2D1_BLEND_MODE_SOFT_LIGHT | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /> | 
| D2D1_BLEND_MODE_HARD_LIGHT | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /> | 
| D2D1_BLEND_MODE_VIVID_LIGHT | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /> | 
| D2D1_BLEND_MODE_LINEAR_LIGHT | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /> | 
| D2D1_BLEND_MODE_PIN_LIGHT | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /> | 
| D2D1_BLEND_MODE_HARD_MIX | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /> | 
| D2D1_BLEND_MODE_DIFFERENCE | Fórmulas de combinação básicas <em>com f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = abs(F<sub>RGB</sub> – B<sub>RGB</sub>) | 
| D2D1_BLEND_MODE_EXCLUSION | Fórmulas de mesclagem básicas com <em>f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 * F<sub>RGB</sub> * B<sub>RGB</sub> | 
| D2D1_BLEND_MODE_HUE | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /> | 
| D2D1_BLEND_MODE_SATURATION | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /> | 
| D2D1_BLEND_MODE_COLOR | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /> | 
| D2D1_BLEND_MODE_LUMINOSITY | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /> | 
| D2D1_BLEND_MODE_DISSOLVE | Considerando:<ul><li>Uma coordenada de cena XY para o pixel atual</li><li>Um gerador de número pseudoleato determinístico rand(XY) com base na coordenada de semente XY, com distribuição sem imparcialidade de valores de [0, 1]</li></ul><br /><img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br /> | 
| D2D1_BLEND_MODE_SUBTRACT | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /> | 
| D2D1_BLEND_MODE_DIVISION | Fórmula de combinação básica apenas para alfa. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /> | 




 

> [!Note]  
> Para todos os modos blend, o valor de saída é pré-ultado e fixado ao intervalo \[ 0, 1 \] .

 

## <a name="hsl-color-space-conversions"></a>Conversões de espaço de cor HSL

O componente de luminosidade é calculado usando os pesos RGB aqui:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Convertendo de RGB para HSL

![fórmula matemática que descreve a transformação da cor rgb para a cor hsl.](images/blend-rgb-to-hsl-1.png)

Isso coloca *S* e *L* no intervalo \[ 0,0, 1,0 e H no \] intervalo  \[ -1.0, 5.0 \] .

### <a name="converting-from-hsl-to-rgb"></a>Convertendo de HSL para RGB

Para converter a outra maneira, usamos o inverso dos cálculos anteriores.

Se *S* = 0, *então R*  =  *G*  =  *B*  =  *L*

Caso contrário, há seis casos dependentes de matiz:

Se *H* for maior que 0, os valores estão no setor vermelho/magenta em *que R*  >  *B*  >  *G*.

![etapa matemática igualiton uma das seis convertendo a cor hsl em rgb.](images/blend-hsl-to-rgb-1rm.png)

Se *H* for maior ou igual a 0 e menor que 1, os valores serão no setor vermelho/amarelo em que *R*  >  *G*  >  *B*.

![etapa matemática igualiton dois de seis convertendo a cor hsl em rgb.](images/blend-hsl-to-rgb-1ry.png)

Se *H* for maior ou igual a 1 e menor que 2, os valores serão no setor amarelo/verde em que *G*  >  *R*  >  *B*.

![etapa matemática igualiton três de seis convertendo a cor hsl em rgb.](images/blend-hsl-to-rgb-1yg.png)

Se *H* for maior ou igual a 2 e menor que 3, os valores serão no setor verde/ciano em que *G*  >  *B*  >  *R*.

![etapa matemática igualiton quatro de seis convertendo a cor hsl em rgb.](images/blend-hsl-to-rgb-1gc.png)

Se *H* for maior ou igual a 3 e menor que 4, os valores serão no setor ciano/azul em que *B*  >  *G*  >  *R*.

![etapa matemática igualiton cinco de seis convertendo a cor hsl em rgb.](images/blend-hsl-to-rgb-1cb.png)

Se *H* for maior ou igual a 4, os valores estão no setor azul/magenta em *que B*  >  *R*  >  *G*.

![etapa de equaiton matemática seis de seis convertendo a cor hsl em rgb.](images/blend-hsl-to-rgb-1bm.png)

Como os modos de combinação fazem combinações arbitrárias de componentes HSL de duas cores diferentes, é comum que o valor RGB convertido seja fora de jogo, ou seja, um ou mais componentes de canal podem estar fora do intervalo legal de \[ 0,0, 1,0 \] . Essas cores são voltadas para a gama reduzindo minimamente a saturação, preservando a matiz e a luminosidade:

![fórmula matemática que descreve as correções necessárias para fora de instâncias de jogos.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Bitmap de saída

O bitmap de saída para esse efeito é sempre o tamanho da união das duas imagens de entrada.

## <a name="sample-code"></a>Código de exemplo

Para ver um exemplo desse efeito, baixe o [exemplo Direct2D de efeito composto.](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para aplicativos Windows 7 área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para aplicativos Windows 7 área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

