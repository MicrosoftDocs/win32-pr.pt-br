---
title: Interface (RRAS)
description: Uma interface é uma conexão lógica com uma rede. Cada interface é identificada por um índice exclusivo. Os protocolos de roteamento multicast (como MOSPF) lidam com todos os tipos de interfaces da mesma forma.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103917887"
---
# <a name="interface-rras"></a><span data-ttu-id="e6e68-105">Interface (RRAS)</span><span class="sxs-lookup"><span data-stu-id="e6e68-105">Interface (RRAS)</span></span>

<span data-ttu-id="e6e68-106">Uma interface é uma conexão lógica com uma rede.</span><span class="sxs-lookup"><span data-stu-id="e6e68-106">An interface is a logical connection to a network.</span></span> <span data-ttu-id="e6e68-107">Cada interface é identificada por um índice exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e6e68-107">Each interface is identified by a unique index.</span></span> <span data-ttu-id="e6e68-108">Os protocolos de roteamento multicast (como MOSPF) lidam com todos os tipos de interfaces da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="e6e68-108">Multicast routing protocols (such as MOSPF) deal with all types of interfaces similarly.</span></span>

<span data-ttu-id="e6e68-109">No caso de uma interface de LAN, a interface corresponde a um dispositivo físico real no computador (o adaptador de LAN).</span><span class="sxs-lookup"><span data-stu-id="e6e68-109">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer (the LAN adapter).</span></span> <span data-ttu-id="e6e68-110">No caso de uma interface WAN, a interface é mapeada para uma porta quando uma conexão é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="e6e68-110">In the case of a WAN interface, the interface is mapped to a port when a connection is established.</span></span> <span data-ttu-id="e6e68-111">As interfaces WAN podem ser baseadas em túneis e a porta pode ser uma porta de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="e6e68-111">WAN interfaces can be based on tunnels and the port could be a virtual private network (VPN) port.</span></span>

<span data-ttu-id="e6e68-112">Os sistemas operacionais Windows 2000 e posteriores dão suporte a uma interface "ponto a multiponto".</span><span class="sxs-lookup"><span data-stu-id="e6e68-112">Windows 2000 and later operating systems support a "point-to-multipoint" interface.</span></span> <span data-ttu-id="e6e68-113">Esse tipo de interface pode ser exibido como uma coleção de links ponto a ponto que compartilham um único ponto de rescisão.</span><span class="sxs-lookup"><span data-stu-id="e6e68-113">This type of interface can be viewed as a collection of point-to-point links that share a single termination point.</span></span>

<span data-ttu-id="e6e68-114">Para identificar exclusivamente um link exato em uma interface ponto a multiponto, a API MGM usa o endereço do próximo salto da ID da interface.</span><span class="sxs-lookup"><span data-stu-id="e6e68-114">To uniquely identify an exact link in a point-to-multipoint interface, the MGM API uses the next hop address of the interface ID.</span></span> <span data-ttu-id="e6e68-115">Para dar suporte a essa identificação, a API MGM usa uma ID de interface estendida, que inclui um endereço de [próximo salto](next-hop.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e68-115">To support this identification, the MGM API uses an extended interface ID, which includes a [next hop](next-hop.md) address.</span></span>

 

 




