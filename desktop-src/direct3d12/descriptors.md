---
title: Descritores
description: Os descritores são a unidade primária de associação para um único recurso no D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104289"
---
# <a name="descriptors"></a><span data-ttu-id="400ba-103">Descritores</span><span class="sxs-lookup"><span data-stu-id="400ba-103">Descriptors</span></span>

<span data-ttu-id="400ba-104">Os descritores são a unidade primária de associação para um único recurso no D3D12.</span><span class="sxs-lookup"><span data-stu-id="400ba-104">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="400ba-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="400ba-105">In this section</span></span>



| <span data-ttu-id="400ba-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="400ba-106">Topic</span></span>                                                       | <span data-ttu-id="400ba-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="400ba-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="400ba-108">Visão geral dos descritores</span><span class="sxs-lookup"><span data-stu-id="400ba-108">Descriptors Overview</span></span>](descriptors-overview.md)<br/> | <span data-ttu-id="400ba-109">Os descritores são criados por chamadas à API e identificam recursos.</span><span class="sxs-lookup"><span data-stu-id="400ba-109">Descriptors are created by API calls and identify resources.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="400ba-110">Criando descritores</span><span class="sxs-lookup"><span data-stu-id="400ba-110">Creating Descriptors</span></span>](creating-descriptors.md)<br/> | <span data-ttu-id="400ba-111">Descreve e mostra exemplos de como criar exibições de índice, vértice e buffer constante; recurso de sombreador, destino de renderização, acesso não ordenado, saída de fluxo e exibições de estêncil de profundidade; e amostras.</span><span class="sxs-lookup"><span data-stu-id="400ba-111">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="400ba-112">Todos os métodos para criar descritores são threads livres.</span><span class="sxs-lookup"><span data-stu-id="400ba-112">All methods for creating descriptors are free threaded.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="400ba-113">Copiar descritores</span><span class="sxs-lookup"><span data-stu-id="400ba-113">Copying Descriptors</span></span>](copying-descriptors.md)<br/>   | <span data-ttu-id="400ba-114">Os métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) na interface do dispositivo usam a CPU para copiar imediatamente os descritores.</span><span class="sxs-lookup"><span data-stu-id="400ba-114">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="400ba-115">Eles podem ser chamados de threads livres desde que vários threads na CPU ou GPU não executem gravações potencialmente conflitantes.</span><span class="sxs-lookup"><span data-stu-id="400ba-115">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="400ba-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="400ba-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="400ba-117">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="400ba-117">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="400ba-118">Tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="400ba-118">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="400ba-119">Associação de recursos</span><span class="sxs-lookup"><span data-stu-id="400ba-119">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="400ba-120">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="400ba-120">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





