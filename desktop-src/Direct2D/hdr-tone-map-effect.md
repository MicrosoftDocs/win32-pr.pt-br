---
title: Efeito do mapa de tom do HDR
description: Esse efeito ajusta o intervalo dinâmico de uma imagem para melhor adequar seu conteúdo à capacidade da exibição de saída.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: ce47159abe4bdf0615a76960c4c5e2db289156e89989012f659e437e93727cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260056"
---
# <a name="hdr-tone-map-effect"></a>Efeito do mapa de tom do HDR

Esse efeito ajusta o intervalo dinâmico de uma imagem para melhor adequar seu conteúdo à capacidade da exibição de saída.

As propriedades para esse efeito são identificadas pela [**enumeração D2D1_HDRTONEMAP_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)e a CLSID é **CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Propriedades de efeito

| Nome de exibição e enumeração de índice | Tipo e valor padrão | Description |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | O nível de luz máximo (ou MaxCLL) da imagem, em nits. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | O MaxCLL com suporte pelo destino de saída, em nits normalmente definido como &mdash; o MaxCLL da exibição. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Quando definido como _HDR , **a** curva de mapeamento de tom é ajustada para se ajustar melhor ao comportamento de exibições comuns do HDR. |

## <a name="remarks"></a>Comentários
O valor de `InputMaxLuminance` é normalmente derivado dos metadados da imagem. Para casos em que [os metadados](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)não estão presentes, você pode usar a função **D2DAdvancedColorImagesRenderer::ComputeHdrMetadata** (no exemplo de renderização de imagem de cor avançada do Direct2D ) para calcular o nível máximo de luz (MaxCLL) de uma imagem, em nits.

O valor de `OutputMaxLuminance` foi projetado para ser derivado da exibição, usando [**DXGI_OUTPUT_DESC1::MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).

O efeito do mapa de tom HDR tem curvas de mapa de tom diferentes, dependendo se a exibição é uma exibição HDR ou uma exibição SDR/WCG.

Esse efeito destina-se a [](white-level-adjustment-effect.md) ser combinado com o efeito de ajuste de nível branco para permitir que você renderizar imagens HDR Direct2D com o gerenciamento de cores e mapeamento de tom apropriados. Ele destina-se a qualquer estrutura que queira fornecer uma melhor experiência de exibição de imagem HDR na classe que lida com todos os formatos de imagem hdr do Windows e adapta-se aos recursos da exibição (seja HDR ou WCG/SDR). Os efeitos devem ser encadeados em sequência, conforme descrito abaixo.

- Pegue a imagem de entrada, cujo espaço de cor definido por seu codec. Os metadados podem especificar whitePoint. Os metadados podem especificar o nível de luminância de entrada.
- Aplique o efeito de gerenciamento de cores. Converta em espaço CCCS (scRGB).
- Aplique o efeito de mapa de tom HDR. Reduza o nível de luz da imagem para o nível desejado.
- Aplique o efeito de ajuste em nível de branco. Dimensione o nível em branco da imagem para o nível em branco exigido pela cadeia de permuta.
- Aplique o efeito de gerenciamento de cores novamente. Se estiver renderizar para 8bpc, converta em sRGB.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 10, versão 1809 (10.0; Build 17763) \[ Aplicativos UWP de aplicativos da área \| de trabalho\] |
| parâmetro | d2d1effects \_ 2.h |
| Biblioteca | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_HDRTONEMAP_PROP enumeração](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
