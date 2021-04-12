---
title: Efeito de gerenciamento de cores
description: Use o efeito de gerenciamento de cores para transformar uma imagem de um perfil de cor ICC (International Color Consortium) para outro. O efeito transforma a imagem de acordo com a especificação ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- efeito de gerenciamento de cores
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369536"
---
# <a name="color-management-effect"></a>Efeito de gerenciamento de cores

Use o efeito de gerenciamento de cores para transformar uma imagem de um perfil de cor ICC (International Color Consortium) para outro. O efeito transforma a imagem de acordo com a [especificação ICC](https://www.color.org).

O CLSID para esse efeito é CLSID \_ D2D1ColorManagement.

- [Propriedades do efeito](#effect-properties)
- [Modos de intenção de renderização](#rendering-intent-modes)
- [Modos alfa da imagem de entrada](#input-image-alpha-modes)
- [Conformidade com a especificação ICC](#compliance-with-icc-specification)
- [Comportamento do canal alfa](#alpha-channel-behavior)
- [Modos de qualidade](#quality-modes)
- [Código de exemplo](#sample-code)
- [Requirements](#requirements)
- [Tópicos relacionados](#related-topics)

## <a name="effect-properties"></a>Propriedades do efeito

| Nome de exibição e enumeração de índice | Descrição |
|-|-|
| SourceContext<br/> \_Contexto de \_ \_ cor de origem d2d1 COLORMANAGEMENT prop \_ \_<br/> | As informações de espaço de cores de origem. O tipo é [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> O valor padrão é NULL.<br/> |
| SourceIntent<br/> \_Tentativa de \_ \_ RENDERIZAÇÃO de origem d2d1 COLORMANAGEMENT prop \_ \_<br/> | Qual tentativa de renderização ICC usar. O tipo é a \_ tentativa de RENDERIZAÇÃO d2d1 COLORMANAGEMENT \_ \_ .<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT de \_ tentativa de renderização \_ \_ perceptiva.<br/> |
| DestinationContext<br/> \_Contexto de \_ \_ cor de destino d2d1 COLORMANAGEMENT prop \_ \_<br/> | As informações de espaço de cores de destino. O tipo é [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> O valor padrão é NULL.<br/> |
| DestinationIntent<br/> \_Tentativa de \_ \_ RENDERIZAÇÃO de destino d2d1 COLORMANAGEMENT prop \_ \_<br/> | Qual tentativa de renderização ICC usar. O tipo é a \_ tentativa de RENDERIZAÇÃO d2d1 COLORMANAGEMENT \_ \_ .<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT de \_ tentativa de renderização \_ \_ perceptiva.<br/> |
| Alphamode<br/> Modo alfa do D2D1 \_ COLORMANAGEMENT \_ prop \_ \_<br/> | Como interpretar dados alfa contidos na imagem de entrada. O tipo é D2D1 \_ COLORMANAGEMENT \_ Alpha \_ Mode.<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT \_ Alpha \_ mode \_ premultiplicado.<br/> |
| Qualidade<br/> \_Qualidade de \_ prop d2d1 COLORMANAGEMENT \_<br/> | O nível de qualidade da transformação. O tipo é D2D1 \_ COLORMANAGEMENT \_ Quality.<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal.<br/> |

## <a name="rendering-intent-modes"></a>Modos de intenção de renderização

| Enumeração | Descrição |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ tentativa de renderização \_ \_ perceptiva | O efeito compacta ou expande a gama de cores completa da imagem para preencher a gama de cores do dispositivo, para que o saldo cinza seja preservado, mas a precisão colorimétrico não possa ser preservada. |
| Colorimétrico relativo da D2D1 COLORMANAGEMENT para a \_ \_ renderização \_ \_ relativa \_ | O efeito preserva o croma de cores na imagem, com a possível despesa de matiz e claridade. |
| \_Saturação da \_ tentativa de RENDERIZAÇÃO \_ \_ de d2d1 COLORMANAGEMENT | O efeito ajusta as cores que ficam fora do intervalo de cores que o dispositivo de saída renderiza para a cor mais próxima disponível. Ele não preserva o ponto branco. |
| \_ \_ \_ Colorimétrico absoluto da tentativa de renderização \_ d2d1 COLORMANAGEMENT \_ | O efeito ajusta as cores que estão fora do intervalo que o dispositivo de saída pode processar para a cor mais próxima que pode ser renderizada. O efeito não altera as outras cores e preserva o ponto branco. |

## <a name="input-image-alpha-modes"></a>Modos alfa da imagem de entrada

| Enumeração | Descrição |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ \_ modo alfa \_ premultiplicado | O efeito pressupõe que o modo alfa é premultiplicado. |
| \_ \_ Modo Alpha d2d1 \_ COLORMANAGEMENT \_ reto | O efeito pressupõe que o modo alfa é reto. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 alterações de comportamento
    
Se seu aplicativo usa o espaço de [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) ou um dos valores de enumeração de [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) que usam o espaço de cores SMPTE St. 2084 (perceptiva quantizador), o aplicativo pretende trabalhar com dados HDR.

As APIs [**ID2D1DeviceContext5:: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) e [**ID2D1DeviceContext5:: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) não são contadas para isso; em vez disso, o conteúdo HDR é dimensionado para caber no intervalo de 0-1 durante a operação de desdimensionamento de G2084.

Na prática, o conteúdo codificado neste espaço de gama usa um WhiteLevel de referência de 10.000 nits, que normalmente seria representado em CCCS como 10.000/80 = 125,0. Portanto, para facilitar melhor seu aplicativo, é mais simples para essa conversão de gama também dimensionar a luminância por um fator de 125. A partir do Windows 10, versão 1809 (10,0; Build 17763), o comportamento do efeito de gerenciamento de cores é que ele aplica esse dimensionamento. Isso significa que você, como desenvolvedor, não precisa aplicar um segundo efeito de [ajuste de nível branco](white-level-adjustment-effect.md) no pipeline.

## <a name="compliance-with-icc-specification"></a>Conformidade com a especificação ICC

O efeito de gerenciamento de cores é compatível com a especificação ICC v 4.3, com estas limitações:

- O efeito dá suporte a espaços de cores de 1, 3 e 4 canais.
- O efeito não dá suporte a perfis de cor ColorSpace ou nomeados.

## <a name="alpha-channel-behavior"></a>Comportamento do canal alfa

Em geral, o efeito define alfa como 1 (opaco) se não houver dados alfa na imagem de origem e os dados alfa serão descartados se não houver espaço na imagem de destino. A tabela aqui descreve o comportamento alfa.

<table>
<thead>
<tr class="header">
<th>Colorspace de origem, formato de pixel</th>
<th>Colorspace de destino, formato de pixel</th>
<th>Comportamento alfa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 canal, formato R pixel $ {REMOVE} $<br />
</td>
<td>formato de 1 canal, R pixel</td>
<td>(Não há dados alfa)</td>
</tr>
<tr class="even">
<td>1 canal, formato de pixel RGBA</td>
<td>Os dados Alfa são definidos como 1 (opaco)</td>

</tr>
<tr class="odd">
<td>3 canal, formato de pixel RGBA</td>
<td>Os dados Alfa são definidos como 1 (opaco)</td>

</tr>
<tr class="even">
<td>4 canais, formato de pixel RGBA</td>
<td>(Não há dados alfa)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 canal, formato de pixel RGBA $ {REMOVE} $<br />
</td>
<td>formato de 1 canal, R pixel</td>
<td>Os dados Alfa são descartados</td>
</tr>
<tr class="even">
<td>1 canal, formato de pixel RGBA</td>
<td>Dados Alfa são passados por</td>

</tr>
<tr class="odd">
<td>3 canal, formato de pixel RGBA</td>
<td>Dados Alfa são passados por</td>

</tr>
<tr class="even">
<td>4 canais, formato de pixel RGBA</td>
<td>Os dados Alfa são descartados</td>

</tr>
<tr class="odd">
<td rowspan="4">3 canal, formato de pixel RGBA $ {REMOVE} $<br />
</td>
<td>formato de 1 canal, R pixel</td>
<td>Os dados Alfa são descartados</td>
</tr>
<tr class="even">
<td>1 canal, formato de pixel RGBA</td>
<td>Dados Alfa são passados por</td>

</tr>
<tr class="odd">
<td>3 canal, formato de pixel RGBA</td>
<td>Dados Alfa são passados por</td>

</tr>
<tr class="even">
<td>4 canais, formato de pixel RGBA</td>
<td>Os dados Alfa são descartados</td>

</tr>
<tr class="odd">
<td rowspan="4">4 Channel, formato de pixel RGBA $ {REMOVE} $<br />
</td>
<td>formato de 1 canal, R pixel</td>
<td>(Não há dados alfa)</td>
</tr>
<tr class="even">
<td>1 canal, formato de pixel RGBA</td>
<td>Os dados Alfa são definidos como 1 (opaco)</td>

</tr>
<tr class="odd">
<td>3 canal, formato de pixel RGBA</td>
<td>Os dados Alfa são definidos como 1 (opaco)</td>

</tr>
<tr class="even">
<td>4 canais, formato de pixel RGBA</td>
<td>(Não há dados alfa)</td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>Modos de qualidade

| Mode | Descrição |
|-|-|
| Prova de qualidade de D2D1 \_ COLORMANAGEMENT \_ \_ | O modo de qualidade mais baixo. Esse modo requer o nível de recurso 9 \_ 1 ou superior. |
| D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal | Modo de qualidade normal. Esse modo requer o nível de recurso 9 \_ 1 ou superior. |
| D2D1 \_ COLORMANAGEMENT \_ qualidade \_ melhor | O modo de melhor qualidade. Esse modo requer o nível de recurso 10 \_ 0 ou superior, bem como buffers de precisão de ponto flutuante. Esse modo dá suporte à precisão de ponto flutuante, bem como ao intervalo estendido, conforme definido na especificação ICC v 4.3. |

O efeito de gerenciamento de cores falha ao desenhar se o aplicativo solicitar um modo de qualidade que não tenha suporte do hardware. Você pode determinar o nível do recurso ao chamar [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice). Você pode verificar o suporte ao buffer de ponto flutuante chamando [**ID2D1EffectContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) com o valor [**d2d1 \_ buffer \_ Precision \_ 32BPC \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).

## <a name="sample-code"></a>Código de exemplo

Para obter um exemplo desse efeito, baixe o [exemplo de ajuste de foto de efeitos de Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)e veja a lição 4 do exemplo.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro | d2d1effects. h |
| Biblioteca | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
