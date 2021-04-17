---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
description: Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. Consulte D3D12 \_ gráficos \_ pipeline \_ State \_ DESC e D3D12 \_ Compute \_ pipeline \_ State \_ desc. | Estrutura de CD3DX12_PIPELINE_STATE_STREAM (D3dx12. h)
ms.assetid: C0CEFC67-72B3-4A8D-9C88-381990FC9898
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM
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
ms.openlocfilehash: 8d52b9090fa1d3870027bbe360164627472c039e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791283"
---
# <a name="cd3dx12_pipeline_state_stream-structure"></a>\_Estrutura do \_ fluxo de estado do pipeline CD3DX12 \_

Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada. Consulte [**D3D12 \_ gráficos \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ Compute \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).

\_ \_ O fluxo de estado do pipeline CD3DX12 \_ dá suporte à atualização do Windows 10 para criadores e mais recente, mas não dá suporte a novos recursos da atualização de criadores de outono, como exibir a instanciação. Para dar suporte a recursos da atualização de criadores de outono, use [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) em vez disso.

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

**\_ \_ \_ Fluxo de estado do pipeline CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ \_ Fluxo de estado do pipeline CD3DX12 (const D3D12 \_ GRAPHICS \_ \_ estado pipeline \_ desc& DESC)**
</dt> <dd>

Cria uma nova instância de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ , inicializada com valores copiados de uma estrutura de fluxo de **\_ estado de pipeline \_ \_ CD3DX12** .

</dd> <dt>

**\_ \_ \_ Fluxo de estado do pipeline CD3DX12 (const D3D12 \_ estado do pipeline de computação \_ \_ \_ desc& DESC)**
</dt> <dd>

Cria uma nova instância de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ , inicializada com valores copiados de uma estrutura de fluxo de **\_ estado de pipeline \_ \_ CD3DX12** .

</dd> <dt>

**GraphicsDescV0()**
</dt> <dd>

Retorna o conteúdo do objeto de \_ fluxo de estado do pipeline CD3DX12 \_ \_ como um estado de pipeline de gráficos do D3D12 \_ \_ \_ \_ estrutura desc por valor. Observe que \_ o estado de pipeline de gráficos D3D12 \_ \_ \_ DESC não inclui o membro **cs** , portanto, esse valor é perdido na conversão.

</dd> <dt>

**ComputeDescV0()**
</dt> <dd>

Retorna o conteúdo do objeto de \_ fluxo de estado do pipeline CD3DX12 \_ \_ como \_ uma \_ estrutura desc de estado do pipeline de computação D3D12 \_ \_ por valor. Observe que \_ \_ \_ o estado Desc do pipeline de computação D3D12 não \_ inclui os membros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **blendstate**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** , para que esses valores sejam perdidos na conversão.

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

\_ \_ O fluxo de estado do pipeline CD3DX12 \_ dá suporte à atualização do Windows 10 para criadores e mais recente, mas não oferece suporte a tipos de subobjetos adicionados na atualização de criadores de outono do Windows 10, como para o modo de exibição de instanciação. Para oferecer suporte a tipos de subobjetos adicionados na atualização de criadores de outono, use [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) em vez disso.

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

[**CD3DX12 \_ de \_ estado de pipeline \_ STREAM1**](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[**Desc. de estado do pipeline de \_ gráficos D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[**\_Desc de \_ estado do pipeline de computação D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





