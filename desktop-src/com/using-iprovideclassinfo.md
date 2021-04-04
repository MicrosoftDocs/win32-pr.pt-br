---
title: Usando IProvideClassInfo
description: Usando IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008437"
---
# <a name="using-iprovideclassinfo"></a><span data-ttu-id="cc141-103">Usando IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="cc141-103">Using IProvideClassInfo</span></span>

<span data-ttu-id="cc141-104">Um objeto conectável pode oferecer as interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) para que seus clientes possam examinar facilmente suas informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="cc141-104">A connectable object can offer the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) interfaces so that its clients can easily examine its type information.</span></span> <span data-ttu-id="cc141-105">Esse recurso é importante ao lidar com interfaces de saída, que, por definição, são definidos por um objeto, mas implementados por um cliente em seu próprio objeto Sink.</span><span class="sxs-lookup"><span data-stu-id="cc141-105">This capability is important when dealing with outgoing interfaces, which, by definition, are defined by an object but implemented by a client on its own sink object.</span></span> <span data-ttu-id="cc141-106">Em alguns casos, uma interface de saída é conhecida em tempo de compilação tanto para o objeto connectável quanto para o objeto Sink; Esse é o caso com [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span><span class="sxs-lookup"><span data-stu-id="cc141-106">In some cases, an outgoing interface is known at compile time to both the connectable object and the sink object; such is the case with [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span></span>

<span data-ttu-id="cc141-107">Em outros casos, no entanto, somente o objeto conectável sabe suas definições de interface de saída no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="cc141-107">In other cases, however, only the connectable object knows its outgoing interface definitions at compile time.</span></span> <span data-ttu-id="cc141-108">Nesses casos, o cliente deve obter as informações de tipo da interface de saída para que ela possa fornecer dinamicamente um coletor com suporte aos pontos de entrada certos, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cc141-108">In these cases, the client must obtain the type information for the outgoing interface so that it can dynamically provide a sink supporting the right entry points, as follows:</span></span>

1.  <span data-ttu-id="cc141-109">O cliente enumera os pontos de conexão e, em seguida, para obter o IIDs de interfaces de saída com suporte do objeto connectável, chama [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) para cada ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="cc141-109">The client enumerates the connection points and then, to obtain the IIDs of outgoing interfaces supported by the connectable object, calls [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) for each connection point.</span></span>
2.  <span data-ttu-id="cc141-110">O cliente consulta o objeto que pôde ser conectado para uma das interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="cc141-110">The client queries the connectable object for one of the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces.</span></span>
3.  <span data-ttu-id="cc141-111">O cliente chama métodos nas interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) para obter as informações de tipo para a interface de saída.</span><span class="sxs-lookup"><span data-stu-id="cc141-111">The client calls methods in the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces to get the type information for the outgoing interface.</span></span>
4.  <span data-ttu-id="cc141-112">O cliente cria um objeto de coletor que dá suporte à interface de saída.</span><span class="sxs-lookup"><span data-stu-id="cc141-112">The client creates a sink object supporting the outgoing interface.</span></span>
5.  <span data-ttu-id="cc141-113">O processo continua e o cliente chama [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) para conectar seu coletor ao ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="cc141-113">The process continues, and the client calls [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) to connect its sink to the connection point.</span></span>

<span data-ttu-id="cc141-114">Nas informações de tipo, a [**origem**](/windows/desktop/Midl/source) do atributo marca uma [**interface**](/windows/desktop/Midl/interface) ou [**dispinterface**](/windows/desktop/Midl/dispinterface) listada em uma [**coclass**](/windows/desktop/Midl/coclass) como uma interface de saída.</span><span class="sxs-lookup"><span data-stu-id="cc141-114">In the type information, the attribute [**source**](/windows/desktop/Midl/source) marks an [**interface**](/windows/desktop/Midl/interface) or [**dispinterface**](/windows/desktop/Midl/dispinterface) listed under a [**coclass**](/windows/desktop/Midl/coclass) as an outgoing interface.</span></span> <span data-ttu-id="cc141-115">Aqueles listados sem esse atributo são considerados interfaces de entrada.</span><span class="sxs-lookup"><span data-stu-id="cc141-115">Those listed without this attribute are considered incoming interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc141-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc141-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc141-117">Interfaces de objeto conectáveis</span><span class="sxs-lookup"><span data-stu-id="cc141-117">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cc141-118">Fornecendo informações de classe</span><span class="sxs-lookup"><span data-stu-id="cc141-118">Providing Class Information</span></span>](providing-class-information.md)
</dt> </dl>

 

 