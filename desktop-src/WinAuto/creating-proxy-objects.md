---
title: Criando objetos de proxy
description: Além de criar classes que implementam Propriedades e métodos do IAccessible, os desenvolvedores de servidores também podem precisar criar objetos de proxy que monitorem a vida útil de objetos acessíveis.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635253"
---
# <a name="creating-proxy-objects"></a><span data-ttu-id="764f3-103">Criando objetos de proxy</span><span class="sxs-lookup"><span data-stu-id="764f3-103">Creating Proxy Objects</span></span>

<span data-ttu-id="764f3-104">Além de criar classes que implementam Propriedades e métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , os desenvolvedores de servidores também podem precisar criar objetos de *proxy* que monitorem a vida útil de objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="764f3-104">In addition to designing classes that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods, server developers may also need to design *proxy* objects that monitor the life span of accessible objects.</span></span> <span data-ttu-id="764f3-105">Se um objeto acessível em um aplicativo estiver disponível todo o tempo em que o aplicativo está sendo executado, você não precisará criar um objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="764f3-105">If an accessible object in an application is available the entire time the application is running, then you do not need to create a proxy object.</span></span> <span data-ttu-id="764f3-106">Se for possível destruir o objeto acessível enquanto o aplicativo estiver em execução, você deverá criar um objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="764f3-106">If it is possible to destroy the accessible object while the application is running, then you must create a proxy object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="764f3-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="764f3-107">In this section</span></span>

-   [<span data-ttu-id="764f3-108">O que são objetos proxy?</span><span class="sxs-lookup"><span data-stu-id="764f3-108">What Are Proxy Objects?</span></span>](what-are-proxy-objects.md)
-   [<span data-ttu-id="764f3-109">Por que os objetos proxy são necessários</span><span class="sxs-lookup"><span data-stu-id="764f3-109">Why Proxy Objects Are Needed</span></span>](why-proxy-objects-are-needed.md)
-   [<span data-ttu-id="764f3-110">Considerações de design para objetos de proxy</span><span class="sxs-lookup"><span data-stu-id="764f3-110">Design Considerations for Proxy Objects</span></span>](design-considerations-for-proxy-objects.md)

 

 




