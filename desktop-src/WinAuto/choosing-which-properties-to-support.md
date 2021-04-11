---
title: Escolhendo quais propriedades para dar suporte
description: As propriedades IAccessible fornecem uma maneira para os desenvolvedores de servidor descreverem uma grande variedade de elementos da interface do usuário.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292419"
---
# <a name="choosing-which-properties-to-support"></a><span data-ttu-id="76156-103">Escolhendo quais propriedades para dar suporte</span><span class="sxs-lookup"><span data-stu-id="76156-103">Choosing Which Properties to Support</span></span>

<span data-ttu-id="76156-104">As propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornecem uma maneira para os desenvolvedores de servidor descreverem uma grande variedade de elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="76156-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties provide a way for server developers to describe a wide variety of user interface elements.</span></span> <span data-ttu-id="76156-105">Mas nem todas as propriedades são aplicáveis a todos os tipos de elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="76156-105">But not all of the properties are applicable for every kind of user interface element.</span></span> <span data-ttu-id="76156-106">Além disso, algumas propriedades fornecem informações descritivas que são úteis, mas não essenciais.</span><span class="sxs-lookup"><span data-stu-id="76156-106">Additionally, some properties provide descriptive information that is useful but not essential.</span></span>

<span data-ttu-id="76156-107">Os servidores devem dar suporte às seguintes propriedades e métodos para cada objeto:</span><span class="sxs-lookup"><span data-stu-id="76156-107">Servers must support the following properties and methods for every object:</span></span>

-   [<span data-ttu-id="76156-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="76156-108">**Name**</span></span>](name-property.md)
-   [<span data-ttu-id="76156-109">**Role**</span><span class="sxs-lookup"><span data-stu-id="76156-109">**Role**</span></span>](role-property.md)
-   [<span data-ttu-id="76156-110">**Status**</span><span class="sxs-lookup"><span data-stu-id="76156-110">**State**</span></span>](state-property.md)
-   <span data-ttu-id="76156-111">[**Localização**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) e [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span><span class="sxs-lookup"><span data-stu-id="76156-111">[**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)</span></span>
-   <span data-ttu-id="76156-112">[**Pai**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) e [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span><span class="sxs-lookup"><span data-stu-id="76156-112">[**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) and [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)</span></span>

<span data-ttu-id="76156-113">As propriedades e o método a seguir devem ter suporte se forem aplicáveis ao objeto:</span><span class="sxs-lookup"><span data-stu-id="76156-113">The following properties and method must be supported if they are applicable to the object:</span></span>

-   [<span data-ttu-id="76156-114">**KeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="76156-114">**KeyboardShortcut**</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="76156-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="76156-115">**Value**</span></span>](value-property.md)

<span data-ttu-id="76156-116">As propriedades e o método a seguir devem ter suporte se o objeto tiver filhos:</span><span class="sxs-lookup"><span data-stu-id="76156-116">The following properties and method must be supported if the object has children:</span></span>

-   <span data-ttu-id="76156-117">[**Filho**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) e [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span><span class="sxs-lookup"><span data-stu-id="76156-117">[**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) and [**ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)</span></span>
-   <span data-ttu-id="76156-118">[**Foco, seleção**](selection-and-focus-properties-and-methods.md)e [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span><span class="sxs-lookup"><span data-stu-id="76156-118">[**Focus, Selection**](selection-and-focus-properties-and-methods.md), and [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)</span></span>

<span data-ttu-id="76156-119">As propriedades a seguir são opcionais, mas fornecem informações descritivas úteis sobre o objeto.</span><span class="sxs-lookup"><span data-stu-id="76156-119">The following properties are optional, but provide useful descriptive information about the object.</span></span> <span data-ttu-id="76156-120">A propriedade [**Description**](description-property.md) é implementada para descrever bitmaps e outras imagens.</span><span class="sxs-lookup"><span data-stu-id="76156-120">The [**Description**](description-property.md) property is implemented to describe bitmaps and other images.</span></span>

-   [<span data-ttu-id="76156-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="76156-121">**Description**</span></span>](description-property.md)
-   <span data-ttu-id="76156-122">[**DefaultAction**](defaultaction-property.md) e [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span><span class="sxs-lookup"><span data-stu-id="76156-122">[**DefaultAction**](defaultaction-property.md) and [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)</span></span>
-   [<span data-ttu-id="76156-123">**Ajuda**</span><span class="sxs-lookup"><span data-stu-id="76156-123">**Help**</span></span>](help-property.md)
-   [<span data-ttu-id="76156-124">**HelpTopic**</span><span class="sxs-lookup"><span data-stu-id="76156-124">**HelpTopic**</span></span>](helptopic-property.md)

 

 




