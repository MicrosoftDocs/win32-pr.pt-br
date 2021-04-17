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
# <a name="cd3dx12_pipeline_state_stream1-structure"></a><span data-ttu-id="77b04-106">\_ \_ Estrutura STREAM1 do estado do pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="77b04-106">CD3DX12\_PIPELINE\_STATE\_STREAM1 structure</span></span>

<span data-ttu-id="77b04-107">Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada.</span><span class="sxs-lookup"><span data-stu-id="77b04-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="77b04-108">Consulte [**D3D12 \_ gráficos \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ Compute \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="77b04-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="77b04-109">\_ \_ \_ O estado do pipeline do CD3DX12 STREAM1 dá suporte à atualização dos criadores de outono do Windows 10 com novos recursos, como exibir a instanciação.</span><span class="sxs-lookup"><span data-stu-id="77b04-109">CD3DX12\_PIPELINE\_STATE\_STREAM1 supports the Windows 10 Fall Creators Update with new features such as view instancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b04-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77b04-110">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="77b04-111">Membros</span><span class="sxs-lookup"><span data-stu-id="77b04-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="77b04-112">**CD3DX12 \_ \_ de estado \_ de pipeline STREAM1 ()**</span><span class="sxs-lookup"><span data-stu-id="77b04-112">**CD3DX12\_PIPELINE\_STATE\_STREAM1()**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-113">Cria uma instância nova e não inicializada de um STREAM1 de \_ estado de pipeline CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="77b04-113">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-114">**\_ \_ Estado de pipeline CD3DX12 \_ STREAM1 (const \_ D3D12 \_ Graphics \_ estado pipeline \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="77b04-114">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-115">Cria uma nova instância de um \_ estado de pipeline CD3DX12 \_ \_ STREAM1, inicializada com valores copiados de uma estrutura **\_ \_ \_ STREAM1 de estado de pipeline CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="77b04-115">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-116">**\_ \_ Estado de pipeline CD3DX12 \_ STREAM1 (const D3D12 \_ COMPUTE \_ pipeline \_ estado \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="77b04-116">**CD3DX12\_PIPELINE\_STATE\_STREAM1(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-117">Cria uma nova instância de um \_ estado de pipeline CD3DX12 \_ \_ STREAM1, inicializada com valores copiados de uma estrutura **\_ \_ \_ STREAM1 de estado de pipeline CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="77b04-117">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM1, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM1** structure.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-118">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="77b04-118">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-119">Retorna o conteúdo do \_ objeto STREAM1 do estado do pipeline CD3DX12 \_ \_ como um \_ estado de pipeline de gráficos D3D12 \_ \_ \_ estrutura desc por valor.</span><span class="sxs-lookup"><span data-stu-id="77b04-119">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="77b04-120">Observe que \_ o estado de pipeline de gráficos D3D12 \_ \_ \_ DESC não inclui o membro **cs** , portanto, esse valor é perdido na conversão.</span><span class="sxs-lookup"><span data-stu-id="77b04-120">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-121">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="77b04-121">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-122">Retorna o conteúdo do \_ objeto STREAM1 do estado do pipeline CD3DX12 \_ \_ como uma \_ estrutura desc de estado do pipeline de computação D3D12 \_ \_ \_ por valor.</span><span class="sxs-lookup"><span data-stu-id="77b04-122">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM1 object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="77b04-123">Observe que \_ \_ \_ o estado Desc do pipeline de computação D3D12 não \_ inclui os membros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **blendstate**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** , para que esses valores sejam perdidos na conversão.</span><span class="sxs-lookup"><span data-stu-id="77b04-123">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-124">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="77b04-124">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-125">Descreve os sinalizadores de estado do pipeline, que controlam recursos como "depuração de ferramenta".</span><span class="sxs-lookup"><span data-stu-id="77b04-125">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="77b04-126">**NodeMask**</span><span class="sxs-lookup"><span data-stu-id="77b04-126">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-127">Descreve a máscara de nó de estado do pipeline, que é usada para identificar os nós (adaptadores físicos do dispositivo) aos quais o PSO se aplica em cenários de vários adaptadores; cada bit na máscara corresponde a um único nó.</span><span class="sxs-lookup"><span data-stu-id="77b04-127">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="77b04-128">Para cenários de adaptador único, defina esse valor como 0.</span><span class="sxs-lookup"><span data-stu-id="77b04-128">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-129">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="77b04-129">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-130">Descreve a assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="77b04-130">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-131">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="77b04-131">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-132">Descreve o formato de buffer de entrada para o estágio de Assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="77b04-132">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="77b04-133">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="77b04-133">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-134">Descreve o valor de índice especial do buffer de entrada que indica uma recorte (descontinuidade) ao usar a topologia de faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="77b04-134">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-135">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="77b04-135">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-136">Descreve a topologia primitiva e sua ordem.</span><span class="sxs-lookup"><span data-stu-id="77b04-136">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-137">**VS**</span><span class="sxs-lookup"><span data-stu-id="77b04-137">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-138">Descreve o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="77b04-138">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-139">**GS**</span><span class="sxs-lookup"><span data-stu-id="77b04-139">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-140">Descreve o sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="77b04-140">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-141">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="77b04-141">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-142">Descreve o buffer de saída de streaming.</span><span class="sxs-lookup"><span data-stu-id="77b04-142">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-143">**HS**</span><span class="sxs-lookup"><span data-stu-id="77b04-143">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-144">Descreve o sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="77b04-144">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-145">**DS**</span><span class="sxs-lookup"><span data-stu-id="77b04-145">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-146">Descreve o sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="77b04-146">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-147">**PROFISSIONAIS**</span><span class="sxs-lookup"><span data-stu-id="77b04-147">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-148">Descreve o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="77b04-148">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-149">**CS**</span><span class="sxs-lookup"><span data-stu-id="77b04-149">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-150">Descreve o sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="77b04-150">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-151">**Blendstate**</span><span class="sxs-lookup"><span data-stu-id="77b04-151">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-152">Descreve o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="77b04-152">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-153">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="77b04-153">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-154">Descreve o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="77b04-154">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-155">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="77b04-155">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-156">Descreve o formato de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="77b04-156">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-157">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="77b04-157">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-158">Descreve o estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="77b04-158">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-159">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="77b04-159">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-160">Descreve os formatos de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="77b04-160">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-161">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="77b04-161">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-162">Descreve a contagem de amostras e a qualidade.</span><span class="sxs-lookup"><span data-stu-id="77b04-162">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-163">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="77b04-163">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-164">Descreve a máscara de exemplo usada com o estado de mistura.</span><span class="sxs-lookup"><span data-stu-id="77b04-164">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="77b04-165">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="77b04-165">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="77b04-166">Descreve um PSO armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="77b04-166">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77b04-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="77b04-167">Remarks</span></span>

<span data-ttu-id="77b04-168">[**CD3DX12 \_ O \_ \_ fluxo de estado do pipeline**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) dá suporte à atualização dos criadores de outono do Windows 10, mas não dá suporte a tipos de subobjetos adicionados à atualização de criadores de outono do Windows 10, como para a criação de instâncias de exibição.</span><span class="sxs-lookup"><span data-stu-id="77b04-168">[**CD3DX12\_PIPELINE\_STATE\_STREAM**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM**) supports the Windows 10 Fall Creators Update, but doesn't support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="77b04-169">Para dar suporte aos novos tipos de subobjetos, use CD3DX12 \_ pipeline \_ State \_ STREAM1 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="77b04-169">To support the new subobject types, use CD3DX12\_PIPELINE\_STATE\_STREAM1 instead.</span></span>

<span data-ttu-id="77b04-170">As variáveis de membro acessíveis dessa estrutura são todos os TYPEDEFs do \_ modelo de \_ subobjeto Stream do estado do pipeline CD3DX12 \_ \_ , que combina os dados do marcador de tipo de subobjeto e subobjeto em um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="77b04-170">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="77b04-171">Esses TYPEDEFs são:</span><span class="sxs-lookup"><span data-stu-id="77b04-171">Those typedefs are:</span></span>

<span data-ttu-id="77b04-172"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="77b04-172"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="77b04-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77b04-173">Requirements</span></span>



| <span data-ttu-id="77b04-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="77b04-174">Requirement</span></span> | <span data-ttu-id="77b04-175">Valor</span><span class="sxs-lookup"><span data-stu-id="77b04-175">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77b04-176">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77b04-176">Header</span></span><br/> | <dl> <span data-ttu-id="77b04-177"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="77b04-177"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77b04-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="77b04-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b04-179">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="77b04-179">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="77b04-180">**\_Fluxo de \_ estado do pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="77b04-180">**CD3DX12\_PIPELINE\_STATE\_STREAM**</span></span>](cd3dx12-pipeline-state-stream.md)
</dt> <dt>

[<span data-ttu-id="77b04-181">**Desc. de estado do pipeline de \_ gráficos D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77b04-181">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="77b04-182">**\_Desc de \_ estado do pipeline de computação D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77b04-182">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





