---
title: Elementos personalizados da interface do usuário
description: Os desenvolvedores de servidor criam objetos acessíveis com base na interface do usuário de um aplicativo.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822384"
---
# <a name="custom-user-interface-elements"></a><span data-ttu-id="06447-103">Elementos personalizados da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="06447-103">Custom User Interface Elements</span></span>

<span data-ttu-id="06447-104">Os desenvolvedores de servidor criam objetos acessíveis com base na interface do usuário de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06447-104">Server developers design accessible objects based on an application's UI.</span></span> <span data-ttu-id="06447-105">Como [acessibilidade ativa implementa a interface IAccessible em nome dos elementos da interface do usuário fornecidos pelo sistema](appendix-a--supported-user-interface-elements-reference.md) , como caixas de listagem, menus e controles TrackBar, você precisa implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) somente para os seguintes tipos de elementos personalizados da interface do usuário:</span><span class="sxs-lookup"><span data-stu-id="06447-105">Because [Active Accessibility implements the IAccessible interface on behalf of system-provided user interface elements](appendix-a--supported-user-interface-elements-reference.md) such as list boxes, menus, and trackbar controls, you need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface only for the following kinds of custom UI elements:</span></span>

-   <span data-ttu-id="06447-106">Controles personalizados criados pelo registro de uma classe de janela definida pelo aplicativo</span><span class="sxs-lookup"><span data-stu-id="06447-106">Custom controls created by registering an application-defined window class</span></span>
-   <span data-ttu-id="06447-107">Controles personalizados desenhados diretamente na tela que não têm um **HWND** associado</span><span class="sxs-lookup"><span data-stu-id="06447-107">Custom controls drawn directly on the screen that do not have an associated **HWND**</span></span>
-   <span data-ttu-id="06447-108">Controles personalizados, como Microsoft ActiveX e controles Java</span><span class="sxs-lookup"><span data-stu-id="06447-108">Custom controls such as Microsoft ActiveX and Java controls</span></span>
-   <span data-ttu-id="06447-109">Controles ou objetos na janela do cliente do aplicativo que ainda não estão expostos</span><span class="sxs-lookup"><span data-stu-id="06447-109">Controls or objects in the application's client window that aren't already exposed</span></span>

<span data-ttu-id="06447-110">Os controles e menus desenhados pelo proprietário estarão acessíveis contanto que você siga as diretrizes discutidas em [atalhos para expor elementos personalizados da interface do usuário](shortcuts-for-exposing-custom-user-interface-elements.md).</span><span class="sxs-lookup"><span data-stu-id="06447-110">Owner-drawn controls and menus are accessible as long as you follow the guidelines discussed in [Shortcuts for Exposing Custom User Interface Elements](shortcuts-for-exposing-custom-user-interface-elements.md).</span></span> <span data-ttu-id="06447-111">Se você seguir essas diretrizes, não precisará implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para controles e menus desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="06447-111">If you follow these guidelines, then you do not need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for owner-drawn controls and menus.</span></span>

<span data-ttu-id="06447-112">Na maioria dos casos, os controles de subclasse e de subclasse são acessíveis porque o sistema manipula a funcionalidade básica do controle.</span><span class="sxs-lookup"><span data-stu-id="06447-112">In most cases, superclassed and subclassed controls are accessible because the system handles the basic functionality of the control.</span></span> <span data-ttu-id="06447-113">No entanto, se um controle de subclasse ou de subclasse modificar significativamente o comportamento do controle fornecido pelo sistema no qual ele se baseia, você deverá implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="06447-113">However, if a superclassed or subclassed control significantly modifies the behavior of the system-provided control on which it is based, then you must implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="06447-114">Para obter mais informações, consulte [expondo controles com base em controles do sistema](exposing-controls-based-on-system-controls.md).</span><span class="sxs-lookup"><span data-stu-id="06447-114">For more information, see [Exposing Controls Based on System Controls](exposing-controls-based-on-system-controls.md).</span></span>

<span data-ttu-id="06447-115">Se um aplicativo usar apenas elementos de interface do usuário fornecidos pelo sistema, ele não precisará implementar o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), exceto a janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="06447-115">If an application uses only system-provided user interface elements, then it does not need to implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), except for its client window.</span></span> <span data-ttu-id="06447-116">Por exemplo, um aplicativo que inclui um editor de texto, não implementado usando um controle de edição, expõe linhas de texto como objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="06447-116">For example, an application that includes a text editor, not implemented using an edit control, exposes lines of text as accessible objects.</span></span> <span data-ttu-id="06447-117">Observe que o Microsoft Acessibilidade Ativa expõe automaticamente o texto em controles Edit e Rich Edit como uma única cadeia de texto na propriedade [**Value**](value-property.md) do controle.</span><span class="sxs-lookup"><span data-stu-id="06447-117">Note that Microsoft Active Accessibility automatically exposes the text in edit and rich edit controls as a single string of text in the [**Value**](value-property.md) property of the control.</span></span>

 

 




