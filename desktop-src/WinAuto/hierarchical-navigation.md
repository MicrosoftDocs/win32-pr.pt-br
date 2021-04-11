---
title: Navegação hierárquica
description: Geralmente, os clientes devem se mover entre objetos com base em suas relações pai-filho. Por exemplo, um cliente pode já ter informações sobre um controle de barra de ferramentas, mas não tem informações sobre os botões contidos nele.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159792"
---
# <a name="hierarchical-navigation"></a><span data-ttu-id="ca9ab-104">Navegação hierárquica</span><span class="sxs-lookup"><span data-stu-id="ca9ab-104">Hierarchical Navigation</span></span>

<span data-ttu-id="ca9ab-105">Geralmente, os clientes devem se mover entre objetos com base em suas relações pai-filho.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-105">Often clients must move between objects based on their parent-child relationships.</span></span> <span data-ttu-id="ca9ab-106">Por exemplo, um cliente pode já ter informações sobre um controle de barra de ferramentas, mas não tem informações sobre os botões contidos nele.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-106">For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.</span></span>

<span data-ttu-id="ca9ab-107">A interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expõe as relações hierárquicas entre objetos.</span><span class="sxs-lookup"><span data-stu-id="ca9ab-107">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface exposes the hierarchical relationships between objects.</span></span> <span data-ttu-id="ca9ab-108">Os clientes podem navegar de um objeto pai para seus filhos ou de um objeto filho para seu pai chamando [**IAccessible:: get \_ AccParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) ou [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span><span class="sxs-lookup"><span data-stu-id="ca9ab-108">Clients can navigate from a parent object to its children or from a child object to its parent by calling [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) or [**IAccessible::get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span></span>

 

 




