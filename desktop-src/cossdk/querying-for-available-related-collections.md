---
description: Consultando coleções relacionadas disponíveis
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Consultando coleções relacionadas disponíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296113"
---
# <a name="querying-for-available-related-collections"></a><span data-ttu-id="a23e4-103">Consultando coleções relacionadas disponíveis</span><span class="sxs-lookup"><span data-stu-id="a23e4-103">Querying for Available Related Collections</span></span>

<span data-ttu-id="a23e4-104">Se você estiver escrevendo uma ferramenta de administração de finalidade geral, é provável que você precise escrever rotinas para navegar pela hierarquia de coleção inteira.</span><span class="sxs-lookup"><span data-stu-id="a23e4-104">If you are writing a general-purpose administration tool, it is likely that you will need to write routines for navigating the entire collection hierarchy.</span></span> <span data-ttu-id="a23e4-105">Para dar suporte a isso, o COM+ tem um recurso que permite que você consulte dinamicamente as coleções relacionadas que estão disponíveis em qualquer coleção específica.</span><span class="sxs-lookup"><span data-stu-id="a23e4-105">To support this, COM+ has a facility that enables you to dynamically query for the related collections that are available from any given collection.</span></span>

<span data-ttu-id="a23e4-106">A coleção [**RelatedCollectionInfo**](relatedcollectioninfo.md) está disponível em qualquer coleção que você esteja mantendo e contém um item para cada coleção relacionada disponível.</span><span class="sxs-lookup"><span data-stu-id="a23e4-106">The [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection is available from any collection that you might be holding and contains an item for each available related collection.</span></span> <span data-ttu-id="a23e4-107">Você pode enumerar esses itens para determinar se uma determinada coleção está disponível.</span><span class="sxs-lookup"><span data-stu-id="a23e4-107">You can enumerate through these items to determine whether a given collection is available.</span></span>

<span data-ttu-id="a23e4-108">Você pode obter a coleção [**RelatedCollectionInfo**](relatedcollectioninfo.md) de qualquer coleção que estiver mantendo usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , deixando o segundo parâmetro em branco, em que você normalmente especificaria a propriedade de chave de um item pai.</span><span class="sxs-lookup"><span data-stu-id="a23e4-108">You can get the [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a23e4-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a23e4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a23e4-110">Navegando na hierarquia da coleção COM+</span><span class="sxs-lookup"><span data-stu-id="a23e4-110">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="a23e4-111">Populando coleções COM+</span><span class="sxs-lookup"><span data-stu-id="a23e4-111">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="a23e4-112">Recuperando coleções no catálogo COM+</span><span class="sxs-lookup"><span data-stu-id="a23e4-112">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



