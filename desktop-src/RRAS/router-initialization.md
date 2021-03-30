---
title: Inicialização do roteador
description: As informações de configuração do roteador, os gerenciadores de roteadores e os protocolos/clientes de roteamento são divididos em informações globais e por informações de interface e são armazenados no registro e no arquivo de catálogo telefônico do roteador, router. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- roteadores RRAS, inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634751"
---
# <a name="router-initialization"></a><span data-ttu-id="c100c-104">Inicialização do roteador</span><span class="sxs-lookup"><span data-stu-id="c100c-104">Router Initialization</span></span>

<span data-ttu-id="c100c-105">As informações de configuração do roteador, os gerenciadores de roteadores e os protocolos/clientes de roteamento são divididos em informações globais e por informações de interface e são armazenados no registro e no arquivo de catálogo telefônico do roteador, router. pbk.</span><span class="sxs-lookup"><span data-stu-id="c100c-105">Configuration information for the router, the router managers and the routing protocols/clients is divided into global information and per interface information and is stored in the registry and the router's phone-book file, Router.pbk.</span></span>

<span data-ttu-id="c100c-106">Quando o processo do roteador é iniciado, DIM (Dynamic interface Manager) lê a configuração do roteador no registro.</span><span class="sxs-lookup"><span data-stu-id="c100c-106">When the router process starts, DIM (Dynamic Interface Manager) reads the router configuration from the registry.</span></span> <span data-ttu-id="c100c-107">DIM cria as interfaces que são especificadas pelas informações de interface.</span><span class="sxs-lookup"><span data-stu-id="c100c-107">DIM creates the interfaces that are specified by the interface information.</span></span>

<span data-ttu-id="c100c-108">DIM também recupera as informações globais do Gerenciador de roteador.</span><span class="sxs-lookup"><span data-stu-id="c100c-108">DIM also retrieves the global router manager information.</span></span> <span data-ttu-id="c100c-109">DIM inicia os gerenciadores de roteador que correspondem a essas informações e transmite as informações.</span><span class="sxs-lookup"><span data-stu-id="c100c-109">DIM starts the router managers that correspond to this information, and passes them the information.</span></span> <span data-ttu-id="c100c-110">Por exemplo, se DIM encontrar informações globais para o Gerenciador de roteador IP no registro, DIM iniciará o Gerenciador de roteador IP e passará a ele as informações globais.</span><span class="sxs-lookup"><span data-stu-id="c100c-110">For example, if DIM finds global information for the IP router manager in the registry, DIM starts the IP router manager and passes it the global information.</span></span> <span data-ttu-id="c100c-111">Se nenhuma informação global estiver presente no registro para um Gerenciador de roteador específico, DIM não iniciará esse Gerenciador de roteador.</span><span class="sxs-lookup"><span data-stu-id="c100c-111">If no global information is present in the registry for a particular router manager, DIM does not start that router manager.</span></span>

<span data-ttu-id="c100c-112">Os gerenciadores de roteadores examinam as informações globais recebidas do DIM.</span><span class="sxs-lookup"><span data-stu-id="c100c-112">The router managers examine the global information received from DIM.</span></span> <span data-ttu-id="c100c-113">Se o Gerenciador de roteador encontrar informações específicas a um cliente específico dentro das informações globais, o Gerenciador de roteador carregará a DLL para o cliente (por exemplo IpNAT.dll) e inicializará o cliente chamando as funções [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) e [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) do cliente.</span><span class="sxs-lookup"><span data-stu-id="c100c-113">If the router manager finds information specific to a particular client within the global information, the router manager loads the DLL for the client (for example IpNAT.dll) and initializes the client by calling the client's [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) and [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) functions.</span></span> <span data-ttu-id="c100c-114">O Gerenciador de roteador passa as informações globais específicas do cliente para o cliente na chamada para [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span><span class="sxs-lookup"><span data-stu-id="c100c-114">The router manager passes the client-specific global information to the client in the call to [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span></span>

<span data-ttu-id="c100c-115">Em cada estágio, as informações passadas para a próxima entidade são opacas para a entidade que a precede.</span><span class="sxs-lookup"><span data-stu-id="c100c-115">At each stage, the information being passed to the next entity is opaque to the entity preceding it.</span></span> <span data-ttu-id="c100c-116">Ou seja, DIM não interpreta as informações globais para o Gerenciador do roteador IP, além do fato de que as informações são destinadas ao Gerenciador do roteador IP.</span><span class="sxs-lookup"><span data-stu-id="c100c-116">That is, DIM does not interpret the global information for the IP Router Manager, beyond the fact that the information is meant for the IP Router Manager.</span></span> <span data-ttu-id="c100c-117">Da mesma forma, o Gerenciador de roteador IP não interpreta as informações específicas do OSPF além do fato de que são informações de OSPF.</span><span class="sxs-lookup"><span data-stu-id="c100c-117">Similarly, the IP Router Manager does not interpret the OSPF specific information beyond the fact that it is OSPF information.</span></span>

 

 




