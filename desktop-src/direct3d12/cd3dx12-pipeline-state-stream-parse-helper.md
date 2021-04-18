---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER (D3dx12. h)
description: Cria um \_ \_ \_ objeto de fluxo de estado de pipeline CD3DX12 interno a partir dos detalhes do subobjeto passados para as funções de membro correspondentes. Essa estrutura implementa a interface ID3DX12PipelineParserCallbacks.
ms.assetid: 7D4FFD1D-9FA3-4482-A67B-E742611030BC
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PARSE_HELPER
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
ms.openlocfilehash: 44cc6228f690abd677e1adc8552293e440452ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810695"
---
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a>\_Estrutura do \_ \_ auxiliar de análise do fluxo de estado do \_ pipeline do CD3DX12 \_

Cria um \_ \_ \_ objeto de fluxo de estado de pipeline CD3DX12 interno a partir dos detalhes do subobjeto passados para as funções de membro correspondentes. Essa estrutura implementa a interface [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .

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

O [**estado do \_ pipeline CD3DX12 interno \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md). Seu estado atual representa o efeito cumulativo dos métodos de retorno de chamada que foram chamados nesse objeto.

</dd> <dt>

**FlagsCb ( \_ sinalizadores de sinalizadores de estado do pipeline D3D12 \_ \_ )**
</dt> <dd>

Inicializa o membro **flags** de **PipelineStream** usando o valor do parâmetro *flags* .

</dd> <dt>

**NodeMaskCb (UINT NodeMask)**
</dt> <dd>

Inicializa o membro **NodeMask** de **PipelineStream** usando o valor do parâmetro *NodeMask* .

</dd> <dt>

**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**
</dt> <dd>

Inicializa o membro **pRootSignature** de **PipelineStream** usando o valor do parâmetro *pRootSignature* .

</dd> <dt>

**InputLayoutCb (const D3D12 \_ layout de entrada \_ \_ desc& InputLayout)**
</dt> <dd>

Inicializa o membro **InputLayout** de **PipelineStream** usando o valor do parâmetro *InputLayout* .

</dd> <dt>

**IBStripCutValueCb ( \_ valor de \_ recorte de faixa de buffer de índice D3D12 \_ \_ \_ IBStripCutValue)**
</dt> <dd>

Inicializa o membro **IBStripCutValue** de **PipelineStream** usando o valor do parâmetro *IBStripCutValue* .

</dd> <dt>

**PrimitiveTopologyTypeCb ( \_ tipo de \_ topologia primitivo D3D12 \_ PrimitiveTopologyType)**
</dt> <dd>

Inicializa o membro **PrimitiveTopologyType** de **PipelineStream** usando o valor do parâmetro *PrimitiveTopologyType* .

</dd> <dt>

**VSCb (const D3D12 do \_ sombreador de \_ bytes& vs)**
</dt> <dd>

Inicializa o membro **vs** (Vertex Shader) de **PipelineStream** usando o valor do parâmetro *vs* .

</dd> <dt>

**GSCb (const D3D12 \_ Shader \_ bytes& GS)**
</dt> <dd>

Inicializa o membro **GS** (Geometry Shader) de **PipelineStream** usando o valor do parâmetro *GS* .

</dd> <dt>

**StreamOutputCb (const D3D12 \_ Stream \_ OUTPUT \_ desc& StreamOutput)**
</dt> <dd>

Inicializa o membro **StreamOutput** de **PipelineStream** usando o valor do parâmetro *StreamOutput* .

</dd> <dt>

**HSCb (código de \_ bytes do sombreador const D3D12 \_& HS)**
</dt> <dd>

Inicializa o membro **HS** (envoltória Shader) de **PipelineStream** usando o valor do parâmetro *HS* .

</dd> <dt>

**DSCb (código de \_ bytes de sombreador const D3D12 \_& DS)**
</dt> <dd>

Inicializa o membro **DS** (sombreador de domínio) de **PipelineStream** usando o valor do parâmetro *DS* .

</dd> <dt>

**PSCb (const D3D12 \_ Shader \_ código de bytes& PS)**
</dt> <dd>

Inicializa o membro **PS** (Pixel Shader) de **PipelineStream** usando o valor do parâmetro *PS* .

</dd> <dt>

**CSCb (const D3D12 \_ Shader \_ código de bytes& cs)**
</dt> <dd>

Inicializa o membro **cs** de **PipelineStream** usando o valor do parâmetro *cs* .

</dd> <dt>

**BlendStateCb (const D3D12 \_ Blend \_ desc& blendstate)**
</dt> <dd>

Inicializa o membro **blendstate** de **PipelineStream** usando o valor do parâmetro *blendstate* .

</dd> <dt>

**DepthStencilStateCb (const D3D12 \_ Depth \_ estêncil \_ desc& DepthStencilState)**
</dt> <dd>

Inicializa o membro **DepthStencilState** de **PipelineStream** usando o valor do parâmetro *DepthStencilState* , um [**estêncil de \_ profundidade de D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).

</dd> <dt>

**DepthStencilState1Cb (const D3D12 \_ Depth \_ estêncil \_ DESC1& DepthStencilState)**
</dt> <dd>

Inicializa o membro **DepthStencilState** de **PipelineStream** usando o valor do parâmetro *DepthStencilState* , um [**estêncil de \_ profundidade \_ D3D12 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).

</dd> <dt>

**DSVFormatCb ( \_ DSVFormat de formato dxgi)**
</dt> <dd>

Inicializa o membro **DSVFormat** de **PipelineStream** usando o valor do parâmetro *DSVFormat* .

</dd> <dt>

**RasterizerStateCb (const D3D12 \_ rasterizador \_ desc& RasterizerState)**
</dt> <dd>

Inicializa o membro **RasterizerState** de **PipelineStream** usando o valor do parâmetro *RasterizerState* .

</dd> <dt>

**RTVFormatsCb (matriz de \_ formato const D3D12 RT \_ \_& RTVFormats)**
</dt> <dd>

Inicializa o membro **RTVFormats** de **PipelineStream** usando o valor do parâmetro *RTVFormats* .

</dd> <dt>

**SampleDescCb ( \_ exemplo desc de const \_& SampleDesc)**
</dt> <dd>

Inicializa o membro **SampleDesc** de **PipelineStream** usando o valor do parâmetro *SampleDesc* .

</dd> <dt>

**SampleMaskCb (UINT SampleMask)**
</dt> <dd>

Inicializa o membro **SampleMask** de **PipelineStream** usando o valor do parâmetro *SampleMask* .

</dd> <dt>

**ViewInstancingCb (const D3D12 \_ View \_ instanciação \_& ViewInstancingDesc)**
</dt> <dd>

Inicializa o membro **ViewInstancingDesc** de **PipelineStream** usando o valor do parâmetro *ViewInstancingDesc* .

</dd> <dt>

**CachedPSOCb (const D3D12 \_ estado de \_ pipeline em cache \_& CachedPSO)**
</dt> <dd>

Inicializa o membro **CachedPSO** de **PipelineStream** usando o valor do parâmetro *CachedPSO* .

</dd> <dt>

**ErrorBadInputParameter (UINT)**
</dt> <dd>

Não faz nada.

</dd> <dt>

**ErrorDuplicateSubobject ( \_ tipo de \_ subobjeto do estado do pipeline D3D12 \_ \_ )**
</dt> <dd>

Não faz nada.

</dd> <dt>

**ErrorUnknownSubobject (UINT)**
</dt> <dd>

Não faz nada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando passado como o segundo parâmetro para a função [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , os detalhes do objeto STREAM1 do [**\_ \_ estado do \_ pipeline CD3DX12**](cd3dx12-pipeline-state-stream1.md) interno são clonados do [**\_ fluxo de \_ estado \_ \_ do pipeline D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passado como o primeiro parâmetro. Esse processo valida a descrição do fluxo de origem. Se D3DX12ParsePipelineStream retornar **S \_ OK**, a descrição do fluxo de origem e o **estado de \_ pipeline CD3DX12 resultante \_ \_ STREAM1PipelineStream** serão válidos; caso contrário, ambos serão inválidos. Fluxos inválidos e outros erros são relatados somente por meio do valor de retorno de D3DX12ParsePipelineStream; Essa estrutura implementa os retornos de chamada de erro para não fazer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
</dt> <dt>

[**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





