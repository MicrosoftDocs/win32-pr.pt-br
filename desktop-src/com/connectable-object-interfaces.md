---
title: Interfaces de objeto conectáveis
description: Interfaces de objeto conectáveis
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823014"
---
# <a name="connectable-object-interfaces"></a><span data-ttu-id="658f1-103">Interfaces de objeto conectáveis</span><span class="sxs-lookup"><span data-stu-id="658f1-103">Connectable Object Interfaces</span></span>

<span data-ttu-id="658f1-104">O suporte para objetos conectáveis requer suporte para quatro interfaces:</span><span class="sxs-lookup"><span data-stu-id="658f1-104">Support for connectable objects requires support for four interfaces:</span></span>

-   <span data-ttu-id="658f1-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) no objeto conectável</span><span class="sxs-lookup"><span data-stu-id="658f1-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) on the connectable object</span></span>
-   <span data-ttu-id="658f1-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) no objeto de ponto de conexão</span><span class="sxs-lookup"><span data-stu-id="658f1-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) on the connection point object</span></span>
-   <span data-ttu-id="658f1-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) em um objeto enumerador</span><span class="sxs-lookup"><span data-stu-id="658f1-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) on an enumerator object</span></span>
-   <span data-ttu-id="658f1-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) em um objeto enumerador</span><span class="sxs-lookup"><span data-stu-id="658f1-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) on an enumerator object</span></span>

<span data-ttu-id="658f1-109">Os dois últimos são definidos como enumeradores padrão para os tipos **IConnectionPoint \*** e [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span><span class="sxs-lookup"><span data-stu-id="658f1-109">The latter two are defined as standard enumerators for the types **IConnectionPoint \*** and [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span></span>

<span data-ttu-id="658f1-110">Além disso, o objeto conectável pode, opcionalmente, dar suporte a [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para fornecer informações suficientes para um cliente para que o cliente possa fornecer suporte para a interface de saída em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="658f1-110">Additionally, the connectable object can optionally support [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) to provide enough information to a client so that the client can provide support for the outgoing interface at run time.</span></span>

<span data-ttu-id="658f1-111">Por fim, o cliente deve fornecer um objeto Sink que implementa a interface de saída, que é uma interface COM personalizada definida pelo objeto que pode ser conectado.</span><span class="sxs-lookup"><span data-stu-id="658f1-111">Finally, the client must provide a sink object that implements the outgoing interface, which is a custom COM interface defined by the connectable object.</span></span>

<span data-ttu-id="658f1-112">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="658f1-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="658f1-113">Usando IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="658f1-113">Using IConnectionPointContainer</span></span>](using-iconnectionpointcontainer.md)
-   [<span data-ttu-id="658f1-114">Usando IConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="658f1-114">Using IConnectionPoint</span></span>](using-iconnectionpoint.md)
-   [<span data-ttu-id="658f1-115">Usando IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="658f1-115">Using IProvideClassInfo</span></span>](using-iprovideclassinfo.md)

## <a name="related-topics"></a><span data-ttu-id="658f1-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="658f1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="658f1-117">Arquitetura de objetos conectáveis</span><span class="sxs-lookup"><span data-stu-id="658f1-117">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




