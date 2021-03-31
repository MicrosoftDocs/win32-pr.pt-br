---
title: Visão geral técnica
description: O Microsoft Acessibilidade Ativa melhora a maneira como os recursos de acessibilidade (programas especializados que ajudam as pessoas com deficiências a usar computadores com mais eficiência) funcionam com aplicativos em execução no Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636717"
---
# <a name="technical-overview"></a><span data-ttu-id="2b5dd-103">Visão geral técnica</span><span class="sxs-lookup"><span data-stu-id="2b5dd-103">Technical Overview</span></span>

<span data-ttu-id="2b5dd-104">O Microsoft Acessibilidade Ativa melhora a maneira como os recursos de acessibilidade (programas especializados que ajudam as pessoas com deficiências a usar computadores com mais eficiência) funcionam com aplicativos em execução no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-104">Microsoft Active Accessibility improves the way accessibility aids (specialized programs that help people with disabilities use computers more effectively) work with applications running on Microsoft Windows.</span></span>

<span data-ttu-id="2b5dd-105">O Microsoft Acessibilidade Ativa é baseado no Component Object Model (COM), que foi desenvolvido pela Microsoft e é um padrão da indústria que define uma maneira comum para que aplicativos e sistemas operacionais se comuniquem.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-105">Microsoft Active Accessibility is based on the Component Object Model (COM), which was developed by Microsoft and is an industry standard that defines a common way for applications and operating systems to communicate.</span></span> <span data-ttu-id="2b5dd-106">O Microsoft Acessibilidade Ativa consiste nos seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="2b5dd-106">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="2b5dd-107">O [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)da interface com, que expõe informações sobre elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-107">The COM interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), which exposes information about UI elements.</span></span> <span data-ttu-id="2b5dd-108">O **IAccessible** também tem propriedades e métodos para obter informações sobre e manipular esse elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-108">**IAccessible** also has properties and methods for obtaining information about and manipulating that UI element.</span></span>
-   <span data-ttu-id="2b5dd-109">WinEvents, um sistema de eventos que permite que os servidores Notifiquem os clientes quando um objeto acessível é alterado.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-109">WinEvents, an event system that allows servers to notify clients when an accessible object changes.</span></span>
-   <span data-ttu-id="2b5dd-110">Oleacc.dll, uma DLL de suporte ou de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-110">Oleacc.dll, a support or run-time DLL.</span></span>

<span data-ttu-id="2b5dd-111">A DLL do Microsoft Acessibilidade Ativa, Oleacc.dll, consiste nos seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="2b5dd-111">The Microsoft Active Accessibility DLL, Oleacc.dll, consists of the following components:</span></span>

-   <span data-ttu-id="2b5dd-112">Funções que permitem que os clientes solicitem um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (por exemplo, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span><span class="sxs-lookup"><span data-stu-id="2b5dd-112">Functions that allow clients to request an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer (for example, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span></span>
-   <span data-ttu-id="2b5dd-113">Funções que permitem que os servidores retornem um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um cliente (por exemplo, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span><span class="sxs-lookup"><span data-stu-id="2b5dd-113">Functions that allow servers to return an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a client (for example, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span></span>
-   <span data-ttu-id="2b5dd-114">Funções para obter texto localizado para os códigos de função e de estado (por exemplo, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) e [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span><span class="sxs-lookup"><span data-stu-id="2b5dd-114">Functions for getting localized text for the role and state codes (for example, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) and [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span></span>
-   <span data-ttu-id="2b5dd-115">Algumas funções auxiliares ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span><span class="sxs-lookup"><span data-stu-id="2b5dd-115">Some helper functions ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span></span>
-   <span data-ttu-id="2b5dd-116">Código que fornece a implementação padrão do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para controles de usuário e COMCTL padrão.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-116">Code that provides the default implementation of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) for standard USER and COMCTL controls.</span></span> <span data-ttu-id="2b5dd-117">Como eles implementam o **IAccessible** em nome dos controles do sistema, eles são conhecidos como *proxies*.</span><span class="sxs-lookup"><span data-stu-id="2b5dd-117">Because these implement **IAccessible** on behalf of the system controls, they are known as *proxies*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2b5dd-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2b5dd-118">In this section</span></span>

-   [<span data-ttu-id="2b5dd-119">Como Acessibilidade Ativa funciona</span><span class="sxs-lookup"><span data-stu-id="2b5dd-119">How Active Accessibility Works</span></span>](how-active-accessibility-works.md)
-   [<span data-ttu-id="2b5dd-120">Noções básicas do Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="2b5dd-120">Active Accessibility Basics</span></span>](active-accessibility-basics.md)
-   [<span data-ttu-id="2b5dd-121">Diretrizes do servidor</span><span class="sxs-lookup"><span data-stu-id="2b5dd-121">Server Guidelines</span></span>](server-guidelines.md)
-   [<span data-ttu-id="2b5dd-122">Diretrizes do cliente</span><span class="sxs-lookup"><span data-stu-id="2b5dd-122">Client Guidelines</span></span>](client-guidelines.md)
-   [<span data-ttu-id="2b5dd-123">Diretrizes de COM e Unicode</span><span class="sxs-lookup"><span data-stu-id="2b5dd-123">COM and Unicode Guidelines</span></span>](com-and-unicode-guidelines.md)

 

 




