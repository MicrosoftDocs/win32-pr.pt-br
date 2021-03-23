---
title: Usar descritores diretamente na assinatura raiz
description: Os aplicativos podem colocar os descritores diretamente na assinatura raiz para evitar ter de passar por um heap de descritor.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548310"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="ea358-103">Usar descritores diretamente na assinatura raiz</span><span class="sxs-lookup"><span data-stu-id="ea358-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="ea358-104">Os aplicativos podem colocar os descritores diretamente na assinatura raiz para evitar ter de passar por um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="ea358-104">Applications can put descriptors directly in the root signature to avoid having to go through a descriptor heap.</span></span> <span data-ttu-id="ea358-105">Esses descritores demoram muito espaço na assinatura raiz (consulte a seção limites de assinatura raiz), de modo que os aplicativos precisam usá-los com moderação.</span><span class="sxs-lookup"><span data-stu-id="ea358-105">These descriptors take a lot of space in the root signature (see the root signature limits section), so applications have to use them sparingly.</span></span>

<span data-ttu-id="ea358-106">Um exemplo de uso seria colocar uma constante CBV (exibições de buffer) que está sendo alterada por empate no layout raiz para que o espaço de heap do descritor não precise ser alocado pelo aplicativo por empate (e salve o ponteiro de uma tabela de descritores no novo local no heap do descritor).</span><span class="sxs-lookup"><span data-stu-id="ea358-106">An example usage would be to place a constant buffer views (CBV) that is changing per draw in the root layout so that descriptor heap space doesn't have to be allocated by the application per draw (and save pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="ea358-107">Ao colocar algo na assinatura de raiz, o aplicativo está apenas entregando a responsabilidade de controle de versão para o driver, mas essa é a infraestrutura que eles já têm.</span><span class="sxs-lookup"><span data-stu-id="ea358-107">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver, but this is infrastructure that they already have.</span></span>

<span data-ttu-id="ea358-108">Para a renderização que usa extremamente poucos recursos, o uso de tabela/heap de descritor poderá não ser necessário se todos os descritores necessários puderem ser colocados diretamente na assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="ea358-108">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="ea358-109">Os únicos tipos de descritores com suporte na assinatura raiz são:</span><span class="sxs-lookup"><span data-stu-id="ea358-109">The only types of descriptors supported in the root signature are:</span></span>
- <span data-ttu-id="ea358-110">CBVs.</span><span class="sxs-lookup"><span data-stu-id="ea358-110">CBVs.</span></span>
- <span data-ttu-id="ea358-111">SRVs (Shader Resource views)/unordered Access views (UAVs) de recursos de buffer em que o formato SRV/UAV contém apenas componentes de 32 bit FLOAT/UINT/Santo (não há conversão de formato).</span><span class="sxs-lookup"><span data-stu-id="ea358-111">Shader Resource Views (SRVs)/Unordered Access Views (UAVs) of buffer resources where the SRV/UAV format contains only 32 bit FLOAT/UINT/SINT components (there is no format conversion).</span></span>
- <span data-ttu-id="ea358-112">SRVs de estruturas de aceleração de raytracing, em assinaturas raiz locais ou globais.</span><span class="sxs-lookup"><span data-stu-id="ea358-112">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="ea358-113">UAVs na raiz não pode ter contadores associados a eles.</span><span class="sxs-lookup"><span data-stu-id="ea358-113">UAVs in the root cannot have counters associated with them.</span></span> <span data-ttu-id="ea358-114">Os descritores na assinatura raiz aparecem cada um dos descritores individuais separados &mdash; que não podem ser indexados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="ea358-114">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="ea358-115">No exemplo acima, `mySceneData` não pode ser declarado como uma matriz, como em `cbuffer mySceneData[2]` se ele for mapeado para um descritor na assinatura raiz, já que a indexação entre descritores não é suportada na assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="ea358-115">In the above example, `mySceneData` cannot be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature, since indexing across descriptors is not supported in the root signature.</span></span> <span data-ttu-id="ea358-116">O aplicativo pode definir buffers de constantes individuais separados e defini-los como uma entrada separada na assinatura raiz, se desejado.</span><span class="sxs-lookup"><span data-stu-id="ea358-116">The application can define separate individual constant buffers and define them each as a separate entry in the root signature if desired.</span></span> <span data-ttu-id="ea358-117">Observe que, dentro de `mySceneData` acima, há uma matriz `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="ea358-117">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="ea358-118">A indexação dinâmica no buffer de constantes é válida-um descritor na assinatura raiz se comporta exatamente como o mesmo descritor se for acessado por meio de um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="ea358-118">Dynamic indexing within the constant buffer is valid - a descriptor in the root signature behaves just like the same descriptor would behave if accessed through a descriptor heap.</span></span> <span data-ttu-id="ea358-119">Isso está em contraste com constantes de inalinhamento diretamente na assinatura raiz, que também aparece como um buffer constante, exceto com a restrição de que a indexação dinâmica dentro das constantes embutidas não é permitida, portanto, `bar[2]` não seria permitida lá.</span><span class="sxs-lookup"><span data-stu-id="ea358-119">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` would not be allowed there.</span></span>

<span data-ttu-id="ea358-120">As APIs a seguir (da interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) são para definir os descritores diretamente na assinatura raiz:</span><span class="sxs-lookup"><span data-stu-id="ea358-120">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature:</span></span>

-   [<span data-ttu-id="ea358-121">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="ea358-121">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="ea358-122">**SetGraphicsRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="ea358-122">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="ea358-123">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="ea358-123">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="ea358-124">**SetGraphicsRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="ea358-124">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="ea358-125">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="ea358-125">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="ea358-126">**SetGraphicsRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="ea358-126">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> <span data-ttu-id="ea358-127">Não há nenhum conceito de "matriz de descritor raiz" no Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="ea358-127">There is no concept of a "root descriptor array" in Direct3D 12.</span></span> <span data-ttu-id="ea358-128">Só há suporte para matrizes de descritores em heaps de descritores.</span><span class="sxs-lookup"><span data-stu-id="ea358-128">Descriptor arrays are only supported in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea358-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea358-129">Related topics</span></span>

[<span data-ttu-id="ea358-130">Assinaturas raiz</span><span class="sxs-lookup"><span data-stu-id="ea358-130">Root Signatures</span></span>](root-signatures.md)
