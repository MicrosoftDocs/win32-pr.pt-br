---
title: API de anotação dinâmica
description: A API de anotação dinâmica é uma extensão do Microsoft Acessibilidade Ativa que permite aos desenvolvedores personalizar o suporte do IAccessible existente sem precisar usar a subclasse ou as técnicas de encapsulamento propensos a erros.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916646"
---
# <a name="dynamic-annotation-api"></a><span data-ttu-id="ebaa9-103">API de anotação dinâmica</span><span class="sxs-lookup"><span data-stu-id="ebaa9-103">Dynamic Annotation API</span></span>

<span data-ttu-id="ebaa9-104">A API de anotação dinâmica é uma extensão do Microsoft Acessibilidade Ativa que permite aos desenvolvedores personalizar o suporte do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente sem precisar usar a subclasse ou as técnicas de encapsulamento propensos a erros.</span><span class="sxs-lookup"><span data-stu-id="ebaa9-104">The Dynamic Annotation API is an extension to Microsoft Active Accessibility that allows developers to customize existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support without having to use error-prone subclassing or wrapping techniques.</span></span> <span data-ttu-id="ebaa9-105">Esse mecanismo também permite que os desenvolvedores transmitam dicas ou outras informações úteis para os proxies de Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="ebaa9-105">This mechanism also allows developers to pass hints or other useful information to the Oleacc.dll proxies.</span></span>

<span data-ttu-id="ebaa9-106">A anotação dinâmica normalmente é usada para corrigir ou corrigir uma instância imprecisa de um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) exposto por um proxy de Oleacc.dll existente.</span><span class="sxs-lookup"><span data-stu-id="ebaa9-106">Dynamic Annotation is typically used to correct or amend an inaccurate instance of an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object exposed by an existing Oleacc.dll proxy.</span></span> <span data-ttu-id="ebaa9-107">Por exemplo, você pode usá-lo para substituir as propriedades de [**nome**](name-property.md) e [**função**](role-property.md) fornecidas pelo proxy padrão e para fornecer as propriedades [**Description**](description-property.md) e [**Help**](help-property.md) (que podem não ser fornecidas pelo proxy padrão).</span><span class="sxs-lookup"><span data-stu-id="ebaa9-107">For example, you can use it to override the [**Name**](name-property.md) and [**Role**](role-property.md) properties provided by the default proxy, and to supply [**Description**](description-property.md) and [**Help**](help-property.md) properties (which may not be provided by the default proxy).</span></span>

<span data-ttu-id="ebaa9-108">Com o Windows 7, os desenvolvedores podem usar a API de anotação dinâmica para anotar as propriedades de automação da interface do usuário da Microsoft, bem como as propriedades do Microsoft Acessibilidade Ativa dos objetos de proxy que Oleacc.dll cria para controles padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="ebaa9-108">With Windows 7, developers can use the Dynamic Annotation API to annotate Microsoft UI Automation properties as well as Microsoft Active Accessibility properties of the proxy objects that Oleacc.dll creates for standard Windows controls.</span></span> <span data-ttu-id="ebaa9-109">Os objetos de proxy de Oleacc.dll servem para clientes de automação da interface do usuário e do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="ebaa9-109">The Oleacc.dll proxy objects serve both Microsoft Active Accessibility and UI Automation clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ebaa9-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ebaa9-110">In this section</span></span>

-   [<span data-ttu-id="ebaa9-111">Informações gerais</span><span class="sxs-lookup"><span data-stu-id="ebaa9-111">Background Information</span></span>](background-information.md)
-   [<span data-ttu-id="ebaa9-112">Alternativas para anotação dinâmica</span><span class="sxs-lookup"><span data-stu-id="ebaa9-112">Alternatives to Dynamic Annotation</span></span>](alternatives-to-dynamic-annotation.md)
-   [<span data-ttu-id="ebaa9-113">Tipos de anotação dinâmica</span><span class="sxs-lookup"><span data-stu-id="ebaa9-113">Types of Dynamic Annotation</span></span>](types-of-dynamic-annotation.md)
-   [<span data-ttu-id="ebaa9-114">Anotação direta</span><span class="sxs-lookup"><span data-stu-id="ebaa9-114">Direct Annotation</span></span>](direct-annotation.md)
-   [<span data-ttu-id="ebaa9-115">Anotação de mapa de valor</span><span class="sxs-lookup"><span data-stu-id="ebaa9-115">Value Map Annotation</span></span>](value-map-annotation.md)
-   [<span data-ttu-id="ebaa9-116">Anotação do servidor</span><span class="sxs-lookup"><span data-stu-id="ebaa9-116">Server Annotation</span></span>](server-annotation.md)
-   [<span data-ttu-id="ebaa9-117">Problemas e limitações</span><span class="sxs-lookup"><span data-stu-id="ebaa9-117">Issues and Limitations</span></span>](issues-and-limitations.md)

 

 




