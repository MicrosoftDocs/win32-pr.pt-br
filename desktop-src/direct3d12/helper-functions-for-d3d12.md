---
title: Funções auxiliares do D3D12
description: Essas funções auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funções auxiliares
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798366"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="7bac1-105">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="7bac1-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="7bac1-106">Essas funções auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="7bac1-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7bac1-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7bac1-107">In this section</span></span>



| <span data-ttu-id="7bac1-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="7bac1-108">Topic</span></span>                                                                                             | <span data-ttu-id="7bac1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7bac1-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bac1-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="7bac1-110">**CommandListCast**</span></span>](cd3dx12-shader-bytecode.md)<br/>                                     | <span data-ttu-id="7bac1-111">Esse modelo de função converte um ponteiro constante para qualquer lista de comandos em um ponteiro const para um ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="7bac1-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="7bac1-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="7bac1-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="7bac1-113">Calcula um índice de subrecurso para uma textura.</span><span class="sxs-lookup"><span data-stu-id="7bac1-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="7bac1-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="7bac1-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="7bac1-115">Gera a fatia MIP, a fatia da matriz e a fatia do plano que correspondem ao índice de subrecurso especificado.</span><span class="sxs-lookup"><span data-stu-id="7bac1-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="7bac1-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="7bac1-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="7bac1-117">Obtém o número de planos para o formato DXGI especificado para o adaptador virtual especificado (um **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="7bac1-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="7bac1-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="7bac1-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="7bac1-119">Indica se o layout é opaco.</span><span class="sxs-lookup"><span data-stu-id="7bac1-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="7bac1-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="7bac1-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="7bac1-121">Retorna o tipo de subobjeto que corresponde à classe base do tipo de subobjeto passado.</span><span class="sxs-lookup"><span data-stu-id="7bac1-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="7bac1-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="7bac1-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="7bac1-123">Analisa uma descrição de fluxo de estado de pipeline, chamando um retorno de chamada definido pelo usuário para cada instância de subobjeto analisada.</span><span class="sxs-lookup"><span data-stu-id="7bac1-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="7bac1-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7bac1-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="7bac1-125">Ajuda a habilitar os recursos da assinatura raiz 1,1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz.</span><span class="sxs-lookup"><span data-stu-id="7bac1-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="7bac1-126">Esse método auxiliar reconstrói uma assinatura raiz da versão 1,0 quando a versão 1,1 não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="7bac1-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="7bac1-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="7bac1-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="7bac1-128">Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados.</span><span class="sxs-lookup"><span data-stu-id="7bac1-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="7bac1-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="7bac1-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="7bac1-130">Copia uma linha de subrecurso por linha.</span><span class="sxs-lookup"><span data-stu-id="7bac1-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="7bac1-131">**Updatesubresources**</span><span class="sxs-lookup"><span data-stu-id="7bac1-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="7bac1-132">Atualiza os subrecursos, todas as matrizes de subrecurso devem ser preenchidas, normalmente chamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="7bac1-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="7bac1-133">**Updatesubresources (alocação de heap)**</span><span class="sxs-lookup"><span data-stu-id="7bac1-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="7bac1-134">Atualiza os subrecursos com uma implementação de alocação de heap.</span><span class="sxs-lookup"><span data-stu-id="7bac1-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="7bac1-135">**Updatesubresources (alocação de pilha)**</span><span class="sxs-lookup"><span data-stu-id="7bac1-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="7bac1-136">Atualiza os subrecursos com uma implementação de alocação de pilha.</span><span class="sxs-lookup"><span data-stu-id="7bac1-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="7bac1-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bac1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bac1-138">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7bac1-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="7bac1-139">Estruturas e funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="7bac1-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





