---
title: RPC da Microsoft
description: RPC da Microsoft
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634819"
---
# <a name="microsoft-rpc"></a><span data-ttu-id="2f337-103">RPC da Microsoft</span><span class="sxs-lookup"><span data-stu-id="2f337-103">Microsoft RPC</span></span>

<span data-ttu-id="2f337-104">O Microsoft RPC é um modelo de programação em um ambiente de computação distribuído.</span><span class="sxs-lookup"><span data-stu-id="2f337-104">Microsoft RPC is a model for programming in a distributed computing environment.</span></span> <span data-ttu-id="2f337-105">O objetivo do RPC é fornecer comunicação transparente para que o cliente pareça estar diretamente se comunicando com o servidor.</span><span class="sxs-lookup"><span data-stu-id="2f337-105">The goal of RPC is to provide transparent communication so that the client appears to be directly communicating with the server.</span></span> <span data-ttu-id="2f337-106">A implementação do RPC da Microsoft é compatível com o ambiente de computação distribuída (uso) do Open Software Foundation (DCE).</span><span class="sxs-lookup"><span data-stu-id="2f337-106">Microsoft's implementation of RPC is compatible with the Open Software Foundation (OSF) Distributed Computing Environment (DCE) RPC.</span></span>

<span data-ttu-id="2f337-107">Você pode configurar o RPC para usar um ou mais transportes, um ou mais serviços de nome e um ou mais servidores de segurança.</span><span class="sxs-lookup"><span data-stu-id="2f337-107">You can configure RPC to use one or more transports, one or more name services, and one or more security servers.</span></span> <span data-ttu-id="2f337-108">As interfaces para esses provedores são manipuladas pelo RPC.</span><span class="sxs-lookup"><span data-stu-id="2f337-108">The interfaces to those providers are handled by RPC.</span></span> <span data-ttu-id="2f337-109">Como o Microsoft RPC foi projetado para funcionar com vários provedores, você pode escolher os provedores que funcionam melhor para sua rede.</span><span class="sxs-lookup"><span data-stu-id="2f337-109">Because Microsoft RPC is designed to work with multiple providers, you can choose the providers that work best for your network.</span></span> <span data-ttu-id="2f337-110">O transporte é responsável por transmitir os dados pela rede.</span><span class="sxs-lookup"><span data-stu-id="2f337-110">The transport is responsible for transmitting the data across the network.</span></span> <span data-ttu-id="2f337-111">O nome do serviço usa um nome de objeto, como um moniker, e localiza seu local na rede.</span><span class="sxs-lookup"><span data-stu-id="2f337-111">The name service takes an object name, such as a moniker, and finds its location on the network.</span></span> <span data-ttu-id="2f337-112">O servidor de segurança oferece aos aplicativos a opção de negar acesso a usuários e/ou grupos específicos.</span><span class="sxs-lookup"><span data-stu-id="2f337-112">The security server offers applications the option of denying access to specific users and/or groups.</span></span> <span data-ttu-id="2f337-113">Consulte [regras de design de interface](interface-design-rules.md) para obter informações mais detalhadas sobre a segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f337-113">See [Interface Design Rules](interface-design-rules.md) for more detailed information about application security.</span></span>

<span data-ttu-id="2f337-114">Além das bibliotecas de tempo de execução RPC, o Microsoft RPC inclui o IDL (Interface Definition Language) e seu compilador.</span><span class="sxs-lookup"><span data-stu-id="2f337-114">In addition to the RPC run-time libraries, Microsoft RPC includes the Interface Definition Language (IDL) and its compiler.</span></span> <span data-ttu-id="2f337-115">Embora o arquivo IDL seja uma parte padrão do RPC, a Microsoft o aprimorou para estender sua funcionalidade para dar suporte a interfaces COM personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2f337-115">Although the IDL file is a standard part of RPC, Microsoft has enhanced it to extend its functionality to support custom COM interfaces.</span></span> <span data-ttu-id="2f337-116">O compilador de linguagem IDL da Microsoft (MIDL) usa o arquivo IDL que descreve sua interface personalizada para gerar vários arquivos discutidos na [criação e no registro de uma DLL de proxy](building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="2f337-116">The Microsoft Interface Definition Language (MIDL) compiler uses the IDL file that describes your custom interface to generate several files discussed in [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f337-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f337-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f337-118">Channel</span><span class="sxs-lookup"><span data-stu-id="2f337-118">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="2f337-119">Comunicação entre objetos</span><span class="sxs-lookup"><span data-stu-id="2f337-119">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="2f337-120">Detalhes de marshaling</span><span class="sxs-lookup"><span data-stu-id="2f337-120">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="2f337-121">Proxy</span><span class="sxs-lookup"><span data-stu-id="2f337-121">Proxy</span></span>](proxy.md)
</dt> <dt>

[<span data-ttu-id="2f337-122">Gerenciador</span><span class="sxs-lookup"><span data-stu-id="2f337-122">Stub</span></span>](stub.md)
</dt> </dl>

 

 




