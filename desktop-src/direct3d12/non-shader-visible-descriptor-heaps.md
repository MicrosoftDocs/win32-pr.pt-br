---
title: Heaps de descritor visíveis sem sombreador
description: Alguns heaps de descritores não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparo dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível de sombreador é necessário.
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548233"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="5dbbe-103">Heaps de descritor visíveis sem sombreador</span><span class="sxs-lookup"><span data-stu-id="5dbbe-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="5dbbe-104">Alguns heaps de descritores não podem ser referenciados por sombreadores por meio de tabelas de descritor, mas existem para auxiliar o aplicativo no preparo dos descritores antes de gravar uma lista de comandos ou porque nenhum heap visível de sombreador é necessário.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="5dbbe-105">Exibições não visíveis</span><span class="sxs-lookup"><span data-stu-id="5dbbe-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="5dbbe-106">Resumo</span><span class="sxs-lookup"><span data-stu-id="5dbbe-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="5dbbe-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dbbe-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="5dbbe-108">Exibições não visíveis</span><span class="sxs-lookup"><span data-stu-id="5dbbe-108">Non-visible views</span></span>

<span data-ttu-id="5dbbe-109">Todos os heaps de descritores, incluindo os heaps de descritores acessíveis ao sombreador descritos anteriormente, podem ser manipulados pelas listas de CPU e/ou comando, dependendo do pool de memória e das propriedades de acesso da CPU que o aplicativo seleciona para um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="5dbbe-110">Para [heaps de descritor visíveis do sombreador](shader-visible-descriptor-heaps.md), o motivo óbvio para negar o acesso do sombreador a esses heaps de descritor é enquanto eles estão sendo preparados.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="5dbbe-111">Em seguida, esses heaps tornam-se visíveis ao sombreador e acessados por meio de tabelas de descritores na execução da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="5dbbe-112">No entanto, não há nenhum requisito para preparar os heaps visíveis do sombreador, eles podem ser preenchidos diretamente.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="5dbbe-113">Outros descritores são vinculados ao pipeline com seu conteúdo registrado diretamente na lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="5dbbe-114">Esses descritores só servem para converter os parâmetros de exibição no tempo de registro da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="5dbbe-115">Esses heaps sempre são visíveis sem sombreador e contêm o seguinte.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="5dbbe-116">Renderizar exibições de destino (RTVs)</span><span class="sxs-lookup"><span data-stu-id="5dbbe-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="5dbbe-117">Exibições de estêncil de profundidade (DSVs)</span><span class="sxs-lookup"><span data-stu-id="5dbbe-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="5dbbe-118">As exibições do buffer de índice (IBVs), as exibições de buffer de vértice (VBVs) e as exibições de saída de fluxo (SOVs) são passadas diretamente para métodos de API, não têm tipos de heap específicos.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="5dbbe-119">Após a gravação na lista de comandos (com uma chamada como [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), por exemplo), a memória usada para manter os descritores dessa chamada estará imediatamente disponível para reutilização após a chamada.</span><span class="sxs-lookup"><span data-stu-id="5dbbe-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="5dbbe-120">Até mesmo as tabelas de descritor têm opções em que um aplicativo pode permitir que a implementação escolha registrar o conteúdo da tabela na gravação da lista de comandos (em vez de desreferenciar o ponteiro da tabela na execução).</span><span class="sxs-lookup"><span data-stu-id="5dbbe-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="5dbbe-121">Resumo</span><span class="sxs-lookup"><span data-stu-id="5dbbe-121">Summary</span></span>



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | <span data-ttu-id="5dbbe-122">**sombreador visível, CPU somente gravação**</span><span class="sxs-lookup"><span data-stu-id="5dbbe-122">**shader visible, CPU write only**</span></span> | <span data-ttu-id="5dbbe-123">**Não-sombreador visível, CPU de leitura/gravação**</span><span class="sxs-lookup"><span data-stu-id="5dbbe-123">**non-shader visible, CPU read/write**</span></span> |
| <span data-ttu-id="5dbbe-124">**CBV, SRV, UAV**</span><span class="sxs-lookup"><span data-stu-id="5dbbe-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="5dbbe-125">sim</span><span class="sxs-lookup"><span data-stu-id="5dbbe-125">yes</span></span>                                | <span data-ttu-id="5dbbe-126">sim</span><span class="sxs-lookup"><span data-stu-id="5dbbe-126">yes</span></span>                                    |
| <span data-ttu-id="5dbbe-127">**CORES**</span><span class="sxs-lookup"><span data-stu-id="5dbbe-127">**SAMPLER**</span></span>       | <span data-ttu-id="5dbbe-128">sim</span><span class="sxs-lookup"><span data-stu-id="5dbbe-128">yes</span></span>                                | <span data-ttu-id="5dbbe-129">sim</span><span class="sxs-lookup"><span data-stu-id="5dbbe-129">yes</span></span>                                    |
| <span data-ttu-id="5dbbe-130">**DAF**</span><span class="sxs-lookup"><span data-stu-id="5dbbe-130">**RTV**</span></span>           | <span data-ttu-id="5dbbe-131">não</span><span class="sxs-lookup"><span data-stu-id="5dbbe-131">no</span></span>                                 | <span data-ttu-id="5dbbe-132">sim</span><span class="sxs-lookup"><span data-stu-id="5dbbe-132">yes</span></span>                                    |
| <span data-ttu-id="5dbbe-133">**DSV**</span><span class="sxs-lookup"><span data-stu-id="5dbbe-133">**DSV**</span></span>           | <span data-ttu-id="5dbbe-134">não</span><span class="sxs-lookup"><span data-stu-id="5dbbe-134">no</span></span>                                 | <span data-ttu-id="5dbbe-135">sim</span><span class="sxs-lookup"><span data-stu-id="5dbbe-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="5dbbe-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dbbe-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dbbe-137">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="5dbbe-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




