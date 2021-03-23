---
title: Configurando e populando heaps de descritor
description: Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são aqueles que contêm descritores para os quais as tabelas de descrição podem ser usadas (no máximo uma de cada vez).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548237"
---
# <a name="setting-and-populating-descriptor-heaps"></a><span data-ttu-id="65c7d-103">Configurando e populando heaps de descritor</span><span class="sxs-lookup"><span data-stu-id="65c7d-103">Setting and Populating Descriptor Heaps</span></span>

<span data-ttu-id="65c7d-104">Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são aqueles que contêm descritores para os quais as tabelas de descrição podem ser usadas (no máximo uma de cada vez).</span><span class="sxs-lookup"><span data-stu-id="65c7d-104">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span>

-   [<span data-ttu-id="65c7d-105">Definindo heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="65c7d-105">Setting descriptor heaps</span></span>](#setting-and-populating-descriptor-heaps)
-   [<span data-ttu-id="65c7d-106">Populando heaps de descritor</span><span class="sxs-lookup"><span data-stu-id="65c7d-106">Populating descriptor heaps</span></span>](#populating-descriptor-heaps)
-   [<span data-ttu-id="65c7d-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65c7d-107">Related topics</span></span>](#related-topics)

## <a name="setting-descriptor-heaps"></a><span data-ttu-id="65c7d-108">Definindo heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="65c7d-108">Setting descriptor heaps</span></span>

<span data-ttu-id="65c7d-109">Os tipos de heap de descritores que podem ser definidos em uma lista de comandos são:</span><span class="sxs-lookup"><span data-stu-id="65c7d-109">The types of descriptor heap that can be set on a command list are:</span></span>

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

<span data-ttu-id="65c7d-110">Os heaps que estão sendo definidos na lista de comandos também devem ter sido criados como sombreador visível.</span><span class="sxs-lookup"><span data-stu-id="65c7d-110">The heaps being set on the command list must also have been created as shader visible.</span></span> <span data-ttu-id="65c7d-111">Há três tipos de lista de comandos: direta, pacote e computação.</span><span class="sxs-lookup"><span data-stu-id="65c7d-111">There are three types of command list: DIRECT, BUNDLE, and COMPUTE.</span></span>

<span data-ttu-id="65c7d-112">Depois que um heap de descritor é definido em uma lista de comandos, as chamadas subsequentes que definem tabelas de descritores se referem ao heap do descritor atual.</span><span class="sxs-lookup"><span data-stu-id="65c7d-112">After a descriptor heap is set on a command list, subsequent calls that define descriptor tables refer to the current descriptor heap.</span></span> <span data-ttu-id="65c7d-113">O estado da tabela do descritor é indefinido no início de uma lista de comandos e depois que os heaps do descritor são alterados em uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="65c7d-113">Descriptor table state is undefined at the beginning of a command list and after descriptor heaps are changed on a command list.</span></span> <span data-ttu-id="65c7d-114">A definição redundante do mesmo heap de descritor não faz com que as configurações da tabela de descritores sejam indefinidas.</span><span class="sxs-lookup"><span data-stu-id="65c7d-114">Redundantly setting the same descriptor heap does not cause descriptor table settings to be undefined.</span></span>

<span data-ttu-id="65c7d-115">Em um pacote, por outro lado, os heaps de descritor só podem ser definidos uma vez (as chamadas redundantes definindo o mesmo heap duas vezes não produzem um erro); caso contrário, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="65c7d-115">In a bundle, by contrast, the descriptor heaps can only be set once (redundant calls setting the same heap twice do not produce an error); otherwise, the behavior is undefined.</span></span> <span data-ttu-id="65c7d-116">Os heaps de descritores definidos devem corresponder ao estado quando qualquer lista de comandos chama o pacote; caso contrário, o comportamento será indefinido.</span><span class="sxs-lookup"><span data-stu-id="65c7d-116">The descriptor heaps that are set must match the state when any command list calls the bundle; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="65c7d-117">Isso permite que os pacotes herdem e editem as configurações da tabela de descritor da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="65c7d-117">This allows bundles to inherit and edit the command list’s descriptor table settings.</span></span> <span data-ttu-id="65c7d-118">Os agrupamentos que não alteram tabelas de descritores (herdam apenas delas) não precisam definir um heap de descritor e serão herdados apenas da lista de comandos de chamada.</span><span class="sxs-lookup"><span data-stu-id="65c7d-118">Bundles that don’t change descriptor tables (only inherit them) don’t need to set a descriptor heap at all and will just inherit from the calling command list.</span></span>

<span data-ttu-id="65c7d-119">Quando os heaps de descritor são definidos (usando [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), todos os heaps que estão sendo usados são definidos em uma única chamada (e todos os heaps definidos anteriormente são desdefinidos pela chamada).</span><span class="sxs-lookup"><span data-stu-id="65c7d-119">When descriptor heaps are set (using [**ID3D12GraphicsCommandList::SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), all the heaps being used are set in a single call (and all previously set heaps are unset by the call).</span></span> <span data-ttu-id="65c7d-120">No máximo um heap de cada tipo listado acima pode ser definido na chamada.</span><span class="sxs-lookup"><span data-stu-id="65c7d-120">At most one heap of each type listed above can be set in the call.</span></span>

## <a name="populating-descriptor-heaps"></a><span data-ttu-id="65c7d-121">Populando heaps de descritor</span><span class="sxs-lookup"><span data-stu-id="65c7d-121">Populating descriptor heaps</span></span>

<span data-ttu-id="65c7d-122">Depois que um aplicativo cria um heap de descritor, ele pode usar métodos no dispositivo para gerar descritores diretamente no heap ou copiar descritores de um lugar para outro.</span><span class="sxs-lookup"><span data-stu-id="65c7d-122">After an application has created a descriptor heap, it can then use methods on the device to either generate descriptors directly into the heap or copy descriptors from one place to another.</span></span>

<span data-ttu-id="65c7d-123">O conteúdo inicial da memória de heap do descritor é indefinido, portanto, fazer com que a GPU ou o driver referencie a memória não inicializada para renderização possa causar resultados indefinidos, como uma redefinição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65c7d-123">The initial contents of descriptor heap memory is undefined, so asking the GPU or driver to reference uninitialized memory for rendering can cause undefined results such as a device reset.</span></span>

<span data-ttu-id="65c7d-124">Se o aplicativo configurar um heap de descritor para ser visível da CPU, a CPU poderá chamar métodos para criar descritores no heap e copiar de um local para outro (incluindo entre heaps) de uma maneira isenta e livre de threads.</span><span class="sxs-lookup"><span data-stu-id="65c7d-124">If the application configures a descriptor heap to be CPU visible, then the CPU can call methods to create descriptors into the heap and copy from place to place (including across heaps) in an immediate, free threaded manner.</span></span> <span data-ttu-id="65c7d-125">Se o heap tiver sido configurado como SHADER_VISIBLE, a leitura pela CPU não será permitida.</span><span class="sxs-lookup"><span data-stu-id="65c7d-125">If the heap has been configured as SHADER_VISIBLE, reading by the CPU is not permitted.</span></span>



## <a name="related-topics"></a><span data-ttu-id="65c7d-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65c7d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65c7d-127">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="65c7d-127">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




