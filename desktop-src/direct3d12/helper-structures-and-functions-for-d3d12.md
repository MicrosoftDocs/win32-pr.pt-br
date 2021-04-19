---
title: Estruturas e funções auxiliares do D3D12
description: Essas estruturas auxiliares e funções auxiliares são declaradas em d3dx12. h.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Funções auxiliares
- Estruturas auxiliares
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769637"
---
# <a name="helper-structures-and-functions-for-d3d12"></a><span data-ttu-id="998ba-106">Estruturas e funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="998ba-106">Helper Structures and Functions for D3D12</span></span>

<span data-ttu-id="998ba-107">Essas estruturas auxiliares e funções auxiliares são declaradas em **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="998ba-107">These helper structures and helper functions are declared in **d3dx12.h**.</span></span>

<span data-ttu-id="998ba-108">Você pode usar essas estruturas auxiliares para criar e inicializar estruturas do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="998ba-108">You can use these helper structures to create and initialize Direct3D structures.</span></span> <span data-ttu-id="998ba-109">Essas estruturas auxiliares se comportam como classes C++.</span><span class="sxs-lookup"><span data-stu-id="998ba-109">These helper structures behave like C++ classes.</span></span> <span data-ttu-id="998ba-110">Cada estrutura auxiliar normalmente tem um construtor padrão, um construtor explícito, um destruidor e um operador cast para a estrutura D3D12 associada.</span><span class="sxs-lookup"><span data-stu-id="998ba-110">Each helper structure typically has a default constructor, an explicit constructor, a destructor, and a cast operator for the associated D3D12 structure.</span></span> <span data-ttu-id="998ba-111">Cada estrutura auxiliar tem um prefixo ' C' e está associada a uma estrutura D3D12 que não tem o prefixo ' C'.</span><span class="sxs-lookup"><span data-stu-id="998ba-111">Each helper structure has a 'C' prefix and is associated with a D3D12 structure which lacks the 'C' prefix.</span></span> <span data-ttu-id="998ba-112">A maioria das estruturas auxiliares contém métodos de inicialização de membros, alguns contêm funções de comparação.</span><span class="sxs-lookup"><span data-stu-id="998ba-112">Most helper structures contain initialization member methods, some contain comparison functions.</span></span>

<span data-ttu-id="998ba-113">**d3dx12. h** está disponível separadamente dos cabeçalhos do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="998ba-113">**d3dx12.h** is available separately from the Direct3D 12 headers.</span></span> <span data-ttu-id="998ba-114">Você pode baixar o **d3dx12. h** da [biblioteca auxiliar do D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span><span class="sxs-lookup"><span data-stu-id="998ba-114">You can download **d3dx12.h** from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="998ba-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="998ba-115">In this section</span></span>



| <span data-ttu-id="998ba-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="998ba-116">Topic</span></span>                                                                     | <span data-ttu-id="998ba-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="998ba-117">Description</span></span>                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="998ba-118">Interfaces auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="998ba-118">Helper Interfaces for D3D12</span></span>](helper-interfaces-for-d3d12.md)<br/> | <span data-ttu-id="998ba-119">Essas interfaces auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="998ba-119">These helper interfaces help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>        |
| [<span data-ttu-id="998ba-120">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="998ba-120">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)<br/> | <span data-ttu-id="998ba-121">Essas estruturas auxiliares ajudam a inicializar muitas das estruturas do Direct3D 12 e são declaradas em **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="998ba-121">These helper structures help initialize many of the Direct3D 12 structures, and are declared in **d3dx12.h**.</span></span><br/> |
| [<span data-ttu-id="998ba-122">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="998ba-122">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)<br/>   | <span data-ttu-id="998ba-123">Essas funções auxiliares ajudam particularmente na manipulação de subrecursos e são declaradas em **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="998ba-123">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="998ba-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="998ba-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="998ba-125">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="998ba-125">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





