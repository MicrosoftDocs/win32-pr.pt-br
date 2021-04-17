---
title: Objeto downloadcollection
description: Objeto downloadcollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Armazenamentos online do Windows Media Player, objeto Downloadcollection
- repositórios online, objeto Downloadcollection
- tipo 2 lojas online, objeto Downloadcollection
- Downloadcollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8275cbd2661bdce9c428800206c14b9c55942c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761468"
---
# <a name="downloadcollection-object"></a><span data-ttu-id="b9526-107">Objeto downloadcollection</span><span class="sxs-lookup"><span data-stu-id="b9526-107">DownloadCollection Object</span></span>

> [!Note]  
> <span data-ttu-id="b9526-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="b9526-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b9526-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="b9526-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b9526-110">O objeto **downloadcollection** contém propriedades e métodos para lidar com coleções de itens de download.</span><span class="sxs-lookup"><span data-stu-id="b9526-110">The **DownloadCollection** object contains properties and methods to handle collections of download items.</span></span> <span data-ttu-id="b9526-111">Ele pode ser usado por páginas da Web hospedadas no modo completo do Windows Media Player e que têm acesso ao objeto **externo** , como lojas online.</span><span class="sxs-lookup"><span data-stu-id="b9526-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as online stores.</span></span>

<span data-ttu-id="b9526-112">O objeto **downloadcollection** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9526-112">The **DownloadCollection** object supports the following properties.</span></span>



| <span data-ttu-id="b9526-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b9526-113">Property</span></span>                              | <span data-ttu-id="b9526-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9526-114">Description</span></span>                                  |
|---------------------------------------|----------------------------------------------|
| [<span data-ttu-id="b9526-115">contagem</span><span class="sxs-lookup"><span data-stu-id="b9526-115">count</span></span>](downloadcollection-count.md) | <span data-ttu-id="b9526-116">Recupera o número de downloads pendentes.</span><span class="sxs-lookup"><span data-stu-id="b9526-116">Retrieves the number of pending downloads.</span></span>   |
| [<span data-ttu-id="b9526-117">id</span><span class="sxs-lookup"><span data-stu-id="b9526-117">id</span></span>](downloadcollection-id.md)       | <span data-ttu-id="b9526-118">Recupera a ID da coleção de download.</span><span class="sxs-lookup"><span data-stu-id="b9526-118">Retrieves the ID of the download collection.</span></span> |



 

<span data-ttu-id="b9526-119">O objeto **downloadcollection** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9526-119">The **DownloadCollection** object supports the following methods.</span></span>



| <span data-ttu-id="b9526-120">Método</span><span class="sxs-lookup"><span data-stu-id="b9526-120">Method</span></span>                                                | <span data-ttu-id="b9526-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9526-121">Description</span></span>                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="b9526-122">Limpar</span><span class="sxs-lookup"><span data-stu-id="b9526-122">Clear</span></span>](downloadcollection-clear.md)                 | <span data-ttu-id="b9526-123">Remove todos os itens de uma coleção de download.</span><span class="sxs-lookup"><span data-stu-id="b9526-123">Removes all items from a download collection.</span></span> |
| [<span data-ttu-id="b9526-124">item</span><span class="sxs-lookup"><span data-stu-id="b9526-124">item</span></span>](downloadcollection-item.md)                   | <span data-ttu-id="b9526-125">Recupera um objeto de download pendente.</span><span class="sxs-lookup"><span data-stu-id="b9526-125">Retrieves a pending download object.</span></span>          |
| [<span data-ttu-id="b9526-126">removeItem</span><span class="sxs-lookup"><span data-stu-id="b9526-126">removeItem</span></span>](downloadcollection-removeitem.md)       | <span data-ttu-id="b9526-127">Remove um item de download de uma coleção.</span><span class="sxs-lookup"><span data-stu-id="b9526-127">Removes a download item from a collection.</span></span>    |
| [<span data-ttu-id="b9526-128">startDownload</span><span class="sxs-lookup"><span data-stu-id="b9526-128">startDownload</span></span>](downloadcollection-startdownload.md) | <span data-ttu-id="b9526-129">Enfileira um download.</span><span class="sxs-lookup"><span data-stu-id="b9526-129">Queues a download.</span></span>                            |



 

<span data-ttu-id="b9526-130">O objeto **downloadcollection** é acessado por meio dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9526-130">The **DownloadCollection** object is accessed through the following methods.</span></span>



| <span data-ttu-id="b9526-131">Objeto</span><span class="sxs-lookup"><span data-stu-id="b9526-131">Object</span></span>                                        | <span data-ttu-id="b9526-132">Método</span><span class="sxs-lookup"><span data-stu-id="b9526-132">Method</span></span>                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="b9526-133">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="b9526-133">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="b9526-134">createbaixecollection</span><span class="sxs-lookup"><span data-stu-id="b9526-134">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) |
| [<span data-ttu-id="b9526-135">DownloadManager</span><span class="sxs-lookup"><span data-stu-id="b9526-135">DownloadManager</span></span>](downloadmanager-object.md) | [<span data-ttu-id="b9526-136">getbaixecollection</span><span class="sxs-lookup"><span data-stu-id="b9526-136">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       |



 

<span data-ttu-id="b9526-137">Para fins de ilustração, o **DownloadManager**. **Getbaixecollection**(*CollectionId*) é usado nas seções de sintaxe de referência.</span><span class="sxs-lookup"><span data-stu-id="b9526-137">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9526-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9526-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9526-139">**Referência para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="b9526-139">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




