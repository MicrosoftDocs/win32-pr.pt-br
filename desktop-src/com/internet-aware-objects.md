---
title: Objetos Internet-Aware
description: Objetos Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917724"
---
# <a name="internet-aware-objects"></a><span data-ttu-id="0d4bf-103">Objetos Internet-Aware</span><span class="sxs-lookup"><span data-stu-id="0d4bf-103">Internet-Aware Objects</span></span>

<span data-ttu-id="0d4bf-104">Há determinadas categorias identificadas para cobrir as interfaces persistência; Elas foram identificadas como resultado da definição de como os controles funcionam pela Internet.</span><span class="sxs-lookup"><span data-stu-id="0d4bf-104">There are certain categories identified to cover the persistency interfaces; these have been identified as a result of defining how controls function across the Internet.</span></span> <span data-ttu-id="0d4bf-105">Um contêiner que não dá suporte a todo o intervalo de interfaces persistência deve garantir que ele não hospede um controle que exija uma combinação de interfaces para as quais ele não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="0d4bf-105">A container that does not support the full range of persistency interfaces should ensure that it does not host a control that requires a combination of interfaces that it does not support.</span></span>

<span data-ttu-id="0d4bf-106">As tabelas a seguir descrevem o significado de várias categorias como categorias implementadas e obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="0d4bf-106">The following tables describe the meaning for various categories as both implemented and required categories.</span></span>



| <span data-ttu-id="0d4bf-107">Categorias necessárias</span><span class="sxs-lookup"><span data-stu-id="0d4bf-107">Required Categories</span></span>                                                                                                                                                                                | <span data-ttu-id="0d4bf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d4bf-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4bf-109">CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATID \_ PERSISTSTOMEMORY, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0d4bf-109">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersisitsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0d4bf-110">Cada uma dessas categorias é mutuamente exclusiva e usada apenas quando um objeto dá suporte a apenas um mecanismo de persistência (portanto, a exclusão mútua).</span><span class="sxs-lookup"><span data-stu-id="0d4bf-110">Each of these categories is mutually exclusive and only used when an object supports only one persistence mechanism at all (hence the mutual exclusion).</span></span> <span data-ttu-id="0d4bf-111">Contêineres que não dão suporte ao mecanismo de persistência descrito por uma dessas categorias devem impedir a criação de qualquer objeto de classes, portanto marcados.</span><span class="sxs-lookup"><span data-stu-id="0d4bf-111">Containers that do not support the persistence mechanism described by one of these categories should prevent themselves from creating any objects of classes so marked.</span></span><br/> |
| <span data-ttu-id="0d4bf-112">RequiresDataPathHost de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-112">CATID\_RequiresDataPathHost</span></span><br/>                                                                                                                                                             | <span data-ttu-id="0d4bf-113">O objeto requer a capacidade de salvar dados em um ou mais caminhos e requer envolvimento de contêiner, portanto, exigindo suporte de contêiner para [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d4bf-113">The object requires the ability to save data to one or more paths and requires container involvement, therefore requiring container support for [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span></span><br/>                                                                                                                                  |



 



| <span data-ttu-id="0d4bf-114">Categorias implementadas</span><span class="sxs-lookup"><span data-stu-id="0d4bf-114">Implemented Categories</span></span>                                                                                                                                                                            | <span data-ttu-id="0d4bf-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d4bf-115">Description</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4bf-116">CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATID \_ PERSISTSTOMEMORY, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0d4bf-116">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersistsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0d4bf-117">O objeto dá suporte ao mecanismo de IPersist correspondente \* para a categoria.</span><span class="sxs-lookup"><span data-stu-id="0d4bf-117">Object supports the corresponding IPersist\* mechanism for the category.</span></span><br/> |



 

<span data-ttu-id="0d4bf-118">A tabela a seguir fornece as CATIDs exatas atribuídas a cada categoria:</span><span class="sxs-lookup"><span data-stu-id="0d4bf-118">The following table provides the exact CATIDs assigned to each category:</span></span>



| <span data-ttu-id="0d4bf-119">Categoria</span><span class="sxs-lookup"><span data-stu-id="0d4bf-119">Category</span></span>                                | <span data-ttu-id="0d4bf-120">CATID</span><span class="sxs-lookup"><span data-stu-id="0d4bf-120">CATID</span></span>                                           |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="0d4bf-121">RequiresDataPathHost de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-121">CATID\_RequiresDataPathHost</span></span><br/>  | <span data-ttu-id="0d4bf-122">0de86a50-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-122">0de86a50-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d4bf-123">PersistsToMoniker de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-123">CATID\_PersistsToMoniker</span></span> <br/>    | <span data-ttu-id="0d4bf-124">0de86a51-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-124">0de86a51-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d4bf-125">PersistsToStorage de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-125">CATID\_PersistsToStorage</span></span> <br/>    | <span data-ttu-id="0d4bf-126">0de86a52-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-126">0de86a52-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d4bf-127">PersistsToStreamInit de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-127">CATID\_PersistsToStreamInit</span></span> <br/> | <span data-ttu-id="0d4bf-128">0de86a53-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-128">0de86a53-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d4bf-129">PersistsToStream de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-129">CATID\_PersistsToStream</span></span> <br/>     | <span data-ttu-id="0d4bf-130">0de86a54-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-130">0de86a54-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d4bf-131">PersistsToMemory de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-131">CATID\_PersistsToMemory</span></span> <br/>     | <span data-ttu-id="0d4bf-132">0de86a55-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-132">0de86a55-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d4bf-133">PersistsToFile de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-133">CATID\_PersistsToFile</span></span> <br/>       | <span data-ttu-id="0d4bf-134">0de86a56-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-134">0de86a56-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="0d4bf-135">PersistsToPropertyBag de CATID \_</span><span class="sxs-lookup"><span data-stu-id="0d4bf-135">CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="0d4bf-136">0de86a57-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="0d4bf-136">0de86a57-2baa-11cf-a229-00aa003d7352</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0d4bf-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d4bf-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d4bf-138">Categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="0d4bf-138">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

