---
title: Propriedade State
description: A propriedade State descreve o status de um objeto em um momento no tempo. Todos os objetos dão suporte à propriedade State.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822990"
---
# <a name="state-property"></a><span data-ttu-id="991fc-104">Propriedade State</span><span class="sxs-lookup"><span data-stu-id="991fc-104">State Property</span></span>

<span data-ttu-id="991fc-105">A propriedade **State** descreve o status de um objeto em um momento no tempo.</span><span class="sxs-lookup"><span data-stu-id="991fc-105">The **State** property describes an object's status at a moment in time.</span></span> <span data-ttu-id="991fc-106">Todos os objetos dão suporte à propriedade **State** .</span><span class="sxs-lookup"><span data-stu-id="991fc-106">All objects support the **State** property.</span></span>

<span data-ttu-id="991fc-107">A propriedade **State** é recuperada chamando [**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span><span class="sxs-lookup"><span data-stu-id="991fc-107">The **State** property is retrieved by calling [**IAccessible::get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span></span>

<span data-ttu-id="991fc-108">O Microsoft Acessibilidade Ativa fornece [constantes de estado de objeto](object-state-constants.md), definidas em OleAcc. h, que são combinadas para identificar o estado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="991fc-108">Microsoft Active Accessibility provides [object state constants](object-state-constants.md), defined in oleacc.h, that are combined to identify an object's state.</span></span> <span data-ttu-id="991fc-109">É recomendável que os desenvolvedores de servidor usem esses valores de estado predefinidos.</span><span class="sxs-lookup"><span data-stu-id="991fc-109">It is recommended that server developers use these predefined state values.</span></span> <span data-ttu-id="991fc-110">Se valores de estado predefinidos forem retornados, os clientes usarão [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) para recuperar uma cadeia de caracteres localizada que descreve o estado.</span><span class="sxs-lookup"><span data-stu-id="991fc-110">If predefined state values are returned, clients use [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) to retrieve a localized string that describes the state.</span></span>

<span data-ttu-id="991fc-111">Os gráficos que, ocasionalmente, são animados devem ter a propriedade **State** definida como [**estado do \_ sistema \_ animado**](object-state-constants.md) e a propriedade [**role**](role-property.md) definida como [**\_ \_ elemento gráfico do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="991fc-111">Graphics that are occasionally animated should have the **State** property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) and the [**Role**](role-property.md) property set to [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

 

 




