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
# <a name="cd3dx12_pipeline_state_stream_parse_helper-structure"></a><span data-ttu-id="de9ca-105">\_Estrutura do \_ \_ auxiliar de análise do fluxo de estado do \_ pipeline do CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="de9ca-105">CD3DX12\_PIPELINE\_STATE\_STREAM\_PARSE\_HELPER structure</span></span>

<span data-ttu-id="de9ca-106">Cria um \_ \_ \_ objeto de fluxo de estado de pipeline CD3DX12 interno a partir dos detalhes do subobjeto passados para as funções de membro correspondentes.</span><span class="sxs-lookup"><span data-stu-id="de9ca-106">Builds an internal CD3DX12\_PIPELINE\_STATE\_STREAM object from subobject details passed into the corresponding member functions.</span></span> <span data-ttu-id="de9ca-107">Essa estrutura implementa a interface [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="de9ca-107">This struct implements the [**ID3DX12PipelineParserCallbacks**](id3dx12pipelineparsercallbacks.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9ca-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de9ca-108">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="de9ca-109">Membros</span><span class="sxs-lookup"><span data-stu-id="de9ca-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="de9ca-110">**PipelineStream**</span><span class="sxs-lookup"><span data-stu-id="de9ca-110">**PipelineStream**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-111">O [**estado do \_ pipeline CD3DX12 interno \_ \_ STREAM1**](cd3dx12-pipeline-state-stream1.md).</span><span class="sxs-lookup"><span data-stu-id="de9ca-111">The internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md).</span></span> <span data-ttu-id="de9ca-112">Seu estado atual representa o efeito cumulativo dos métodos de retorno de chamada que foram chamados nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="de9ca-112">Its current state represents the cumulative effect of callback methods that have been called on this object.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-113">**FlagsCb ( \_ sinalizadores de sinalizadores de estado do pipeline D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="de9ca-113">**FlagsCb(D3D12\_PIPELINE\_STATE\_FLAGS Flags)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-114">Inicializa o membro **flags** de **PipelineStream** usando o valor do parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-114">Initializes the **Flags** member of **PipelineStream** using the value of the *Flags* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-115">**NodeMaskCb (UINT NodeMask)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-115">**NodeMaskCb(UINT NodeMask)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-116">Inicializa o membro **NodeMask** de **PipelineStream** usando o valor do parâmetro *NodeMask* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-116">Initializes the **NodeMask** member of **PipelineStream** using the value of the *Nodemask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-117">**RootSignatureCb (ID3D12RootSignature \* pRootSignature)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-117">**RootSignatureCb(ID3D12RootSignature\* pRootSignature)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-118">Inicializa o membro **pRootSignature** de **PipelineStream** usando o valor do parâmetro *pRootSignature* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-118">Initializes the **pRootSignature** member of **PipelineStream** using the value of the *pRootSignature* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-119">**InputLayoutCb (const D3D12 \_ layout de entrada \_ \_ desc& InputLayout)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-119">**InputLayoutCb(const D3D12\_INPUT\_LAYOUT\_DESC& InputLayout)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-120">Inicializa o membro **InputLayout** de **PipelineStream** usando o valor do parâmetro *InputLayout* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-120">Initializes the **InputLayout** member of **PipelineStream** using the value of the *InputLayout* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-121">**IBStripCutValueCb ( \_ valor de \_ recorte de faixa de buffer de índice D3D12 \_ \_ \_ IBStripCutValue)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-121">**IBStripCutValueCb(D3D12\_INDEX\_BUFFER\_STRIP\_CUT\_VALUE IBStripCutValue)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-122">Inicializa o membro **IBStripCutValue** de **PipelineStream** usando o valor do parâmetro *IBStripCutValue* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-122">Initializes the **IBStripCutValue** member of **PipelineStream** using the value of the *IBStripCutValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-123">**PrimitiveTopologyTypeCb ( \_ tipo de \_ topologia primitivo D3D12 \_ PrimitiveTopologyType)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-123">**PrimitiveTopologyTypeCb(D3D12\_PRIMITIVE\_TOPOLOGY\_TYPE PrimitiveTopologyType)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-124">Inicializa o membro **PrimitiveTopologyType** de **PipelineStream** usando o valor do parâmetro *PrimitiveTopologyType* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-124">Initializes the **PrimitiveTopologyType** member of **PipelineStream** using the value of the *PrimitiveTopologyType* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-125">**VSCb (const D3D12 do \_ sombreador de \_ bytes& vs)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-125">**VSCb(const D3D12\_SHADER\_BYTECODE& VS)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-126">Inicializa o membro **vs** (Vertex Shader) de **PipelineStream** usando o valor do parâmetro *vs* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-126">Initializes the **VS** (vertex shader) member of **PipelineStream** using the value of the *VS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-127">**GSCb (const D3D12 \_ Shader \_ bytes& GS)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-127">**GSCb(const D3D12\_SHADER\_BYTECODE& GS)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-128">Inicializa o membro **GS** (Geometry Shader) de **PipelineStream** usando o valor do parâmetro *GS* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-128">Initializes the **GS** (geometry shader) member of **PipelineStream** using the value of the *GS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-129">**StreamOutputCb (const D3D12 \_ Stream \_ OUTPUT \_ desc& StreamOutput)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-129">**StreamOutputCb(const D3D12\_STREAM\_OUTPUT\_DESC& StreamOutput)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-130">Inicializa o membro **StreamOutput** de **PipelineStream** usando o valor do parâmetro *StreamOutput* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-130">Initializes the **StreamOutput** member of **PipelineStream** using the value of the *StreamOutput* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-131">**HSCb (código de \_ bytes do sombreador const D3D12 \_& HS)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-131">**HSCb(const D3D12\_SHADER\_BYTECODE& HS)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-132">Inicializa o membro **HS** (envoltória Shader) de **PipelineStream** usando o valor do parâmetro *HS* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-132">Initializes the **HS** (hull shader) member of **PipelineStream** using the value of the *HS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-133">**DSCb (código de \_ bytes de sombreador const D3D12 \_& DS)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-133">**DSCb(const D3D12\_SHADER\_BYTECODE& DS)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-134">Inicializa o membro **DS** (sombreador de domínio) de **PipelineStream** usando o valor do parâmetro *DS* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-134">Initializes the **DS** (domain shader) member of **PipelineStream** using the value of the *DS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-135">**PSCb (const D3D12 \_ Shader \_ código de bytes& PS)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-135">**PSCb(const D3D12\_SHADER\_BYTECODE& PS)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-136">Inicializa o membro **PS** (Pixel Shader) de **PipelineStream** usando o valor do parâmetro *PS* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-136">Initializes the **PS** (pixel shader) member of **PipelineStream** using the value of the *PS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-137">**CSCb (const D3D12 \_ Shader \_ código de bytes& cs)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-137">**CSCb(const D3D12\_SHADER\_BYTECODE& CS)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-138">Inicializa o membro **cs** de **PipelineStream** usando o valor do parâmetro *cs* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-138">Initializes the **CS** member of **PipelineStream** using the value of the *CS* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-139">**BlendStateCb (const D3D12 \_ Blend \_ desc& blendstate)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-139">**BlendStateCb(const D3D12\_BLEND\_DESC& BlendState)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-140">Inicializa o membro **blendstate** de **PipelineStream** usando o valor do parâmetro *blendstate* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-140">Initializes the **BlendState** member of **PipelineStream** using the value of the *BlendState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-141">**DepthStencilStateCb (const D3D12 \_ Depth \_ estêncil \_ desc& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-141">**DepthStencilStateCb(const D3D12\_DEPTH\_STENCIL\_DESC& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-142">Inicializa o membro **DepthStencilState** de **PipelineStream** usando o valor do parâmetro *DepthStencilState* , um [**estêncil de \_ profundidade de D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span><span class="sxs-lookup"><span data-stu-id="de9ca-142">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc).</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-143">**DepthStencilState1Cb (const D3D12 \_ Depth \_ estêncil \_ DESC1& DepthStencilState)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-143">**DepthStencilState1Cb(const D3D12\_DEPTH\_STENCIL\_DESC1& DepthStencilState)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-144">Inicializa o membro **DepthStencilState** de **PipelineStream** usando o valor do parâmetro *DepthStencilState* , um [**estêncil de \_ profundidade \_ D3D12 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span><span class="sxs-lookup"><span data-stu-id="de9ca-144">Initializes the **DepthStencilState** member of **PipelineStream** using the value of the *DepthStencilState* parameter, a [**D3D12\_DEPTH\_STENCIL\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1).</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-145">**DSVFormatCb ( \_ DSVFormat de formato dxgi)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-145">**DSVFormatCb(DXGI\_FORMAT DSVFormat)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-146">Inicializa o membro **DSVFormat** de **PipelineStream** usando o valor do parâmetro *DSVFormat* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-146">Initializes the **DSVFormat** member of **PipelineStream** using the value of the *DSVFormat* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-147">**RasterizerStateCb (const D3D12 \_ rasterizador \_ desc& RasterizerState)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-147">**RasterizerStateCb(const D3D12\_RASTERIZER\_DESC& RasterizerState)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-148">Inicializa o membro **RasterizerState** de **PipelineStream** usando o valor do parâmetro *RasterizerState* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-148">Initializes the **RasterizerState** member of **PipelineStream** using the value of the *RasterizerState* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-149">**RTVFormatsCb (matriz de \_ formato const D3D12 RT \_ \_& RTVFormats)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-149">**RTVFormatsCb(const D3D12\_RT\_FORMAT\_ARRAY& RTVFormats)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-150">Inicializa o membro **RTVFormats** de **PipelineStream** usando o valor do parâmetro *RTVFormats* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-150">Initializes the **RTVFormats** member of **PipelineStream** using the value of the *RTVFormats* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-151">**SampleDescCb ( \_ exemplo desc de const \_& SampleDesc)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-151">**SampleDescCb(const DXGI\_SAMPLE\_DESC& SampleDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-152">Inicializa o membro **SampleDesc** de **PipelineStream** usando o valor do parâmetro *SampleDesc* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-152">Initializes the **SampleDesc** member of **PipelineStream** using the value of the *SampleDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-153">**SampleMaskCb (UINT SampleMask)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-153">**SampleMaskCb(UINT SampleMask)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-154">Inicializa o membro **SampleMask** de **PipelineStream** usando o valor do parâmetro *SampleMask* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-154">Initializes the **SampleMask** member of **PipelineStream** using the value of the *SampleMask* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-155">**ViewInstancingCb (const D3D12 \_ View \_ instanciação \_& ViewInstancingDesc)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-155">**ViewInstancingCb(const D3D12\_VIEW\_INSTANCING\_DESC& ViewInstancingDesc)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-156">Inicializa o membro **ViewInstancingDesc** de **PipelineStream** usando o valor do parâmetro *ViewInstancingDesc* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-156">Initializes the **ViewInstancingDesc** member of **PipelineStream** using the value of the *ViewInstancingDesc* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-157">**CachedPSOCb (const D3D12 \_ estado de \_ pipeline em cache \_& CachedPSO)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-157">**CachedPSOCb(const D3D12\_CACHED\_PIPELINE\_STATE& CachedPSO)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-158">Inicializa o membro **CachedPSO** de **PipelineStream** usando o valor do parâmetro *CachedPSO* .</span><span class="sxs-lookup"><span data-stu-id="de9ca-158">Initializes the **CachedPSO** member of **PipelineStream** using the value of the *CachedPSO* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-159">**ErrorBadInputParameter (UINT)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-159">**ErrorBadInputParameter(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-160">Não faz nada.</span><span class="sxs-lookup"><span data-stu-id="de9ca-160">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-161">**ErrorDuplicateSubobject ( \_ tipo de \_ subobjeto do estado do pipeline D3D12 \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="de9ca-161">**ErrorDuplicateSubobject(D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-162">Não faz nada.</span><span class="sxs-lookup"><span data-stu-id="de9ca-162">Does nothing.</span></span>

</dd> <dt>

<span data-ttu-id="de9ca-163">**ErrorUnknownSubobject (UINT)**</span><span class="sxs-lookup"><span data-stu-id="de9ca-163">**ErrorUnknownSubobject(UINT)**</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-164">Não faz nada.</span><span class="sxs-lookup"><span data-stu-id="de9ca-164">Does nothing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de9ca-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="de9ca-165">Remarks</span></span>

<span data-ttu-id="de9ca-166">Quando passado como o segundo parâmetro para a função [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) , os detalhes do objeto STREAM1 do [**\_ \_ estado do \_ pipeline CD3DX12**](cd3dx12-pipeline-state-stream1.md) interno são clonados do [**\_ fluxo de \_ estado \_ \_ do pipeline D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passado como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de9ca-166">When passed as the second parameter to the [**D3DX12ParsePipelineStream**](d3dx12parsepipelinestream.md) function, the details of the internal [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](cd3dx12-pipeline-state-stream1.md) object are cloned from the [**D3D12\_PIPELINE\_STATE\_STREAM\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) passed as the first parameter.</span></span> <span data-ttu-id="de9ca-167">Esse processo valida a descrição do fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="de9ca-167">This process validates the source stream description.</span></span> <span data-ttu-id="de9ca-168">Se D3DX12ParsePipelineStream retornar **S \_ OK**, a descrição do fluxo de origem e o **estado de \_ pipeline CD3DX12 resultante \_ \_ STREAM1PipelineStream** serão válidos; caso contrário, ambos serão inválidos.</span><span class="sxs-lookup"><span data-stu-id="de9ca-168">If D3DX12ParsePipelineStream returns **S\_OK**, then both the source stream description and the resulting **CD3DX12\_PIPELINE\_STATE\_STREAM1PipelineStream** are valid; otherwise both are invalid.</span></span> <span data-ttu-id="de9ca-169">Fluxos inválidos e outros erros são relatados somente por meio do valor de retorno de D3DX12ParsePipelineStream; Essa estrutura implementa os retornos de chamada de erro para não fazer nada.</span><span class="sxs-lookup"><span data-stu-id="de9ca-169">Invalid streams and other errors are reported only through the return value of D3DX12ParsePipelineStream; this structure implements the error callbacks to do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9ca-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de9ca-170">Requirements</span></span>



| <span data-ttu-id="de9ca-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9ca-171">Requirement</span></span> | <span data-ttu-id="de9ca-172">Valor</span><span class="sxs-lookup"><span data-stu-id="de9ca-172">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="de9ca-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de9ca-173">Header</span></span><br/> | <dl> <span data-ttu-id="de9ca-174"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="de9ca-174"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9ca-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="de9ca-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9ca-176">Estruturas auxiliares para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="de9ca-176">Helper Structures for Direct3D 12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="de9ca-177">**ID3DX12PipelineParserCallbacks**</span><span class="sxs-lookup"><span data-stu-id="de9ca-177">**ID3DX12PipelineParserCallbacks**</span></span>](id3dx12pipelineparsercallbacks.md)
</dt> </dl>

 

 





