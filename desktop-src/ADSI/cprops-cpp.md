---
title: CPROPS. CPP
description: No exemplo de componente do provedor, um exemplo de uma implementação de cache de propriedade pode ser encontrado em cProps. cpp. Os métodos com suporte são listados na tabela a seguir.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822226"
---
# <a name="cpropscpp"></a><span data-ttu-id="7ba63-104">CPROPS. CPP</span><span class="sxs-lookup"><span data-stu-id="7ba63-104">CPROPS.CPP</span></span>

<span data-ttu-id="7ba63-105">No exemplo de componente do provedor, um exemplo de uma implementação de cache de propriedade pode ser encontrado em cProps. cpp.</span><span class="sxs-lookup"><span data-stu-id="7ba63-105">In the example provider component, an example of a property cache implementation can be found in cprops.cpp.</span></span> <span data-ttu-id="7ba63-106">Os métodos com suporte são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ba63-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="7ba63-107">Método</span><span class="sxs-lookup"><span data-stu-id="7ba63-107">Method</span></span>                                           | <span data-ttu-id="7ba63-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ba63-108">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba63-109">**CPropertyCache:: AddProperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-109">**CPropertyCache::addproperty**</span></span>                  | <span data-ttu-id="7ba63-110">Estenda o cache de propriedades adicionando um novo.</span><span class="sxs-lookup"><span data-stu-id="7ba63-110">Extend the property cache by adding a new one.</span></span>                                                                      |
| <span data-ttu-id="7ba63-111">**CPropertyCache:: updateproperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-111">**CPropertyCache::updateproperty**</span></span>               | <span data-ttu-id="7ba63-112">Pesquise a propriedade, libere seu conteúdo e use novos valores, em vez disso; em seguida, marque o cache alterado para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ba63-112">Look up the property, free its contents, and use new values instead; then mark the cache changed for this property.</span></span> |
| <span data-ttu-id="7ba63-113">**CPropertyCache:: findproperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-113">**CPropertyCache::findproperty**</span></span>                 | <span data-ttu-id="7ba63-114">Pesquisar esta propriedade por nome; Salve seu índice.</span><span class="sxs-lookup"><span data-stu-id="7ba63-114">Look up this property by name; save its index.</span></span>                                                                      |
| <span data-ttu-id="7ba63-115">**CPropertyCache:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-115">**CPropertyCache::getproperty**</span></span>                  | <span data-ttu-id="7ba63-116">Localize a propriedade no cache, se disponível, caso contrário, chame **GetInfo**.</span><span class="sxs-lookup"><span data-stu-id="7ba63-116">Find the property in the cache if available, otherwise call **GetInfo**.</span></span> <span data-ttu-id="7ba63-117">Defina o índice e a cópia nos novos valores.</span><span class="sxs-lookup"><span data-stu-id="7ba63-117">Set the index and copy in the new values.</span></span>  |
| <span data-ttu-id="7ba63-118">**CPropertyCache::p utproperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-118">**CPropertyCache::putproperty**</span></span>                  | <span data-ttu-id="7ba63-119">Localize a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ba63-119">Find the property.</span></span> <span data-ttu-id="7ba63-120">Libere o que estava lá e coloque novos valores.</span><span class="sxs-lookup"><span data-stu-id="7ba63-120">Free what was there and put in new values.</span></span>                                                       |
| <span data-ttu-id="7ba63-121">**CPropertyCache::CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="7ba63-121">**CPropertyCache::CPropertyCache**</span></span>               | <span data-ttu-id="7ba63-122">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="7ba63-122">Standard constructor.</span></span>                                                                                               |
| <span data-ttu-id="7ba63-123">**CPropertyCache:: ~ CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="7ba63-123">**CPropertyCache::~CPropertyCache**</span></span>              | <span data-ttu-id="7ba63-124">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="7ba63-124">Standard destructor.</span></span>                                                                                                |
| <span data-ttu-id="7ba63-125">**CPropertyCache::createpropertycache**</span><span class="sxs-lookup"><span data-stu-id="7ba63-125">**CPropertyCache::createpropertycache**</span></span>          | <span data-ttu-id="7ba63-126">Crie o cache.</span><span class="sxs-lookup"><span data-stu-id="7ba63-126">Create the cache.</span></span>                                                                                                   |
| <span data-ttu-id="7ba63-127">**CPropertyCache::unboundgetproperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-127">**CPropertyCache::unboundgetproperty**</span></span>           | <span data-ttu-id="7ba63-128">Localize a propriedade no cache e defina-a com esses valores.</span><span class="sxs-lookup"><span data-stu-id="7ba63-128">Find the property in the cache and set it to these values.</span></span>                                                          |
| <span data-ttu-id="7ba63-129">**CPropertyCache::SampleDSMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="7ba63-129">**CPropertyCache::SampleDSMarshallProperties**</span></span>   | <span data-ttu-id="7ba63-130">Empacotar valores e dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ba63-130">Marshal property data and values.</span></span>                                                                                   |
| <span data-ttu-id="7ba63-131">**CPropertyCache:: marshallproperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-131">**CPropertyCache::marshallproperty**</span></span>             | <span data-ttu-id="7ba63-132">Marshale de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ba63-132">Marshal a property.</span></span>                                                                                                 |
| <span data-ttu-id="7ba63-133">**CPropertyCache::SampleDSUnMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="7ba63-133">**CPropertyCache::SampleDSUnMarshallProperties**</span></span> | <span data-ttu-id="7ba63-134">Desempacotar dados de propriedade e valores.</span><span class="sxs-lookup"><span data-stu-id="7ba63-134">Unmarshal property data and values.</span></span>                                                                                 |
| <span data-ttu-id="7ba63-135">**CPropertyCache:: unmarshalproperty**</span><span class="sxs-lookup"><span data-stu-id="7ba63-135">**CPropertyCache::unmarshallproperty**</span></span>           | <span data-ttu-id="7ba63-136">Desempacotar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7ba63-136">Unmarshal a property.</span></span>                                                                                               |



 

 

 




