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
# <a name="cd3dx12_pipeline_state_stream-structure"></a><span data-ttu-id="4c4e7-106">\_Estrutura do \_ fluxo de estado do pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="4c4e7-106">CD3DX12\_PIPELINE\_STATE\_STREAM structure</span></span>

<span data-ttu-id="4c4e7-107">Uma estrutura auxiliar para criar e trabalhar com os Estados de pipeline de computação e elementos gráficos por meio de uma interface combinada.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-107">A helper structure for creating and working with graphics and compute pipeline states through a combined interface.</span></span> <span data-ttu-id="4c4e7-108">Consulte [**D3D12 \_ gráficos \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) e [**D3D12 \_ Compute \_ pipeline \_ State \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span><span class="sxs-lookup"><span data-stu-id="4c4e7-108">See [**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) and [**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc).</span></span>

<span data-ttu-id="4c4e7-109">\_ \_ O fluxo de estado do pipeline CD3DX12 \_ dá suporte à atualização do Windows 10 para criadores e mais recente, mas não dá suporte a novos recursos da atualização de criadores de outono, como exibir a instanciação.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-109">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer but doesn't support new features of the Fall Creators update, such as view instancing.</span></span> <span data-ttu-id="4c4e7-110">Para dar suporte a recursos da atualização de criadores de outono, use [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-110">To support features of the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4e7-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c4e7-111">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="4c4e7-112">Membros</span><span class="sxs-lookup"><span data-stu-id="4c4e7-112">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c4e7-113">**\_ \_ \_ Fluxo de estado do pipeline CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-113">**CD3DX12\_PIPELINE\_STATE\_STREAM()**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-114">Cria uma nova instância, não inicializada, de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4c4e7-114">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-115">**\_ \_ \_ Fluxo de estado do pipeline CD3DX12 (const D3D12 \_ GRAPHICS \_ \_ estado pipeline \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-115">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-116">Cria uma nova instância de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ , inicializada com valores copiados de uma estrutura de fluxo de **\_ estado de pipeline \_ \_ CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="4c4e7-116">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-117">**\_ \_ \_ Fluxo de estado do pipeline CD3DX12 (const D3D12 \_ estado do pipeline de computação \_ \_ \_ desc& DESC)**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-117">**CD3DX12\_PIPELINE\_STATE\_STREAM(const D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC& Desc)**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-118">Cria uma nova instância de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ , inicializada com valores copiados de uma estrutura de fluxo de **\_ estado de pipeline \_ \_ CD3DX12** .</span><span class="sxs-lookup"><span data-stu-id="4c4e7-118">Creates a new instance of a CD3DX12\_PIPELINE\_STATE\_STREAM, initialized with values copied from a **CD3DX12\_PIPELINE\_STATE\_STREAM** structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-119">**GraphicsDescV0()**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-119">**GraphicsDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-120">Retorna o conteúdo do objeto de \_ fluxo de estado do pipeline CD3DX12 \_ \_ como um estado de pipeline de gráficos do D3D12 \_ \_ \_ \_ estrutura desc por valor.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-120">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="4c4e7-121">Observe que \_ o estado de pipeline de gráficos D3D12 \_ \_ \_ DESC não inclui o membro **cs** , portanto, esse valor é perdido na conversão.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-121">Note that D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC does not include the **CS** member, so this value is lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-122">**ComputeDescV0()**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-122">**ComputeDescV0()**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-123">Retorna o conteúdo do objeto de \_ fluxo de estado do pipeline CD3DX12 \_ \_ como \_ uma \_ estrutura desc de estado do pipeline de computação D3D12 \_ \_ por valor.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-123">returns the contents of the CD3DX12\_PIPELINE\_STATE\_STREAM object as a D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC structure by value.</span></span> <span data-ttu-id="4c4e7-124">Observe que \_ \_ \_ o estado Desc do pipeline de computação D3D12 não \_ inclui os membros **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **vs**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **blendstate**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc** ou **SampleMask** , para que esses valores sejam perdidos na conversão.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-124">Note that D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC does not include the **InputLayout**, **IBStripCutValue**, **PrimitiveTopologyType**, **VS**, **GS**, **StreamOutput**, **HS**, **DS**, **PS**, **BlendState**, **DepthStencilState**, **DSVFormat**, **RasterizerState**, **NumRootSignature**, **RTVFormats**, **SampleDesc**, or **SampleMask** members, so these values are lost in the conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-125">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-125">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-126">Descreve os sinalizadores de estado do pipeline, que controlam recursos como "depuração de ferramenta".</span><span class="sxs-lookup"><span data-stu-id="4c4e7-126">Describes the pipeline state flags, which control features such as "tool debug".</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-127">**NodeMask**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-127">**NodeMask**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-128">Descreve a máscara de nó de estado do pipeline, que é usada para identificar os nós (adaptadores físicos do dispositivo) aos quais o PSO se aplica em cenários de vários adaptadores; cada bit na máscara corresponde a um único nó.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-128">Describes the pipeline state node mask, which is used to identify the nodes (physical adapters of the device) that the PSO applies to in Multi-Adapter scenarios; each bit in the mask corresponds to a single node.</span></span> <span data-ttu-id="4c4e7-129">Para cenários de adaptador único, defina esse valor como 0.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-129">For single-adapter scenarios, set this value to 0.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-130">**pRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-130">**pRootSignature**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-131">Descreve a assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-131">Describes the root signature.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-132">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-132">**InputLayout**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-133">Descreve o formato de buffer de entrada para o estágio de Assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="4c4e7-133">Describes the input-buffer format for the input-assembler stage</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-134">**IBStripCutValue**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-134">**IBStripCutValue**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-135">Descreve o valor de índice especial do buffer de entrada que indica uma recorte (descontinuidade) ao usar a topologia de faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-135">Describes the special index value of the input buffer that indicates a cut (discontinuity) when using triangle-strip topology.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-136">**PrimitiveTopologyType**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-136">**PrimitiveTopologyType**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-137">Descreve a topologia primitiva e sua ordem.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-137">Describes the primitive topology and its order.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-138">**VS**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-138">**VS**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-139">Descreve o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-139">Describes the vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-140">**GS**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-140">**GS**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-141">Descreve o sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-141">Describes the geometry shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-142">**StreamOutput**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-142">**StreamOutput**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-143">Descreve o buffer de saída de streaming.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-143">Describes the streaming output-buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-144">**HS**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-144">**HS**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-145">Descreve o sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-145">Describes the hull shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-146">**DS**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-146">**DS**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-147">Descreve o sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-147">Describes the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-148">**PROFISSIONAIS**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-148">**PS**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-149">Descreve o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-149">Describes the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-150">**CS**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-150">**CS**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-151">Descreve o sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-151">Describes the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-152">**Blendstate**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-152">**BlendState**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-153">Descreve o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-153">Describes the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-154">**DepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-154">**DepthStencilState**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-155">Descreve o estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-155">Describes the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-156">**DSVFormat**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-156">**DSVFormat**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-157">Descreve o formato de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-157">Describes the depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-158">**RasterizerState**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-158">**RasterizerState**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-159">Descreve o estado do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-159">Describes the rasterizer state.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-160">**RTVFormats**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-160">**RTVFormats**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-161">Descreve os formatos de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-161">Describes the render target formats.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-162">**SampleDesc**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-162">**SampleDesc**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-163">Descreve a contagem de amostras e a qualidade.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-163">Describes the sample count and quality.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-164">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-164">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-165">Descreve a máscara de exemplo usada com o estado de mistura.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-165">Describes the sample mask used with the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="4c4e7-166">**CachedPSO**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-166">**CachedPSO**</span></span>
</dt> <dd>

<span data-ttu-id="4c4e7-167">Descreve um PSO armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-167">Describes a cached PSO.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c4e7-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4e7-168">Remarks</span></span>

<span data-ttu-id="4c4e7-169">\_ \_ O fluxo de estado do pipeline CD3DX12 \_ dá suporte à atualização do Windows 10 para criadores e mais recente, mas não oferece suporte a tipos de subobjetos adicionados na atualização de criadores de outono do Windows 10, como para o modo de exibição de instanciação.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-169">CD3DX12\_PIPELINE\_STATE\_STREAM supports Windows 10 Creators Update and newer, but doesn not support subobject types added in Windows 10 Fall Creators update, such as for view instancing.</span></span> <span data-ttu-id="4c4e7-170">Para oferecer suporte a tipos de subobjetos adicionados na atualização de criadores de outono, use [**CD3DX12 \_ pipeline \_ State \_ STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-170">To support subobject types added in the Fall Creators update, use [**CD3DX12\_PIPELINE\_STATE\_STREAM1**](https://www.bing.com/search?q=**CD3DX12\_PIPELINE\_STATE\_STREAM1**) instead.</span></span>

<span data-ttu-id="4c4e7-171">As variáveis de membro acessíveis dessa estrutura são todos os TYPEDEFs do \_ modelo de \_ subobjeto Stream do estado do pipeline CD3DX12 \_ \_ , que combina os dados do marcador de tipo de subobjeto e subobjeto em um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4c4e7-171">The accessible member variables of this structure are all typedefs of the CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template, which combines the subobject type-marker and subobject data into a single object suitable for a stream description.</span></span>

<span data-ttu-id="4c4e7-172">Esses TYPEDEFs são:</span><span class="sxs-lookup"><span data-stu-id="4c4e7-172">Those typedefs are:</span></span>

<span data-ttu-id="4c4e7-173"><dl> </dl></span><span class="sxs-lookup"><span data-stu-id="4c4e7-173"><dl> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4c4e7-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c4e7-174">Requirements</span></span>



| <span data-ttu-id="4c4e7-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4e7-175">Requirement</span></span> | <span data-ttu-id="4c4e7-176">Valor</span><span class="sxs-lookup"><span data-stu-id="4c4e7-176">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4e7-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c4e7-177">Header</span></span><br/> | <dl> <span data-ttu-id="4c4e7-178"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c4e7-178"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c4e7-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c4e7-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4e7-180">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="4c4e7-180">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="4c4e7-181">**CD3DX12 \_ de \_ estado de pipeline \_ STREAM1**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-181">**CD3DX12\_PIPELINE\_STATE\_STREAM1**</span></span>](cd3dx12-pipeline-state-stream1.md)
</dt> <dt>

[<span data-ttu-id="4c4e7-182">**Desc. de estado do pipeline de \_ gráficos D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-182">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
</dt> <dt>

[<span data-ttu-id="4c4e7-183">**\_Desc de \_ estado do pipeline de computação D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c4e7-183">**D3D12\_COMPUTE\_PIPELINE\_STATE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
</dt> </dl>

 

 





