---
title: Objeto DownloadManager
description: Objeto DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Armazenamentos online do Windows Media Player, objeto DownloadManager
- repositórios online, objeto DownloadManager
- tipo 2 lojas online, objeto DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822733"
---
# <a name="downloadmanager-object"></a><span data-ttu-id="c9101-107">Objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="c9101-107">DownloadManager Object</span></span>

> [!Note]  
> <span data-ttu-id="c9101-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="c9101-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c9101-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="c9101-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c9101-110">O objeto **DownloadManager** é o objeto raiz do Gerenciador de download do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c9101-110">The **DownloadManager** object is the root object for the Windows Media Player Download Manager.</span></span> <span data-ttu-id="c9101-111">Ele pode ser usado por páginas da Web hospedadas nos painéis de tarefas do serviço de loja online.</span><span class="sxs-lookup"><span data-stu-id="c9101-111">It can be used by webpages that are hosted in online store service task panes.</span></span>

<span data-ttu-id="c9101-112">O objeto **DownloadManager** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9101-112">The **DownloadManager** object supports the following methods.</span></span>



| <span data-ttu-id="c9101-113">Método</span><span class="sxs-lookup"><span data-stu-id="c9101-113">Method</span></span>                                                                   | <span data-ttu-id="c9101-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9101-114">Description</span></span>                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="c9101-115">createbaixecollection</span><span class="sxs-lookup"><span data-stu-id="c9101-115">createDownloadCollection</span></span>](downloadmanager-createdownloadcollection.md) | <span data-ttu-id="c9101-116">Cria uma coleção de download vazia.</span><span class="sxs-lookup"><span data-stu-id="c9101-116">Creates an empty download collection.</span></span>        |
| [<span data-ttu-id="c9101-117">getbaixecollection</span><span class="sxs-lookup"><span data-stu-id="c9101-117">getDownloadCollection</span></span>](downloadmanager-getdownloadcollection.md)       | <span data-ttu-id="c9101-118">Recupera a coleção de download especificada.</span><span class="sxs-lookup"><span data-stu-id="c9101-118">Retrieves the specified download collection.</span></span> |



 

<span data-ttu-id="c9101-119">O objeto **DownloadManager** é acessado usando **external. DownloadManager**.</span><span class="sxs-lookup"><span data-stu-id="c9101-119">The **DownloadManager** object is accessed by using **external.DownloadManager**.</span></span> <span data-ttu-id="c9101-120">Para fins de ilustração, supõe-se que esse valor tenha sido atribuído a uma variável chamada "DownloadManager", que será usada para identificar esse objeto nas seções de sintaxe de referência.</span><span class="sxs-lookup"><span data-stu-id="c9101-120">For illustration purposes, it is assumed that this value has been assigned to a variable named "DownloadManager", which will be used to identify this object in the reference syntax sections.</span></span>

<span data-ttu-id="c9101-121">No Windows Media Player 10 ou posterior, a propriedade e o objeto **DownloadManager** são acessíveis somente de painéis de tarefas do serviço de loja online.</span><span class="sxs-lookup"><span data-stu-id="c9101-121">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="c9101-122">Você não pode usar o **DownloadManager** de outros recursos em que o objeto **externo** está disponível, como HtmlView, exibição do centro de informações e informações do álbum.</span><span class="sxs-lookup"><span data-stu-id="c9101-122">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9101-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9101-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9101-124">**Referência para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="c9101-124">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




