---
title: Comunicação de cliente/servidor
description: O mecanismo WinEvents fornece uma maneira para que os servidores se comuniquem facilmente com os clientes do Microsoft Acessibilidade Ativa.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "105813624"
---
# <a name="clientserver-communication"></a><span data-ttu-id="4b86e-103">Comunicação de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="4b86e-103">Client/Server Communication</span></span>

<span data-ttu-id="4b86e-104">O mecanismo [WinEvents](winevents-overview.md) fornece uma maneira para que os servidores se comuniquem facilmente com os clientes do Microsoft acessibilidade ativa.</span><span class="sxs-lookup"><span data-stu-id="4b86e-104">The [WinEvents](winevents-overview.md) mechanism provides a way for servers to communicate easily with Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="4b86e-105">Os clientes geralmente coletam informações reagindo ao WinEvents (por exemplo, o foco seguinte), mas são livres para solicitar informações de um servidor a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="4b86e-105">Clients often collect information by reacting to WinEvents (for example, following focus), but they are free to request information from a server at any time.</span></span>

<span data-ttu-id="4b86e-106">Para solicitar informações para um objeto acessível que gera um WinEvent, um cliente deve processar o evento e estabelecer uma conexão com o objeto acessível relevante.</span><span class="sxs-lookup"><span data-stu-id="4b86e-106">To request information for an accessible object that generates a WinEvent, a client must process the event and establish a connection with the relevant accessible object.</span></span> <span data-ttu-id="4b86e-107">Para fazer isso, o cliente executa as seis etapas a seguir:</span><span class="sxs-lookup"><span data-stu-id="4b86e-107">To do this, the client performs the following six steps:</span></span>

-   <span data-ttu-id="4b86e-108">Um servidor chama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para gerar uma notificação WinEvent para cada alteração em seus elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b86e-108">A server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to generate a WinEvent notification for each change to its user interface elements.</span></span>
-   <span data-ttu-id="4b86e-109">O código de gerenciamento WinEvent no usuário determina se algum aplicativo cliente registrou uma [*função de Hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent usando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e chama a função de retorno de chamada registrada.</span><span class="sxs-lookup"><span data-stu-id="4b86e-109">The WinEvent management code in USER determines if any client applications have registered a WinEvent [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and calls the registered callback function.</span></span>
-   <span data-ttu-id="4b86e-110">Em sua função de retorno de chamada, o cliente solicita acesso ao objeto que gerou o evento chamando [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ou outras funções de recuperação de objeto acessíveis.</span><span class="sxs-lookup"><span data-stu-id="4b86e-110">In its callback function, the client requests access to the object that generated the event by calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) or other accessible object retrieval functions.</span></span> <span data-ttu-id="4b86e-111">Para obter mais informações, consulte [recuperando um objeto IAccessible](retrieving-an-iaccessible-object.md).</span><span class="sxs-lookup"><span data-stu-id="4b86e-111">For more information, see [Retrieving an IAccessible Object](retrieving-an-iaccessible-object.md).</span></span>
-   <span data-ttu-id="4b86e-112">Essa API do Microsoft Acessibilidade Ativa envia ao aplicativo de servidor uma mensagem do [**WM \_ GetObject**](wm-getobject.md) para recuperar o objeto acessível.</span><span class="sxs-lookup"><span data-stu-id="4b86e-112">This Microsoft Active Accessibility API sends the server application a [**WM\_GETOBJECT**](wm-getobject.md) message to retrieve the accessible object.</span></span>
-   <span data-ttu-id="4b86e-113">Em resposta ao [**WM \_ GetObject**](wm-getobject.md), o aplicativo de servidor retorna zero ou retorna um valor que atua como uma referência única para o objeto que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="4b86e-113">In response to [**WM\_GETOBJECT**](wm-getobject.md), the server application either returns zero or returns a value that acts as a one-time reference to the object that generated the event.</span></span>
-   <span data-ttu-id="4b86e-114">Se o servidor retornar zero, o Microsoft Acessibilidade Ativa criará um objeto proxy e fornecerá seu endereço ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4b86e-114">If the server returns zero, Microsoft Active Accessibility creates a proxy object and gives its address to the client.</span></span> <span data-ttu-id="4b86e-115">Caso contrário, o Microsoft Acessibilidade Ativa usa essa referência para recuperar o endereço de uma interface de objeto, como [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou [**IDispatch**](idispatch-interface.md), e fornece esse endereço ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4b86e-115">Otherwise, Microsoft Active Accessibility uses this reference to retrieve the address of an object interface such as [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or [**IDispatch**](idispatch-interface.md), and gives that address to the client.</span></span>

<span data-ttu-id="4b86e-116">Depois que o cliente tem um endereço de interface, ele pode chamar as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e os métodos do objeto acessível para recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="4b86e-116">Once the client has an interface address, it can call the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of the accessible object to retrieve information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4b86e-117">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="4b86e-117">In this section</span></span>

-   [<span data-ttu-id="4b86e-118">WinEvents e Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="4b86e-118">WinEvents and Active Accessibility</span></span>](winevents-overview.md)
-   [<span data-ttu-id="4b86e-119">Como o WM \_ GetObject funciona</span><span class="sxs-lookup"><span data-stu-id="4b86e-119">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
-   [<span data-ttu-id="4b86e-120">Recuperando um objeto IAccessible</span><span class="sxs-lookup"><span data-stu-id="4b86e-120">Retrieving an IAccessible Object</span></span>](retrieving-an-iaccessible-object.md)

 

 




