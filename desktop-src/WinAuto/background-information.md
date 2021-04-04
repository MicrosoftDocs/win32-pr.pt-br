---
title: Informações gerais
description: O componente do Microsoft Acessibilidade Ativa, oleacc.dll, cria objetos de proxy que implementam o IAccessible em nome de controles padrão do Windows.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084047"
---
# <a name="background-information"></a><span data-ttu-id="be327-103">Informações gerais</span><span class="sxs-lookup"><span data-stu-id="be327-103">Background Information</span></span>

<span data-ttu-id="be327-104">O componente do Microsoft Acessibilidade Ativa, oleacc.dll, cria objetos de proxy que implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) em nome de controles padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="be327-104">The Microsoft Active Accessibility component, oleacc.dll, creates proxy objects that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) on behalf of standard Windows controls.</span></span> <span data-ttu-id="be327-105">Como esses proxies usam mensagens padrão do Windows e APIs específicas de controle para coletar informações sobre cada controle, não havia nenhum mecanismo direto para personalizar as informações que esses proxies expõem por meio do **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="be327-105">Because these proxies use standard Windows messages and control-specific APIs to collect information about each control, there has been no direct mechanism for customizing the information these proxies expose through **IAccessible**.</span></span>

<span data-ttu-id="be327-106">No momento, você pode personalizar uma implementação de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente usando as técnicas de subclasse e encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="be327-106">Currently, you can customize an existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation using subclassing and wrapping techniques.</span></span> <span data-ttu-id="be327-107">No entanto, essas técnicas são entediantes e sujeitas a erros.</span><span class="sxs-lookup"><span data-stu-id="be327-107">However, these techniques are tedious and error-prone.</span></span> <span data-ttu-id="be327-108">Na verdade, a maior parte do código escrito para substituir uma ou duas propriedades está preocupada com a implementação de subclasse e quebra automática; apenas uma pequena fração executa a tarefa real de substituir informações.</span><span class="sxs-lookup"><span data-stu-id="be327-108">In fact, the majority of the code written to override one or two properties is concerned with implementing subclassing and wrapping; only a small fraction carries out the real task of overriding information.</span></span> <span data-ttu-id="be327-109">A anotação dinâmica melhora a situação fornecendo recursos semelhantes sem exigir que você escreva o código de subclasse ou encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="be327-109">Dynamic Annotation improves the situation by providing similar capabilities without requiring you to write subclassing or wrapping code.</span></span> <span data-ttu-id="be327-110">Em vez disso, você pode se concentrar em fornecer código que forneça as informações corretas.</span><span class="sxs-lookup"><span data-stu-id="be327-110">Instead, you can focus on providing code that supplies the correct information.</span></span> <span data-ttu-id="be327-111">A anotação dinâmica permite que os desenvolvedores transmitam dicas e outras informações úteis para OLEACC para personalizar as informações que ele expõe.</span><span class="sxs-lookup"><span data-stu-id="be327-111">Dynamic Annotation allows developers to pass hints and other useful information to OLEACC to customize the information it exposes.</span></span> <span data-ttu-id="be327-112">Esse recurso sozinho reduzirá o custo de suporte ao Microsoft Acessibilidade Ativa e permitirá que os desenvolvedores aprimorem muito a acessibilidade de suas interfaces de usuário.</span><span class="sxs-lookup"><span data-stu-id="be327-112">This capability alone will reduce the cost of supporting Microsoft Active Accessibility and allow developers to greatly improve the accessibility of their user interfaces.</span></span>

 

 




