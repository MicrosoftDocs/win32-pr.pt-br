---
title: Proxy
description: Um proxy reside no espaço de endereço do processo de chamada e atua como um substituto para o objeto remoto.
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "105780693"
---
# <a name="proxy"></a><span data-ttu-id="bb9b3-103">Proxy</span><span class="sxs-lookup"><span data-stu-id="bb9b3-103">Proxy</span></span>

<span data-ttu-id="bb9b3-104">Um proxy reside no espaço de endereço do processo de chamada e atua como um substituto para o objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-104">A proxy resides in the address space of the calling process and acts as a surrogate for the remote object.</span></span> <span data-ttu-id="bb9b3-105">Da perspectiva do objeto de chamada, o proxy é o objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-105">From the perspective of the calling object, the proxy is the object.</span></span> <span data-ttu-id="bb9b3-106">Normalmente, a função do proxy é empacotar os parâmetros da interface para chamadas para métodos em suas interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-106">Typically, the proxy's role is to package the interface parameters for calls to methods in its object interfaces.</span></span> <span data-ttu-id="bb9b3-107">O proxy empacota os parâmetros em um buffer de mensagens e passa o buffer para o canal, que manipula o transporte entre os processos.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-107">The proxy packages the parameters into a message buffer and passes the buffer onto the channel, which handles the transport between processes.</span></span> <span data-ttu-id="bb9b3-108">O proxy é implementado como um objeto agregado, ou composto.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-108">The proxy is implemented as an aggregate, or composite, object.</span></span> <span data-ttu-id="bb9b3-109">Ele contém uma peça do gerente, fornecida pelo sistema, chamada Gerenciador de proxy e um ou mais componentes específicos de interface chamados de proxies de interface.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-109">It contains a system-provided, manager piece called the proxy manager and one or more interface-specific components called interface proxies.</span></span> <span data-ttu-id="bb9b3-110">O número de proxies de interface é igual ao número de interfaces de objeto que foram expostas a esse cliente específico.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-110">The number of interface proxies equals the number of object interfaces that have been exposed to that particular client.</span></span> <span data-ttu-id="bb9b3-111">Para o cliente estar de conformidade com o modelo de objeto de componente, o proxy parece ser o objeto real.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-111">To the client complying with the component object model, the proxy appears to be the real object.</span></span>

> [!Note]  
> <span data-ttu-id="bb9b3-112">Com o marshaling personalizado, o proxy pode ser implementado da mesma forma ou pode se comunicar diretamente com o objeto sem usar um stub.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-112">With custom marshaling, the proxy can be implemented similarly or it can communicate directly with the object without using a stub.</span></span>

 

<span data-ttu-id="bb9b3-113">Cada proxy de interface é um objeto de componente que implementa o código de marshaling para uma das interfaces do objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-113">Each interface proxy is a component object that implements the marshaling code for one of the object's interfaces.</span></span> <span data-ttu-id="bb9b3-114">O proxy representa o objeto para o qual ele fornece o código de marshaling.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-114">The proxy represents the object for which it provides marshaling code.</span></span> <span data-ttu-id="bb9b3-115">Cada proxy também implementa a interface [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) .</span><span class="sxs-lookup"><span data-stu-id="bb9b3-115">Each proxy also implements the [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) interface.</span></span> <span data-ttu-id="bb9b3-116">Embora a interface de objeto representada pelo proxy seja pública, a implementação de **IRpcProxyBuffer** é privada e usada internamente no proxy.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-116">Although the object interface represented by the proxy is public, the **IRpcProxyBuffer** implementation is private and is used internally within the proxy.</span></span> <span data-ttu-id="bb9b3-117">O Gerenciador de proxy controla os proxies de interface e também contém a implementação pública da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle para a agregação.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-117">The proxy manager keeps track of the interface proxies and also contains the public implementation of the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface for the aggregate.</span></span> <span data-ttu-id="bb9b3-118">Cada proxy de interface pode existir em uma DLL separada que é carregada quando a interface à qual ele dá suporte é materializada para o cliente.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-118">Each interface proxy can exist in a separate DLL that is loaded when the interface it supports is materialized to the client.</span></span>

## <a name="structure-of-the-proxy"></a><span data-ttu-id="bb9b3-119">Estrutura do proxy</span><span class="sxs-lookup"><span data-stu-id="bb9b3-119">Structure of the Proxy</span></span>

<span data-ttu-id="bb9b3-120">O diagrama a seguir mostra a estrutura de um proxy que dá suporte ao empacotamento padrão de parâmetros que pertencem a duas interfaces: IA1 e IA2.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-120">The following diagram shows the structure of a proxy that supports the standard marshaling of parameters belonging to two interfaces: IA1 and IA2.</span></span> <span data-ttu-id="bb9b3-121">Cada proxy de interface implementa [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) para comunicação interna entre as partes agregadas.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-121">Each interface proxy implements [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) for internal communication between the aggregate pieces.</span></span> <span data-ttu-id="bb9b3-122">Quando o proxy está pronto para passar seus parâmetros de marshaling pelo limite do processo, ele chama os métodos na interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) , que é implementada pelo canal.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-122">When the proxy is ready to pass its marshaled parameters across the process boundary, it calls methods in the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface, which is implemented by the channel.</span></span> <span data-ttu-id="bb9b3-123">O canal, por sua vez, encaminha a chamada para a biblioteca de tempo de execução RPC para que possa acessar seu destino no objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9b3-123">The channel in turn forwards the call to the RPC run-time library so that it can reach its destination in the object.</span></span>

![Diagrama que mostra a estrutura do proxy.](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a><span data-ttu-id="bb9b3-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb9b3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb9b3-126">Channel</span><span class="sxs-lookup"><span data-stu-id="bb9b3-126">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="bb9b3-127">Comunicação entre objetos</span><span class="sxs-lookup"><span data-stu-id="bb9b3-127">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="bb9b3-128">Detalhes de marshaling</span><span class="sxs-lookup"><span data-stu-id="bb9b3-128">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="bb9b3-129">RPC da Microsoft</span><span class="sxs-lookup"><span data-stu-id="bb9b3-129">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="bb9b3-130">Gerenciador</span><span class="sxs-lookup"><span data-stu-id="bb9b3-130">Stub</span></span>](stub.md)
</dt> </dl>

 

 