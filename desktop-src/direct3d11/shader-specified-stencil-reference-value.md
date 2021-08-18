---
title: Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 11)
description: Saiba mais sobre o valor de referência de estêncil nos gráficos do Direct3D 11. A habilitação de sombreadores de pixel para usar o valor de referência de estêncil permite um controle fino sobre as operações de estêncil.
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d780c7a800f4291b3cce01c6f974cdeedaa8f590fc76fdf8afa8b3fb3c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632306"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a>Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 11)

A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.

O valor especificado do sombreador substitui o *valor de referência de estêncil* especificado pela API para essa invocação, o que significa que a alteração afeta o teste de estêncil e quando OP OP D3D11 stencil Place \_ \_ \_ replace (um membro de [**D3D11 \_ stencil \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) é usado para gravar o valor de referência no buffer de estêncil.

Em versões anteriores do D3D11, o valor de referência do estêncil só pode ser especificado pelo método [**ID3D11DeviceContext:: OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) . Isso significa que esse valor só pode ser definido em uma granularidade por empate. Este recurso do D3D 11.3 permite que os desenvolvedores leiam e usem o valor de referência do estêncil ( `SV_StencilRef` ) que é a saída de um sombreador de pixel, o que significa que ele pode ser especificado em uma granularidade por pixel ou por amostra.

Esse recurso é opcional no D3D 11.3. Para testar seu suporte, verifique o `PSSpecifiedStencilRefSupported` campo booliano do [**\_ recurso D3D11 \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) usando [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)

Aqui está um exemplo do uso de `SV_StencilRef` em um sombreador de pixel:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D 11,3](direct3d-11-3-features.md)
</dt> <dt>

[Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
