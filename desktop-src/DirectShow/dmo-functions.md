---
description: Funções de DMO
ms.assetid: 0a380dc0-23f0-4ef0-898a-3b5afddf5eaa
title: Funções de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f41750f5e442d93d3cacb2499bf2986a53cda6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456362"
---
# <a name="dmo-functions"></a><span data-ttu-id="e2cd3-103">Funções de DMO</span><span class="sxs-lookup"><span data-stu-id="e2cd3-103">DMO Functions</span></span>

<span data-ttu-id="e2cd3-104">Esta seção descreve as funções do Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="e2cd3-104">This section describes the Microsoft DirectX Media Object (DMO) functions.</span></span>



| <span data-ttu-id="e2cd3-105">Função</span><span class="sxs-lookup"><span data-stu-id="e2cd3-105">Function</span></span>                                             | <span data-ttu-id="e2cd3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2cd3-106">Description</span></span>                                                   |
|------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="e2cd3-107">**DMOEnum**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-107">**DMOEnum**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)                           | <span data-ttu-id="e2cd3-108">Enumera DMOs listados no registro.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-108">Enumerates DMOs listed in the registry.</span></span>                       |
| [<span data-ttu-id="e2cd3-109">**DMOGetName**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-109">**DMOGetName**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogetname)                     | <span data-ttu-id="e2cd3-110">Recupera o nome de um DMO do registro.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-110">Retrieves the name of a DMO from the registry.</span></span>                |
| [<span data-ttu-id="e2cd3-111">**DMOGetTypes**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-111">**DMOGetTypes**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogettypes)                   | <span data-ttu-id="e2cd3-112">Recupera os tipos de mídia registrados para um DMO.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-112">Retrieves the media types registered for a DMO.</span></span>               |
| [<span data-ttu-id="e2cd3-113">**DMORegister**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-113">**DMORegister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister)                   | <span data-ttu-id="e2cd3-114">Registra um DMO.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-114">Registers a DMO.</span></span>                                              |
| [<span data-ttu-id="e2cd3-115">**DMOUnregister**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-115">**DMOUnregister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister)               | <span data-ttu-id="e2cd3-116">Cancela o registro de um DMO.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-116">Unregisters a DMO.</span></span>                                            |
| [<span data-ttu-id="e2cd3-117">**MoCopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-117">**MoCopyMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocopymediatype)           | <span data-ttu-id="e2cd3-118">Copia uma estrutura de tipo de mídia para outra.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-118">Copies one media type structure to another.</span></span>                   |
| [<span data-ttu-id="e2cd3-119">**MoCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-119">**MoCreateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocreatemediatype)       | <span data-ttu-id="e2cd3-120">Aloca uma nova estrutura de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-120">Allocates a new media type structure.</span></span>                         |
| [<span data-ttu-id="e2cd3-121">**MoDeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-121">**MoDeleteMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-modeletemediatype)       | <span data-ttu-id="e2cd3-122">Exclui uma estrutura de tipo de mídia que foi alocada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-122">Deletes a media type structure that was previously allocated.</span></span> |
| [<span data-ttu-id="e2cd3-123">**MoDuplicateMediaType**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-123">**MoDuplicateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moduplicatemediatype) | <span data-ttu-id="e2cd3-124">Duplica uma estrutura de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-124">Duplicates a media type structure.</span></span>                            |
| [<span data-ttu-id="e2cd3-125">**MoFreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-125">**MoFreeMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mofreemediatype)           | <span data-ttu-id="e2cd3-126">Libera os membros alocados de uma estrutura de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-126">Frees the allocated members of a media type structure.</span></span>        |
| [<span data-ttu-id="e2cd3-127">**MoInitMediaType**</span><span class="sxs-lookup"><span data-stu-id="e2cd3-127">**MoInitMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moinitmediatype)           | <span data-ttu-id="e2cd3-128">Inicializa uma estrutura de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e2cd3-128">Initializes a media type structure.</span></span>                           |



 

## <a name="related-topics"></a><span data-ttu-id="e2cd3-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2cd3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2cd3-130">Referência de DMO</span><span class="sxs-lookup"><span data-stu-id="e2cd3-130">DMO Reference</span></span>](dmo-reference.md)
</dt> </dl>

 

 



