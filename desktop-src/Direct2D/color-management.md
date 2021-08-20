---
title: Efeito de gerenciamento de cores
description: Use o efeito de gerenciamento de cores para transformar uma imagem de um perfil de cor do ICC (International Color Consortium) para outro. O efeito transforma a imagem de acordo com a especificação de ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- efeito de gerenciamento de cores
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 274591312ab110a24fb315d01f72d23a22a938ad41f380620d94a865602e82a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826694"
---
# <a name="color-management-effect"></a>Efeito de gerenciamento de cores

Use o efeito de gerenciamento de cores para transformar uma imagem de um perfil de cor do ICC (International Color Consortium) para outro. O efeito transforma a imagem de acordo com a [especificação de ICC](https://www.color.org).

O CLSID para esse efeito é CLSID \_ D2D1ColorManagement.

- [Propriedades de efeito](#effect-properties)
- [Modos de intenção de renderização](#rendering-intent-modes)
- [Modos alfa da imagem de entrada](#input-image-alpha-modes)
- [Conformidade com a especificação de ICC](#compliance-with-icc-specification)
- [Comportamento do canal alfa](#alpha-channel-behavior)
- [Modos de qualidade](#quality-modes)
- [Código de exemplo](#sample-code)
- [Requirements](#requirements)
- [Tópicos relacionados](#related-topics)

## <a name="effect-properties"></a>Propriedades de efeito

| Nome de exibição e enumeração de índice | Descrição |
|-|-|
| SourceContext<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ SOURCE \_ COLOR \_ CONTEXT<br/> | As informações de espaço de cor de origem. O tipo é [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> O valor padrão é NULL.<br/> |
| SourceIntent<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ SOURCE \_ RENDERING \_ INTENT<br/> | Qual intenção de renderização ICC usar. O tipo é D2D1 \_ COLORMANAGEMENT \_ \_ RENDERING INTENT.<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT \_ \_ RENDERING INTENT \_ PERCEPTUAL.<br/> |
| DestinationContext<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ DESTINATION \_ COLOR \_ CONTEXT<br/> | As informações de espaço de cores de destino. O tipo é [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> O valor padrão é NULL.<br/> |
| DestinationIntent<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ DESTINATION \_ RENDERING \_ INTENT<br/> | Qual intenção de renderização ICC usar. O tipo é D2D1 \_ COLORMANAGEMENT \_ \_ RENDERING INTENT.<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT \_ \_ RENDERING INTENT \_ PERCEPTUAL.<br/> |
| AlphaMode<br/> MODO ALFA D2D1 \_ COLORMANAGEMENT \_ PROP \_ \_<br/> | Como interpretar dados alfa contidos na imagem de entrada. O tipo é D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE.<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE \_ PREMULTIPLIED.<br/> |
| Qualidade<br/> D2D1 \_ COLORMANAGEMENT \_ PROP \_ QUALITY<br/> | O nível de qualidade da transformação. O tipo é D2D1 \_ COLORMANAGEMENT \_ QUALITY.<br/> O valor padrão é D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL.<br/> |

## <a name="rendering-intent-modes"></a>Modos de intenção de renderização

| Enumeração | Descrição |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ PERCEPTUAL | O efeito compacta ou expande a gama de cores completa da imagem para preencher a gama de cores do dispositivo, para que o equilíbrio cinza seja preservado, mas a precisão colorimétrica não possa ser preservada. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ RELATIVE \_ COLORIMETRIC | O efeito preserva o chroma de cores na imagem às possíveis despesas de matiz e luz. |
| SATURAÇÃO DA INTENÇÃO \_ DE \_ RENDERIZAÇÃO DE COLORMANAGEMENT \_ \_ D2D1 | O efeito ajusta as cores que estão fora do intervalo de cores que o dispositivo de saída renderiza para a cor mais próxima disponível. Ele não preserva o ponto em branco. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ ABSOLUTE \_ COLORIMETRIC | O efeito ajusta todas as cores que estão fora do intervalo que o dispositivo de saída pode renderizar para a cor mais próxima que pode ser renderizada. O efeito não altera as outras cores e preserva o ponto em branco. |

## <a name="input-image-alpha-modes"></a>Modos alfa da imagem de entrada

| Enumeração | Descrição |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE \_ PREMULTIPLIED | O efeito presume que o modo alfa é pré-ultado. |
| D2D1 \_ MODO ALFA DE COLORMANAGEMENT \_ \_ \_ RETA | O efeito pressu que o modo alfa é reto. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 de comportamento
    
Se seu aplicativo usar o [espaço D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) ou um dos valores de enumeração [do DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) que usam o espaço de cores SMPTE ST.2084 (Perceptual Quantizer), o aplicativo pretende trabalhar com dados HDR.

As APIs [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) e [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) não são responsáveis por isso; em vez disso, o conteúdo do HDR é dimensionado para caber no intervalo de 0 a 1 durante a operação G2084 DeGamma.

Na prática, o conteúdo codificado nesse espaço gama usa uma referência WhiteLevel de 10.000 Nits, que normalmente seria representado no CCCS como 10.000 /80 = 125,0. Portanto, para facilitar melhor seu aplicativo, é mais simples para essa conversão gama também dimensionar a luminância em um fator de 125. A partir Windows 10, versão 1809 (10.0; Build 17763), o comportamento do efeito de gerenciamento de cores é tal que ele aplica esse dimensionamento. Isso significa que você, como desenvolvedor, não precisa aplicar um segundo efeito de ajuste de nível [branco](white-level-adjustment-effect.md) no pipeline.

## <a name="compliance-with-icc-specification"></a>Conformidade com a especificação de ICC

O efeito de gerenciamento de cores está em conformidade com a especificação do ICC v4.3, com estas limitações:

- O efeito dá suporte a espaços de cores de 1, 3 e 4 canais.
- O efeito não dá suporte a perfis ColorSpace ou Cor Nomeada.

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
<td rowspan="4">1 canal, formato de pixel R ${REMOVE}$<br />
</td>
<td>1 canal, formato de pixel R</td>
<td>(Sem dados alfa)</td>
</tr>
<tr class="even">
<td>1 canal, formato de pixel RGBA</td>
<td>Os dados alfa são definidos como 1 (opaco)</td>

</tr>
<tr class="odd">
<td>3 canais, formato de pixel RGBA</td>
<td>Os dados alfa são definidos como 1 (opaco)</td>

</tr>
<tr class="even">
<td>4 canais, formato de pixel RGBA</td>
<td>(Sem dados alfa)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 canal, formato de pixel RGBA ${REMOVE}$<br />
</td>
<td>1 canal, formato de pixel R</td>
<td>Os dados alfa são descartados</td>
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

para obter um exemplo desse efeito, baixe o [exemplo de ajuste de foto Direct2D effects](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)e veja a lição 4 do exemplo.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Cabeçalho | d2d1effects. h |
| Biblioteca | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
