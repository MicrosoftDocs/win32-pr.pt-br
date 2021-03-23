---
title: Sistemas com vários adaptadores
description: Descreve o suporte no Direct3D 12 para sistemas que têm vários adaptadores instalados, abrangendo cenários em que seu aplicativo se destina explicitamente a vários adaptadores de GPU e cenários em que os drivers usam implicitamente vários adaptadores de GPU em nome do seu aplicativo.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d7d3985c880c4d1732a96b98ac6d3c6579dab8e6
ms.sourcegitcommit: 9d530b0a2396f2274e9ed693c1f5f10556aadebb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/09/2020
ms.locfileid: "104548215"
---
# <a name="multi-adapter-systems"></a>Sistemas com vários adaptadores

Descreve o suporte no Direct3D 12 para sistemas que têm vários adaptadores instalados, abrangendo cenários em que seu aplicativo se destina explicitamente a vários adaptadores de GPU e cenários em que os drivers usam implicitamente vários adaptadores de GPU em nome do seu aplicativo.

## <a name="multi-adapter-overview"></a>Visão geral de vários adaptadores

Um adaptador de GPU pode ser qualquer adaptador (gráficos ou computação, discretos ou integrados), de qualquer fabricante que ofereça suporte ao Direct3D 12.

Vários adaptadores são referenciados como *nós*. Vários elementos, como as filas, se aplicam a cada nó, portanto, se houver dois nós, haverá duas filas 3D padrão. Outros elementos, como o estado do pipeline e as assinaturas raiz e de comando, podem fazer referência a um ou mais ou a todos os nós, conforme mostrado no diagrama.

![filas se aplicam a cada adaptador de gráficos](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Compartilhando heaps entre adaptadores

Consulte o tópico [heaps compartilhados](shared-heaps.md) .

## <a name="multi-adapter-apis-and-node-masks"></a>APIs de vários adaptadores e máscaras de nó

Semelhante às APIs do Direct3D anteriores, cada conjunto de adaptadores vinculados é enumerado como um único objeto [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) . Todas as saídas anexadas a qualquer adaptador no link são enumeradas como anexadas ao único objeto **IDXGIAdapter3** .

Seu aplicativo pode determinar o número de adaptadores físicos associados a um determinado dispositivo chamando [**ID3D12Device:: GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount).

Muitas APIs no Direct3D 12 aceitam uma *máscara de nó* (uma máscara de bits), que indica o conjunto de nós aos quais a chamada à API se refere. Cada nó tem um índice baseado em zero. Mas na máscara do nó, zero é convertido para o bit 1; 1 converte para o bit 2; e assim por diante.

### <a name="single-nodes"></a>Nós únicos

Ao chamar as seguintes APIs (nó único), seu aplicativo especifica um único nó com o qual a chamada à API será associada. Na maioria das vezes, isso é especificado por uma máscara de nó. Cada bit na máscara corresponde a um único nó. Para todas as APIs descritas nesta seção, você deve definir exatamente um bit na máscara do nó.

-   [**D3D12 \_ Fila de comandos \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) : tem um membro *NodeMask* .
-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : cria uma fila de uma [**estrutura \_ \_ \_ desc de fila de comandos D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**Createcommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : usa um parâmetro *nodeMask* .
-   [**D3D12 \_ HEAP de DESCRITOr \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) : tem um membro *NodeMask* .
-   [**CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) : cria um heap de descritor de uma estrutura [**\_ desc de \_ heap \_ de descritor de D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) .
-   [**D3D12 \_ HEAP de consulta \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) : tem um membro *NodeMask* .
-   [**CreateQueryHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) : cria um heap de consulta de uma estrutura [**\_ desc de \_ heap \_ de consulta D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) .

### <a name="multiple-nodes"></a>Vários nós

Ao chamar as seguintes APIs (vários nós), seu aplicativo especifica um conjunto de nós com os quais a chamada à API será associada. Você especifica a afinidade de nó como uma máscara de nó, potencialmente com vários bits definidos. Se o seu aplicativo passar 0 para essa máscara de bits, o driver do Direct3D 12 converterá isso na máscara de bits 1 (indicando que o objeto está associado ao nó 0).

-   [**D3D12 \_ \_Camada de \_ compartilhamento \_ entre nós**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) : determina o suporte para compartilhamento entre nós.
-   [**D3D12 \_ \_Opções de \_ D3D12 \_ de dados de recurso**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : estrutura que faz referência à [**\_ \_ \_ \_ camada de compartilhamento entre nós D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier).
-   [**D3D12 \_ \_ \_ Arquitetura de dados de recurso**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) : contém um membro *NodeIndex* .
-   [**D3D12 \_ Estado do pipeline de gráficos \_ \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : tem um membro *NodeMask* .
-   [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) : cria um objeto de estado de pipeline de gráficos a partir de uma estrutura [**desc de estado de \_ pipeline de gráficos \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .
-   [**D3D12 \_ Estado do pipeline de computação \_ \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) : tem um membro *NodeMask* .
-   [**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) : cria um objeto de estado de pipeline de computação a partir de uma estrutura [**desc de estado de \_ pipeline de computação \_ \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .
-   [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature): usa um parâmetro *nodeMask* .
-   [**D3D12 \_ Assinatura de comando \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc): tem um membro *NodeMask* .
-   [**CreateCommandSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) : cria um objeto de assinatura de comando de uma estrutura [**\_ desc de \_ assinatura \_ de comando D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc) .

### <a name="resource-creation-apis"></a>APIs de criação de recursos

As APIs a seguir fazem referência a máscaras de nó.

-   [**D3D12 \_ \_Propriedades de heap**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : tem membros *CreationNodeMask* e *VisibleNodeMask* .
-   [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) : tem um parâmetro *visibleMask* .
-   [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) : tem um parâmetro *nodeMask* .

Ao criar um recurso reservado, nenhum índice ou máscara de nó é especificado. O recurso reservado pode ser mapeado em um heap em qualquer nó (seguindo as regras de compartilhamento entre nós).

O método [**MakeResident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) funciona internamente com filas de adaptadores, não há necessidade de que seu aplicativo especifique nada para isso.

Ao chamar as seguintes APIs [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) , seu aplicativo não precisa especificar um conjunto de nós ao qual a chamada à API será associada, pois a chamada à API se aplica a todos os nós.

-   [**Createfence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**Createsampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) : com uma *cerca* como um parâmetro. Com um *recurso* ou um *heap* como parâmetros, esse método não aceita nós como parâmetros porque as máscaras de nó são herdadas dos objetos criados anteriormente.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)