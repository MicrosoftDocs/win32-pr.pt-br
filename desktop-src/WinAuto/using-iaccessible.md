---
title: Usando a interface IAccessible
description: A interface IAccessible é uma coleção de métodos que expõem os atributos e comportamentos mais comuns de uma ampla gama de elementos de interface do usuário.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292296"
---
# <a name="using-the-iaccessible-interface"></a><span data-ttu-id="aee92-103">Usando a interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="aee92-103">Using the IAccessible Interface</span></span>

<span data-ttu-id="aee92-104">A interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é uma coleção de métodos que expõem os atributos e comportamentos mais comuns de uma ampla gama de elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="aee92-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is a collection of methods that expose the most common attributes and behaviors of a wide range of UI elements.</span></span> <span data-ttu-id="aee92-105">Um elemento de interface do usuário é um controle, como um menu ou botão de ação, que faz parte da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="aee92-105">A UI element is a control, such as a menu or push button, that is part of the user interface.</span></span> <span data-ttu-id="aee92-106">Um objeto acessível é um elemento de interface do usuário que tem uma interface de **IAccessible** significativa.</span><span class="sxs-lookup"><span data-stu-id="aee92-106">An accessible object is a UI element that has a meaningful **IAccessible** interface.</span></span>

<span data-ttu-id="aee92-107">Algumas das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) não são aplicáveis a todos os tipos de elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="aee92-107">Some of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties are not applicable to every kind of user interface element.</span></span> <span data-ttu-id="aee92-108">Além disso, a implementação do **IAccessible** varia de aplicativo para aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aee92-108">Also, the implementation of **IAccessible** varies from application to application.</span></span>

<span data-ttu-id="aee92-109">Embora os parâmetros e valores de retorno para as propriedades e métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sejam totalmente especificados, como um cliente deve usar uma propriedade ou como um servidor deve implementar uma propriedade, às vezes, está sujeito à interpretação.</span><span class="sxs-lookup"><span data-stu-id="aee92-109">Although the parameters and return values for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods are fully specified, how a client should use a property or how a server should implement a property is sometimes subject to interpretation.</span></span>

<span data-ttu-id="aee92-110">Esta seção fornece sugestões, diretrizes e exemplos para ajudar aplicativos cliente a obter informações sobre elementos de interface do usuário e para ajudar aplicativos de servidor a fornecer informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="aee92-110">This section provides suggestions, guidelines, and examples for helping client applications obtain information about UI elements and for helping server applications provide appropriate information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aee92-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="aee92-111">In this section</span></span>

-   [<span data-ttu-id="aee92-112">Conteúdo de propriedades descritivas</span><span class="sxs-lookup"><span data-stu-id="aee92-112">Content of Descriptive Properties</span></span>](content-of-descriptive-properties.md)
-   [<span data-ttu-id="aee92-113">Propriedades e métodos de seleção e foco</span><span class="sxs-lookup"><span data-stu-id="aee92-113">Selection and Focus Properties and Methods</span></span>](selection-and-focus-properties-and-methods.md)
-   [<span data-ttu-id="aee92-114">Propriedades e métodos de navegação de objeto</span><span class="sxs-lookup"><span data-stu-id="aee92-114">Object Navigation Properties and Methods</span></span>](object-navigation-properties-and-methods.md)

 

 




