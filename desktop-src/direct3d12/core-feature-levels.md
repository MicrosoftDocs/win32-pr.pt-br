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
# <a name="the-direct3d-12-core-10-feature-level"></a>O nível de recurso do Direct3D 12 Core 1.0

O nível de recurso Core 1,0 é um subconjunto do conjunto de recursos completo do Direct3D 12. O nível de recurso do Core 1,0 pode ser exposto por uma categoria de dispositivos conhecida como *dispositivos somente de computação*. O modelo de driver geral para dispositivos somente de computação é o MCDM (modelo de driver de computação da Microsoft). MCDM é um par reduzido para baixo do WDDM (modelo de driver de dispositivo) do Windows, que tem um escopo maior.

Um dispositivo que dá suporte *apenas* aos recursos dentro de um nível de recurso principal é conhecido como um *dispositivo principal*.

> [!NOTE]
> *Dispositivo somente de computação*, dispositivo *MCDM*, *dispositivo de nível de recurso principal* e *dispositivo de núcleo* , todos significam a mesma coisa. Preferiremos o *dispositivo principal* para simplificar a simplicidade.

## <a name="creating-a-core-device"></a>Criando um dispositivo principal

Em geral, para criar um dispositivo Direct3D 12, você chama a função [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) e especifica um nível de recurso mínimo.

Se você especificar um nível de recurso de 9 a 12, o dispositivo retornado será um dispositivo repleto de recursos, como uma GPU tradicional (que dá suporte a um superconjunto da funcionalidade de um dispositivo principal). Um dispositivo principal nunca é retornado para esse intervalo de níveis de recurso.

Por outro lado, se você especificar um nível de recurso principal (por exemplo, [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), o dispositivo retornado poderá ser repleto de recursos ou pode ser um dispositivo principal.

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

Se você especificar um `_CORE` nível de recurso, a camada de tempo de execução/depuração validará que os recursos usados pelo aplicativo são permitidos por esse `_CORE` nível de recurso. Esse conjunto de recursos é definido mais adiante neste tópico.

## <a name="shader-model-for-core-devices"></a>Modelo de sombreador para dispositivos principais

Um dispositivo principal dá suporte ao modelo de sombreador 5.0 +.

O tempo de execução executa a conversão de modelos de sombreador não DXIL de 5. x para 6,0 DXIL. Portanto, o driver precisa dar suporte apenas a 6. x.

## <a name="resource-management-model-for-core-devices"></a>Modelo de gerenciamento de recursos para dispositivos principais

- Dimensões de recurso com suporte: somente buffers brutos e estruturados (sem buffers de tipo, texture1d/2D etc.)
- Não há suporte para recursos reservados (lado a lado)
- Não há suporte para heaps personalizados
- Não há suporte para nenhum desses sinalizadores de heap:
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Observe que os atomicers do sombreador são necessários, esse sinalizador é para outro recurso, Atomic-adaptadores)

## <a name="resource-binding-model-for-core-devices"></a>Modelo de associação de recursos para dispositivos principais

- Suporte apenas para camada 1 de associação de recursos
- Exceções:
  - Não há suporte para amostragens de textura
  - Suporte para 64 UAVs, como o nível de recurso 11.1 + (em oposição a apenas 8)
  - As implementações não precisam implementar a verificação de limites em acessos de sombreador aos recursos por meio de descritores, os acessos fora dos limites produzem um comportamento indefinido.
    - Como um subproduto, não há suporte para o sinalizador de intervalo do descritor D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS em assinaturas raiz.
- Os descritores de UAV/CBV só podem ser feitos em recursos de heaps padrão (portanto, não há heaps de upload/readback). Isso força seu aplicativo a fazer cópias para obter dados entre a CPU< >GPU.
- Apesar de ser a camada de funcionalidade de associação mais baixa, ainda há alguns recursos necessários até mesmo nesta camada vale a pena chamar:
  - Os heaps de descritores podem ser atualizados depois que as listas de comandos são registradas (consulte D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE na especificação de associação de recursos)
  - Descritores de raiz são basicamente ponteiros GPUVA
    - Embora não haja suporte a MMU/VA, os VAs de buffer que são usados nos descritores de raiz podem ser emulados por implementações, resolvendo patches.

### <a name="structured-buffer-restrictions"></a>Restrições de buffer estruturado

Os buffers estruturados devem ter um endereço base com 4 bytes alinhados e o stride deve ser 2 ou um múltiplo de 4. O caso de um stride de 2 é para aplicativos com dados de 16 bits, particularmente dado que não há suporte para buffers tipados no D3D_FEATURE_LEVEL_1_0_CORE.

O stride especificado nos descritores deve corresponder ao Stride especificado em HLSL.  

## <a name="command-queue-support-for-core-devices"></a>Suporte de fila de comando para dispositivos principais

Somente as filas de computação e cópia (sem 3D, vídeo, etc. filas).

## <a name="shader-support-for-core-devices"></a>Suporte a sombreador para dispositivos principais

Somente sombreadores de computação, nenhum sombreador de gráficos (vértice, sombreadores de pixel etc.) nem qualquer funcionalidade relacionada, como destinos de renderização, cadeias de permuta, montadores de entrada.

### <a name="arithmetic-precision"></a>Precisão aritmética

Os dispositivos principais não precisam dar suporte a normas para operações de ponto flutuante de 16 bits.

## <a name="supported-apis-for-core-devices"></a>APIs com suporte para dispositivos principais

A lista a seguir representa o subconjunto com suporte da interface de programação de aplicativo completa (as APIs que *não* têm suporte no nível de recurso Core 1,0 *não* estão listadas).

### <a name="id3d12device-methods"></a>Métodos ID3D12Device

* [ID3D12Device::CheckFeatureSupport](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device::CopyDescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device::CopyDescriptorsSimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device::CreateCommandAllocator](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device:: createcommandlist](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device::CreateCommandQueue](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device::CreateCommandSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device::CreateCommittedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device::CreateComputePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device::CreateConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device::CreateDescriptorHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device:: createfence](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device:: createheap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device::CreatePlacedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device::CreateQueryHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device::CreateRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device::CreateShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device::CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device::CreateUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device:: remover](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device::GetAdapterLuid](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device:: GetCopyableFootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device::GetCustomHeapProperties](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device::GetDescriptorHandleIncrementSize](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device::GetDeviceRemovedReason](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device::GetNodeCount](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device::MakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device::OpenSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device::OpenSharedHandleByName](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device::SetStablePowerState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>Métodos ID3D12Device1

* [ID3D12Device1::CreatePipelineLibrary](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1::SetEventOnMultipleFenceCompletion](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>Métodos ID3D12Device2

* [ID3D12Device2:: createpipelinestate](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>Métodos ID3D12Device3

* [ID3D12Device3::OpenExistingHeapFromAddress](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3::EnqueueMakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>Métodos ID3D12Device4

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>Métodos ID3D12Device5

* [ID3D12Device5::CreateMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5:: createstateobject](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5::EnumerateMetaCommandParameters](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5::EnumerateMetaCommands](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5::RemoveDevice](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>Métodos ID3D12CommandQueue

* [ID3D12CommandQueue::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue:: endEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue::ExecuteCommandLists](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue::GetClockCalibration](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue:: GetDesc](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue::GetTimestampFrequency](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue:: setmarcer](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue:: Signal](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue:: aguardar](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>Métodos ID3D12CommandList

* [ID3D12CommandList:: GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>Métodos ID3D12GraphicsCommandList

* [ID3D12GraphicsCommandList::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList::BeginQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList:: Clearstate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList:: fechar](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList::CopyBufferRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList::CopyResource](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList::CopyTextureRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList::D ispatch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList:: endEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList:: endquery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList:: Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList::ResolveQueryData](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList::ResourceBarrier](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList::SetComputeRootConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList::SetComputeRootDescriptorTable](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList::SetComputeRootShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList::SetComputeRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList::SetDescriptorHeaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList:: setmarcer](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList:: setpipelinestate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList::SetPredication](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>Métodos ID3D12GraphicsCommandList1

* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>Métodos ID3D12GraphicsCommandList2

* [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>Métodos ID3D12GraphicsCommandList4

* [ID3D12GraphicsCommandList4::ExecuteMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4::InitializeMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
