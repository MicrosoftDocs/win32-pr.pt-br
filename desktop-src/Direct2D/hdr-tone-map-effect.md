---
title: Efeito de mapa de tons HDR
description: Esse efeito ajusta o intervalo dinâmico de uma imagem para melhor adequar seu conteúdo à capacidade da exibição de saída.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 4c9234e1b50e155173630a2ff7d94756c5be6130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824502"
---
# <a name="hdr-tone-map-effect"></a>Efeito de mapa de tons HDR

Esse efeito ajusta o intervalo dinâmico de uma imagem para melhor adequar seu conteúdo à capacidade da exibição de saída.

As propriedades desse efeito são identificadas pela [**enumeração D2D1_HDRTONEMAP_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)e o CLSID é **CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Propriedades do efeito

| Nome de exibição e enumeração de índice | Tipo e valor padrão | Descrição |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | O nível de luz máximo (ou MaxCLL) da imagem, em nits. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | O MaxCLL com suporte do destino de saída, em nits normalmente, é &mdash; definido como o MaxCLL da exibição. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Quando definido como **_HDR**, a curva de mapeamento de Tom é ajustada para se ajustar melhor ao comportamento das exibições HDR comuns. |

## <a name="remarks"></a>Comentários
O valor de `InputMaxLuminance` é normalmente derivado dos metadados da imagem. Para casos em que os metadados não estão presentes, você pode usar a função **D2DAdvancedColorImagesRenderer:: ComputeHdrMetadata** (no [exemplo de renderização de imagem de cor avançada Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)) para calcular o nível de luz máximo (MaxCLL) de uma imagem, em nits.

O valor de `OutputMaxLuminance` é projetado para ser derivado da exibição, usando [**DXGI_OUTPUT_DESC1:: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).

O efeito do mapa de tons HDR tem curvas de mapa de Tom diferentes, dependendo se a exibição é uma exibição HDR ou uma exibição SDR/WCG.

Esse efeito deve ser combinado com o efeito de [ajuste de nível branco](white-level-adjustment-effect.md) para permitir que você processe imagens HDR no Direct2D com o gerenciamento de cores e o mapeamento de Tom adequados. Ele é destinado a qualquer estrutura que queira fornecer uma experiência de exibição de imagem HDR de melhor qualidade que manipule todos os formatos de imagem HDR do Windows e se adapte aos recursos da tela (seja HDR ou WCG/SDR). Os efeitos devem ser encadeados em sequência, conforme descrito abaixo.

- Pegue a imagem de entrada, cujo espaço de cores definido por seu codec. Os metadados podem especificar whitePoint. Os metadados podem especificar o nível de luminância de entrada.
- Aplique o efeito de gerenciamento de cores. Converter em espaço scRGB (CCCS).
- Aplique o efeito de mapa de Tom HDR. Reduza o nível de luz da imagem para o nível desejado.
- Aplique o efeito de ajuste de nível branco. Dimensione o nível branco da imagem para o nível branco exigido pela cadeia de permuta.
- Aplique o efeito de gerenciamento de cores novamente. Se estiver renderizando para 8bpc, converta em sRGB.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 10, versão 1809 (10,0; Build 17763) aplicativos de \[ Desktop aplicativos \| UWP\] |
| parâmetro | d2d1effects \_ 2. h |
| Biblioteca | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Enumeração de D2D1_HDRTONEMAP_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
