---
title: CD3DX12_PIPELINE_STATE_STREAM (D3dx12.h)
description: Uma estrutura auxiliar para criar e trabalhar com gráficos e estados de pipeline de computação por meio de uma interface combinada. Consulte D3D12 \_ GRAPHICS \_ PIPELINE STATE \_ \_ DESC e D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC. | CD3DX12_PIPELINE_STATE_STREAM (D3dx12.h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- CD3DX12_PIPELINE_STATE_STREAM estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e45c46c39a21aaeb53a2980fa3c082947e92cd5bb4ab3eccbbb225001a6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733978"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>Estrutura CD3DX12 \_ PIPELINE \_ STATE \_ STREAM

Uma estrutura auxiliar para criar e trabalhar com gráficos e estados de pipeline de computação por meio de uma interface combinada. Consulte [**D3D12 \_ GRAPHICS \_ PIPELINE STATE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ COMPUTE PIPELINE STATE \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

O CD3DX12 PIPELINE STATE STREAM dá suporte Atualização do Windows 10 para Criadores e mais recente, mas não dá suporte a novos recursos da atualização do Fall Creators, como o \_ instanciamento \_ de \_ exibição. Para dar suporte aos recursos da atualização do Fall Creators, use [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1.**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**)

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM {
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM();
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM                       CD3DX12_PIPELINE_STATE_STREAM(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
  D3D12_GRAPHICS_PIPELINE_STATE_DESC                  GraphicsDescV0();
  D3D12_COMPUTE_PIPELINE_STATE_DESC                   ComputeDescV0();
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS                 Flags;
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK             NodeMask;
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE        pRootSignature;
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT          InputLayout;
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE    IBStripCutValue;
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY    PrimitiveTopologyType;
  CD3DX12_PIPELINE_STATE_STREAM_VS                    VS;
  CD3DX12_PIPELINE_STATE_STREAM_GS                    GS;
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT         StreamOutput;
  CD3DX12_PIPELINE_STATE_STREAM_HS                    HS;
  CD3DX12_PIPELINE_STATE_STREAM_DS                    DS;
  CD3DX12_PIPELINE_STATE_STREAM_PS                    PS;
  CD3DX12_PIPELINE_STATE_STREAM_CS                    CS;
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC            BlendState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1        DepthStencilState;
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT  DSVFormat;
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER            RasterizerState;
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS RTVFormats;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC           SampleDesc;
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK           SampleMask;
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO            CachedPSO;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM()**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um FLUXO DE ESTADO DE PIPELINE CD3DX12. \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM(const D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC& Desc)**
</dt> <dd>

Cria uma nova instância de um FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializado com valores copiados de uma estrutura \_ \_ \_ **CD3DX12 \_ PIPELINE \_ STATE \_ STREAM.**

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM(const D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC& Desc)**
</dt> <dd>

Cria uma nova instância de um FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializado com valores copiados de uma estrutura \_ \_ \_ **CD3DX12 \_ PIPELINE \_ STATE \_ STREAM.**

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

retorna o conteúdo do objeto CD3DX12 PIPELINE STATE STREAM como uma estrutura \_ \_ \_ D3D12 \_ GRAPHICS \_ PIPELINE STATE \_ \_ DESC por valor. Observe que D3D12 GRAPHICS PIPELINE STATE DESC não inclui o membro \_ \_ \_ \_ **CS,** portanto, esse valor é perdido na conversão.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

retorna o conteúdo do objeto CD3DX12 PIPELINE STATE STREAM como uma estrutura \_ \_ \_ D3D12 \_ COMPUTE \_ PIPELINE STATE \_ \_ DESC por valor. Observe que D3D12 COMPUTE PIPELINE STATE DESC não inclui \_ \_ \_ \_ **InputLayout,** **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats,** **SampleDesc** ou **SampleMask,** portanto, esses valores são perdidos na conversão.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Descreve os sinalizadores de estado do pipeline, que controlam recursos como "depuração de ferramentas".

</dd> <dt>

**NodeMask**
</dt> <dd>

Descreve a máscara de nó de estado do pipeline, que é usada para identificar os nós (adaptadores físicos do dispositivo) aos quais o PSO se aplica em cenários de vários adaptadores; cada bit na máscara corresponde a um único nó. Para cenários de adaptador único, de definido esse valor como 0.

</dd> <dt>

**pRootSignature**
</dt> <dd>

Descreve a assinatura raiz.

</dd> <dt>

**InputLayout**
</dt> <dd>

Descreve o formato de buffer de entrada para o estágio de assembler de entrada

</dd> <dt>

**IBStripCutValue**
</dt> <dd>

Descreve o valor de índice especial do buffer de entrada que indica um corte (descontinuidade) ao usar a topologia de faixa de triângulo.

</dd> <dt>

**PrimitiveTopologyType**
</dt> <dd>

Descreve a topologia primitiva e sua ordem.

</dd> <dt>

**VS**
</dt> <dd>

Descreve o sombreador de vértice.

</dd> <dt>

**GS**
</dt> <dd>

Descreve o sombreador de geometria.

</dd> <dt>

**StreamOutput**
</dt> <dd>

Descreve o buffer de saída de streaming.

</dd> <dt>

**Hs**
</dt> <dd>

Descreve o sombreador de chassi.

</dd> <dt>

**DS**
</dt> <dd>

Descreve o sombreador de domínio.

</dd> <dt>

**Ps**
</dt> <dd>

Descreve o sombreador de pixel.

</dd> <dt>

**CS**
</dt> <dd>

Descreve o sombreador de computação.

</dd> <dt>

**BlendState**
</dt> <dd>

Descreve o estado de combinação.

</dd> <dt>

**DepthStencilState**
</dt> <dd>

Descreve o estado de estêncil de profundidade.

</dd> <dt>

**DSVFormat**
</dt> <dd>

Descreve o formato de estêncil de profundidade.

</dd> <dt>

**RasterizerState**
</dt> <dd>

Descreve o estado do rasterizador.

</dd> <dt>

**RTVFormats**
</dt> <dd>

Descreve os formatos de destino de renderização.

</dd> <dt>

**SampleDesc**
</dt> <dd>

Descreve a contagem e a qualidade de exemplo.

</dd> <dt>

**SampleMask**
</dt> <dd>

Descreve a máscara de exemplo usada com o estado blend.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Descreve um PSO armazenado em cache.

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM dá suporte Atualização do Windows 10 para Criadores e mais recente, mas não dá suporte a tipos de subobjeto adicionados na atualização do Windows 10 Fall Creators, como para exibição de \_ \_ \_ instanciamento. Para dar suporte a tipos de subobjeto adicionados na atualização do Fall Creators, use [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1.**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**)

As variáveis de membro acessíveis dessa estrutura são todas typedefs do modelo \_ SUBOBJECT DE FLUXO DE ESTADO DO PIPELINE CD3DX12, que combina os dados subobjeto de tipo e subobjeto em um único objeto adequado para uma descrição de \_ \_ \_ fluxo.

Esses typedefs são:

<dl> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**D3D12 \_ GRAPHICS \_ PIPELINE \_ STATE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**D3D12 DESC DE ESTADO \_ DO PIPELINE \_ DE \_ \_ COMPUTAÇÃO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





