---
title: Remoção indireta de desenho e GPU
description: O exemplo D3D12ExecuteIndirect demonstra como usar comandos indiretos para desenhar conteúdo. Ele também demonstra como esses comandos podem ser manipulados na GPU em um sombreador de computação antes de serem emitidos.
ms.assetid: 09F90837-D6BF-498E-8018-5C28EDD9BDC3
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b016170fbd3b675d5d5a20c1de87f24b04d4804
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548219"
---
# <a name="indirect-drawing-and-gpu-culling"></a><span data-ttu-id="4611e-104">Remoção indireta de desenho e GPU</span><span class="sxs-lookup"><span data-stu-id="4611e-104">Indirect drawing and GPU culling</span></span>

<span data-ttu-id="4611e-105">O exemplo D3D12ExecuteIndirect demonstra como usar comandos indiretos para desenhar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4611e-105">The D3D12ExecuteIndirect sample demonstrates how to use indirect commands to draw content.</span></span> <span data-ttu-id="4611e-106">Ele também demonstra como esses comandos podem ser manipulados na GPU em um sombreador de computação antes de serem emitidos.</span><span class="sxs-lookup"><span data-stu-id="4611e-106">It also demonstrates how these commands can be manipulated on the GPU in a compute shader before they are issued.</span></span>

-   [<span data-ttu-id="4611e-107">Definir os comandos indiretos</span><span class="sxs-lookup"><span data-stu-id="4611e-107">Define the indirect commands</span></span>](#define-the-indirect-commands)
-   [<span data-ttu-id="4611e-108">Criar um gráfico e uma assinatura de raiz de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-108">Create a graphics and compute root signature</span></span>](#create-a-graphics-and-compute-root-signature)
-   [<span data-ttu-id="4611e-109">Criar um modo de exibição de recurso de sombreador (SRV) para o sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-109">Create a shader resource view (SRV) for the compute shader</span></span>](#create-a-shader-resource-view-srv-for-the-compute-shader)
-   [<span data-ttu-id="4611e-110">Criar os buffers de comando indiretos</span><span class="sxs-lookup"><span data-stu-id="4611e-110">Create the indirect command buffers</span></span>](#create-the-indirect-command-buffers)
-   [<span data-ttu-id="4611e-111">Criar o UAVs de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-111">Create the compute UAVs</span></span>](#create-the-compute-uavs)
-   [<span data-ttu-id="4611e-112">Desenhando o quadro</span><span class="sxs-lookup"><span data-stu-id="4611e-112">Drawing the frame</span></span>](#drawing-the-frame)
-   [<span data-ttu-id="4611e-113">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="4611e-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="4611e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4611e-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="4611e-115">O exemplo cria um buffer de comando que descreve as chamadas de desenho 1024.</span><span class="sxs-lookup"><span data-stu-id="4611e-115">The sample creates a command buffer that describes 1024 draw calls.</span></span> <span data-ttu-id="4611e-116">Cada chamada de desenho renderiza um triângulo com uma cor, posição e velocidade aleatórias.</span><span class="sxs-lookup"><span data-stu-id="4611e-116">Each draw call renders a triangle with a random color, position, and velocity.</span></span> <span data-ttu-id="4611e-117">Os triângulos animam-se de na tela.</span><span class="sxs-lookup"><span data-stu-id="4611e-117">The triangles animate endlessly across the screen.</span></span> <span data-ttu-id="4611e-118">Há dois modos neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="4611e-118">There are two modes in this sample.</span></span> <span data-ttu-id="4611e-119">No primeiro modo, um sombreador de computação inspeciona os comandos indiretos e decide se deve ou não adicionar esse comando a um modo de exibição de acesso não ordenado (UAV) que descreve quais comandos devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="4611e-119">In the first mode, a compute shader inspects the indirect commands and decides whether or not to add that command to an unordered access view (UAV) describing which commands that should be executed.</span></span> <span data-ttu-id="4611e-120">No segundo modo, todos os comandos são simplesmente executados.</span><span class="sxs-lookup"><span data-stu-id="4611e-120">In the second mode, all commands are simply executed.</span></span> <span data-ttu-id="4611e-121">Pressionar a barra de espaços alternará entre os modos.</span><span class="sxs-lookup"><span data-stu-id="4611e-121">Pressing the spacebar will toggle between modes.</span></span>

## <a name="define-the-indirect-commands"></a><span data-ttu-id="4611e-122">Definir os comandos indiretos</span><span class="sxs-lookup"><span data-stu-id="4611e-122">Define the indirect commands</span></span>

<span data-ttu-id="4611e-123">Começamos definindo como devem ser os comandos indiretos.</span><span class="sxs-lookup"><span data-stu-id="4611e-123">We start out by defining what the indirect commands should look like.</span></span> <span data-ttu-id="4611e-124">Neste exemplo, os comandos que desejamos executar são:</span><span class="sxs-lookup"><span data-stu-id="4611e-124">In this sample the commands we want to execute are to:</span></span>

<dl> 1. <span data-ttu-id="4611e-125">Atualize a exibição de buffer constante (CBV).</span><span class="sxs-lookup"><span data-stu-id="4611e-125">Update the constant buffer view (CBV).</span></span>  
2. <span data-ttu-id="4611e-126">Desenhe o triângulo.</span><span class="sxs-lookup"><span data-stu-id="4611e-126">Draw the triangle.</span></span>  
</dl>

<span data-ttu-id="4611e-127">Esses comandos de desenho são representados pela seguinte estrutura na definição de classe **D3D12ExecuteIndirect** .</span><span class="sxs-lookup"><span data-stu-id="4611e-127">These drawing commands are represented by the following structure in the **D3D12ExecuteIndirect** class definition.</span></span> <span data-ttu-id="4611e-128">Os comandos são executados sequencialmente na ordem em que são definidos nesta estrutura.</span><span class="sxs-lookup"><span data-stu-id="4611e-128">Commands are executed sequentially in the order they are defined in this structure.</span></span>

``` syntax
  
// Data structure to match the command signature used for ExecuteIndirect.
struct IndirectCommand
{
       D3D12_GPU_VIRTUAL_ADDRESS cbv;
       D3D12_DRAW_ARGUMENTS drawArguments;
};
```



| <span data-ttu-id="4611e-129">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-129">Call flow</span></span>                                              | <span data-ttu-id="4611e-130">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-130">Parameters</span></span> |
|--------------------------------------------------------|------------|
| <span data-ttu-id="4611e-131">\_Endereço virtual de GPU D3D12 \_ \_ (simplesmente um UINT64)</span><span class="sxs-lookup"><span data-stu-id="4611e-131">D3D12\_GPU\_VIRTUAL\_ADDRESS (simply a UINT64)</span></span>         |            |
| [<span data-ttu-id="4611e-132">**\_Argumentos de desenho D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-132">**D3D12\_DRAW\_ARGUMENTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments) |            |



 

<span data-ttu-id="4611e-133">Para acompanhar a estrutura de dados, uma assinatura de comando também é criada, o que instrui a GPU como interpretar os dados passados para a API [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .</span><span class="sxs-lookup"><span data-stu-id="4611e-133">To accompany the data structure, a command signature is also created which instructs the GPU how to interpret the data passed in to the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span> <span data-ttu-id="4611e-134">Isso, e a maior parte do código a seguir, é adicionado ao método **Loadassets** .</span><span class="sxs-lookup"><span data-stu-id="4611e-134">This, and the most of the following code, is added to the **LoadAssets** method.</span></span>

``` syntax
// Create the command signature used for indirect drawing.
{
       // Each command consists of a CBV update and a DrawInstanced call.
       D3D12_INDIRECT_ARGUMENT_DESC argumentDescs[2] = {};
       argumentDescs[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT_BUFFER_VIEW;
       argumentDescs[0].ConstantBufferView.RootParameterIndex = Cbv;
       argumentDescs[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

       D3D12_COMMAND_SIGNATURE_DESC commandSignatureDesc = {};
       commandSignatureDesc.pArgumentDescs = argumentDescs;
       commandSignatureDesc.NumArgumentDescs = _countof(argumentDescs);
       commandSignatureDesc.ByteStride = sizeof(IndirectCommand);

       ThrowIfFailed(m_device->CreateCommandSignature(&commandSignatureDesc, m_rootSignature.Get(), IID_PPV_ARGS(&m_commandSignature)));
}
```



| <span data-ttu-id="4611e-135">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-135">Call flow</span></span>                                                               | <span data-ttu-id="4611e-136">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-136">Parameters</span></span>                                                              |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="4611e-137">**\_Argumento indireto D3D12 \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="4611e-137">**D3D12\_INDIRECT\_ARGUMENT\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) | [<span data-ttu-id="4611e-138">**\_Tipo de \_ argumento INdireto D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-138">**D3D12\_INDIRECT\_ARGUMENT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type) |
| [<span data-ttu-id="4611e-139">**\_Desc de \_ assinatura de comando D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-139">**D3D12\_COMMAND\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc) |                                                                         |
| [<span data-ttu-id="4611e-140">**CreateCommandSignature**</span><span class="sxs-lookup"><span data-stu-id="4611e-140">**CreateCommandSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)   |                                                                         |



 

## <a name="create-a-graphics-and-compute-root-signature"></a><span data-ttu-id="4611e-141">Criar um gráfico e uma assinatura de raiz de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-141">Create a graphics and compute root signature</span></span>

<span data-ttu-id="4611e-142">Também criamos elementos gráficos e uma assinatura de raiz de computação.</span><span class="sxs-lookup"><span data-stu-id="4611e-142">We also create both a graphics and a compute root signature.</span></span> <span data-ttu-id="4611e-143">A assinatura raiz de gráficos apenas define um CBV raiz.</span><span class="sxs-lookup"><span data-stu-id="4611e-143">The graphics root signature just defines a root CBV.</span></span> <span data-ttu-id="4611e-144">Observe que mapeamos o índice desse parâmetro raiz no [**\_ argumento indireto D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (mostrado acima) quando a assinatura de comando é definida.</span><span class="sxs-lookup"><span data-stu-id="4611e-144">Note that we map the index of this root parameter in the [**D3D12\_INDIRECT\_ARGUMENT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc) (shown above) when the command signature is defined.</span></span> <span data-ttu-id="4611e-145">A assinatura raiz de computação define:</span><span class="sxs-lookup"><span data-stu-id="4611e-145">The compute root signature defines:</span></span>

-   <span data-ttu-id="4611e-146">Uma tabela de descritor comum com três slots (dois SRV e um UAV):</span><span class="sxs-lookup"><span data-stu-id="4611e-146">A common descriptor table with three slots (two SRV’s and one UAV):</span></span>
    -   <span data-ttu-id="4611e-147">Um SRV expõe os buffers de constantes para o sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-147">One SRV exposes the constant buffers to the compute shader</span></span>
    -   <span data-ttu-id="4611e-148">Um SRV expõe o buffer de comando para o sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-148">One SRV exposes the command buffer to the compute shader</span></span>
    -   <span data-ttu-id="4611e-149">O UAV é onde o sombreador de computação salva os comandos para os triângulos visíveis</span><span class="sxs-lookup"><span data-stu-id="4611e-149">The UAV is where the compute shader saves the commands for the visible triangles</span></span>
-   <span data-ttu-id="4611e-150">Quatro constantes raiz:</span><span class="sxs-lookup"><span data-stu-id="4611e-150">Four root constants:</span></span>
    -   <span data-ttu-id="4611e-151">Metade da largura de um lado do triângulo</span><span class="sxs-lookup"><span data-stu-id="4611e-151">Half the width of one side of the triangle</span></span>
    -   <span data-ttu-id="4611e-152">A posição z dos vértices do triângulo</span><span class="sxs-lookup"><span data-stu-id="4611e-152">The z position of the triangle vertices</span></span>
    -   <span data-ttu-id="4611e-153">O deslocamento +/-x do plano de remoção no espaço homogêneo \[ -1, 1\]</span><span class="sxs-lookup"><span data-stu-id="4611e-153">The +/- x offset of the culling plane in homogenous space \[-1,1\]</span></span>
    -   <span data-ttu-id="4611e-154">O número de comandos indiretos no buffer de comando</span><span class="sxs-lookup"><span data-stu-id="4611e-154">The number of indirect commands in the command buffer</span></span>

``` syntax
// Create the root signatures.
{
       CD3DX12_ROOT_PARAMETER rootParameters[GraphicsRootParametersCount];
       rootParameters[Cbv].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_VERTEX);

       CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
       rootSignatureDesc.Init(_countof(rootParameters), rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

       ComPtr<ID3DBlob> signature;
       ComPtr<ID3DBlob> error;
       ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

       // Create compute signature.
       CD3DX12_DESCRIPTOR_RANGE ranges[2];
       ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 2, 0);
       ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

       CD3DX12_ROOT_PARAMETER computeRootParameters[ComputeRootParametersCount];
       computeRootParameters[SrvUavTable].InitAsDescriptorTable(2, ranges);
       computeRootParameters[RootConstants].InitAsConstants(4, 0);

       CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc;
       computeRootSignatureDesc.Init(_countof(computeRootParameters), computeRootParameters);

       ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
       ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
}
```



| <span data-ttu-id="4611e-155">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-155">Call flow</span></span>                                                             | <span data-ttu-id="4611e-156">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-156">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="4611e-157">**\_Parâmetro raiz \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="4611e-157">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="4611e-158">**\_Visibilidade do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-158">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="4611e-159">**Desc. de \_ assinatura raiz CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-159">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="4611e-160">**\_Sinalizadores de \_ assinatura \_ raiz D3D12**</span><span class="sxs-lookup"><span data-stu-id="4611e-160">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="4611e-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4611e-161">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="4611e-162">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4611e-162">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="4611e-163">**\_Versão da \_ assinatura \_ raiz do D3D**</span><span class="sxs-lookup"><span data-stu-id="4611e-163">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="4611e-164">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4611e-164">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="4611e-165">**\_Intervalo do descritor de CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-165">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="4611e-166">**\_Tipo de intervalo do descritor D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-166">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="4611e-167">**\_Parâmetro raiz \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="4611e-167">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="4611e-168">**\_Visibilidade do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-168">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="4611e-169">**Desc. de \_ assinatura raiz CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4611e-169">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="4611e-170">**\_Sinalizadores de \_ assinatura \_ raiz D3D12**</span><span class="sxs-lookup"><span data-stu-id="4611e-170">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="4611e-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4611e-171">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="4611e-172">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4611e-172">**D3D12SerializeRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="4611e-173">**\_Versão da \_ assinatura \_ raiz do D3D**</span><span class="sxs-lookup"><span data-stu-id="4611e-173">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="4611e-174">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="4611e-174">**CreateRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-a-shader-resource-view-srv-for-the-compute-shader"></a><span data-ttu-id="4611e-175">Criar um modo de exibição de recurso de sombreador (SRV) para o sombreador de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-175">Create a shader resource view (SRV) for the compute shader</span></span>

<span data-ttu-id="4611e-176">Depois de criar os objetos de estado do pipeline, os buffers de vértice, um estêncil de profundidade e os buffers de constantes, o exemplo cria um modo de exibição de recurso de sombreador (SRV) do buffer de constante para que o sombreador de computação possa acessar os dados no buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="4611e-176">After creating the pipeline state objects, vertex buffers, a depth stencil, and the constant buffers, the sample then creates a shader resource view (SRV) of the constant buffer so that the compute shader can access the data in the constant buffer.</span></span>

``` syntax
// Create shader resource views (SRV) of the constant buffers for the
// compute shader to read from.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(ConstantBufferData);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE cbvSrvHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CbvSrvOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_constantBuffer.Get(), &srvDesc, cbvSrvHandle);
              cbvSrvHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4611e-177">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-177">Call flow</span></span></th>
<th><span data-ttu-id="4611e-178">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-178">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4611e-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-179"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="4611e-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-180"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="4611e-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-181">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="4611e-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="4611e-182">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-183"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="4611e-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-184"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-185"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-indirect-command-buffers"></a><span data-ttu-id="4611e-186">Criar os buffers de comando indiretos</span><span class="sxs-lookup"><span data-stu-id="4611e-186">Create the indirect command buffers</span></span>

<span data-ttu-id="4611e-187">Em seguida, criamos os buffers de comando indiretos e definimos seu conteúdo usando o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="4611e-187">We then create the indirect command buffers and define their content using the following code.</span></span> <span data-ttu-id="4611e-188">Nós desenhamos os mesmos vértices de triângulo 1024 vezes, mas apontam para um local de buffer de constantes diferente com cada chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="4611e-188">We draw the same triangle vertices 1024 times, but point to a different constant buffer location with each draw call.</span></span>

``` syntax
       D3D12_GPU_VIRTUAL_ADDRESS gpuAddress = m_constantBuffer->GetGPUVirtualAddress();
       UINT commandIndex = 0;

       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              for (UINT n = 0; n < TriangleCount; n++)
              {
                    commands[commandIndex].cbv = gpuAddress;
                    commands[commandIndex].drawArguments.VertexCountPerInstance = 3;
                    commands[commandIndex].drawArguments.InstanceCount = 1;
                    commands[commandIndex].drawArguments.StartVertexLocation = 0;
                    commands[commandIndex].drawArguments.StartInstanceLocation = 0;

                    commandIndex++;
                    gpuAddress += sizeof(ConstantBufferData);
              }
       }
```



| <span data-ttu-id="4611e-189">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-189">Call flow</span></span>                    | <span data-ttu-id="4611e-190">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-190">Parameters</span></span>                                                          |
|------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="4611e-191">\_ \_ Endereço virtual da GPU D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="4611e-191">D3D12\_GPU\_VIRTUAL\_ADDRESS</span></span> | [<span data-ttu-id="4611e-192">**GetGPUVirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="4611e-192">**GetGPUVirtualAddress**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress) |



 

<span data-ttu-id="4611e-193">Depois de carregar os buffers de comando para a GPU, também criamos um SRV deles para que o sombreador de computação seja lido.</span><span class="sxs-lookup"><span data-stu-id="4611e-193">After uploading the command buffers to the GPU, we also create an SRV of them for the compute shader to read from.</span></span> <span data-ttu-id="4611e-194">Isso é muito semelhante ao SRV criado do buffer de constantes.</span><span class="sxs-lookup"><span data-stu-id="4611e-194">This is very similar to the SRV created of the constant buffer.</span></span>

``` syntax
// Create SRVs for the command buffers.
       D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
       srvDesc.Format = DXGI_FORMAT_UNKNOWN;
       srvDesc.ViewDimension = D3D12_SRV_DIMENSION_BUFFER;
       srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
       srvDesc.Buffer.NumElements = TriangleCount;
       srvDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       srvDesc.Buffer.Flags = D3D12_BUFFER_SRV_FLAG_NONE;

       CD3DX12_CPU_DESCRIPTOR_HANDLE commandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), CommandsOffset, m_cbvSrvUavDescriptorSize);
       for (UINT frame = 0; frame < FrameCount; frame++)
       {
              srvDesc.Buffer.FirstElement = frame * TriangleCount;
              m_device->CreateShaderResourceView(m_commandBuffer.Get(), &srvDesc, commandsHandle);
              commandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
       }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4611e-195">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-195">Call flow</span></span></th>
<th><span data-ttu-id="4611e-196">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-196">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4611e-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-197"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc"><strong>D3D12_SHADER_RESOURCE_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="4611e-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-198"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="4611e-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-199">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_srv_dimension"><strong>D3D12_SRV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="4611e-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span><span class="sxs-lookup"><span data-stu-id="4611e-200">
<a href="constants.md">D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING</a></span></span><br /><span data-ttu-id="4611e-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-201">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_srv_flags"><strong>D3D12_BUFFER_SRV_FLAG</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-202"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="4611e-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-203"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-204"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview"><strong>CreateShaderResourceView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="create-the-compute-uavs"></a><span data-ttu-id="4611e-205">Criar o UAVs de computação</span><span class="sxs-lookup"><span data-stu-id="4611e-205">Create the compute UAVs</span></span>

<span data-ttu-id="4611e-206">Precisamos criar o UAVs que armazenará os resultados do trabalho de computação.</span><span class="sxs-lookup"><span data-stu-id="4611e-206">We need to create the UAVs that will store the results of the compute work.</span></span> <span data-ttu-id="4611e-207">Quando um triângulo é considerado pelo sombreador de computação ser visível para o destino de renderização, ele será anexado a esse UAV e, em seguida, consumido pela API [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .</span><span class="sxs-lookup"><span data-stu-id="4611e-207">When a triangle is deemed by the compute shader to be visible to the render target, it will be appended to this UAV and then consumed by the [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) API.</span></span>

``` syntax
CD3DX12_CPU_DESCRIPTOR_HANDLE processedCommandsHandle(m_cbvSrvUavHeap->GetCPUDescriptorHandleForHeapStart(), ProcessedCommandsOffset, m_cbvSrvUavDescriptorSize);
for (UINT frame = 0; frame < FrameCount; frame++)
{
       // Allocate a buffer large enough to hold all of the indirect commands
       // for a single frame as well as a UAV counter.
       commandBufferDesc = CD3DX12_RESOURCE_DESC::Buffer(CommandBufferSizePerFrame + sizeof(UINT), D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS);
       CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_DEFAULT);
       ThrowIfFailed(m_device->CreateCommittedResource(
             &heapProps,
             D3D12_HEAP_FLAG_NONE,
             &commandBufferDesc,
             D3D12_RESOURCE_STATE_COPY_DEST,
             nullptr,
             IID_PPV_ARGS(&m_processedCommandBuffers[frame])));

       D3D12_UNORDERED_ACCESS_VIEW_DESC uavDesc = {};
       uavDesc.Format = DXGI_FORMAT_UNKNOWN;
       uavDesc.ViewDimension = D3D12_UAV_DIMENSION_BUFFER;
       uavDesc.Buffer.FirstElement = 0;
       uavDesc.Buffer.NumElements = TriangleCount;
       uavDesc.Buffer.StructureByteStride = sizeof(IndirectCommand);
       uavDesc.Buffer.CounterOffsetInBytes = CommandBufferSizePerFrame;
       uavDesc.Buffer.Flags = D3D12_BUFFER_UAV_FLAG_NONE;

       m_device->CreateUnorderedAccessView(
             m_processedCommandBuffers[frame].Get(),
             m_processedCommandBuffers[frame].Get(),
             &uavDesc,
             processedCommandsHandle);

       processedCommandsHandle.Offset(CbvSrvUavDescriptorCountPerFrame, m_cbvSrvUavDescriptorSize);
}
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4611e-208">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-208">Call flow</span></span></th>
<th><span data-ttu-id="4611e-209">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-209">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4611e-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-210"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="4611e-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-211"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-212"><a href="cd3dx12-resource-desc.md"><strong>CD3DX12_RESOURCE_DESC</strong></a></span></span></td>
<td><span data-ttu-id="4611e-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-213"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags"><strong>D3D12_RESOURCE_FLAGS</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-214"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource"><strong>CreateCommittedResource</strong></a></span></span></td>
<td><dl><span data-ttu-id="4611e-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-215"><a href="cd3dx12-heap-properties.md"><strong>CD3DX12_HEAP_PROPERTIES</strong></a></span></span><br /><span data-ttu-id="4611e-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-216">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type"><strong>D3D12_HEAP_TYPE</strong></a></span></span><br /><span data-ttu-id="4611e-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-217">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags"><strong>D3D12_HEAP_FLAG</strong></a></span></span><br /><span data-ttu-id="4611e-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-218">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-219"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc"><strong>D3D12_UNORDERED_ACCESS_VIEW_DESC</strong></a></span></span></td>
<td><dl><span data-ttu-id="4611e-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-220"><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format"><strong>DXGI_FORMAT</strong></a></span></span><br /><span data-ttu-id="4611e-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-221">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_uav_dimension"><strong>D3D12_UAV_DIMENSION</strong></a></span></span><br /><span data-ttu-id="4611e-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-222">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags"><strong>D3D12_BUFFER_UAV_FLAGS</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-223"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview"><strong>CreateUnorderedAccessView</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

## <a name="drawing-the-frame"></a><span data-ttu-id="4611e-224">Desenhando o quadro</span><span class="sxs-lookup"><span data-stu-id="4611e-224">Drawing the frame</span></span>

<span data-ttu-id="4611e-225">Quando chegar a hora de desenhar o quadro, se estivermos no modo em que o sombreador de computação está sendo invocado e os comandos indiretos estiverem sendo processados pela GPU, primeiro [**expedirei**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) esse trabalho para preencher nosso buffer de comando para [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect).</span><span class="sxs-lookup"><span data-stu-id="4611e-225">When it comes time to draw the frame, if we are in the mode when the compute shader is being invoked and indirect commands are being processed by the GPU, we will first [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch) that work to populate our command buffer for [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect).</span></span> <span data-ttu-id="4611e-226">Os trechos de código a seguir são adicionados ao método **PopulateCommandLists** .</span><span class="sxs-lookup"><span data-stu-id="4611e-226">The following code snippets are added to the **PopulateCommandLists** method.</span></span>

``` syntax
// Record the compute commands that will cull triangles and prevent them from being processed by the vertex shader.
if (m_enableCulling)
{
       UINT frameDescriptorOffset = m_frameIndex * CbvSrvUavDescriptorCountPerFrame;
       D3D12_GPU_DESCRIPTOR_HANDLE cbvSrvUavHandle = m_cbvSrvUavHeap->GetGPUDescriptorHandleForHeapStart();

       m_computeCommandList->SetComputeRootSignature(m_computeRootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_computeCommandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_computeCommandList->SetComputeRootDescriptorTable(
              SrvUavTable,
              CD3DX12_GPU_DESCRIPTOR_HANDLE(cbvSrvUavHandle, CbvSrvOffset + frameDescriptorOffset, m_cbvSrvUavDescriptorSize));

       m_computeCommandList->SetComputeRoot32BitConstants(RootConstants, 4, reinterpret_cast<void*>(&m_csRootConstants), 0);

       // Reset the UAV counter for this frame.
       m_computeCommandList->CopyBufferRegion(m_processedCommandBuffers[m_frameIndex].Get(), CommandBufferSizePerFrame, m_processedCommandBufferCounterReset.Get(), 0, sizeof(UINT));

       D3D12_RESOURCE_BARRIER barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_processedCommandBuffers[m_frameIndex].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_UNORDERED_ACCESS);
       m_computeCommandList->ResourceBarrier(1, &barrier);

       m_computeCommandList->Dispatch(static_cast<UINT>(ceil(TriangleCount / float(ComputeThreadBlockSize))), 1, 1);
}

ThrowIfFailed(m_computeCommandList->Close());
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4611e-227">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-227">Call flow</span></span></th>
<th><span data-ttu-id="4611e-228">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-228">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4611e-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-229"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle"><strong>D3D12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="4611e-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-230"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart"><strong>GetGPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-231"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature"><strong>SetComputeRootSignature</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-232"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-233"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-234"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable"><strong>SetComputeRootDescriptorTable</strong></a></span></span></td>
<td><span data-ttu-id="4611e-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-235"><a href="cd3dx12-gpu-descriptor-handle.md"><strong>CD3DX12_GPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-236"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants"><strong>SetComputeRoot32BitConstants</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-237"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion"><strong>CopyBufferRegion</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-238"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="4611e-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-239"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="4611e-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-240">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-241"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-242"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch"><strong>Dispatch</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Fechar</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-243"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="4611e-244">Em seguida, executaremos os comandos no UAV (seleção de GPU habilitada) ou no buffer de comando completo (seleção de GPU desabilitada).</span><span class="sxs-lookup"><span data-stu-id="4611e-244">Then we will execute the commands in either the UAV (GPU culling enabled) or the full command buffer (GPU culling disabled).</span></span>

``` syntax
// Record the rendering commands.
{
       // Set necessary state.
       m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());

       ID3D12DescriptorHeap* ppHeaps[] = { m_cbvSrvUavHeap.Get() };
       m_commandList->SetDescriptorHeaps(_countof(ppHeaps), ppHeaps);

       m_commandList->RSSetViewports(1, &m_viewport);
       m_commandList->RSSetScissorRects(1, m_enableCulling ? &m_cullingScissorRect : &m_scissorRect);

       // Indicate that the command buffer will be used for indirect drawing
       // and that the back buffer will be used as a render target.
       D3D12_RESOURCE_BARRIER barriers[2] = {
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_enableCulling ? m_processedCommandBuffers[m_frameIndex].Get() : m_commandBuffer.Get(),
                    m_enableCulling ? D3D12_RESOURCE_STATE_UNORDERED_ACCESS : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE,
                    D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT),
              CD3DX12_RESOURCE_BARRIER::Transition(
                    m_renderTargets[m_frameIndex].Get(),
                    D3D12_RESOURCE_STATE_PRESENT,
                    D3D12_RESOURCE_STATE_RENDER_TARGET)
       };

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
       CD3DX12_CPU_DESCRIPTOR_HANDLE dsvHandle(m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
       m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, &dsvHandle);

       // Record commands.
       const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
       m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
       m_commandList->ClearDepthStencilView(dsvHandle, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

       m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP);
       m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);

       if (m_enableCulling)
       {
              // Draw the triangles that have not been culled.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    0,
                    m_processedCommandBuffers[m_frameIndex].Get(),
                    CommandBufferSizePerFrame);
       }
       else
       {
              // Draw all of the triangles.
              m_commandList->ExecuteIndirect(
                    m_commandSignature.Get(),
                    TriangleCount,
                    m_commandBuffer.Get(),
                    CommandBufferSizePerFrame * m_frameIndex,
                    nullptr,
                    0);
       }

       // Indicate that the command buffer may be used by the compute shader
       // and that the back buffer will now be used to present.
       barriers[0].Transition.StateBefore = D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT;
       barriers[0].Transition.StateAfter = m_enableCulling ? D3D12_RESOURCE_STATE_COPY_DEST : D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE;
       barriers[1].Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
       barriers[1].Transition.StateAfter = D3D12_RESOURCE_STATE_PRESENT;

       m_commandList->ResourceBarrier(_countof(barriers), barriers);

       ThrowIfFailed(m_commandList->Close());
}
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4611e-245">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-245">Call flow</span></span></th>
<th><span data-ttu-id="4611e-246">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-246">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4611e-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-247"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature"><strong>SetGraphicsRootSignature</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-248"><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12descriptorheap"><strong>ID3D12DescriptorHeap</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-249"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps"><strong>SetDescriptorHeaps</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-250"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports"><strong>RSSetViewports</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-251"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects"><strong>RSSetScissorRects</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-252"><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier"><strong>D3D12_RESOURCE_BARRIER</strong></a></span></span></td>
<td><dl><span data-ttu-id="4611e-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-253"><a href="cd3dx12-resource-barrier.md"><strong>CD3DX12_RESOURCE_BARRIER</strong></a></span></span><br /><span data-ttu-id="4611e-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-254">
<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-255"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-256"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="4611e-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-257"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-258"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets"><strong>OMSetRenderTargets</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-259"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview"><strong>ClearRenderTargetView</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-260"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview"><strong>ClearDepthStencilView</strong></a></span></span></td>
<td><span data-ttu-id="4611e-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-261"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_clear_flags"><strong>D3D12_CLEAR_FLAGS</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-262"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology"><strong>IASetPrimitiveTopology</strong></a></span></span></td>
<td><span data-ttu-id="4611e-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-263"><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology"><strong>D3D_PRIMITIVE_TOPOLOGY</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-264"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers"><strong>IASetVertexBuffers</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="4611e-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-265"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect"><strong>ExecuteIndirect</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="4611e-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-266"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier"><strong>ResourceBarrier</strong></a></span></span></td>
<td><span data-ttu-id="4611e-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-267"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4611e-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Fechar</strong></a></span><span class="sxs-lookup"><span data-stu-id="4611e-268"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close"><strong>Close</strong></a></span></span></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="4611e-269">Se estivermos no modo de seleção de GPU, teremos a fila de comandos gráficos aguardando a conclusão do trabalho de computação antes de começar a executar os comandos indiretos.</span><span class="sxs-lookup"><span data-stu-id="4611e-269">If we are in GPU culling mode, we will have the graphics command queue wait for the compute work to complete before it begins executing the indirect commands.</span></span> <span data-ttu-id="4611e-270">No método **OnRender** , o trecho a seguir é adicionado.</span><span class="sxs-lookup"><span data-stu-id="4611e-270">In the **OnRender** method the following snippet is added.</span></span>

``` syntax
// Execute the compute work.
if (m_enableCulling)
{
       ID3D12CommandList* ppCommandLists[] = { m_computeCommandList.Get() };
       m_computeCommandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
       m_computeCommandQueue->Signal(m_computeFence.Get(), m_fenceValues[m_frameIndex]);

       // Execute the rendering work only when the compute work is complete.
       m_commandQueue->Wait(m_computeFence.Get(), m_fenceValues[m_frameIndex]);
}

// Execute the rendering work.
ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);
```



| <span data-ttu-id="4611e-271">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="4611e-271">Call flow</span></span>                                                             | <span data-ttu-id="4611e-272">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4611e-272">Parameters</span></span> |
|-----------------------------------------------------------------------|------------|
| [<span data-ttu-id="4611e-273">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="4611e-273">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="4611e-274">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="4611e-274">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |
| [<span data-ttu-id="4611e-275">**Aviso**</span><span class="sxs-lookup"><span data-stu-id="4611e-275">**Signal**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                           |            |
| [<span data-ttu-id="4611e-276">**Aguarde**</span><span class="sxs-lookup"><span data-stu-id="4611e-276">**Wait**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                               |            |
| [<span data-ttu-id="4611e-277">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="4611e-277">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                        |            |
| [<span data-ttu-id="4611e-278">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="4611e-278">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="4611e-279">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="4611e-279">Run the sample</span></span>

<span data-ttu-id="4611e-280">O exemplo com a remoção de primitiva de GPU.</span><span class="sxs-lookup"><span data-stu-id="4611e-280">The sample with GPU primitive culling.</span></span>

![captura de tela da amostra indireta exectue com seleção de GPU](images/executeindirect-withculling.png)

<span data-ttu-id="4611e-282">O exemplo sem a remoção de primitiva de GPU.</span><span class="sxs-lookup"><span data-stu-id="4611e-282">The sample without GPU primitive culling.</span></span>

![captura de tela da amostra indireta exectue sem a remoção de GPU](images/executeindirect-withoutculling.png)

## <a name="related-topics"></a><span data-ttu-id="4611e-284">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4611e-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4611e-285">Instruções passo a passo de código do D3D12</span><span class="sxs-lookup"><span data-stu-id="4611e-285">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="4611e-286">Tutoriais de vídeo do DirectX Advanced Learning: executar a remoção de GPU indireta e assíncrona</span><span class="sxs-lookup"><span data-stu-id="4611e-286">DirectX advanced learning video tutorials : Execute Indirect and Async GPU culling</span></span>](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[<span data-ttu-id="4611e-287">Desenho indireto</span><span class="sxs-lookup"><span data-stu-id="4611e-287">Indirect Drawing</span></span>](indirect-drawing.md)
</dt> </dl>

 

 
