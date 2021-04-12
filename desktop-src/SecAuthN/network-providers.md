---
description: Um provedor de rede é uma DLL que dá suporte a um protocolo de rede específico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Provedores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170806"
---
# <a name="network-providers"></a><span data-ttu-id="b81e4-103">Provedores de rede</span><span class="sxs-lookup"><span data-stu-id="b81e4-103">Network Providers</span></span>

<span data-ttu-id="b81e4-104">Um provedor de rede é uma DLL que dá suporte a um protocolo de rede específico.</span><span class="sxs-lookup"><span data-stu-id="b81e4-104">A network provider is a DLL that supports a specific network protocol.</span></span> <span data-ttu-id="b81e4-105">Ele também implementa a [API do provedor de rede](network-provider-api.md).</span><span class="sxs-lookup"><span data-stu-id="b81e4-105">It also implements the [Network Provider API](network-provider-api.md).</span></span> <span data-ttu-id="b81e4-106">Isso permite que ele interaja com o sistema operacional Windows para receber solicitações de rede padrão, como solicitações de conexão ou desconexão.</span><span class="sxs-lookup"><span data-stu-id="b81e4-106">This enables it to interact with the Windows operating system to receive standard network requests, such as connection or disconnection requests.</span></span> <span data-ttu-id="b81e4-107">Para lidar com essas solicitações, o provedor de rede chama a API específica da rede apropriada ao protocolo de rede que o provedor de rede suporta.</span><span class="sxs-lookup"><span data-stu-id="b81e4-107">To handle these requests, the network provider then calls the network-specific API that is appropriate to the network protocol the network provider supports.</span></span> <span data-ttu-id="b81e4-108">Em outras palavras, o provedor de rede encapsula a funcionalidade específica da rede em uma DLL, que expõe uma interface padrão ao Windows.</span><span class="sxs-lookup"><span data-stu-id="b81e4-108">In other words, the network provider wraps the network-specific functionality in a DLL, which exposes a standard interface to Windows.</span></span>

<span data-ttu-id="b81e4-109">Usando provedores de rede, o Windows pode dar suporte a vários tipos diferentes de protocolos de rede sem precisar saber os detalhes específicos da rede de cada rede.</span><span class="sxs-lookup"><span data-stu-id="b81e4-109">Using network providers, Windows can support many different types of network protocols without having to know the network-specific details of each network.</span></span> <span data-ttu-id="b81e4-110">Isso é essencial porque novos protocolos de rede estão sendo desenvolvidos o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="b81e4-110">This is essential because new network protocols are being developed all the time.</span></span> <span data-ttu-id="b81e4-111">Com os provedores de rede, o suporte a um novo protocolo simplesmente requer a criação e a instalação de um novo provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="b81e4-111">With network providers, supporting a new protocol simply requires creating and installing a new network provider.</span></span>

<span data-ttu-id="b81e4-112">Para obter informações sobre as funções e estruturas do provedor de rede, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b81e4-112">For information about network provider functions and structures, see the following topics:</span></span>

-   [<span data-ttu-id="b81e4-113">Funções de provedor de rede</span><span class="sxs-lookup"><span data-stu-id="b81e4-113">Network Provider Functions</span></span>](authentication-functions.md)
-   [<span data-ttu-id="b81e4-114">Estruturas de provedor de rede</span><span class="sxs-lookup"><span data-stu-id="b81e4-114">Network Provider Structures</span></span>](authentication-structures.md)

 

 



