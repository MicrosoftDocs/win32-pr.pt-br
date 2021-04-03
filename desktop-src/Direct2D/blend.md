---
title: Efeito de mesclagem
description: Use o efeito de mistura para combinar 2 imagens. Esse efeito tem 26 modos de mesclagem.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- efeito de mistura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824743"
---
# <a name="blend-effect"></a>Efeito de mesclagem

Use o efeito de mistura para combinar 2 imagens. Esse efeito tem 26 modos de mesclagem.

O CLSID para esse efeito é CLSID \_ D2D1Blend.

-   [Exemplos de mesclagem](#blending-examples)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de mesclagem](#blend-modes)
-   [Conversões de espaço de cores HSL](#hsl-color-space-conversions)
    -   [Convertendo de RGB em HSL](#converting-from-rgb-to-hsl)
    -   [Convertendo de HSL para RGB](#converting-from-hsl-to-rgb)
-   [Bitmap de saída](#output-bitmap)
-   [Código de exemplo](#sample-code)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="blending-examples"></a>Exemplos de mesclagem

Aqui está uma imagem de exemplo de cada modo de mesclagem do efeito de mistura. Uma lista completa dos modos de mesclagem e as propriedades do modo correspondente estão na próxima seção

![captura de tela de exemplo de efeito de todos os modos de mistura disponíveis.](images/blend-modes.png)

Aqui está outro exemplo que usa o modo de exclusão.



| Antes da imagem 1                                                             |
|----------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg)    |
| Antes da imagem 2                                                             |
| ![a segunda imagem antes do efeito.](images/4-arthimetic-composite2.jpg) |
| After (após)                                                                      |
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



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                 | Descrição                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> \_Modo de \_ prop d2d1 Blend \_<br/> | O modo de mesclagem usado para o efeito. Consulte [modos de mesclagem](#blend-modes) para obter mais informações. O tipo é o \_ modo de mesclagem d2d1 \_ .<br/> O valor padrão é \_ multiplicar modo de mesclagem d2d1 \_ \_ .<br/> |



 

## <a name="blend-modes"></a>Modos do Blend

A tabela aqui mostra todos os modos de mesclagem desse efeito. As funções auxiliares necessárias para computar a saída do efeito estão na próxima seção.

Cor: O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>A</sub>) + B <sub>RGB</sub> \* B <sub>a</sub> \* (1-f <sub>a</sub>)

Alfa: O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>A</sub>) + B<sub>A</sub>

Em que:

-   O<sub>PRGB</sub> é a cor de saída previamente multiplicada
-   O<sub>A</sub> é Alfa de saída
-   B<sub>RGB</sub> é a cor de destino não multiplicada previamente
-   B<sub>A é o</sub> destino alfa
-   F<sub>RGB</sub> é a cor de origem não multiplicada previamente
-   F<sub>A</sub> é fonte alfa
-   *f*(S <sub>RGB</sub>, D <sub>RGB</sub>) é uma função de mistura que varia de acordo com o modo de mesclagem

Alguns dos modos de mesclagem exigem a conversão de e para o espaço de cores de matiz, saturação, luminosidade (HSL) para RGB.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enumeração</th>
<th>Subscrito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKEN</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_MULTIPLY</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_COLOR_BURN</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LINEAR_BURN</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKER_COLOR</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTEN</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SCREEN</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR_DODGE</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_DODGE</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTER_COLOR</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_OVERLAY</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_SOFT_LIGHT</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_LIGHT</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_VIVID_LIGHT</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_LIGHT</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_PIN_LIGHT</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_MIX</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIFFERENCE</td>
<td>Fórmulas de mesclagem básicas com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> - B<sub>RGB</sub>)</td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_EXCLUSION</td>
<td>Fórmulas de mesclagem básica com <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + b<sub>RGB</sub>   2 * f<sub>RGB</sub> * B<sub>RGB</sub></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_HUE</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SATURATION</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LUMINOSITY</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DISSOLVE</td>
<td>Considerando:
<ul>
<li>Uma coordenada de cena XY para o pixel atual</li>
<li>Um gerador de números pseudo aleatórios (XY) determinístico com base na coordenada de semente XY, com distribuição não polarizada de valores de [0, 1]</li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SUBTRACT</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIVISION</td>
<td>Fórmula de mesclagem básica somente para alfa. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Para todos os modos de mesclagem, o valor de saída é premultiplicado e clamped para o intervalo de \[ 0, 1 \] .

 

## <a name="hsl-color-space-conversions"></a>Conversões de espaço de cores HSL

O componente de luminosidade é calculado usando os pesos RGB aqui:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Convertendo de RGB em HSL

![fórmula matemática que descreve a transformação de cor RGB para cor HSL.](images/blend-rgb-to-hsl-1.png)

Isso coloca *S* e *L* no intervalo de \[ 0,0, 1,0 \] e *H* no intervalo \[ -1,0, 5,0 \] .

### <a name="converting-from-hsl-to-rgb"></a>Convertendo de HSL para RGB

Para converter a outra maneira, usamos o inverso dos cálculos anteriores.

Se *S* = 0, *R*  =  *G*  =  *B*  =  *L*

Caso contrário, há seis casos dependentes de matiz:

Se *H* for maior que 0, os valores estarão no setor vermelho/magenta em que *R*  >  *B*  >  *G*.

![matemática equaiton etapa um dos seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1rm.png)

Se *H* for maior ou igual a 0 e menor que 1, os valores estarão no setor vermelho/amarelo em que *R*  >  *G*  >  *B*.

![matemática equaiton etapa dois de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1ry.png)

Se *H* for maior ou igual a 1 e menor que 2, os valores estarão no setor amarelo/verde em que *G*  >  *R*  >  *B*.

![matemática equaiton etapa três de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1yg.png)

Se *H* for maior ou igual a 2 e menor que 3, os valores estarão no setor verde/ciano em que *G*  >  *B*  >  *R*.

![matemática equaiton etapa quatro de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1gc.png)

Se *H* for maior ou igual a 3 e menor que 4, os valores estarão no setor ciano/azul em que *B*  >  *G*  >  *R*.

![matemática equaiton etapa cinco de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1cb.png)

Se *H* for maior ou igual a 4, os valores estarão no setor azul/magenta em que *B*  >  *R*  >  *G*.

![matemática equaiton etapa seis de seis convertendo cor HSL em RGB.](images/blend-hsl-to-rgb-1bm.png)

Como os modos de mesclagem fazem combinações arbitrárias de componentes HSL de duas cores diferentes, é comum que o valor RGB convertido esteja fora de gama, ou seja, um ou mais componentes de canal possam estar fora do intervalo legal de \[ 0,0, 1,0 \] . Essas cores são revertidas de acordo com a redução mínima da saturação, preservando, ao mesmo tempo, a matiz e a luminosidade:

![fórmula matemática que descreve as correções necessárias para as instâncias fora de gamut.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Bitmap de saída

O bitmap de saída para esse efeito é sempre o tamanho da União das duas imagens de entrada.

## <a name="sample-code"></a>Código de exemplo

Para obter um exemplo desse efeito, baixe o [exemplo de modos de efeito composto Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

