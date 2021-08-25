---
title: CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER (D3dx12.h)
description: Cria um objeto INTERNO CD3DX12 PIPELINE STATE STREAM de detalhes \_ \_ de \_ subobjeto passados para as funções de membro correspondentes. Esse struct implementa a interface ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d20c34fb2c32cc588a12ac820cd80083d3c3139fa85cbf36810379a21618e80c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851246"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>Estrutura AUXILIAR DE ANÁLISE DE FLUXO \_ DE ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_

Cria um objeto INTERNO CD3DX12 PIPELINE STATE STREAM de detalhes \_ \_ de \_ subobjeto passados para as funções de membro correspondentes. Esse struct implementa a interface [**ID3DX12PipelineParserCallbacks.**](id3dx12pipelineparsercallbacks.md)

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER  : public ID3DX12PipelineParserCallbacks{
  CD3DX12_PIPELINE_STATE_STREAM1 PipelineStream;
  void                           FlagsCb(D3D12_PIPELINE_STATE_FLAGS Flags);
  void                           NodeMaskCb(UINT NodeMask);
  void                           RootSignatureCb(ID3D12RootSignature* pRootSignature);
  void                           InputLayoutCb(const D3D12_INPUT_LAYOUT_DESC& InputLayout);
  void                           IBStripCutValueCb(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE IBStripCutValue);
  void                           PrimitiveTopologyTypeCb(D3D12_PRIMITIVE_TOPOLOGY_TYPE PrimitiveTopologyType);
  void                           VSCb(const D3D12_SHADER_BYTECODE& VS);
  void                           GSCb(const D3D12_SHADER_BYTECODE& GS);
  void                           StreamOutputCb(const D3D12_STREAM_OUTPUT_DESC& StreamOutput);
  void                           HSCb(const D3D12_SHADER_BYTECODE& HS);
  void                           DSCb(const D3D12_SHADER_BYTECODE& DS);
  void                           PSCb(const D3D12_SHADER_BYTECODE& PS);
  void                           CSCb(const D3D12_SHADER_BYTECODE& CS);
  void                           BlendStateCb(const D3D12_BLEND_DESC& BlendState);
  void                           DepthStencilStateCb(const D3D12_DEPTH_STENCIL_DESC& DepthStencilState);
  void                           DepthStencilState1Cb(const D3D12_DEPTH_STENCIL_DESC1& DepthStencilState);
  void                           DSVFormatCb(DXGI_FORMAT DSVFormat);
  void                           RasterizerStateCb(const D3D12_RASTERIZER_DESC& RasterizerState);
  void                           RTVFormatsCb(const D3D12_RT_FORMAT_ARRAY& RTVFormats);
  void                           SampleDescCb(const DXGI_SAMPLE_DESC& SampleDesc);
  void                           SampleMaskCb(UINT SampleMask);
  void                           ViewInstancingCb(const D3D12_VIEW_INSTANCING_DESC& ViewInstancingDesc);
  void                           CachedPSOCb(const D3D12_CACHED_PIPELINE_STATE& CachedPSO);
  void                           ErrorBadInputParameter(UINT);
  void                           ErrorDuplicateSubobject(D3D12_PIPELINE_STATE_SUBOBJECT_TYPE);
  void                           ErrorUnknownSubobject(UINT);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**PipelineStream**
</dt> <dd>

O [**CD3DX12 \_ PIPELINE INTERNO STATE \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md). Seu estado atual representa o efeito cumulativo dos métodos de retorno de chamada que foram chamados nesse objeto.

</dd> <dt>

**SinalizadoresCb(sinalizadores D3D12 \_ PIPELINE \_ STATE \_ FLAGS)**
</dt> <dd>

Inicializa o membro **Flags** de **PipelineStream** usando o valor do *parâmetro Flags.*

</dd> <dt>

**NodeMaskCb(UINT NodeMask)**
</dt> <dd>

Inicializa o membro **NodeMask** de **PipelineStream** usando o valor do *parâmetro Nodemask.*

</dd> <dt>

**RootSignatureCb(ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Inicializa o membro **pRootSignature** de **PipelineStream** usando o valor do *parâmetro pRootSignature.*

</dd> <dt>

**InputLayoutCb(const D3D12 \_ INPUT \_ LAYOUT \_ DESC& InputLayout)**
</dt> <dd>

Inicializa o membro **InputLayout** de **PipelineStream** usando o valor do *parâmetro InputLayout.*

</dd> <dt>

**IBStripCutValueCb(D3D12 \_ INDEX \_ BUFFER \_ STRIP \_ CUT \_ VALUE IBStripCutValue)**
</dt> <dd>

Inicializa o membro **IBStripCutValue** de **PipelineStream** usando o valor do *parâmetro IBStripCutValue.*

</dd> <dt>

**PrimitiveTopologyTypeCb(D3D12 \_ PRIMITIVE \_ TOPOLOGY \_ TYPE PrimitiveTopologyType)**
</dt> <dd>

Inicializa o membro **PrimitiveTopologyType** de **PipelineStream usando** o valor do *parâmetro PrimitiveTopologyType.*

</dd> <dt>

**VSCb(const D3D12 \_ SHADER \_ BYTECODE& VS)**
</dt> <dd>

Inicializa o membro **VS** (sombreador de vértice) **de PipelineStream** usando o valor do *parâmetro VS.*

</dd> <dt>

**GSCb(const D3D12 \_ SHADER \_ BYTECODE& GS)**
</dt> <dd>

Inicializa o membro **GS** (sombreador de geometria) de **PipelineStream** usando o valor do *parâmetro GS.*

</dd> <dt>

**StreamOutputCb(const D3D12 \_ STREAM \_ OUTPUT \_ DESC& StreamOutput)**
</dt> <dd>

Inicializa o membro **StreamOutput** do **PipelineStream** usando o valor do *parâmetro StreamOutput.*

</dd> <dt>

**HSCb(const D3D12 \_ SHADER \_ BYTECODE& HS)**
</dt> <dd>

Inicializa o membro **HS** (sombreador de chassi) de **PipelineStream** usando o valor do *parâmetro HS.*

</dd> <dt>

**DSCb(const D3D12 \_ SHADER \_ BYTECODE& DS)**
</dt> <dd>

Inicializa o membro **DS** (sombreador de domínio) de **PipelineStream** usando o valor do *parâmetro DS.*

</dd> <dt>

**PSCb(const D3D12 \_ SHADER \_ BYTECODE& PS)**
</dt> <dd>

Inicializa o membro **PS** (sombreador de pixel) de **PipelineStream** usando o valor do *parâmetro PS.*

</dd> <dt>

**CSCb(const D3D12 \_ SHADER \_ BYTECODE& CS)**
</dt> <dd>

Inicializa o membro **CS** de **PipelineStream** usando o valor do *parâmetro CS.*

</dd> <dt>

**BlendStateCb(const D3D12 \_ BLEND \_ DESC& BlendState)**
</dt> <dd>

Inicializa o membro **BlendState** de **PipelineStream** usando o valor do *parâmetro BlendState.*

</dd> <dt>

**DepthStencilStateCb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& DepthStencilState)**
</dt> <dd>

Inicializa o membro **DepthStencilState** de **PipelineStream** usando o valor do parâmetro *DepthStencilState,* um [**D3D12 \_ DEPTH \_ STENCIL \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

</dd> <dt>

**DepthStencilState1Cb(const D3D12 \_ DEPTH \_ STENCIL \_ DESC1& DepthStencilState)**
</dt> <dd>

Inicializa o membro **DepthStencilState** de **PipelineStream** usando o valor do parâmetro *DepthStencilState,* um [**D3D12 \_ DEPTH \_ STENCIL \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**DSVFormatCb(DXGI \_ FORMAT DSVFormat)**
</dt> <dd>

Inicializa o membro **DSVFormat** de **PipelineStream** usando o valor do *parâmetro DSVFormat.*

</dd> <dt>

**RasterizerStateCb(const D3D12 \_ RASTERIZER \_ DESC& RasterizerState)**
</dt> <dd>

Inicializa o membro **RasterizerState** de **PipelineStream** usando o valor do *parâmetro RasterizerState.*

</dd> <dt>

**RTVFormatsCb(const D3D12 \_ RT \_ FORMAT \_ ARRAY& RTVFormats)**
</dt> <dd>

Inicializa o membro **RTVFormats** de **PipelineStream** usando o valor do *parâmetro RTVFormats.*

</dd> <dt>

**SampleDescCb(const DXGI \_ SAMPLE \_ DESC& SampleDesc)**
</dt> <dd>

Inicializa o membro **SampleDesc** de **PipelineStream** usando o valor do *parâmetro SampleDesc.*

</dd> <dt>

**SampleMaskCb(UINT SampleMask)**
</dt> <dd>

Inicializa o membro **SampleMask** de **PipelineStream** usando o valor do *parâmetro SampleMask.*

</dd> <dt>

**ViewInstancingCb(const D3D12 \_ VIEW \_ INSTANCING \_ DESC& ViewInstancingDesc)**
</dt> <dd>

Inicializa o membro **ViewInstancingDesc** de **PipelineStream** usando o valor do *parâmetro ViewInstancingDesc.*

</dd> <dt>

**CachedPSOCb(const D3D12 \_ CACHED \_ PIPELINE \_ STATE& CachedPSO)**
</dt> <dd>

Inicializa o membro **CachedPSO** de **PipelineStream** usando o valor do *parâmetro CachedPSO.*

</dd> <dt>

**ErrorBadInputParameter(UINT)**
</dt> <dd>

Não faz nada.

</dd> <dt>

**ErrorDuplicateSubobject(D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE)**
</dt> <dd>

Não faz nada.

</dd> <dt>

**ErrorUnknownSubobject(UINT)**
</dt> <dd>

Não faz nada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando passados como o segundo parâmetro para a função [**D3DX12ParsePipelineStream,**](d3dx12parsepipelinestream.md) os detalhes do objeto [**INTERNO CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md) são clonados do [**D3D12 \_ PIPELINE STATE STREAM \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passado como o primeiro parâmetro. Esse processo valida a descrição do fluxo de origem. Se D3DX12ParsePipelineStream retornar **S \_ OK,** a descrição do fluxo de origem e o **CD3DX12 \_ PIPELINE STATE \_ \_ STREAM1PipelineStream** resultantes serão válidos; caso contrário, ambos serão inválidos. Fluxos inválidos e outros erros são relatados somente por meio do valor de retorno de D3DX12ParsePipelineStream; essa estrutura implementa os retornos de chamada de erro para não fazer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





