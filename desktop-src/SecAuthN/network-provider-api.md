---
description: Um provedor de rede é uma DLL que permite que o sistema operacional Windows interaja com outros tipos de redes, como Novell. É um cliente do driver WNet do Windows.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: API do provedor de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752539"
---
# <a name="network-provider-api"></a><span data-ttu-id="b63c4-104">API do provedor de rede</span><span class="sxs-lookup"><span data-stu-id="b63c4-104">Network Provider API</span></span>

<span data-ttu-id="b63c4-105">Um provedor de rede é uma DLL que permite que o sistema operacional Windows interaja com outros tipos de redes, como Novell.</span><span class="sxs-lookup"><span data-stu-id="b63c4-105">A network provider is a DLL that enables the Windows operating system to interact with other kinds of networks, such as Novell.</span></span> <span data-ttu-id="b63c4-106">É um cliente do driver WNet do Windows.</span><span class="sxs-lookup"><span data-stu-id="b63c4-106">It is a client of the Windows WNet driver.</span></span> <span data-ttu-id="b63c4-107">Um provedor de rede implementa ações específicas de rede, como fazer uma conexão, e expõe uma interface comum ao Windows.</span><span class="sxs-lookup"><span data-stu-id="b63c4-107">A network provider implements network-specific actions, such as making a connection, and exposes a common interface to Windows.</span></span> <span data-ttu-id="b63c4-108">Essa interface é chamada de API do provedor de rede e consiste em funções implementadas pelo provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="b63c4-108">This interface is called the Network Provider API and consists of functions implemented by the network provider.</span></span> <span data-ttu-id="b63c4-109">Você pode criar uma DLL de provedor de rede para dar suporte a novos protocolos de rede.</span><span class="sxs-lookup"><span data-stu-id="b63c4-109">You can create a network provider DLL to support new network protocols.</span></span>

<span data-ttu-id="b63c4-110">Como cada rede expõe uma interface comum por meio de seu provedor, o Windows pode interagir com vários tipos de redes sem conhecer seus detalhes de implementação específicos da rede.</span><span class="sxs-lookup"><span data-stu-id="b63c4-110">Because each network exposes a common interface through its provider, Windows can interact with several types of networks without knowing their network-specific implementation details.</span></span>

<span data-ttu-id="b63c4-111">O [*roteador do provedor múltiplo*](../secgloss/m-gly.md) (MPR) trata da comunicação com todos os vários provedores de rede no sistema e apresenta uma rede integrada ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b63c4-111">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication with all of the various network providers on the system and presents an integrated network to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b63c4-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b63c4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b63c4-113">Provedores de rede</span><span class="sxs-lookup"><span data-stu-id="b63c4-113">Network Providers</span></span>](network-providers.md)
</dt> <dt>

[<span data-ttu-id="b63c4-114">Gerenciador de Credenciais</span><span class="sxs-lookup"><span data-stu-id="b63c4-114">Credential Manager</span></span>](credential-manager.md)
</dt> <dt>

[<span data-ttu-id="b63c4-115">Roteador de vários provedores</span><span class="sxs-lookup"><span data-stu-id="b63c4-115">Multiple Provider Router</span></span>](multiple-provider-router.md)
</dt> <dt>

[<span data-ttu-id="b63c4-116">Funções implementadas por provedores de rede</span><span class="sxs-lookup"><span data-stu-id="b63c4-116">Functions Implemented by Network Providers</span></span>](functions-implemented-by-network-providers.md)
</dt> <dt>

[<span data-ttu-id="b63c4-117">API de gerenciamento de credenciais</span><span class="sxs-lookup"><span data-stu-id="b63c4-117">Credential Management API</span></span>](credential-management-api.md)
</dt> <dt>

[<span data-ttu-id="b63c4-118">API de notificação de conexão</span><span class="sxs-lookup"><span data-stu-id="b63c4-118">Connection Notification API</span></span>](connection-notification-api.md)
</dt> </dl>

 

 
