---
title: Subalocação em buffers
description: Os buffers têm todos os recursos necessários no D3D12 para que os aplicativos transfiram uma grande variedade de dados transitórios da CPU para a GPU. Esta seção aborda quatro cenários comuns para o uso e o gerenciamento de recursos e buffers.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104680"
---
# <a name="suballocation-within-buffers"></a><span data-ttu-id="563c3-104">Subalocação em buffers</span><span class="sxs-lookup"><span data-stu-id="563c3-104">Suballocation Within Buffers</span></span>

<span data-ttu-id="563c3-105">Os buffers têm todos os recursos necessários no D3D12 para que os aplicativos transfiram uma grande variedade de dados transitórios da CPU para a GPU.</span><span class="sxs-lookup"><span data-stu-id="563c3-105">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="563c3-106">Esta seção aborda quatro cenários comuns para o uso e o gerenciamento de recursos e buffers.</span><span class="sxs-lookup"><span data-stu-id="563c3-106">This section covers four common scenarios for the use and management of resources and buffers.</span></span>

<span data-ttu-id="563c3-107">Semelhante ao D3D11, os aplicativos no D3D12 ainda precisam declarar o uso da memória ao alocar buffers em D3D12 em comparação com os recursos dinâmicos/de preparo no D3D11, mas, em D3D12, os desenvolvedores têm mais flexibilidade e controle mais rígido sobre o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="563c3-107">Similar to D3D11, applications in D3D12 still need to declare the usage of memory when allocating buffers in D3D12 compared to Dynamic/Staging Resources in D3D11, but in D3D12, developers have more flexibility and tighter control over memory usage.</span></span> <span data-ttu-id="563c3-108">Os buffers, por meio da subalocação, têm todos os recursos necessários para o gerenciamento de memória de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="563c3-108">Buffers, through suballocation, have all the features necessary for low-level memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="563c3-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="563c3-109">In this section</span></span>



| <span data-ttu-id="563c3-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="563c3-110">Topic</span></span>                                                                                        | <span data-ttu-id="563c3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="563c3-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="563c3-112">Carregando diferentes tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="563c3-112">Uploading Different Types of Resources</span></span>](uploading-resources.md)<br/>                 | <span data-ttu-id="563c3-113">Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como subalocar e posicionar corretamente os dados nos buffers.</span><span class="sxs-lookup"><span data-stu-id="563c3-113">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="563c3-114">O uso de um único buffer aumenta a flexibilidade do uso de memória e fornece aos aplicativos um controle mais rígido do uso de memória.</span><span class="sxs-lookup"><span data-stu-id="563c3-114">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="563c3-115">Também mostra as diferenças entre os modelos D3D11 e D3D12 para carregar diferentes tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="563c3-115">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span><br/> |
| [<span data-ttu-id="563c3-116">Carregando dados de textura por meio de buffers</span><span class="sxs-lookup"><span data-stu-id="563c3-116">Uploading Texture Data Through Buffers</span></span>](upload-and-readback-of-texture-data.md)<br/> | <span data-ttu-id="563c3-117">Carregar dados de textura 2D ou 3D é semelhante a carregar dados 1D, exceto que os aplicativos precisam prestar mais atenção ao alinhamento de dados relacionado à densidade da linha.</span><span class="sxs-lookup"><span data-stu-id="563c3-117">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="563c3-118">Os buffers podem ser usados de forma ortogonal e simultânea de várias partes do pipeline de gráficos e são muito flexíveis.</span><span class="sxs-lookup"><span data-stu-id="563c3-118">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span> <br/>                                                                                                                       |
| [<span data-ttu-id="563c3-119">Ler dados por meio de um buffer</span><span class="sxs-lookup"><span data-stu-id="563c3-119">Read back data via a buffer</span></span>](readback-data-using-heaps.md)<br/>                    | <span data-ttu-id="563c3-120">Ler dados de volta da GPU, como capturar uma captura de tela, envolve o uso do heap readback.</span><span class="sxs-lookup"><span data-stu-id="563c3-120">Reading back data from the GPU, such as capturing a screen shot, involves the use of the Readback heap.</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="563c3-121">Gerenciamento de recursos baseado em isolamento</span><span class="sxs-lookup"><span data-stu-id="563c3-121">Fence-Based Resource Management</span></span>](fence-based-resource-management.md)<br/>            | <span data-ttu-id="563c3-122">Mostra como gerenciar o tempo de vida de dados de recursos rastreando o progresso da GPU por meio de limites.</span><span class="sxs-lookup"><span data-stu-id="563c3-122">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="563c3-123">A memória pode ser efetivamente reutilizada com limites que gerenciam cuidadosamente a disponibilidade de espaço livre na memória, como em uma implementação de buffer de anéis para um heap de carregamento.</span><span class="sxs-lookup"><span data-stu-id="563c3-123">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span> <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="563c3-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="563c3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="563c3-125">Gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="563c3-125">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





