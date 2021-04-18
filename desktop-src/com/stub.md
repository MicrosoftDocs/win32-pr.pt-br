---
title: Gerenciador
description: O stub, como o proxy, é composto de uma ou mais partes de interface e um gerente.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "105763465"
---
# <a name="stub"></a><span data-ttu-id="ce817-103">Gerenciador</span><span class="sxs-lookup"><span data-stu-id="ce817-103">Stub</span></span>

<span data-ttu-id="ce817-104">O stub, como o proxy, é composto de uma ou mais partes de interface e um gerente.</span><span class="sxs-lookup"><span data-stu-id="ce817-104">The stub, like the proxy, is made up of one or more interface pieces and a manager.</span></span> <span data-ttu-id="ce817-105">Cada stub de interface fornece código para desempacotar os parâmetros e o código que chama uma das interfaces com suporte do objeto.</span><span class="sxs-lookup"><span data-stu-id="ce817-105">Each interface stub provides code to unmarshal the parameters and code that calls one of the object's supported interfaces.</span></span> <span data-ttu-id="ce817-106">Cada stub também fornece uma interface para comunicação interna.</span><span class="sxs-lookup"><span data-stu-id="ce817-106">Each stub also provides an interface for internal communication.</span></span> <span data-ttu-id="ce817-107">O Gerenciador de stub controla os stubs de interface disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ce817-107">The stub manager keeps track of the available interface stubs.</span></span>

<span data-ttu-id="ce817-108">No entanto, há as seguintes diferenças entre o stub e o proxy:</span><span class="sxs-lookup"><span data-stu-id="ce817-108">There are, however, the following differences between the stub and the proxy:</span></span>

-   <span data-ttu-id="ce817-109">A diferença mais importante é que o stub representa o cliente no espaço de endereço do objeto.</span><span class="sxs-lookup"><span data-stu-id="ce817-109">The most important difference is that the stub represents the client in the object's address space.</span></span>
-   <span data-ttu-id="ce817-110">O stub não é implementado como um objeto de agregação porque não há nenhum requisito de que o cliente seja exibido como uma única unidade; cada parte no stub é um componente separado.</span><span class="sxs-lookup"><span data-stu-id="ce817-110">The stub is not implemented as an aggregate object because there is no requirement that the client be viewed as a single unit; each piece in the stub is a separate component.</span></span>
-   <span data-ttu-id="ce817-111">Os stubs de interface são privados em vez de públicos.</span><span class="sxs-lookup"><span data-stu-id="ce817-111">The interface stubs are private rather than public.</span></span>
-   <span data-ttu-id="ce817-112">Os stubs de interface implementam [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), não [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span><span class="sxs-lookup"><span data-stu-id="ce817-112">The interface stubs implement [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), not [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).</span></span>
-   <span data-ttu-id="ce817-113">Em vez dos parâmetros de empacotamento a serem empacotados, o stub os empacota depois que eles foram empacotados e, em seguida, empacota a resposta.</span><span class="sxs-lookup"><span data-stu-id="ce817-113">Instead of packaging parameters to be marshaled, the stub unpackages them after they have been marshaled and then packages the reply.</span></span>

## <a name="structure-of-the-stub"></a><span data-ttu-id="ce817-114">Estrutura do stub</span><span class="sxs-lookup"><span data-stu-id="ce817-114">Structure of the Stub</span></span>

<span data-ttu-id="ce817-115">O diagrama a seguir mostra a estrutura do stub.</span><span class="sxs-lookup"><span data-stu-id="ce817-115">The following diagram shows the structure of the stub.</span></span> <span data-ttu-id="ce817-116">Cada stub de interface é conectado a uma interface no objeto.</span><span class="sxs-lookup"><span data-stu-id="ce817-116">Each interface stub is connected to an interface on the object.</span></span> <span data-ttu-id="ce817-117">O canal despacha as mensagens de entrada para o stub de interface apropriado.</span><span class="sxs-lookup"><span data-stu-id="ce817-117">The channel dispatches incoming messages to the appropriate interface stub.</span></span> <span data-ttu-id="ce817-118">Todos os componentes falam com o canal por meio do [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), a interface que fornece acesso à biblioteca de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="ce817-118">All the components talk to the channel through [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), the interface that provides access to the RPC run-time library.</span></span>

![Captura de tela que mostra a estrutura do stub.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a><span data-ttu-id="ce817-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce817-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce817-121">Channel</span><span class="sxs-lookup"><span data-stu-id="ce817-121">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="ce817-122">Comunicação entre objetos</span><span class="sxs-lookup"><span data-stu-id="ce817-122">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="ce817-123">Detalhes de marshaling</span><span class="sxs-lookup"><span data-stu-id="ce817-123">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="ce817-124">RPC da Microsoft</span><span class="sxs-lookup"><span data-stu-id="ce817-124">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="ce817-125">Proxy</span><span class="sxs-lookup"><span data-stu-id="ce817-125">Proxy</span></span>](proxy.md)
</dt> </dl>

 

 