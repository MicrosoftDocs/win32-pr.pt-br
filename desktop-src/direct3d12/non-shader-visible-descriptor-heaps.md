---
title: Heaps de descritores não visíveis do sombreador
description: Alguns heaps de descritor não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparação dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível para sombreador é necessário.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51d30c7a99250ee0842b79d76ccebb6150bcf9a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343451"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="5c60e-103">Heaps de descritores não visíveis do sombreador</span><span class="sxs-lookup"><span data-stu-id="5c60e-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="5c60e-104">Alguns heaps de descritor não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparação dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível para sombreador é necessário.</span><span class="sxs-lookup"><span data-stu-id="5c60e-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="5c60e-105">Exibições não visíveis</span><span class="sxs-lookup"><span data-stu-id="5c60e-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="5c60e-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5c60e-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="5c60e-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c60e-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="5c60e-108">Exibições não visíveis</span><span class="sxs-lookup"><span data-stu-id="5c60e-108">Non-visible views</span></span>

<span data-ttu-id="5c60e-109">Todos os heaps de descritor, incluindo os heaps de descritor acessíveis do sombreador descritos anteriormente, podem ser manipulados pelas listas de CPU e/ou comando, dependendo do pool de memória e das propriedades de acesso à CPU que o aplicativo seleciona para um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="5c60e-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="5c60e-110">Para heaps de [descritor](shader-visible-descriptor-heaps.md)visíveis do sombreador , o motivo óbvio para negar o acesso do sombreador a esses heaps de descritor é quando eles estão sendo analisados.</span><span class="sxs-lookup"><span data-stu-id="5c60e-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="5c60e-111">Em seguida, esses heaps ficam visíveis para sombreador e acessados por meio de tabelas de descritor na execução da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5c60e-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="5c60e-112">No entanto, não há nenhum requisito para o estágio de heaps visíveis para sombreador, eles podem ser populados diretamente.</span><span class="sxs-lookup"><span data-stu-id="5c60e-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="5c60e-113">Outros descritores são vinculados ao pipeline fazendo com que seu conteúdo seja registrado diretamente na lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5c60e-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="5c60e-114">Esses descritores servem apenas para converter os parâmetros de exibição no tempo de registro da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5c60e-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="5c60e-115">Esses heaps são sempre visíveis sem sombreador e contêm o seguinte.</span><span class="sxs-lookup"><span data-stu-id="5c60e-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="5c60e-116">Renderizar exibições de destino (RTVs)</span><span class="sxs-lookup"><span data-stu-id="5c60e-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="5c60e-117">DSVs (exibições de estêncil de profundidade)</span><span class="sxs-lookup"><span data-stu-id="5c60e-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="5c60e-118">IBVs (Exibições de Buffer de Índice), VBVs (Exibições de Buffer de VBVs) e SOVs (Exibições de Saída de Fluxo) são passados diretamente para métodos de API, não têm tipos de heap específicos.</span><span class="sxs-lookup"><span data-stu-id="5c60e-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="5c60e-119">Depois de gravar na lista de comandos (com uma chamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por exemplo), a memória usada para manter os descritores para essa chamada fica imediatamente disponível para rea uso após a chamada.</span><span class="sxs-lookup"><span data-stu-id="5c60e-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="5c60e-120">Até mesmo tabelas de descritor têm opções em que um aplicativo pode permitir que a implementação opte por registrar o conteúdo da tabela na gravação da lista de comandos (em vez de desreferenciar o ponteiro de tabela em execução).</span><span class="sxs-lookup"><span data-stu-id="5c60e-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="5c60e-121">Resumo</span><span class="sxs-lookup"><span data-stu-id="5c60e-121">Summary</span></span>



|                   | <span data-ttu-id="5c60e-122">Sombreador visível, somente gravação de CPU</span><span class="sxs-lookup"><span data-stu-id="5c60e-122">Shader visible, CPU write only</span></span>                                   | <span data-ttu-id="5c60e-123">Não-sombreador visível, CPU de leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5c60e-123">Non-shader visible, CPU read/write</span></span>                                       |
|-------------------|------------------------------------|----------------------------------------|
| <span data-ttu-id="5c60e-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="5c60e-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="5c60e-125">sim</span><span class="sxs-lookup"><span data-stu-id="5c60e-125">yes</span></span>                                | <span data-ttu-id="5c60e-126">sim</span><span class="sxs-lookup"><span data-stu-id="5c60e-126">yes</span></span>                                    |
| <span data-ttu-id="5c60e-127">**CORES**</span><span class="sxs-lookup"><span data-stu-id="5c60e-127">**SAMPLER**</span></span>       | <span data-ttu-id="5c60e-128">sim</span><span class="sxs-lookup"><span data-stu-id="5c60e-128">yes</span></span>                                | <span data-ttu-id="5c60e-129">sim</span><span class="sxs-lookup"><span data-stu-id="5c60e-129">yes</span></span>                                    |
| <span data-ttu-id="5c60e-130">**DAF**</span><span class="sxs-lookup"><span data-stu-id="5c60e-130">**RTV**</span></span>           | <span data-ttu-id="5c60e-131">não</span><span class="sxs-lookup"><span data-stu-id="5c60e-131">no</span></span>                                 | <span data-ttu-id="5c60e-132">sim</span><span class="sxs-lookup"><span data-stu-id="5c60e-132">yes</span></span>                                    |
| <span data-ttu-id="5c60e-133">**DSV**</span><span class="sxs-lookup"><span data-stu-id="5c60e-133">**DSV**</span></span>           | <span data-ttu-id="5c60e-134">não</span><span class="sxs-lookup"><span data-stu-id="5c60e-134">no</span></span>                                 | <span data-ttu-id="5c60e-135">sim</span><span class="sxs-lookup"><span data-stu-id="5c60e-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="5c60e-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c60e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c60e-137">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="5c60e-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




