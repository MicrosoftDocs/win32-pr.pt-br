---
title: Janela do cliente MDI (referência de elemento da interface do usuário do MSAA)
description: A interface de vários documentos (MDI) é uma especificação que define a interface do usuário padrão para aplicativos escritos para o Windows. Um aplicativo MDI permite que um usuário trabalhe com mais de um documento por vez.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916228"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a><span data-ttu-id="2241d-104">Janela do cliente MDI (referência de elemento da interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="2241d-104">MDI Client Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="2241d-105">A interface de vários documentos (MDI) é uma especificação que define a interface do usuário padrão para aplicativos escritos para o Windows.</span><span class="sxs-lookup"><span data-stu-id="2241d-105">The multiple document interface (MDI) is a specification that defines the standard user interface for applications written for Windows.</span></span> <span data-ttu-id="2241d-106">Um aplicativo MDI permite que um usuário trabalhe com mais de um documento por vez.</span><span class="sxs-lookup"><span data-stu-id="2241d-106">An MDI application enables a user to work with more than one document at a time.</span></span>

<span data-ttu-id="2241d-107">Um aplicativo MDI tem três tipos de janelas: uma janela de quadro, uma janela de cliente e uma série de janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="2241d-107">An MDI application has three kinds of windows: a frame window, a client window, and a number of child windows.</span></span> <span data-ttu-id="2241d-108">A janela do quadro é como a janela principal de um aplicativo e envolve a janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="2241d-108">The frame window is like the main window of an application, and it surrounds the client window.</span></span> <span data-ttu-id="2241d-109">A janela do cliente é um filho da janela do quadro e serve como o plano de fundo para as janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="2241d-109">The client window is a child of the frame window and serves as the background for the child windows.</span></span> <span data-ttu-id="2241d-110">A janela do cliente também fornece suporte para criar e manipular as janelas filhas nas quais os documentos são exibidos.</span><span class="sxs-lookup"><span data-stu-id="2241d-110">The client window also provides support for creating and manipulating the child windows in which documents are displayed.</span></span>

<span data-ttu-id="2241d-111">O nome da classe de janela para uma janela de cliente MDI é "MDIClient".</span><span class="sxs-lookup"><span data-stu-id="2241d-111">The window class name for an MDI client window is "MDIClient".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="2241d-112">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="2241d-112">IAccessible Methods</span></span>

<span data-ttu-id="2241d-113">Uma janela de cliente MDI dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="2241d-113">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="2241d-114">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="2241d-114">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="2241d-115">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="2241d-115">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="2241d-116">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="2241d-116">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="2241d-117">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="2241d-117">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="2241d-118">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="2241d-118">IAccessible Properties</span></span>

<span data-ttu-id="2241d-119">Uma janela do cliente MDI dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="2241d-119">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="2241d-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2241d-120">Property</span></span>                                                                 | <span data-ttu-id="2241d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2241d-121">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2241d-122">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="2241d-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="2241d-123">A propriedade **ChildCount** é o número de janelas filhas nas quais os documentos são exibidos.</span><span class="sxs-lookup"><span data-stu-id="2241d-123">The **ChildCount** property is the number of child windows in which documents are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2241d-124">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="2241d-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2241d-125">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="2241d-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="2241d-126">A propriedade **Name** é "Workspace".</span><span class="sxs-lookup"><span data-stu-id="2241d-126">The **Name** property is "Workspace".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2241d-127">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="2241d-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="2241d-128">A propriedade **Parent** é a janela de quadro MDI.</span><span class="sxs-lookup"><span data-stu-id="2241d-128">The **Parent** property is the MDI frame window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="2241d-129">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="2241d-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="2241d-130">A propriedade **role** é [**\_ \_ cliente do sistema de função**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="2241d-130">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="2241d-131">**obter \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="2241d-131">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2241d-132">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="2241d-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="2241d-133">A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="2241d-133">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2241d-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2241d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2241d-135">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="2241d-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





