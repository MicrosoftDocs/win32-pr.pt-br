---
title: Controle Calendar (referência de elemento de interface do usuário do MSAA)
description: Os controles de calendário fornecem uma maneira simples e intuitiva para um usuário selecionar uma data de uma interface familiar.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822450"
---
# <a name="calendar-control-msaa-ui-element-reference"></a><span data-ttu-id="3b01e-103">Controle Calendar (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="3b01e-103">Calendar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="3b01e-104">Este tópico descreve os objetos de **controle de calendário** para fins de referência de elemento de interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="3b01e-104">This topic describes **Calendar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="3b01e-105">Como criar objetos de **controle de calendário** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="3b01e-105">How to create **Calendar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="3b01e-106">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="3b01e-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="3b01e-107">Os controles de calendário fornecem uma maneira simples e intuitiva para um usuário selecionar uma data de uma interface familiar.</span><span class="sxs-lookup"><span data-stu-id="3b01e-107">Calendar controls provide a simple and intuitive way for a user to select a date from a familiar interface.</span></span>

<span data-ttu-id="3b01e-108">O nome de classe da janela para um controle de calendário mensal é a \_ classe calendário mensal, que é definida como "SysMonthCal32" em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="3b01e-108">The window class name for a month calendar control is MONTHCAL\_CLASS, which is defined as "SysMonthCal32" in Commctrl.h.</span></span> <span data-ttu-id="3b01e-109">As informações neste tópico aplicam-se ao controle de calendário mensal na versão 5 do commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="3b01e-109">Information in this topic applies to the month calendar control in version 5 of Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="3b01e-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="3b01e-110">IAccessible Methods</span></span>

<span data-ttu-id="3b01e-111">Os controles de calendário dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="3b01e-111">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="3b01e-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="3b01e-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="3b01e-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="3b01e-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="3b01e-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="3b01e-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="3b01e-115">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="3b01e-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="3b01e-116">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="3b01e-116">IAccessible Properties</span></span>

<span data-ttu-id="3b01e-117">Os controles de calendário dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="3b01e-117">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="3b01e-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3b01e-118">Property</span></span>                                                                 | <span data-ttu-id="3b01e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b01e-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b01e-120">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="3b01e-120">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="3b01e-121">A propriedade **ChildCount** é zero.</span><span class="sxs-lookup"><span data-stu-id="3b01e-121">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="3b01e-122">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="3b01e-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3b01e-123">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="3b01e-123">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="3b01e-124">A propriedade **Name** é obtida do controle de texto estático que rotula o controle Calendar.</span><span class="sxs-lookup"><span data-stu-id="3b01e-124">The **Name** property is obtained from the static text control that labels the calendar control.</span></span> <span data-ttu-id="3b01e-125">Ao criar controles, os desenvolvedores de servidor devem garantir que um controle de texto estático preceda imediatamente o controle que ele rotula dentro da ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="3b01e-125">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="3b01e-126">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="3b01e-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="3b01e-127">A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.</span><span class="sxs-lookup"><span data-stu-id="3b01e-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="3b01e-128">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="3b01e-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="3b01e-129">A propriedade **role** é [**\_ \_ cliente do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3b01e-129">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="3b01e-130">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="3b01e-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="3b01e-131">A propriedade de **estado** é uma combinação de um ou mais dos [valores](object-state-constants.md)a seguir sistema de estado [**\_ \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_ indisponível**](object-state-constants.md) sistema de Estados \| [**focalizado sistema estado \_ \_ focado**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="3b01e-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md)[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3b01e-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b01e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b01e-133">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="3b01e-133">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





