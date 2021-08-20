---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM2 (D3dx12. h)
description: Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada.
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM2
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM2
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: 18b662217f5e2a59c7925e0f401a9288ea710e8a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812339"
---
# <a name="cd3dx12_pipeline_state_stream2-structure"></a>Estrutura de CD3DX12_PIPELINE_STATE_STREAM2

Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. Consulte [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

O **CD3DX12_PIPELINE_STATE_STREAM2** dá suporte a Build do sistema operacional 19041 + (onde há um pipeline do sombreador de malha).

## <a name="syntax"></a>Sintaxe

```cpp
struct CD3DX12_PIPELINE_STATE_STREAM2
{
    CD3DX12_PIPELINE_STATE_STREAM2();
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc) noexcept;
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS Flags;
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK NodeMask;
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE pRootSignature;
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT InputLayout;
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE IBStripCutValue;
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY PrimitiveTopologyType;
    CD3DX12_PIPELINE_STATE_STREAM_VS VS;
    CD3DX12_PIPELINE_STATE_STREAM_GS GS;
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT StreamOutput;
    CD3DX12_PIPELINE_STATE_STREAM_HS HS;
    CD3DX12_PIPELINE_STATE_STREAM_DS DS;
    CD3DX12_PIPELINE_STATE_STREAM_PS PS;
    CD3DX12_PIPELINE_STATE_STREAM_AS AS;
    CD3DX12_PIPELINE_STATE_STREAM_MS MS;
    CD3DX12_PIPELINE_STATE_STREAM_CS CS;
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC BlendState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 DepthStencilState;
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT DSVFormat;
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER RasterizerState;
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC SampleDesc;
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK SampleMask;
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO CachedPSO;
    CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING ViewInstancingDesc;
    D3D12_GRAPHICS_PIPELINE_STATE_DESC GraphicsDescV0() const noexcept;
    D3D12_COMPUTE_PIPELINE_STATE_DESC ComputeDescV0() const noexcept;
};
```

## <a name="members"></a>Membros

`CD3DX12_PIPELINE_STATE_STREAM2`

Construtor padrão. Cria uma nova instância, não inicializada, de um **CD3DX12_PIPELINE_STATE_STREAM2**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_GRAPHICS_PIPELINE_STATE_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_PIPELINE_STATE_STREAM2** inicializado com o conteúdo de uma estrutura de [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .

Em seguida, você precisará definir os sombreadores de malha e amplificação manualmente, pois eles não têm representação em **D3D12_GRAPHICS_PIPELINE_STATE_DESC**.

`CD3DX12_PIPELINE_STATE_STREAM2(const D3DX12_MESH_SHADER_PIPELINE_STATE_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_PIPELINE_STATE_STREAM2** inicializado com o conteúdo de uma estrutura de [**D3DX12_MESH_SHADER_PIPELINE_STATE_DESC**](d3dx12-mesh-shader-pipeline-state-desc.md) .

`CD3DX12_PIPELINE_STATE_STREAM2(const D3D12_COMPUTE_PIPELINE_STATE_DESC&)`

Construtor que cria uma nova instância de um **CD3DX12_PIPELINE_STATE_STREAM2** inicializado com o conteúdo de uma estrutura de [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .

`Flags`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_FLAGS](cd3dx12-pipeline-state-stream-flags.md)**

Flags (por exemplo, para indicar que o estado do pipeline deve ser compilado com informações adicionais para ajudar na depuração).

`NodeMask`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK](cd3dx12-pipeline-state-stream-node-mask.md)**

Descreve a máscara de nó de estado do pipeline, que é usada para identificar os nós (adaptadores físicos do dispositivo) aos quais o PSO se aplica em cenários de vários adaptadores; cada bit na máscara corresponde a um único nó. Para cenários de adaptador único, use 0.

`pRootSignature`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE](cd3dx12-pipeline-state-stream-root-signature.md)**

Descreve a assinatura raiz.

`InputLayout`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT](cd3dx12-pipeline-state-stream-input-layout.md)**

Descreve o formato de buffer de entrada para o estágio de Assembler de entrada

`IBStripCutValue`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)**

Descreve o valor de índice especial do buffer de entrada que indica uma recorte (descontinuidade) ao usar a topologia de faixa de triângulo.

`PrimitiveTopologyType`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY](cd3dx12-pipeline-state-stream-primitive-topology.md)**

Descreve a topologia primitiva e sua ordem.

`VS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_VS](cd3dx12-pipeline-state-stream-vs.md)**

Descreve o sombreador de vértice.

`GS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_GS](cd3dx12-pipeline-state-stream-gs.md)**

Descreve o sombreador de geometria.

`StreamOutput`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT](cd3dx12-pipeline-state-stream-stream-output.md)**

Descreve o buffer de saída de streaming.

`HS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_HS](cd3dx12-pipeline-state-stream-hs.md)**

Descreve o sombreador envoltória.

`DS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DS](cd3dx12-pipeline-state-stream-ds.md)**

Descreve o sombreador de domínio.

`PS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_PS](cd3dx12-pipeline-state-stream-ps.md)**

Descreve o sombreador de pixel.

`AS`

Tipo: **CD3DX12_PIPELINE_STATE_STREAM_AS**

Descreve o sombreador de amplificação.

`MS`

Tipo: **CD3DX12_PIPELINE_STATE_STREAM_MS**

Descreve o sombreador de malha.

`CS`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_CS](cd3dx12-pipeline-state-stream-cs.md)**

Descreve o sombreador de computação.

`BlendState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC](cd3dx12-pipeline-state-stream-blend-desc.md)**

Descreve o estado de mesclagem.

`DepthStencilState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1](cd3dx12-pipeline-state-stream-depth-stencil1.md)**

Descreve o estado de estêncil de profundidade.

`DSVFormat`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT](cd3dx12-pipeline-state-stream-depth-stencil-format.md)**

Descreve o formato de estêncil de profundidade.

`RasterizerState`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER](cd3dx12-pipeline-state-stream-rasterizer.md)**

Descreve o estado do rasterizador.

`RTVFormats`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS](cd3dx12-pipeline-state-stream-render-target-formats.md)**

Descreve os formatos de destino de renderização.

`SampleDesc`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC](cd3dx12-pipeline-state-stream-sample-desc.md)**

Descreve a contagem de amostras e a qualidade.

`SampleMask`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK](cd3dx12-pipeline-state-stream-sample-mask.md)**

Descreve a máscara de exemplo usada com o estado de mistura.

`CachedPSO`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO](cd3dx12-pipeline-state-stream-cached-pso.md)**

Descreve um PSO armazenado em cache.

`ViewInstancingDesc`

Tipo: **[CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING](cd3dx12-pipeline-state-stream-view-instancing.md)**

Descreve um modo de exibição de configuração de instanciação.

`GraphicsDescV0`

Retorna [**D3D12_GRAPHICS_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc).

Retorna o conteúdo do objeto **CD3DX12_PIPELINE_STATE_STREAM2** como uma estrutura de **D3D12_GRAPHICS_PIPELINE_STATE_DESC** por valor. **D3D12_GRAPHICS_PIPELINE_STATE_DESC** não inclui o membro *cs* , portanto, esse valor é perdido na conversão.

`ComputeDescV0`

Retorna [**D3D12_COMPUTE_PIPELINE_STATE_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

Retorna o conteúdo do objeto **CD3DX12_PIPELINE_STATE_STREAM2** como uma estrutura de **D3D12_COMPUTE_PIPELINE_STATE_DESC** por valor. **D3D12_COMPUTE_PIPELINE_STATE_DESC** não inclui os membros *InputLayout*, *IBStripCutValue*, *PrimitiveTopologyType*, *vs*, *GS*, *StreamOutput*, *HS*, *DS*, *PS*, *blendstate*, *DepthStencilState*, *DSVFormat*, *RasterizerState*, *NumRootSignature*, *RTVFormats*, *SampleDesc* e *SampleMask*, para que esses valores sejam perdidos na conversão.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
