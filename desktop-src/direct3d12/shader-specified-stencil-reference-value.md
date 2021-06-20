---
title: Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 12)
description: Saiba mais sobre o valor de referência de estêncil nos gráficos do Direct3D 12. A habilitação de sombreadores de pixel para usar o valor de referência de estêncil permite um controle fino sobre as operações de estêncil.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408309"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a>Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 12)

A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.

O valor de referência de estêncil normalmente é especificado pelo método [**ID3D12GraphicsCommandList:: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) . Esse método define o valor de referência do estêncil em uma granularidade por empate. No entanto, esse valor pode ser substituído pelo sombreador de pixel.

Esse recurso D3D12 (e D3D 11.3) permite que os desenvolvedores leiam e usem o valor de referência do estêncil (*VA \_ StencilRef*) que é impresso a partir de um sombreador de pixel, permitindo uma granularidade por pixel ou por amostra.

O valor especificado do sombreador substitui o valor de referência especificado pela API para essa invocação, o que significa que a alteração afeta o teste de estêncil e quando a operação de estêncil D3D12 do \_ estêncil \_ op \_ replace (um membro de [**\_ \_ op D3D12 stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) é usada para gravar o valor de referência no buffer do estêncil.

Esse recurso é opcional no D3D12 e no D3D 11.3. Para testar seu suporte, verifique o campo booliano *PSSpecifiedStencilRefSupported* das [**\_ Opções de \_ \_ D3D12 de \_ dados de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) usando [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Aqui está um exemplo do uso de *\_ StencilRef de VA* em um sombreador de pixel:

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização](rendering.md)
</dt> <dt>

[Associação de recursos no HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Modelo do sombreador 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Como especificar assinaturas raiz no HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
