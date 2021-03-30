---
title: Tipos de suporte do IAccessible
description: Tipos de suporte do IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635964"
---
# <a name="types-of-iaccessible-support"></a><span data-ttu-id="3b5b9-103">Tipos de suporte do IAccessible</span><span class="sxs-lookup"><span data-stu-id="3b5b9-103">Types of IAccessible Support</span></span>

<span data-ttu-id="3b5b9-104">Os Microsoft Acessibilidade Ativa Servers têm dois tipos de suporte a [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : nativo e com proxy.</span><span class="sxs-lookup"><span data-stu-id="3b5b9-104">Microsoft Active Accessibility servers have two types of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support: native and proxied.</span></span> <span data-ttu-id="3b5b9-105">Os elementos da interface do usuário usados em um aplicativo determinam qual tipo de suporte é apropriado.</span><span class="sxs-lookup"><span data-stu-id="3b5b9-105">The UI elements used in an application determine which type of support is appropriate.</span></span> <span data-ttu-id="3b5b9-106">Muitos servidores que estão sendo gravados hoje aproveitam totalmente os proxies do **IAccessible** e só implementam o **IAccessible** para esses controles que não são proxies por Oleacc.dll, como controles sem janela ou controles com um nome de classe de janela personalizado.</span><span class="sxs-lookup"><span data-stu-id="3b5b9-106">Many servers being written today take full advantage of **IAccessible** proxies and only implement **IAccessible** for those controls that are not proxied by Oleacc.dll, such as windowless controls or controls with a custom window class name.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3b5b9-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3b5b9-107">In this section</span></span>

-   [<span data-ttu-id="3b5b9-108">Implementação de Acessibilidade Ativa nativo</span><span class="sxs-lookup"><span data-stu-id="3b5b9-108">Native Active Accessibility Implementation</span></span>](native-active-accessibility-implementation.md)
-   [<span data-ttu-id="3b5b9-109">Proxies do IAccessible</span><span class="sxs-lookup"><span data-stu-id="3b5b9-109">IAccessible Proxies</span></span>](iaccessible-proxies.md)

 

 




