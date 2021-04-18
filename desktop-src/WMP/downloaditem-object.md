---
title: Objeto DownloadItem
description: Objeto DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Armazenamentos online do Windows Media Player, objeto DownloadItem
- lojas online, objeto DownloadItem
- tipo 2 lojas online, objeto DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788177"
---
# <a name="downloaditem-object"></a><span data-ttu-id="12cd4-107">Objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="12cd4-107">DownloadItem Object</span></span>

> [!Note]  
> <span data-ttu-id="12cd4-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="12cd4-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="12cd4-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="12cd4-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="12cd4-110">O objeto **DownloadItem** representa uma solicitação de download de arquivo.</span><span class="sxs-lookup"><span data-stu-id="12cd4-110">The **DownloadItem** object represents a file download request.</span></span> <span data-ttu-id="12cd4-111">Ele pode ser usado por páginas da Web hospedadas no modo completo do Windows Media Player e que têm acesso ao objeto **externo** , como os serviços Premium.</span><span class="sxs-lookup"><span data-stu-id="12cd4-111">It can be used by webpages that are hosted in the full mode Windows Media Player and that have access to the **External** object, such as premium services.</span></span>

<span data-ttu-id="12cd4-112">O objeto **DownloadItem** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="12cd4-112">The **DownloadItem** object supports the following properties.</span></span>



| <span data-ttu-id="12cd4-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="12cd4-113">Property</span></span>                                        | <span data-ttu-id="12cd4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="12cd4-114">Description</span></span>                                      |
|-------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="12cd4-115">downloadstate</span><span class="sxs-lookup"><span data-stu-id="12cd4-115">downloadState</span></span>](downloaditem-downloadstate.md) | <span data-ttu-id="12cd4-116">Recupera o estado do download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-116">Retrieves the state of the download.</span></span>             |
| [<span data-ttu-id="12cd4-117">andamento</span><span class="sxs-lookup"><span data-stu-id="12cd4-117">progress</span></span>](downloaditem-progress.md)           | <span data-ttu-id="12cd4-118">Recupera o progresso do download em bytes.</span><span class="sxs-lookup"><span data-stu-id="12cd4-118">Retrieves the progress of the download in bytes.</span></span> |
| [<span data-ttu-id="12cd4-119">size</span><span class="sxs-lookup"><span data-stu-id="12cd4-119">size</span></span>](downloaditem-size.md)                   | <span data-ttu-id="12cd4-120">Recupera o tamanho do download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-120">Retrieves the size of the download.</span></span>              |
| [<span data-ttu-id="12cd4-121">sourceURL</span><span class="sxs-lookup"><span data-stu-id="12cd4-121">sourceURL</span></span>](downloaditem-sourceurl.md)         | <span data-ttu-id="12cd4-122">Recupera a URL de origem do download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-122">Retrieves the source URL of the download.</span></span>        |
| [<span data-ttu-id="12cd4-123">tipo</span><span class="sxs-lookup"><span data-stu-id="12cd4-123">type</span></span>](downloaditem-type.md)                   | <span data-ttu-id="12cd4-124">Recupera o tipo de download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-124">Retrieves the type of the download.</span></span>              |



 

<span data-ttu-id="12cd4-125">O objeto **DownloadItem** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="12cd4-125">The **DownloadItem** object supports the following methods.</span></span>



| <span data-ttu-id="12cd4-126">Método</span><span class="sxs-lookup"><span data-stu-id="12cd4-126">Method</span></span>                                      | <span data-ttu-id="12cd4-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="12cd4-127">Description</span></span>                                                |
|---------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="12cd4-128">cancel</span><span class="sxs-lookup"><span data-stu-id="12cd4-128">cancel</span></span>](downloaditem-cancel.md)           | <span data-ttu-id="12cd4-129">Cancela o download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-129">Cancels the download.</span></span>                                      |
| [<span data-ttu-id="12cd4-130">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="12cd4-130">getItemInfo</span></span>](downloaditem-getiteminfo.md) | <span data-ttu-id="12cd4-131">Recupera o valor de um atributo para o item de download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-131">Retrieves the value of an attribute for the download item.</span></span> |
| [<span data-ttu-id="12cd4-132">pause</span><span class="sxs-lookup"><span data-stu-id="12cd4-132">pause</span></span>](downloaditem-pause.md)             | <span data-ttu-id="12cd4-133">Pausa o download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-133">Pauses the download.</span></span>                                       |
| [<span data-ttu-id="12cd4-134">Volte</span><span class="sxs-lookup"><span data-stu-id="12cd4-134">resume</span></span>](downloaditem-resume.md)           | <span data-ttu-id="12cd4-135">Retoma o download.</span><span class="sxs-lookup"><span data-stu-id="12cd4-135">Resumes the download.</span></span>                                      |



 

<span data-ttu-id="12cd4-136">O objeto **DownloadItem** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="12cd4-136">The **DownloadItem** object is accessed through the following property.</span></span>



| <span data-ttu-id="12cd4-137">Objeto</span><span class="sxs-lookup"><span data-stu-id="12cd4-137">Object</span></span>                                              | <span data-ttu-id="12cd4-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="12cd4-138">Property</span></span>                            |
|-----------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="12cd4-139">Downloadcollection</span><span class="sxs-lookup"><span data-stu-id="12cd4-139">DownloadCollection</span></span>](downloadcollection-object.md) | [<span data-ttu-id="12cd4-140">item</span><span class="sxs-lookup"><span data-stu-id="12cd4-140">item</span></span>](downloadcollection-item.md) |



 

<span data-ttu-id="12cd4-141">Para fins de ilustração, o **DownloadManager**. **Getbaixecollection**(*CollectionId*). **Item**(*ItemId*) é usado nas seções de sintaxe de referência.</span><span class="sxs-lookup"><span data-stu-id="12cd4-141">For purposes of illustration, **DownloadManager**.**getDownloadCollection**(*collectionId*).**item**(*itemId*) is used in the reference syntax sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12cd4-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12cd4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12cd4-143">**Referência para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="12cd4-143">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




