---
description: Populando coleções COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Populando coleções COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296099"
---
# <a name="populating-com-collections"></a><span data-ttu-id="40a6d-103">Populando coleções COM+</span><span class="sxs-lookup"><span data-stu-id="40a6d-103">Populating COM+ Collections</span></span>

<span data-ttu-id="40a6d-104">Depois de recuperar uma coleção e antes de trabalhar diretamente com os itens que ela contém, você deve preencher a coleção usando o método [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) .</span><span class="sxs-lookup"><span data-stu-id="40a6d-104">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection by using the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method.</span></span> <span data-ttu-id="40a6d-105">Isso busca dados para o conteúdo da coleção do catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="40a6d-105">This fetches data for the collection's contents from the COM+ catalog.</span></span>

<span data-ttu-id="40a6d-106">É importante entender que sempre que você usa os objetos COMAdmin para manipular itens ou dados em coleções, você está realmente trabalhando em dados armazenados em cache transitórios; Você não está trabalhando diretamente com o catálogo persistente.</span><span class="sxs-lookup"><span data-stu-id="40a6d-106">It is important to understand that whenever you use the COMAdmin objects to manipulate items or data in collections, you are really working on transiently cached data; you are not working directly with the persisted catalog.</span></span> <span data-ttu-id="40a6d-107">Nada que você faça com uma coleção ou qualquer um de seus itens será refletido no catálogo até que você chame [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) na coleção.</span><span class="sxs-lookup"><span data-stu-id="40a6d-107">Nothing that you do with a collection or any of its items is reflected on the catalog until you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the collection.</span></span> <span data-ttu-id="40a6d-108">Para obter mais detalhes, consulte [salvando ou descartando alterações](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="40a6d-108">For more detail, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="40a6d-109">Qualquer chamada subsequente para [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), antes de chamar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), tem o efeito de descartar alterações pendentes para todos os itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="40a6d-109">Any subsequent calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prior to calling [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), has the effect of discarding pending changes to all items in the collection.</span></span> <span data-ttu-id="40a6d-110">**Popular** sempre popula o cache no qual você está trabalhando com quaisquer dados que sejam persistidos no armazenamento de dados de catálogo subjacente.</span><span class="sxs-lookup"><span data-stu-id="40a6d-110">**Populate** always populates the cache you're working in with whatever data is persisted on the underlying catalog data store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40a6d-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40a6d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40a6d-112">Navegando na hierarquia da coleção COM+</span><span class="sxs-lookup"><span data-stu-id="40a6d-112">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="40a6d-113">Consultando coleções relacionadas disponíveis</span><span class="sxs-lookup"><span data-stu-id="40a6d-113">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="40a6d-114">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="40a6d-114">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



