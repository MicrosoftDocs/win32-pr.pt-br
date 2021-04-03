---
title: Propriedades e métodos de navegação de objeto
description: Os clientes navegam de um objeto para outro usando métodos como IAccessible accNavigate e IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916169"
---
# <a name="object-navigation-properties-and-methods"></a><span data-ttu-id="7bb27-103">Propriedades e métodos de navegação de objeto</span><span class="sxs-lookup"><span data-stu-id="7bb27-103">Object Navigation Properties and Methods</span></span>

<span data-ttu-id="7bb27-104">Os clientes *navegam* de um objeto para outro usando métodos como [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) e [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span><span class="sxs-lookup"><span data-stu-id="7bb27-104">Clients *navigate* from one object to another using methods such as [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span></span> <span data-ttu-id="7bb27-105">Esses métodos permitem que os clientes recuperem uma ID filho ou o endereço da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="7bb27-105">These methods allow clients to retrieve either a child ID or the address of another object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="7bb27-106">A navegação permite que os clientes explorem como os objetos estão relacionados entre si.</span><span class="sxs-lookup"><span data-stu-id="7bb27-106">Navigation allows clients to explore how objects are related to each other.</span></span> <span data-ttu-id="7bb27-107">Observe que navegar para outro objeto não altera a seleção ou o foco.</span><span class="sxs-lookup"><span data-stu-id="7bb27-107">Note that navigating to another object does not change the selection or focus.</span></span>

<span data-ttu-id="7bb27-108">A interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornece propriedades e métodos que dão suporte aos seguintes tipos de navegação:</span><span class="sxs-lookup"><span data-stu-id="7bb27-108">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides properties and methods that support the following kinds of navigation:</span></span>

-   [<span data-ttu-id="7bb27-109">Navegação hierárquica</span><span class="sxs-lookup"><span data-stu-id="7bb27-109">Hierarchical Navigation</span></span>](hierarchical-navigation.md)
-   [<span data-ttu-id="7bb27-110">Navegação espacial e lógica</span><span class="sxs-lookup"><span data-stu-id="7bb27-110">Spatial and Logical Navigation</span></span>](spatial-and-logical-navigation.md)
-   [<span data-ttu-id="7bb27-111">Navegação por meio de teste de clique e local da tela</span><span class="sxs-lookup"><span data-stu-id="7bb27-111">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)

 

 




