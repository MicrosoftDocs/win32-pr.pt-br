---
title: Conteúdo de propriedades descritivas
description: A interface IAccessible fornece propriedades descritivas, que descrevem vários aspectos de um objeto.
ms.assetid: e6c1d1a3-417d-4aea-abac-f84a55f666b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271dc920034802b87afd4c76ab7ede6bb9476d99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498714"
---
# <a name="content-of-descriptive-properties"></a><span data-ttu-id="05df2-103">Conteúdo de propriedades descritivas</span><span class="sxs-lookup"><span data-stu-id="05df2-103">Content of Descriptive Properties</span></span>

<span data-ttu-id="05df2-104">A interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornece propriedades descritivas, que descrevem vários aspectos de um objeto.</span><span class="sxs-lookup"><span data-stu-id="05df2-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides descriptive properties, which describe various aspects of an object.</span></span> <span data-ttu-id="05df2-105">Algumas dessas propriedades são específicas de conteúdo; outras propriedades têm conteúdo que consiste em texto descritivo fornecido pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="05df2-105">Some of these properties are content specific; other properties have content consisting of descriptive text that is provided by the server.</span></span> <span data-ttu-id="05df2-106">O tipo de informações para cada propriedade varia dependendo do objeto.</span><span class="sxs-lookup"><span data-stu-id="05df2-106">The type of information for each property varies depending on the object.</span></span>

<span data-ttu-id="05df2-107">Os tópicos a seguir descrevem as informações que os clientes obtêm dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="05df2-107">The following topics describe information that clients obtain from these properties.</span></span> <span data-ttu-id="05df2-108">Eles também fornecem aos servidores sugestões para escolher o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="05df2-108">They also provide servers with suggestions for choosing content.</span></span>

-   [<span data-ttu-id="05df2-109">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="05df2-109">Name Property</span></span>](name-property.md)
-   [<span data-ttu-id="05df2-110">Propriedade de função</span><span class="sxs-lookup"><span data-stu-id="05df2-110">Role Property</span></span>](role-property.md)
-   [<span data-ttu-id="05df2-111">Propriedade State</span><span class="sxs-lookup"><span data-stu-id="05df2-111">State Property</span></span>](state-property.md)
-   [<span data-ttu-id="05df2-112">Propriedade Value</span><span class="sxs-lookup"><span data-stu-id="05df2-112">Value Property</span></span>](value-property.md)
-   [<span data-ttu-id="05df2-113">Propriedade Description</span><span class="sxs-lookup"><span data-stu-id="05df2-113">Description Property</span></span>](description-property.md)
-   [<span data-ttu-id="05df2-114">Propriedade da ajuda</span><span class="sxs-lookup"><span data-stu-id="05df2-114">Help Property</span></span>](help-property.md)
-   [<span data-ttu-id="05df2-115">Propriedade HelpTopic</span><span class="sxs-lookup"><span data-stu-id="05df2-115">HelpTopic Property</span></span>](helptopic-property.md)
-   [<span data-ttu-id="05df2-116">Propriedade KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="05df2-116">KeyboardShortcut Property</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="05df2-117">Propriedade DefaultAction</span><span class="sxs-lookup"><span data-stu-id="05df2-117">DefaultAction Property</span></span>](defaultaction-property.md)

<span data-ttu-id="05df2-118">Ao criar objetos acessíveis, os desenvolvedores de servidor também devem consultar os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="05df2-118">When designing accessible objects, server developers should also refer to the following topics:</span></span>

-   [<span data-ttu-id="05df2-119">Escolhendo quais propriedades para dar suporte</span><span class="sxs-lookup"><span data-stu-id="05df2-119">Choosing Which Properties to Support</span></span>](choosing-which-properties-to-support.md)
-   [<span data-ttu-id="05df2-120">Escolhendo o conteúdo para propriedades descritivas</span><span class="sxs-lookup"><span data-stu-id="05df2-120">Choosing the Content for Descriptive Properties</span></span>](choosing-the-content-for-descriptive-properties.md)

<span data-ttu-id="05df2-121">Para obter informações sobre os parâmetros e valores de retorno dessas propriedades, consulte a seção [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) da referência do Microsoft acessibilidade ativa [C/C++](c-c---reference.md).</span><span class="sxs-lookup"><span data-stu-id="05df2-121">For information about the parameters and return values of these properties, see the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) section of the Microsoft Active Accessibility[C/C++ Reference](c-c---reference.md).</span></span>

 

 




