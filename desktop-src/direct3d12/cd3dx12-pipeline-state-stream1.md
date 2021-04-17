---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
description: Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. Consulte D3D12 \_ gráficos \_ pipeline \_ State \_ DESC e D3D12 \_ Compute \_ pipeline \_ State \_ desc. | Estrutura de CD3DX12_PIPELINE_STATE_STREAM1 (D3dx12. h)
ms.assetid: 4D3E4D99-E820-4220-92F3-4924791E780F
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd04f58f4f123850c60b67ff9358f6f1f934373
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780341"
---
# <a name="cd3dx12_pipeline_state_stream1-structure"></a>\_ \_ Estrutura STREAM1 do estado do pipeline CD3DX12 \_

Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. Consulte [**D3D12 \_ gráficos \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ Compute \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

\_ \_ \_ O estado do pipeline do CD3DX12 STREAM1 dá suporte à atualização dos criadores de outono do Windows 10 com novos recursos, como exibir a instanciação.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM1 {
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1();
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_GRAPHICS_PIPELINE_STATE_DESC& Desc);
  CD3DX12_PIPELINE_STATE_STREAM1                      CD3DX12_PIPELINE_STATE_STREAM1(const D3D12_COMPUTE_PIPELINE_STATE_DESC& Desc);
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

**CD3DX12 \_ \_ de estado \_ de pipeline STREAM1 ()**
</dt> <dd>

Cria uma instância nova e não inicializada de um STREAM1 de \_ estado de pipeline CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ Estado de pipeline CD3DX12 \_ STREAM1 (const \_ D3D12 \_ Graphics \_ estado pipeline \_ desc& DESC)**
</dt> <dd>

Cria uma nova instância de um \_ estado de pipeline CD3DX12 \_ \_ STREAM1, inicializada com valores copiados de uma estrutura **\_ \_ \_ STREAM1 de estado de pipeline CD3DX12** .

</dd> <dt>

**\_ \_ Estado de pipeline CD3DX12 \_ STREAM1 (const D3D12 \_ COMPUTE \_ pipeline \_ estado \_ desc& DESC)**
</dt> <dd>

Cria uma nova instância de um \_ estado de pipeline CD3DX12 \_ \_ STREAM1, inicializada com valores copiados de uma estrutura **\_ \_ \_ STREAM1 de estado de pipeline CD3DX12** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Retorna o conteúdo do \_ objeto STREAM1 do estado do pipeline CD3DX12 \_ \_ como um \_ estado de pipeline de gráficos D3D12 \_ \_ \_ estrutura desc por valor. Observe que \_ o estado de pipeline de gráficos D3D12 \_ \_ \_ DESC não inclui o membro **cs** , portanto, esse valor é perdido na conversão.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Retorna o conteúdo do \_ objeto STREAM1 do estado do pipeline CD3DX12 \_ \_ como uma \_ estrutura desc de estado do pipeline de computação D3D12 \_ \_ \_ por valor. Observe que \_ \_ \_ o estado Desc do pipeline de computação D3D12 não \_ inclui os membros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **blendstate**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** , para que esses valores sejam perdidos na conversão.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Descreve os sinalizadores de estado do pipeline, que controlam recursos como "depuração de ferramenta".

</dd> <dt>

**NodeMask**
</dt> <dd>

Descreve a máscara de nó de estado do pipeline, que é usada para identificar os nós (adaptadores físicos do dispositivo) aos quais o PSO se aplica em cenários de vários adaptadores; cada bit na máscara corresponde a um único nó. Para cenários de adaptador único, defina esse valor como 0.

</dd> <dt>

**pRootSignature**
</dt> <dd>

Descreve a assinatura raiz.

</dd> <dt>

**InputLayout**
</dt> <dd>

Descreve o formato de buffer de entrada para o estágio de Assembler de entrada

</dd> <dt>

**IBStripCutValue**
</dt> <dd>

Descreve o valor de índice especial do buffer de entrada que indica uma recorte (descontinuidade) ao usar a topologia de faixa de triângulo.

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

**HS**
</dt> <dd>

Descreve o sombreador envoltória.

</dd> <dt>

**DS**
</dt> <dd>

Descreve o sombreador de domínio.

</dd> <dt>

**PROFISSIONAIS**
</dt> <dd>

Descreve o sombreador de pixel.

</dd> <dt>

**CS**
</dt> <dd>

Descreve o sombreador de computação.

</dd> <dt>

**Blendstate**
</dt> <dd>

Descreve o estado de mesclagem.

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

Descreve a contagem de amostras e a qualidade.

</dd> <dt>

**SampleMask**
</dt> <dd>

Descreve a máscara de exemplo usada com o estado de mistura.

</dd> <dt>

**CachedPSO**
</dt> <dd>

Descreve um PSO armazenado em cache.

</dd> </dl>

## <a name="remarks"></a>Comentários

[**CD3DX12 \_ O \_ \_ fluxo de estado do pipeline**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) dá suporte à atualização dos criadores de outono do Windows 10, mas não dá suporte a tipos de subobjetos adicionados à atualização de criadores de outono do Windows 10, como para a criação de instâncias de exibição. Para dar suporte aos novos tipos de subobjetos, use CD3DX12 \_ pipeline \_ State \_ STREAM1 em vez disso.

As variáveis de membro acessíveis dessa estrutura são todos os TYPEDEFs do \_ modelo de \_ subobjeto Stream do estado do pipeline CD3DX12 \_ \_ , que combina os dados do marcador de tipo de subobjeto e subobjeto em um único objeto adequado para uma descrição de fluxo.

Esses TYPEDEFs são:

<dl> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Fluxo de \_ estado do pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[**Desc. de estado do pipeline de \_ gráficos D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**\_Desc de \_ estado do pipeline de computação D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





