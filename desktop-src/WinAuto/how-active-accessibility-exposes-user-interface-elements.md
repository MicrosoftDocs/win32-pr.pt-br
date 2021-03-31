---
title: Como Acessibilidade Ativa expõe elementos da interface do usuário
description: O Microsoft Acessibilidade Ativa cria um objeto proxy para cada elemento da interface do usuário que ele expõe.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159800"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a><span data-ttu-id="9a9be-103">Como Acessibilidade Ativa expõe elementos da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="9a9be-103">How Active Accessibility Exposes User Interface Elements</span></span>

<span data-ttu-id="9a9be-104">O Microsoft Acessibilidade Ativa cria um objeto *proxy* para cada elemento da interface do usuário que ele expõe.</span><span class="sxs-lookup"><span data-stu-id="9a9be-104">Microsoft Active Accessibility creates a *proxy* object for each user interface element that it exposes.</span></span> <span data-ttu-id="9a9be-105">Um objeto proxy atua como um intermediário entre o utilitário cliente e o elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a9be-105">A proxy object acts as an intermediary between the client utility and the UI element.</span></span> <span data-ttu-id="9a9be-106">A finalidade do objeto de proxy é monitorar o período de vida do elemento de interface do usuário e implementar as propriedades e os métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) em nome do elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a9be-106">The purpose of the proxy object is to monitor the life span of the UI element and to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods on behalf of the UI element.</span></span> <span data-ttu-id="9a9be-107">Os desenvolvedores de servidores que criam controles personalizados ou outros elementos personalizados da interface do usuário também devem criar objetos proxy.</span><span class="sxs-lookup"><span data-stu-id="9a9be-107">Server developers who create custom controls or other custom UI elements should also create proxy objects.</span></span> <span data-ttu-id="9a9be-108">Para obter mais informações, consulte [Creating proxy Objects](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9a9be-108">For more information, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

<span data-ttu-id="9a9be-109">Quando o Microsoft Acessibilidade Ativa cria um objeto para expor um controle predefinido ou comum, ele realmente cria pelo menos dois objetos: um para o controle e outro para a janela que circunda o controle.</span><span class="sxs-lookup"><span data-stu-id="9a9be-109">When Microsoft Active Accessibility creates an object to expose a predefined or common control, it actually creates at least two objects: one for the control and one for the window that surrounds the control.</span></span> <span data-ttu-id="9a9be-110">Na maioria dos casos, essas janelas pai têm a [Propriedade Role](role-property.md) da [**janela do \_ sistema \_ de função**](object-roles.md) e têm a mesma [Propriedade Name](name-property.md) e o nome da classe Window que o controle.</span><span class="sxs-lookup"><span data-stu-id="9a9be-110">In most cases, these parent windows have the [Role property](role-property.md) of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and have the same [Name property](name-property.md) and window class name as the control.</span></span> <span data-ttu-id="9a9be-111">As informações sobre o controle que os clientes transmitem para os usuários finais estão contidas no objeto que o Microsoft Acessibilidade Ativa cria para expor o controle, não o objeto pai que expõe a janela que circunda o controle.</span><span class="sxs-lookup"><span data-stu-id="9a9be-111">The information about the control that clients convey to end users is contained in the object that Microsoft Active Accessibility creates to expose the control, not the parent object that exposes the window that surrounds the control.</span></span>

<span data-ttu-id="9a9be-112">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a9be-112">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="9a9be-113">Triagem de objetos desnecessários</span><span class="sxs-lookup"><span data-stu-id="9a9be-113">Screening Out Unnecessary Objects</span></span>](screening-out-unnecessary-objects.md)
-   [<span data-ttu-id="9a9be-114">Fornecendo a propriedade Name</span><span class="sxs-lookup"><span data-stu-id="9a9be-114">Providing the Name Property</span></span>](providing-the-name-property.md)
-   [<span data-ttu-id="9a9be-115">Garantindo que os elementos da interface do usuário sejam nomeados corretamente</span><span class="sxs-lookup"><span data-stu-id="9a9be-115">Ensuring that UI Elements are Correctly Named</span></span>](ensure-that-ui-elements-are-named-correctly.md)
-   [<span data-ttu-id="9a9be-116">Elementos de interface do usuário sem suporte</span><span class="sxs-lookup"><span data-stu-id="9a9be-116">Unsupported User Interface Elements</span></span>](unsupported-user-interface-elements.md)

 

 




