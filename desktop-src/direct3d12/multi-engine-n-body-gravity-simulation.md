---
title: Simulação de gravidade n-Body de vários mecanismos
description: O exemplo D3D12nBodyGravity demonstra como fazer o trabalho de computação de forma assíncrona.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548229"
---
# <a name="multi-engine-n-body-gravity-simulation"></a><span data-ttu-id="7bcf1-103">Simulação de gravidade n-Body de vários mecanismos</span><span class="sxs-lookup"><span data-stu-id="7bcf1-103">Multi-engine n-body gravity simulation</span></span>

<span data-ttu-id="7bcf1-104">O exemplo **D3D12nBodyGravity** demonstra como fazer o trabalho de computação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-104">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="7bcf1-105">O exemplo gira um número de threads cada um com uma fila de comando de computação e agenda o trabalho de computação na GPU que executa uma simulação de gravidade de n-corpo.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-105">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="7bcf1-106">Cada thread opera em dois buffers cheios de posição e dados de velocidade.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-106">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="7bcf1-107">Com cada iteração, o sombreador de computação lê a posição atual e os dados de velocidade de um buffer e grava a próxima iteração no outro buffer.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-107">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="7bcf1-108">Quando a iteração é concluída, o sombreador de computação troca qual buffer é o SRV para ler dados de posição/velocidade e que é o UAV para gravar atualizações de posição/velocidade alterando o estado do recurso em cada buffer.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-108">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span>

-   [<span data-ttu-id="7bcf1-109">Criar as assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="7bcf1-109">Create the root signatures</span></span>](#create-the-root-signatures)
-   [<span data-ttu-id="7bcf1-110">Criar os buffers SRV e UAV</span><span class="sxs-lookup"><span data-stu-id="7bcf1-110">Create the SRV and UAV buffers</span></span>](#create-the-srv-and-uav-buffers)
-   [<span data-ttu-id="7bcf1-111">Criar os buffers de CBV e de vértice</span><span class="sxs-lookup"><span data-stu-id="7bcf1-111">Create the CBV and vertex buffers</span></span>](#create-the-cbv-and-vertex-buffers)
-   [<span data-ttu-id="7bcf1-112">Sincronizar os threads de renderização e de computação</span><span class="sxs-lookup"><span data-stu-id="7bcf1-112">Synchronize the rendering and compute threads</span></span>](#synchronize-the-rendering-and-compute-threads)
-   [<span data-ttu-id="7bcf1-113">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="7bcf1-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="7bcf1-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bcf1-114">Related topics</span></span>](#related-topics)

## <a name="create-the-root-signatures"></a><span data-ttu-id="7bcf1-115">Criar as assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="7bcf1-115">Create the root signatures</span></span>

<span data-ttu-id="7bcf1-116">Começamos criando um gráfico e uma assinatura de raiz de computação, no método **Loadassets** .</span><span class="sxs-lookup"><span data-stu-id="7bcf1-116">We start out by creating both a graphics and a compute root signature, in the **LoadAssets** method.</span></span> <span data-ttu-id="7bcf1-117">Ambas as assinaturas raiz têm uma CBV (exibição de buffer constante) de raiz e uma tabela de descritor de modo de exibição de recurso de sombreador (SRV).</span><span class="sxs-lookup"><span data-stu-id="7bcf1-117">Both root signatures have a root constant buffer view (CBV) and a shader resource view (SRV) descriptor table.</span></span> <span data-ttu-id="7bcf1-118">A assinatura raiz de computação também tem uma tabela de descritor de UAV (exibição de acesso não ordenada).</span><span class="sxs-lookup"><span data-stu-id="7bcf1-118">The compute root signature also has an unordered access view (UAV) descriptor table.</span></span>

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| <span data-ttu-id="7bcf1-119">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="7bcf1-119">Call flow</span></span>                                                             | <span data-ttu-id="7bcf1-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bcf1-120">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="7bcf1-121">**\_Intervalo do descritor de CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-121">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="7bcf1-122">**\_Tipo de intervalo do descritor D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-122">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="7bcf1-123">**\_Parâmetro raiz \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-123">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="7bcf1-124">**\_Visibilidade do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-124">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="7bcf1-125">**Desc. de \_ assinatura raiz CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-125">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="7bcf1-126">**\_Sinalizadores de \_ assinatura \_ raiz D3D12**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-126">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="7bcf1-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7bcf1-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="7bcf1-128">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-128">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="7bcf1-129">**\_Versão da \_ assinatura \_ raiz do D3D**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-129">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="7bcf1-130">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-130">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="7bcf1-131">**Desc. de \_ assinatura raiz CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-131">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) |                                                                       |
| [<span data-ttu-id="7bcf1-132">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-132">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="7bcf1-133">**\_Versão da \_ assinatura \_ raiz do D3D**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-133">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="7bcf1-134">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-134">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a><span data-ttu-id="7bcf1-135">Criar os buffers SRV e UAV</span><span class="sxs-lookup"><span data-stu-id="7bcf1-135">Create the SRV and UAV buffers</span></span>

<span data-ttu-id="7bcf1-136">Os buffers SRV e UAV consistem em uma matriz de dados de posição e velocidade.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-136">The SRV and UAV buffers consist of an array of position and velocity data.</span></span>

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| <span data-ttu-id="7bcf1-137">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="7bcf1-137">Call flow</span></span>                       | <span data-ttu-id="7bcf1-138">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bcf1-138">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="7bcf1-139">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-139">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a><span data-ttu-id="7bcf1-140">Criar os buffers de CBV e de vértice</span><span class="sxs-lookup"><span data-stu-id="7bcf1-140">Create the CBV and vertex buffers</span></span>

<span data-ttu-id="7bcf1-141">Para o pipeline de gráficos, o CBV é um **struct** que contém duas matrizes usadas pelo sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-141">For the graphics pipeline, the CBV is a **struct** containing two matrices used by the geometry shader.</span></span> <span data-ttu-id="7bcf1-142">O sombreador Geometry usa a posição de cada partícula no sistema e gera um quádruplo para representá-lo usando essas matrizes.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-142">The geometry shader takes the position of each particle in the system and generates a quad to represent it using these matrices.</span></span>

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| <span data-ttu-id="7bcf1-143">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="7bcf1-143">Call flow</span></span>                       | <span data-ttu-id="7bcf1-144">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bcf1-144">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="7bcf1-145">**XMMATRIX**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-145">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

<span data-ttu-id="7bcf1-146">Como resultado, o buffer de vértice usado pelo sombreador de vértice na verdade não contém dados posicionais.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-146">As a result, the vertex buffer used by the vertex shader actually does not contain any positional data.</span></span>

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| <span data-ttu-id="7bcf1-147">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="7bcf1-147">Call flow</span></span>                       | <span data-ttu-id="7bcf1-148">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bcf1-148">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="7bcf1-149">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-149">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

<span data-ttu-id="7bcf1-150">Para o pipeline de computação, o CBV é um **struct** que contém algumas constantes usadas pela simulação de gravidade de n-Body no sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-150">For the compute pipeline, the CBV is a **struct** containing some constants used by the n-body gravity simulation in the compute shader.</span></span>

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a><span data-ttu-id="7bcf1-151">Sincronizar os threads de renderização e de computação</span><span class="sxs-lookup"><span data-stu-id="7bcf1-151">Synchronize the rendering and compute threads</span></span>

<span data-ttu-id="7bcf1-152">Depois que os buffers forem inicializados, o trabalho de processamento e de computação será iniciado.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-152">After the buffers are all initialized, the rendering and compute work will begin.</span></span> <span data-ttu-id="7bcf1-153">O thread de computação alterará o estado dos dois buffers de posição/velocidade de frente e para trás entre SRV e UAV à medida que ele itera na simulação, e o thread de renderização precisa garantir que ele agende o trabalho no pipeline de gráficos que opera no SRV.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-153">The compute thread will be changing the state of the two position/velocity buffers back and forth between SRV and UAV as it iterates on the simulation, and the rendering thread needs to ensure that it schedules work on the graphics pipeline that operates on the SRV.</span></span> <span data-ttu-id="7bcf1-154">Os limites são usados para sincronizar o acesso aos dois buffers.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-154">Fences are used to synchronize access to the two buffers.</span></span>

<span data-ttu-id="7bcf1-155">No thread de renderização:</span><span class="sxs-lookup"><span data-stu-id="7bcf1-155">On the Render thread:</span></span>

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| <span data-ttu-id="7bcf1-156">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="7bcf1-156">Call flow</span></span>                                                              | <span data-ttu-id="7bcf1-157">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bcf1-157">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="7bcf1-158">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-158">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [<span data-ttu-id="7bcf1-159">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-159">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [<span data-ttu-id="7bcf1-160">**Getcompletedvalue**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-160">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [<span data-ttu-id="7bcf1-161">**Aguarde**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-161">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [<span data-ttu-id="7bcf1-162">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-162">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="7bcf1-163">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-163">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="7bcf1-164">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-164">**IDXGISwapChain1::Present1**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="7bcf1-165">Para simplificar o exemplo um pouco, o thread de computação aguarda a GPU concluir cada iteração antes de agendar mais trabalho de computação.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-165">To simplify the sample a bit, the compute thread waits for the GPU to complete each iteration before scheduling any more compute work.</span></span> <span data-ttu-id="7bcf1-166">Na prática, os aplicativos provavelmente desejarão manter a fila de computação cheia para alcançar o desempenho máximo da GPU.</span><span class="sxs-lookup"><span data-stu-id="7bcf1-166">In practice, applications will likely want to keep the compute queue full to achieve maximum performance from the GPU.</span></span>

<span data-ttu-id="7bcf1-167">No thread de computação:</span><span class="sxs-lookup"><span data-stu-id="7bcf1-167">On the Compute thread:</span></span>

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| <span data-ttu-id="7bcf1-168">Fluxo de chamadas</span><span class="sxs-lookup"><span data-stu-id="7bcf1-168">Call flow</span></span>                                                                   | <span data-ttu-id="7bcf1-169">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bcf1-169">Parameters</span></span> |
|-----------------------------------------------------------------------------|------------|
| [<span data-ttu-id="7bcf1-170">**ID3D12CommandQueue**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-170">**ID3D12CommandQueue**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [<span data-ttu-id="7bcf1-171">**ID3D12CommandAllocator**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-171">**ID3D12CommandAllocator**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [<span data-ttu-id="7bcf1-172">**ID3D12GraphicsCommandList**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-172">**ID3D12GraphicsCommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [<span data-ttu-id="7bcf1-173">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-173">**ID3D12Fence**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [<span data-ttu-id="7bcf1-174">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-174">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="7bcf1-175">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-175">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [<span data-ttu-id="7bcf1-176">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-176">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [<span data-ttu-id="7bcf1-177">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-177">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [<span data-ttu-id="7bcf1-178">**InterlockedIncrement**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-178">**InterlockedIncrement**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [<span data-ttu-id="7bcf1-179">**Aviso**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-179">**Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [<span data-ttu-id="7bcf1-180">**SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-180">**SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [<span data-ttu-id="7bcf1-181">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-181">**WaitForSingleObject**</span></span>](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [<span data-ttu-id="7bcf1-182">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-182">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="7bcf1-183">**Getcompletedvalue**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-183">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [<span data-ttu-id="7bcf1-184">**Aguarde**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-184">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [<span data-ttu-id="7bcf1-185">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-185">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [<span data-ttu-id="7bcf1-186">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-186">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [<span data-ttu-id="7bcf1-187">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="7bcf1-187">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="7bcf1-188">Execute o exemplo</span><span class="sxs-lookup"><span data-stu-id="7bcf1-188">Run the sample</span></span>

![uma captura de tela da simulação de gravidade do corpo n final](images/nbodygravity.png)

## <a name="related-topics"></a><span data-ttu-id="7bcf1-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bcf1-190">Related topics</span></span>

[<span data-ttu-id="7bcf1-191">Instruções passo a passo de código do D3D12</span><span class="sxs-lookup"><span data-stu-id="7bcf1-191">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)

[<span data-ttu-id="7bcf1-192">Sincronização de vários mecanismos</span><span class="sxs-lookup"><span data-stu-id="7bcf1-192">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)