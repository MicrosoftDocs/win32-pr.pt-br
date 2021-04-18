---
description: Este tópico discute considerações de programação específicas ao usar a infraestrutura de pares.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considerações sobre programação (ponto a ponto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755971"
---
# <a name="programming-considerations-peer-to-peer"></a><span data-ttu-id="15dbe-103">Considerações sobre programação (ponto a ponto)</span><span class="sxs-lookup"><span data-stu-id="15dbe-103">Programming Considerations (Peer-to-Peer)</span></span>

<span data-ttu-id="15dbe-104">Este tópico discute considerações de programação específicas ao usar a infraestrutura de pares.</span><span class="sxs-lookup"><span data-stu-id="15dbe-104">This topic discusses specific programming considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="15dbe-105">Ao usar a infraestrutura de pares para desenvolver aplicativos de mesmo nível, você deve levar em conta as seguintes considerações de programação:</span><span class="sxs-lookup"><span data-stu-id="15dbe-105">When using the Peer Infrastructure to develop peer applications, you must take the following programming considerations into account:</span></span>

-   <span data-ttu-id="15dbe-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="15dbe-106">IPv6</span></span>

    <span data-ttu-id="15dbe-107">A infraestrutura de pares requer que o IPv6 seja instalado e iniciado para permitir que os aplicativos de rede de mesmo nível funcionem.</span><span class="sxs-lookup"><span data-stu-id="15dbe-107">The Peer Infrastructure requires that IPv6 be installed and started to enable peer networking applications to function.</span></span>

-   <span data-ttu-id="15dbe-108">Portas de firewall</span><span class="sxs-lookup"><span data-stu-id="15dbe-108">Firewall Ports</span></span>

    <span data-ttu-id="15dbe-109">Quando um firewall está sendo usado em uma rede (como o firewall de conexão com a Internet IPv6), as portas específicas devem ser abertas para permitir que a infraestrutura de mesmo nível funcione.</span><span class="sxs-lookup"><span data-stu-id="15dbe-109">When a firewall is being used on a network (such as the IPv6 Internet Connection firewall), specific ports must be opened to allow the Peer Infrastructure to function.</span></span> <span data-ttu-id="15dbe-110">As seguintes portas devem estar abertas:</span><span class="sxs-lookup"><span data-stu-id="15dbe-110">The following ports must be open:</span></span>

    <span data-ttu-id="15dbe-111">Porta TCP 3587 para a infraestrutura de agrupamento de pares.</span><span class="sxs-lookup"><span data-stu-id="15dbe-111">TCP port 3587 for the Peer Grouping Infrastructure.</span></span>

    <span data-ttu-id="15dbe-112">Porta UDP 3540 para a infraestrutura de grafo de pares.</span><span class="sxs-lookup"><span data-stu-id="15dbe-112">UDP port 3540 for the Peer Graphing Infrastructure.</span></span>

    > [!Note]  
    > <span data-ttu-id="15dbe-113">Os aplicativos que usam a infraestrutura de grafo de pares sobre TCP escolhem sua própria porta TCP ao chamar [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span><span class="sxs-lookup"><span data-stu-id="15dbe-113">Applications that use the Peer Graphing Infrastructure over TCP choose their own TCP port when calling [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="15dbe-114">Opção de soquete</span><span class="sxs-lookup"><span data-stu-id="15dbe-114">Socket Option</span></span>

    <span data-ttu-id="15dbe-115">Ao tentar se conectar a outros nós de mesmo nível IPv6 diretamente (sem usar a infraestrutura de mesmo nível), verifique se a opção de soquete \_ nível de proteção IPv6 \_ está definida como **nível de proteção \_ \_ irrestrito**.</span><span class="sxs-lookup"><span data-stu-id="15dbe-115">When attempting to connect to other IPv6 peer nodes directly (without using the Peer Infrastructure), ensure that the socket option IPV6\_PROTECTION\_LEVEL is set to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

-   <span data-ttu-id="15dbe-116">Largura de banda</span><span class="sxs-lookup"><span data-stu-id="15dbe-116">Bandwidth</span></span>

    <span data-ttu-id="15dbe-117">Ao usar o PNRP, um aplicativo pode publicar um ou mais [nomes de pares](peer-names.md) que podem ser resolvidos.</span><span class="sxs-lookup"><span data-stu-id="15dbe-117">When using PNRP, an application can publish one or more [peer names](peer-names.md) that can be resolved.</span></span> <span data-ttu-id="15dbe-118">Para cada nome de par registrado com o PNRP, há um aumento na largura de banda de rede que o PNRP usa para publicar o nome do par e mantê-lo disponível para ser resolvido por outros nós.</span><span class="sxs-lookup"><span data-stu-id="15dbe-118">For each peer name registered with PNRP, there is an increase in the network bandwidth that PNRP uses to publish the peer name, and keep it available to be resolved by other nodes.</span></span>

    <span data-ttu-id="15dbe-119">Para evitar o uso de muita largura de banda, os aplicativos devem evitar o registro de grandes números de nomes de pares em um computador.</span><span class="sxs-lookup"><span data-stu-id="15dbe-119">To prevent using too much bandwidth, applications should avoid registering large numbers of peer names on a computer.</span></span> <span data-ttu-id="15dbe-120">Por exemplo, um aplicativo que publica imagens não deve criar um nome de par para cada imagem, mas deve criar um nome de par para o serviço que publica imagens e usar um protocolo diferente para os clientes consultarem o serviço em busca de imagens específicas.</span><span class="sxs-lookup"><span data-stu-id="15dbe-120">For example, an application that publishes pictures should not create a peer name for each picture, but should create one peer name for the service that publishes pictures, and use a different protocol for clients to query the service for specific pictures.</span></span>

-   <span data-ttu-id="15dbe-121">Registro de nome de par</span><span class="sxs-lookup"><span data-stu-id="15dbe-121">Peer Name Registration</span></span>

    <span data-ttu-id="15dbe-122">Alguns aplicativos podem ser necessários para registrar o mesmo [nome de par](peer-names.md) em mais de um computador.</span><span class="sxs-lookup"><span data-stu-id="15dbe-122">Some applications may be required to register the same [peer name](peer-names.md) on more than one computer.</span></span> <span data-ttu-id="15dbe-123">Normalmente, isso acontece se um nome de par estiver associado a uma pessoa que usa mais de um computador.</span><span class="sxs-lookup"><span data-stu-id="15dbe-123">Typically, this happens if a peer name is associated with a person who uses more than one computer.</span></span> <span data-ttu-id="15dbe-124">Um método que você pode usar para registrar o mesmo nome de par em vários computadores é criar um grupo de pares para a pessoa e conectar-se a esse grupo de todos os computadores.</span><span class="sxs-lookup"><span data-stu-id="15dbe-124">One method that you can use to register the same peer name on multiple computers is to create a peer group for the person, and connect to that group from all computers.</span></span> <span data-ttu-id="15dbe-125">Outro método é criar uma identidade de mesmo nível e um nome de par em um computador, exportar a identidade do par desse computador e importá-la em outros computadores.</span><span class="sxs-lookup"><span data-stu-id="15dbe-125">Another method is to create a peer identity and peer name on one computer, export the peer identity from that computer, and import it on other computers.</span></span> <span data-ttu-id="15dbe-126">Isso permite que o mesmo nome de par seguro seja criado em todos os computadores que importaram a identidade de par.</span><span class="sxs-lookup"><span data-stu-id="15dbe-126">This allows the same secure peer name to be created on all the computers that have imported the peer identity.</span></span>

 

 



