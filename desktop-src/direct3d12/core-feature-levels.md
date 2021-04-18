---
title: O nível de recurso do Direct3D 12 Core 1.0
description: O nível de recurso Core 1,0 é um subconjunto do conjunto de recursos completo do Direct3D 12.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/03/2020
ms.locfileid: "105773925"
---
# <a name="the-direct3d-12-core-10-feature-level"></a><span data-ttu-id="8d13f-103">O nível de recurso do Direct3D 12 Core 1.0</span><span class="sxs-lookup"><span data-stu-id="8d13f-103">The Direct3D 12 Core 1.0 Feature Level</span></span>

<span data-ttu-id="8d13f-104">O nível de recurso Core 1,0 é um subconjunto do conjunto de recursos completo do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8d13f-104">The Core 1.0 Feature Level is a subset of the full Direct3D 12 feature set.</span></span> <span data-ttu-id="8d13f-105">O nível de recurso do Core 1,0 pode ser exposto por uma categoria de dispositivos conhecida como *dispositivos somente de computação*.</span><span class="sxs-lookup"><span data-stu-id="8d13f-105">Core 1.0 Feature Level can be exposed by a category of devices known as *compute-only devices*.</span></span> <span data-ttu-id="8d13f-106">O modelo de driver geral para dispositivos somente de computação é o MCDM (modelo de driver de computação da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="8d13f-106">The overall driver model for compute-only devices is the Microsoft Compute Driver Model (MCDM).</span></span> <span data-ttu-id="8d13f-107">MCDM é um par reduzido para baixo do WDDM (modelo de driver de dispositivo) do Windows, que tem um escopo maior.</span><span class="sxs-lookup"><span data-stu-id="8d13f-107">MCDM is a scaled-down peer of the Windows Device Driver Model (WDDM), which has a larger scope.</span></span>

<span data-ttu-id="8d13f-108">Um dispositivo que dá suporte *apenas* aos recursos dentro de um nível de recurso principal é conhecido como um *dispositivo principal*.</span><span class="sxs-lookup"><span data-stu-id="8d13f-108">A device that supports *only* the features within a Core Feature Level is known as a *Core device*.</span></span>

> [!NOTE]
> <span data-ttu-id="8d13f-109">*Dispositivo somente de computação*, dispositivo *MCDM*, *dispositivo de nível de recurso principal* e *dispositivo de núcleo* , todos significam a mesma coisa.</span><span class="sxs-lookup"><span data-stu-id="8d13f-109">*Compute-only device*, *MCDM device*, *Core Feature Level device*, and *Core device* all mean the same thing.</span></span> <span data-ttu-id="8d13f-110">Preferiremos o *dispositivo principal* para simplificar a simplicidade.</span><span class="sxs-lookup"><span data-stu-id="8d13f-110">We'll prefer *Core device* for simplicity.</span></span>

## <a name="creating-a-core-device"></a><span data-ttu-id="8d13f-111">Criando um dispositivo principal</span><span class="sxs-lookup"><span data-stu-id="8d13f-111">Creating a Core device</span></span>

<span data-ttu-id="8d13f-112">Em geral, para criar um dispositivo Direct3D 12, você chama a função [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) e especifica um nível de recurso mínimo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-112">In general, to create a Direct3D 12 device, you call the [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) function, and specify a minimum feature level.</span></span>

<span data-ttu-id="8d13f-113">Se você especificar um nível de recurso de 9 a 12, o dispositivo retornado será um dispositivo repleto de recursos, como uma GPU tradicional (que dá suporte a um superconjunto da funcionalidade de um dispositivo principal).</span><span class="sxs-lookup"><span data-stu-id="8d13f-113">If you specify a feature level of 9 through 12, then the device that's returned is a feature-rich device, such as a traditional GPU (which supports a superset of the functionality of a Core device).</span></span> <span data-ttu-id="8d13f-114">Um dispositivo principal nunca é retornado para esse intervalo de níveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="8d13f-114">A Core device is never returned for that range of feature levels.</span></span>

<span data-ttu-id="8d13f-115">Por outro lado, se você especificar um nível de recurso principal (por exemplo, [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), o dispositivo retornado poderá ser repleto de recursos ou pode ser um dispositivo principal.</span><span class="sxs-lookup"><span data-stu-id="8d13f-115">On the other hand, if you specify a Core feature level (for example, [**D3D_FEATURE_LEVEL::D3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), then the device that's returned could be feature-rich, or it could be a Core device.</span></span>

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

<span data-ttu-id="8d13f-116">Se você especificar um `_CORE` nível de recurso, a camada de tempo de execução/depuração validará que os recursos usados pelo aplicativo são permitidos por esse `_CORE` nível de recurso.</span><span class="sxs-lookup"><span data-stu-id="8d13f-116">If you specify a `_CORE` feature level, then the runtime/debug layer validates that the features your application uses are allowed by that `_CORE` feature level.</span></span> <span data-ttu-id="8d13f-117">Esse conjunto de recursos é definido mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8d13f-117">That set of features is defined later in this topic.</span></span>

## <a name="shader-model-for-core-devices"></a><span data-ttu-id="8d13f-118">Modelo de sombreador para dispositivos principais</span><span class="sxs-lookup"><span data-stu-id="8d13f-118">Shader model for Core devices</span></span>

<span data-ttu-id="8d13f-119">Um dispositivo principal dá suporte ao modelo de sombreador 5.0 +.</span><span class="sxs-lookup"><span data-stu-id="8d13f-119">A Core device supports Shader Model 5.0+.</span></span>

<span data-ttu-id="8d13f-120">O tempo de execução executa a conversão de modelos de sombreador não DXIL de 5. x para 6,0 DXIL.</span><span class="sxs-lookup"><span data-stu-id="8d13f-120">The runtime performs conversion of 5.x non DXIL shader models to 6.0 DXIL.</span></span> <span data-ttu-id="8d13f-121">Portanto, o driver precisa dar suporte apenas a 6. x.</span><span class="sxs-lookup"><span data-stu-id="8d13f-121">So the driver need only support 6.x.</span></span>

## <a name="resource-management-model-for-core-devices"></a><span data-ttu-id="8d13f-122">Modelo de gerenciamento de recursos para dispositivos principais</span><span class="sxs-lookup"><span data-stu-id="8d13f-122">Resource management model for Core devices</span></span>

- <span data-ttu-id="8d13f-123">Dimensões de recurso com suporte: somente buffers brutos e estruturados (sem buffers de tipo, texture1d/2D etc.)</span><span class="sxs-lookup"><span data-stu-id="8d13f-123">Supported resource dimensions: raw and structured buffers only (no typed buffers, texture1d/2D, etc.)</span></span>
- <span data-ttu-id="8d13f-124">Não há suporte para recursos reservados (lado a lado)</span><span class="sxs-lookup"><span data-stu-id="8d13f-124">No support for reserved (tiled) resources</span></span>
- <span data-ttu-id="8d13f-125">Não há suporte para heaps personalizados</span><span class="sxs-lookup"><span data-stu-id="8d13f-125">No support for custom heaps</span></span>
- <span data-ttu-id="8d13f-126">Não há suporte para nenhum desses sinalizadores de heap:</span><span class="sxs-lookup"><span data-stu-id="8d13f-126">No support for any of these heap flags:</span></span>
  - <span data-ttu-id="8d13f-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span><span class="sxs-lookup"><span data-stu-id="8d13f-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span></span>
  - <span data-ttu-id="8d13f-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span><span class="sxs-lookup"><span data-stu-id="8d13f-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span></span>
  - <span data-ttu-id="8d13f-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="8d13f-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span></span>
  - <span data-ttu-id="8d13f-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Observe que os atomicers do sombreador são necessários, esse sinalizador é para outro recurso, Atomic-adaptadores)</span><span class="sxs-lookup"><span data-stu-id="8d13f-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (note shader atomics are required, this flag is for another feature, cross adapter atomics)</span></span>

## <a name="resource-binding-model-for-core-devices"></a><span data-ttu-id="8d13f-131">Modelo de associação de recursos para dispositivos principais</span><span class="sxs-lookup"><span data-stu-id="8d13f-131">Resource binding model for Core devices</span></span>

- <span data-ttu-id="8d13f-132">Suporte apenas para camada 1 de associação de recursos</span><span class="sxs-lookup"><span data-stu-id="8d13f-132">Support for resource binding tier 1 only</span></span>
- <span data-ttu-id="8d13f-133">Exceções:</span><span class="sxs-lookup"><span data-stu-id="8d13f-133">Exceptions:</span></span>
  - <span data-ttu-id="8d13f-134">Não há suporte para amostragens de textura</span><span class="sxs-lookup"><span data-stu-id="8d13f-134">No support for texture samplers</span></span>
  - <span data-ttu-id="8d13f-135">Suporte para 64 UAVs, como o nível de recurso 11.1 + (em oposição a apenas 8)</span><span class="sxs-lookup"><span data-stu-id="8d13f-135">Support for 64 UAVs like Feature Level 11.1+ (as opposed to only 8)</span></span>
  - <span data-ttu-id="8d13f-136">As implementações não precisam implementar a verificação de limites em acessos de sombreador aos recursos por meio de descritores, os acessos fora dos limites produzem um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="8d13f-136">Implementations do not have to implement bounds checking on shader accesses to resources through descriptors, out of bounds accesses produce undefined behavior.</span></span>
    - <span data-ttu-id="8d13f-137">Como um subproduto, não há suporte para o sinalizador de intervalo do descritor D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS em assinaturas raiz.</span><span class="sxs-lookup"><span data-stu-id="8d13f-137">As a byproduct, the descriptor range flag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in root signatures is not supported.</span></span>
- <span data-ttu-id="8d13f-138">Os descritores de UAV/CBV só podem ser feitos em recursos de heaps padrão (portanto, não há heaps de upload/readback).</span><span class="sxs-lookup"><span data-stu-id="8d13f-138">UAV/CBV descriptors can only be made on resources from default heaps (so no upload/readback heaps).</span></span> <span data-ttu-id="8d13f-139">Isso força seu aplicativo a fazer cópias para obter dados entre a CPU< >GPU.</span><span class="sxs-lookup"><span data-stu-id="8d13f-139">This forces your application to do copies to get data across CPU<->GPU.</span></span>
- <span data-ttu-id="8d13f-140">Apesar de ser a camada de funcionalidade de associação mais baixa, ainda há alguns recursos necessários até mesmo nesta camada vale a pena chamar:</span><span class="sxs-lookup"><span data-stu-id="8d13f-140">Despite being the lowest binding capability tier, there are still some features required even in this tier worth calling out:</span></span>
  - <span data-ttu-id="8d13f-141">Os heaps de descritores podem ser atualizados depois que as listas de comandos são registradas (consulte D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE na especificação de associação de recursos)</span><span class="sxs-lookup"><span data-stu-id="8d13f-141">Descriptor heaps can be updated after command lists are recorded (see D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in the resource binding spec)</span></span>
  - <span data-ttu-id="8d13f-142">Descritores de raiz são basicamente ponteiros GPUVA</span><span class="sxs-lookup"><span data-stu-id="8d13f-142">Root descriptors are basically GPUVA pointers</span></span>
    - <span data-ttu-id="8d13f-143">Embora não haja suporte a MMU/VA, os VAs de buffer que são usados nos descritores de raiz podem ser emulados por implementações, resolvendo patches.</span><span class="sxs-lookup"><span data-stu-id="8d13f-143">Even though there is no MMU / VA support, buffer VAs that are used in root descriptors can be emulated by implementations by doing address patching.</span></span>

### <a name="structured-buffer-restrictions"></a><span data-ttu-id="8d13f-144">Restrições de buffer estruturado</span><span class="sxs-lookup"><span data-stu-id="8d13f-144">Structured buffer restrictions</span></span>

<span data-ttu-id="8d13f-145">Os buffers estruturados devem ter um endereço base com 4 bytes alinhados e o stride deve ser 2 ou um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="8d13f-145">Structured buffers must have a base address that is 4 byte aligned, and stride must be 2 or a multiple of 4.</span></span> <span data-ttu-id="8d13f-146">O caso de um stride de 2 é para aplicativos com dados de 16 bits, particularmente dado que não há suporte para buffers tipados no D3D_FEATURE_LEVEL_1_0_CORE.</span><span class="sxs-lookup"><span data-stu-id="8d13f-146">The case for a stride of 2 is for apps with 16 bit data, particularly given there is no support for typed buffers in D3D_FEATURE_LEVEL_1_0_CORE.</span></span>

<span data-ttu-id="8d13f-147">O stride especificado nos descritores deve corresponder ao Stride especificado em HLSL.</span><span class="sxs-lookup"><span data-stu-id="8d13f-147">Stride specified in descriptors must match the stride specified in HLSL.</span></span>  

## <a name="command-queue-support-for-core-devices"></a><span data-ttu-id="8d13f-148">Suporte de fila de comando para dispositivos principais</span><span class="sxs-lookup"><span data-stu-id="8d13f-148">Command queue support for Core devices</span></span>

<span data-ttu-id="8d13f-149">Somente as filas de computação e cópia (sem 3D, vídeo, etc. filas).</span><span class="sxs-lookup"><span data-stu-id="8d13f-149">Compute and copy queues only (no 3D, video, etc. queues).</span></span>

## <a name="shader-support-for-core-devices"></a><span data-ttu-id="8d13f-150">Suporte a sombreador para dispositivos principais</span><span class="sxs-lookup"><span data-stu-id="8d13f-150">Shader support for Core devices</span></span>

<span data-ttu-id="8d13f-151">Somente sombreadores de computação, nenhum sombreador de gráficos (vértice, sombreadores de pixel etc.) nem qualquer funcionalidade relacionada, como destinos de renderização, cadeias de permuta, montadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="8d13f-151">Compute shaders only, no graphics shaders (Vertex, Pixel Shaders, etc.) nor any related functionality such as render targets, swap chains, input assembler.</span></span>

### <a name="arithmetic-precision"></a><span data-ttu-id="8d13f-152">Precisão aritmética</span><span class="sxs-lookup"><span data-stu-id="8d13f-152">Arithmetic precision</span></span>

<span data-ttu-id="8d13f-153">Os dispositivos principais não precisam dar suporte a normas para operações de ponto flutuante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8d13f-153">Core devices do not have to support denorms for 16 bit floating point operations.</span></span>

## <a name="supported-apis-for-core-devices"></a><span data-ttu-id="8d13f-154">APIs com suporte para dispositivos principais</span><span class="sxs-lookup"><span data-stu-id="8d13f-154">Supported APIs for Core devices</span></span>

<span data-ttu-id="8d13f-155">A lista a seguir representa o subconjunto com suporte da interface de programação de aplicativo completa (as APIs que *não* têm suporte no nível de recurso Core 1,0 *não* estão listadas).</span><span class="sxs-lookup"><span data-stu-id="8d13f-155">The list below represents the supported subset of the full application programming interface (APIs that are *not* supported in Core 1.0 Feature Level are *not* listed).</span></span>

### <a name="id3d12device-methods"></a><span data-ttu-id="8d13f-156">Métodos ID3D12Device</span><span class="sxs-lookup"><span data-stu-id="8d13f-156">ID3D12Device methods</span></span>

* [<span data-ttu-id="8d13f-157">ID3D12Device::CheckFeatureSupport</span><span class="sxs-lookup"><span data-stu-id="8d13f-157">ID3D12Device::CheckFeatureSupport</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [<span data-ttu-id="8d13f-158">ID3D12Device::CopyDescriptors</span><span class="sxs-lookup"><span data-stu-id="8d13f-158">ID3D12Device::CopyDescriptors</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [<span data-ttu-id="8d13f-159">ID3D12Device::CopyDescriptorsSimple</span><span class="sxs-lookup"><span data-stu-id="8d13f-159">ID3D12Device::CopyDescriptorsSimple</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [<span data-ttu-id="8d13f-160">ID3D12Device::CreateCommandAllocator</span><span class="sxs-lookup"><span data-stu-id="8d13f-160">ID3D12Device::CreateCommandAllocator</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [<span data-ttu-id="8d13f-161">ID3D12Device:: createcommandlist</span><span class="sxs-lookup"><span data-stu-id="8d13f-161">ID3D12Device::CreateCommandList</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [<span data-ttu-id="8d13f-162">ID3D12Device::CreateCommandQueue</span><span class="sxs-lookup"><span data-stu-id="8d13f-162">ID3D12Device::CreateCommandQueue</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [<span data-ttu-id="8d13f-163">ID3D12Device::CreateCommandSignature</span><span class="sxs-lookup"><span data-stu-id="8d13f-163">ID3D12Device::CreateCommandSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [<span data-ttu-id="8d13f-164">ID3D12Device::CreateCommittedResource</span><span class="sxs-lookup"><span data-stu-id="8d13f-164">ID3D12Device::CreateCommittedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [<span data-ttu-id="8d13f-165">ID3D12Device::CreateComputePipelineState</span><span class="sxs-lookup"><span data-stu-id="8d13f-165">ID3D12Device::CreateComputePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [<span data-ttu-id="8d13f-166">ID3D12Device::CreateConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="8d13f-166">ID3D12Device::CreateConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [<span data-ttu-id="8d13f-167">ID3D12Device::CreateDescriptorHeap</span><span class="sxs-lookup"><span data-stu-id="8d13f-167">ID3D12Device::CreateDescriptorHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [<span data-ttu-id="8d13f-168">ID3D12Device:: createfence</span><span class="sxs-lookup"><span data-stu-id="8d13f-168">ID3D12Device::CreateFence</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [<span data-ttu-id="8d13f-169">ID3D12Device:: createheap</span><span class="sxs-lookup"><span data-stu-id="8d13f-169">ID3D12Device::CreateHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [<span data-ttu-id="8d13f-170">ID3D12Device::CreatePlacedResource</span><span class="sxs-lookup"><span data-stu-id="8d13f-170">ID3D12Device::CreatePlacedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [<span data-ttu-id="8d13f-171">ID3D12Device::CreateQueryHeap</span><span class="sxs-lookup"><span data-stu-id="8d13f-171">ID3D12Device::CreateQueryHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [<span data-ttu-id="8d13f-172">ID3D12Device::CreateRootSignature</span><span class="sxs-lookup"><span data-stu-id="8d13f-172">ID3D12Device::CreateRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [<span data-ttu-id="8d13f-173">ID3D12Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="8d13f-173">ID3D12Device::CreateShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [<span data-ttu-id="8d13f-174">ID3D12Device::CreateSharedHandle</span><span class="sxs-lookup"><span data-stu-id="8d13f-174">ID3D12Device::CreateSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [<span data-ttu-id="8d13f-175">ID3D12Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="8d13f-175">ID3D12Device::CreateUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [<span data-ttu-id="8d13f-176">ID3D12Device:: remover</span><span class="sxs-lookup"><span data-stu-id="8d13f-176">ID3D12Device::Evict</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [<span data-ttu-id="8d13f-177">ID3D12Device::GetAdapterLuid</span><span class="sxs-lookup"><span data-stu-id="8d13f-177">ID3D12Device::GetAdapterLuid</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [<span data-ttu-id="8d13f-178">ID3D12Device:: GetCopyableFootprints</span><span class="sxs-lookup"><span data-stu-id="8d13f-178">ID3D12Device::GetCopyableFootprints</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [<span data-ttu-id="8d13f-179">ID3D12Device::GetCustomHeapProperties</span><span class="sxs-lookup"><span data-stu-id="8d13f-179">ID3D12Device::GetCustomHeapProperties</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [<span data-ttu-id="8d13f-180">ID3D12Device::GetDescriptorHandleIncrementSize</span><span class="sxs-lookup"><span data-stu-id="8d13f-180">ID3D12Device::GetDescriptorHandleIncrementSize</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [<span data-ttu-id="8d13f-181">ID3D12Device::GetDeviceRemovedReason</span><span class="sxs-lookup"><span data-stu-id="8d13f-181">ID3D12Device::GetDeviceRemovedReason</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [<span data-ttu-id="8d13f-182">ID3D12Device::GetNodeCount</span><span class="sxs-lookup"><span data-stu-id="8d13f-182">ID3D12Device::GetNodeCount</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [<span data-ttu-id="8d13f-183">ID3D12Device::GetResourceAllocationInfo</span><span class="sxs-lookup"><span data-stu-id="8d13f-183">ID3D12Device::GetResourceAllocationInfo</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [<span data-ttu-id="8d13f-184">ID3D12Device::MakeResident</span><span class="sxs-lookup"><span data-stu-id="8d13f-184">ID3D12Device::MakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [<span data-ttu-id="8d13f-185">ID3D12Device::OpenSharedHandle</span><span class="sxs-lookup"><span data-stu-id="8d13f-185">ID3D12Device::OpenSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [<span data-ttu-id="8d13f-186">ID3D12Device::OpenSharedHandleByName</span><span class="sxs-lookup"><span data-stu-id="8d13f-186">ID3D12Device::OpenSharedHandleByName</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [<span data-ttu-id="8d13f-187">ID3D12Device::SetStablePowerState</span><span class="sxs-lookup"><span data-stu-id="8d13f-187">ID3D12Device::SetStablePowerState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a><span data-ttu-id="8d13f-188">Métodos ID3D12Device1</span><span class="sxs-lookup"><span data-stu-id="8d13f-188">ID3D12Device1 methods</span></span>

* [<span data-ttu-id="8d13f-189">ID3D12Device1::CreatePipelineLibrary</span><span class="sxs-lookup"><span data-stu-id="8d13f-189">ID3D12Device1::CreatePipelineLibrary</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [<span data-ttu-id="8d13f-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span><span class="sxs-lookup"><span data-stu-id="8d13f-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [<span data-ttu-id="8d13f-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span><span class="sxs-lookup"><span data-stu-id="8d13f-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a><span data-ttu-id="8d13f-192">Métodos ID3D12Device2</span><span class="sxs-lookup"><span data-stu-id="8d13f-192">ID3D12Device2 methods</span></span>

* [<span data-ttu-id="8d13f-193">ID3D12Device2:: createpipelinestate</span><span class="sxs-lookup"><span data-stu-id="8d13f-193">ID3D12Device2::CreatePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a><span data-ttu-id="8d13f-194">Métodos ID3D12Device3</span><span class="sxs-lookup"><span data-stu-id="8d13f-194">ID3D12Device3 methods</span></span>

* [<span data-ttu-id="8d13f-195">ID3D12Device3::OpenExistingHeapFromAddress</span><span class="sxs-lookup"><span data-stu-id="8d13f-195">ID3D12Device3::OpenExistingHeapFromAddress</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* <span data-ttu-id="8d13f-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span><span class="sxs-lookup"><span data-stu-id="8d13f-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span></span>
* [<span data-ttu-id="8d13f-197">ID3D12Device3::EnqueueMakeResident</span><span class="sxs-lookup"><span data-stu-id="8d13f-197">ID3D12Device3::EnqueueMakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a><span data-ttu-id="8d13f-198">Métodos ID3D12Device4</span><span class="sxs-lookup"><span data-stu-id="8d13f-198">ID3D12Device4 methods</span></span>

* [<span data-ttu-id="8d13f-199">ID3D12Device4::GetResourceAllocationInfo1</span><span class="sxs-lookup"><span data-stu-id="8d13f-199">ID3D12Device4::GetResourceAllocationInfo1</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a><span data-ttu-id="8d13f-200">Métodos ID3D12Device5</span><span class="sxs-lookup"><span data-stu-id="8d13f-200">ID3D12Device5 methods</span></span>

* [<span data-ttu-id="8d13f-201">ID3D12Device5::CreateMetaCommand</span><span class="sxs-lookup"><span data-stu-id="8d13f-201">ID3D12Device5::CreateMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [<span data-ttu-id="8d13f-202">ID3D12Device5:: createstateobject</span><span class="sxs-lookup"><span data-stu-id="8d13f-202">ID3D12Device5::CreateStateObject</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [<span data-ttu-id="8d13f-203">ID3D12Device5::EnumerateMetaCommandParameters</span><span class="sxs-lookup"><span data-stu-id="8d13f-203">ID3D12Device5::EnumerateMetaCommandParameters</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [<span data-ttu-id="8d13f-204">ID3D12Device5::EnumerateMetaCommands</span><span class="sxs-lookup"><span data-stu-id="8d13f-204">ID3D12Device5::EnumerateMetaCommands</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [<span data-ttu-id="8d13f-205">ID3D12Device5::RemoveDevice</span><span class="sxs-lookup"><span data-stu-id="8d13f-205">ID3D12Device5::RemoveDevice</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a><span data-ttu-id="8d13f-206">Métodos ID3D12CommandQueue</span><span class="sxs-lookup"><span data-stu-id="8d13f-206">ID3D12CommandQueue methods</span></span>

* [<span data-ttu-id="8d13f-207">ID3D12CommandQueue::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="8d13f-207">ID3D12CommandQueue::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [<span data-ttu-id="8d13f-208">ID3D12CommandQueue:: endEvent</span><span class="sxs-lookup"><span data-stu-id="8d13f-208">ID3D12CommandQueue::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [<span data-ttu-id="8d13f-209">ID3D12CommandQueue::ExecuteCommandLists</span><span class="sxs-lookup"><span data-stu-id="8d13f-209">ID3D12CommandQueue::ExecuteCommandLists</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [<span data-ttu-id="8d13f-210">ID3D12CommandQueue::GetClockCalibration</span><span class="sxs-lookup"><span data-stu-id="8d13f-210">ID3D12CommandQueue::GetClockCalibration</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [<span data-ttu-id="8d13f-211">ID3D12CommandQueue:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="8d13f-211">ID3D12CommandQueue::GetDesc</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [<span data-ttu-id="8d13f-212">ID3D12CommandQueue::GetTimestampFrequency</span><span class="sxs-lookup"><span data-stu-id="8d13f-212">ID3D12CommandQueue::GetTimestampFrequency</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [<span data-ttu-id="8d13f-213">ID3D12CommandQueue:: setmarcer</span><span class="sxs-lookup"><span data-stu-id="8d13f-213">ID3D12CommandQueue::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [<span data-ttu-id="8d13f-214">ID3D12CommandQueue:: Signal</span><span class="sxs-lookup"><span data-stu-id="8d13f-214">ID3D12CommandQueue::Signal</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [<span data-ttu-id="8d13f-215">ID3D12CommandQueue:: aguardar</span><span class="sxs-lookup"><span data-stu-id="8d13f-215">ID3D12CommandQueue::Wait</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a><span data-ttu-id="8d13f-216">Métodos ID3D12CommandList</span><span class="sxs-lookup"><span data-stu-id="8d13f-216">ID3D12CommandList methods</span></span>

* [<span data-ttu-id="8d13f-217">ID3D12CommandList:: GetType</span><span class="sxs-lookup"><span data-stu-id="8d13f-217">ID3D12CommandList::GetType</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a><span data-ttu-id="8d13f-218">Métodos ID3D12GraphicsCommandList</span><span class="sxs-lookup"><span data-stu-id="8d13f-218">ID3D12GraphicsCommandList methods</span></span>

* [<span data-ttu-id="8d13f-219">ID3D12GraphicsCommandList::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="8d13f-219">ID3D12GraphicsCommandList::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [<span data-ttu-id="8d13f-220">ID3D12GraphicsCommandList::BeginQuery</span><span class="sxs-lookup"><span data-stu-id="8d13f-220">ID3D12GraphicsCommandList::BeginQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [<span data-ttu-id="8d13f-221">ID3D12GraphicsCommandList:: Clearstate</span><span class="sxs-lookup"><span data-stu-id="8d13f-221">ID3D12GraphicsCommandList::ClearState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [<span data-ttu-id="8d13f-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="8d13f-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [<span data-ttu-id="8d13f-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="8d13f-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [<span data-ttu-id="8d13f-224">ID3D12GraphicsCommandList:: fechar</span><span class="sxs-lookup"><span data-stu-id="8d13f-224">ID3D12GraphicsCommandList::Close</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [<span data-ttu-id="8d13f-225">ID3D12GraphicsCommandList::CopyBufferRegion</span><span class="sxs-lookup"><span data-stu-id="8d13f-225">ID3D12GraphicsCommandList::CopyBufferRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [<span data-ttu-id="8d13f-226">ID3D12GraphicsCommandList::CopyResource</span><span class="sxs-lookup"><span data-stu-id="8d13f-226">ID3D12GraphicsCommandList::CopyResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [<span data-ttu-id="8d13f-227">ID3D12GraphicsCommandList::CopyTextureRegion</span><span class="sxs-lookup"><span data-stu-id="8d13f-227">ID3D12GraphicsCommandList::CopyTextureRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [<span data-ttu-id="8d13f-228">ID3D12GraphicsCommandList::D ispatch</span><span class="sxs-lookup"><span data-stu-id="8d13f-228">ID3D12GraphicsCommandList::Dispatch</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [<span data-ttu-id="8d13f-229">ID3D12GraphicsCommandList:: endEvent</span><span class="sxs-lookup"><span data-stu-id="8d13f-229">ID3D12GraphicsCommandList::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [<span data-ttu-id="8d13f-230">ID3D12GraphicsCommandList:: endquery</span><span class="sxs-lookup"><span data-stu-id="8d13f-230">ID3D12GraphicsCommandList::EndQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [<span data-ttu-id="8d13f-231">ID3D12GraphicsCommandList:: Reset</span><span class="sxs-lookup"><span data-stu-id="8d13f-231">ID3D12GraphicsCommandList::Reset</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [<span data-ttu-id="8d13f-232">ID3D12GraphicsCommandList::ResolveQueryData</span><span class="sxs-lookup"><span data-stu-id="8d13f-232">ID3D12GraphicsCommandList::ResolveQueryData</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [<span data-ttu-id="8d13f-233">ID3D12GraphicsCommandList::ResourceBarrier</span><span class="sxs-lookup"><span data-stu-id="8d13f-233">ID3D12GraphicsCommandList::ResourceBarrier</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [<span data-ttu-id="8d13f-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span><span class="sxs-lookup"><span data-stu-id="8d13f-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [<span data-ttu-id="8d13f-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span><span class="sxs-lookup"><span data-stu-id="8d13f-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [<span data-ttu-id="8d13f-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="8d13f-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [<span data-ttu-id="8d13f-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="8d13f-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [<span data-ttu-id="8d13f-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="8d13f-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [<span data-ttu-id="8d13f-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span><span class="sxs-lookup"><span data-stu-id="8d13f-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [<span data-ttu-id="8d13f-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="8d13f-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [<span data-ttu-id="8d13f-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span><span class="sxs-lookup"><span data-stu-id="8d13f-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [<span data-ttu-id="8d13f-242">ID3D12GraphicsCommandList:: setmarcer</span><span class="sxs-lookup"><span data-stu-id="8d13f-242">ID3D12GraphicsCommandList::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [<span data-ttu-id="8d13f-243">ID3D12GraphicsCommandList:: setpipelinestate</span><span class="sxs-lookup"><span data-stu-id="8d13f-243">ID3D12GraphicsCommandList::SetPipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [<span data-ttu-id="8d13f-244">ID3D12GraphicsCommandList::SetPredication</span><span class="sxs-lookup"><span data-stu-id="8d13f-244">ID3D12GraphicsCommandList::SetPredication</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a><span data-ttu-id="8d13f-245">Métodos ID3D12GraphicsCommandList1</span><span class="sxs-lookup"><span data-stu-id="8d13f-245">ID3D12GraphicsCommandList1 methods</span></span>

* [<span data-ttu-id="8d13f-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span><span class="sxs-lookup"><span data-stu-id="8d13f-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [<span data-ttu-id="8d13f-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span><span class="sxs-lookup"><span data-stu-id="8d13f-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a><span data-ttu-id="8d13f-248">Métodos ID3D12GraphicsCommandList2</span><span class="sxs-lookup"><span data-stu-id="8d13f-248">ID3D12GraphicsCommandList2 methods</span></span>

* [<span data-ttu-id="8d13f-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span><span class="sxs-lookup"><span data-stu-id="8d13f-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a><span data-ttu-id="8d13f-250">Métodos ID3D12GraphicsCommandList4</span><span class="sxs-lookup"><span data-stu-id="8d13f-250">ID3D12GraphicsCommandList4 methods</span></span>

* [<span data-ttu-id="8d13f-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span><span class="sxs-lookup"><span data-stu-id="8d13f-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [<span data-ttu-id="8d13f-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span><span class="sxs-lookup"><span data-stu-id="8d13f-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
