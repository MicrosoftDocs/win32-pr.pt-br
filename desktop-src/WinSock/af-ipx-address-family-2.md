---
description: A família de endereços IPX define a estrutura de endereçamento para protocolos que usam o endereçamento de soquete IPX padrão. Para esses transportes, um endereço de ponto de extremidade consiste em um número de rede, um endereço de nó e um número de soquete.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Família de endereços AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090410"
---
# <a name="af_ipx-address-family"></a><span data-ttu-id="bd824-104">\_Família de endereços IPX AF</span><span class="sxs-lookup"><span data-stu-id="bd824-104">AF\_IPX Address Family</span></span>

<span data-ttu-id="bd824-105">A família de endereços IPX define a estrutura de endereçamento para protocolos que usam o endereçamento de soquete IPX padrão.</span><span class="sxs-lookup"><span data-stu-id="bd824-105">The IPX address family defines the addressing structure for protocols that use standard IPX socket addressing.</span></span> <span data-ttu-id="bd824-106">Para esses transportes, um endereço de ponto de extremidade consiste em um número de rede, um endereço de nó e um número de soquete.</span><span class="sxs-lookup"><span data-stu-id="bd824-106">For these transports, an endpoint address consists of a network number, node address, and socket number.</span></span>

<span data-ttu-id="bd824-107">O número de rede é um domínio administrativo e normalmente nomeia um único segmento Ethernet ou token ring.</span><span class="sxs-lookup"><span data-stu-id="bd824-107">The network number is an administrative domain and typically names a single Ethernet or token ring segment.</span></span> <span data-ttu-id="bd824-108">O número do nó é um endereço físico de uma estação.</span><span class="sxs-lookup"><span data-stu-id="bd824-108">The node number is a station's physical address.</span></span> <span data-ttu-id="bd824-109">A combinação de NET e node formam um endereço de estação exclusivo que presume ser exclusivo no mundo.</span><span class="sxs-lookup"><span data-stu-id="bd824-109">The combination of net and node form a unique station address that is presumed to be unique in the world.</span></span> <span data-ttu-id="bd824-110">Os números de nó e de rede são representados em texto ASCII em uma notação de bloco ou tracejado como: ' 0101a040, 00001b498765 ' ou ' 01-01-a0-40, 00-00-1B-49-87-65 '.</span><span class="sxs-lookup"><span data-stu-id="bd824-110">Net and node numbers are represented in ASCII text in either block or dashed notation as: '0101a040,00001b498765' or '01-01-a0-40,00-00-1b-49-87-65'.</span></span> <span data-ttu-id="bd824-111">Os zeros à esquerda não precisam estar presentes.</span><span class="sxs-lookup"><span data-stu-id="bd824-111">Leading zeros need not be present.</span></span>

<span data-ttu-id="bd824-112">O número de soquete IPX é um número de serviço de rede/transporte muito parecido com um número de porta TCP e não deve ser confundido com o descritor de soquete Winsock.</span><span class="sxs-lookup"><span data-stu-id="bd824-112">The IPX socket number is a network/transport service number much like a TCP port number and is not to be confused with the Winsock socket descriptor.</span></span> <span data-ttu-id="bd824-113">Os números de soquete IPX são globais para a estação final e não podem ser associados a endereços de rede/nó específicos.</span><span class="sxs-lookup"><span data-stu-id="bd824-113">IPX socket numbers are global to the end station and cannot be bound to specific net/node addresses.</span></span> <span data-ttu-id="bd824-114">Por exemplo, se a estação final tiver duas placas de interface de rede, um soquete associado poderá enviar e receber em ambos os cartões.</span><span class="sxs-lookup"><span data-stu-id="bd824-114">For instance, if the end station has two network interface cards, a bound socket can send and receive on both cards.</span></span> <span data-ttu-id="bd824-115">Em particular, os soquetes de datagramas receberão datagramas de difusão em ambos os cartões.</span><span class="sxs-lookup"><span data-stu-id="bd824-115">In particular, datagram sockets would receive broadcast datagrams on both cards.</span></span>

> [!Caution]  
> <span data-ttu-id="bd824-116">SOCKADDR \_ IPX tem 14 bytes de comprimento e é menor que a estrutura de referência de [**SOCKADDR**](sockaddr-2.md) de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="bd824-116">SOCKADDR\_IPX is 14 bytes long and is shorter than the 16-byte [**sockaddr**](sockaddr-2.md) reference structure.</span></span> <span data-ttu-id="bd824-117">As implementações de IPX/SPX podem aceitar o comprimento de 16 bytes, bem como o comprimento real.</span><span class="sxs-lookup"><span data-stu-id="bd824-117">IPX/SPX implementations may accept the 16-byte length as well as the true length.</span></span> <span data-ttu-id="bd824-118">Se você usar \_ o sockaddr IPX e um comprimento embutido em código de 16 bytes, a implementação poderá assumir que ele tem acesso aos 2 bytes após sua estrutura.</span><span class="sxs-lookup"><span data-stu-id="bd824-118">If you use SOCKADDR\_IPX and a hard-coded length of 16 bytes, the implementation may assume that it has access to the 2 bytes following your structure.</span></span>

 



| <span data-ttu-id="bd824-119">Campo</span><span class="sxs-lookup"><span data-stu-id="bd824-119">Field</span></span>           | <span data-ttu-id="bd824-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bd824-120">Value</span></span>                                    |
|-----------------|------------------------------------------|
| <span data-ttu-id="bd824-121">**\_família SA**</span><span class="sxs-lookup"><span data-stu-id="bd824-121">**sa\_family**</span></span>  | <span data-ttu-id="bd824-122">Endereço IPX da família \_ de endereços em ordem de host.</span><span class="sxs-lookup"><span data-stu-id="bd824-122">Address family AF\_IPX in host order.</span></span>    |
| <span data-ttu-id="bd824-123">**\_Netnum SA**</span><span class="sxs-lookup"><span data-stu-id="bd824-123">**Sa\_netnum**</span></span>  | <span data-ttu-id="bd824-124">Identificador de rede IPX na ordem de rede.</span><span class="sxs-lookup"><span data-stu-id="bd824-124">IPX network identifier in network order.</span></span> |
| <span data-ttu-id="bd824-125">**\_Nodenum SA**</span><span class="sxs-lookup"><span data-stu-id="bd824-125">**Sa\_nodenum**</span></span> | <span data-ttu-id="bd824-126">Endereço do nó de estação, liberado à direita.</span><span class="sxs-lookup"><span data-stu-id="bd824-126">Station node address, flushed right.</span></span>     |
| <span data-ttu-id="bd824-127">**\_Soquete SA**</span><span class="sxs-lookup"><span data-stu-id="bd824-127">**Sa\_socket**</span></span>  | <span data-ttu-id="bd824-128">Número de soquete IPX na ordem de rede.</span><span class="sxs-lookup"><span data-stu-id="bd824-128">IPX socket number in network order.</span></span>      |



 

 

 



