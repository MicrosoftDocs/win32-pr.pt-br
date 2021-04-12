---
title: Diretrizes do servidor
description: Para que o Microsoft Acessibilidade Ativa funcione como projetado, os servidores devem fornecer informações de acessibilidade aos clientes.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363763"
---
# <a name="server-guidelines"></a><span data-ttu-id="15ef2-103">Diretrizes do servidor</span><span class="sxs-lookup"><span data-stu-id="15ef2-103">Server Guidelines</span></span>

<span data-ttu-id="15ef2-104">Para que o Microsoft Acessibilidade Ativa funcione como projetado, os servidores devem fornecer informações de acessibilidade aos clientes.</span><span class="sxs-lookup"><span data-stu-id="15ef2-104">For Microsoft Active Accessibility to work as designed, servers must provide accessibility information to clients.</span></span>

<span data-ttu-id="15ef2-105">Para implementar o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), os desenvolvedores de servidor devem seguir este processo básico.</span><span class="sxs-lookup"><span data-stu-id="15ef2-105">To implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), server developers must follow this basic process.</span></span>

1.  <span data-ttu-id="15ef2-106">Crie objetos acessíveis implementando as propriedades e os métodos do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para seus elementos personalizados de interface do usuário e para o cliente do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15ef2-106">Create accessible objects by implementing the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods for your custom user interface elements and for your application's client.</span></span> <span data-ttu-id="15ef2-107">Certifique-se de fornecer uma interface dupla que dê suporte a **IAccessible** e [**IDispatch**](idispatch-interface.md) para que os clientes escritos no Microsoft Visual Basic e várias linguagens de script possam obter informações sobre os objetos.</span><span class="sxs-lookup"><span data-stu-id="15ef2-107">Be sure to provide a dual interface that supports both **IAccessible** and [**IDispatch**](idispatch-interface.md) so that clients written in Microsoft Visual Basic and various scripting languages can get information about the objects.</span></span>
2.  <span data-ttu-id="15ef2-108">Chame [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para notificar os clientes sobre alterações em seus elementos personalizados da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="15ef2-108">Call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to notify clients of changes to your custom user interface elements.</span></span>
3.  <span data-ttu-id="15ef2-109">Manipule o [**WM \_ GetObject**](wm-getobject.md) para fornecer acesso aos seus objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="15ef2-109">Handle [**WM\_GETOBJECT**](wm-getobject.md) to provide access to your accessible objects.</span></span>

<span data-ttu-id="15ef2-110">Para obter sugestões e diretrizes para a criação de objetos acessíveis, consulte o [Guia do desenvolvedor para servidores de acessibilidade ativa](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="15ef2-110">For suggestions and guidelines for designing accessible objects, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="15ef2-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="15ef2-111">In this section</span></span>

-   [<span data-ttu-id="15ef2-112">Como os servidores implementam IDs filho</span><span class="sxs-lookup"><span data-stu-id="15ef2-112">How Servers Implement Child IDs</span></span>](how-servers-implement-child-ids.md)

 

 




