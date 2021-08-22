---
title: Efeito de mapa de tom branco
description: Esse efeito permite que o nível branco de uma imagem seja dimensionado linearmente. Isso é especialmente útil quando você converte entre o espaço de luminância de exibição referenciado e o espaço de luminância mencionado na cena, ou vice-versa.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 646ad47ad671618f29d1691878de93b5e5141855787c53fdad44025487835ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292626"
---
# <a name="white-level-adjustment-effect"></a>Efeito de ajuste de nível branco

Esse efeito permite que o nível branco de uma imagem seja dimensionado linearmente. Isso é especialmente útil quando você converte entre o espaço de luminância de exibição referenciado e o espaço de luminância mencionado na cena, ou vice-versa.

As propriedades desse efeito são identificadas pela [**enumeração D2D1_WHITELEVELADJUSTMENT_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)e o CLSID é **CLSID_D2D1WhiteLevelAdjustment**.

## <a name="effect-properties"></a>Propriedades do efeito

| Nome de exibição e enumeração de índice | Tipo e valor padrão | Descrição |
|-|-|-|
| InputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_INPUT_WHITE_LEVEL | FLOAT | O nível branco da imagem de entrada, em nits. |
| OutputWhiteLevel, D2D1_WHITELEVELADJUSTMENT_PROP_OUTPUT_WHITE_LEVEL | FLOAT | O nível branco da imagem de saída, em nits. |

## <a name="remarks"></a>Comentários
esse efeito deve ser combinado com o efeito de [mapa de tons hdr](hdr-tone-map-effect.md) para permitir que você processe imagens HDR em Direct2D com o gerenciamento de cores e o mapeamento de tom adequados. Consulte os **comentários** deste tópico para obter mais detalhes. os efeitos são direcionados a qualquer estrutura que queira fornecer uma experiência de exibição de imagem hdr de melhor qualidade que lide com todos os Windows formatos de imagem hdr e se adapte aos recursos da tela (seja HDR ou WCG/SDR).

na Windows, supõe-se que todo o conteúdo do SDR/WCG esteja em um espaço de luminância de exibição conhecido, o que significa que o nível de branco do conteúdo deve ser dimensionado para o nível branco da tela antes de ser apresentado. No entanto, nem sempre é responsabilidade do seu aplicativo fazer isso. Por outro lado, supõe-se que o conteúdo HDR esteja em um espaço de luminância referido pela cena, o que significa que ele não deve ser expandido para coincidir com o nível branco da exibição. Dito isso, seu aplicativo pode precisar executar o dimensionamento em algumas circunstâncias ao renderizar conteúdo HDR para garantir que esse é o resultado líquido.

quando a área de trabalho Windows está no modo SDR ou WCG, a área de trabalho é composta em um espaço de luminância de exibição conhecido. mas se o Windows área de trabalho estiver no modo HDR, a composição de área de trabalho ocorrerá em um espaço de luminância referido pela cena. Dito isso, o Gerenciador de Janelas da Área de Trabalho (DWM) em si executa ajustes de luminância (geralmente chamados de SDRBoost) para superfícies de composição de 8 bits, e isso simplifica seu aplicativo para esse caso. Mesmo assim, o aumento automático significa que a função do seu aplicativo na conversão de um espaço de luminância para outro depende do formato de composição que seu aplicativo está usando para apresentar seu conteúdo.

A tabela a seguir descreve os casos em que o aplicativo deve e não deve executar um ajuste de nível branco, bem como o que esse ajuste deve ser. Em geral, o ajuste depende de três fatores.

1. Colorspace de conteúdo de entrada. Se seu conteúdo de entrada contém valores altos de luminância de intervalo dinâmico (HDR) ou não. O conteúdo do WCG se comporta da mesma forma que o SDR para o comportamento de luminância.
2. Formato de composição. O formato de pixel da superfície de destino que é apresentada ao DWM &mdash; , por exemplo, uma [cadeia de permuta](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) ou uma superfície de [composição](/uwp/api/Windows.UI.Composition.ICompositionSurface). durante a renderização usando Direct2D, isso é **UINT8** ou **FP16**.
3. Modo de cor avançado da área de trabalho. Se o DWM está sendo executado no modo SDR, WCG ou HDR para a exibição atual. Obtenha essas informações por meio de [**DXGI_OUTPUT_DESC1:: colorspace**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) ou [**AdvancedColorInfo. CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind).

Com base nesses três fatores, você deve definir os valores apropriados para as `InputWhiteLevel` `OutputWhiteLevel` Propriedades e.

|Conteúdo de entrada|Formato de composição|Modo de cor avançado|InputWhiteLevel|OutputWhiteLevel|
|-|-|-|-|-|
|SDR/WCG|**UINT8**|Qualquer|N/D|N/D|
|SDR/WCG|**FP16**|SDR/WCG|N/D|N/D|
|SDR/WCG|**FP16**|HDR|SDRWhite|80|
|HDR|Qualquer|SDR/WCG|80|[**DXGI_OUTPUT_DESC1:: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)|
|HDR|**UINT8**|HDR|80|SDRWhite|
|HDR|**FP16**|HDR|N/D|N/D|

Na tabela, o valor 80 é o nível branco de referência, em nits, para o conteúdo sRGB ou scRGB. Para isso, você pode usar a constante [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](/windows/desktop/direct2d/direct2d-constants), que é definida em `d2d1effects_2.h` . O valor `SDRWhite` é o número de nits que a exibição deve usar para exibir o conteúdo de sRGB branco. Você pode recuperar esse valor acessando a propriedade [**AdvancedColorInfo. SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits) . O valor N/A significa que o ajuste de nível de branco não é usado neste cenário; Você pode remover o efeito do grafo ou definir valores para um não op.

Observe que, nos casos em que um ajuste de nível branco não é necessário para o aplicativo, o DWM ou a exibição pode estar manipulando a conversão do espaço de luminância de exibição referenciado para o espaço de luminescência referido pela cena.

- No modo SDR/WCG, a conversão ocorre após a composição do DWM e se aplica a todo o conteúdo apresentado à exibição. A exibição executa implicitamente essa conversão.
- No modo HDR, a conversão é executada automaticamente pelo DWM antes da composição, desde que a superfície de composição do seu aplicativo seja SDR.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 10, versão 1809 (10,0; Build 17763) aplicativos de \[ Desktop aplicativos \| UWP\] |
| Cabeçalho | d2d1effects \_ 2. h |
| Biblioteca | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Enumeração de D2D1_WHITELEVELADJUSTMENT_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_whiteleveladjustment_prop)
