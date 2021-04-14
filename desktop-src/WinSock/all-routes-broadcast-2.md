---
description: Uma difusão geral através da Internet é obtida definindo os campos SA \_ netnum e SA \_ nodenum para os binários (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Difusão de todas as rotas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461120"
---
# <a name="all-routes-broadcast"></a><span data-ttu-id="4c947-103">Difusão de todas as rotas</span><span class="sxs-lookup"><span data-stu-id="4c947-103">All Routes Broadcast</span></span>

<span data-ttu-id="4c947-104">Uma difusão geral através da Internet é obtida definindo os campos **SA \_ netnum** e **SA \_ nodenum** para os binários (1).</span><span class="sxs-lookup"><span data-stu-id="4c947-104">A general broadcast through the Internet is achieved by setting the **sa\_netnum** and **sa\_nodenum** fields to binary ones (1).</span></span> <span data-ttu-id="4c947-105">O provedor de serviços Converte essa solicitação em um pacote de tipo 20, que os roteadores IPX reconhecem e encaminham.</span><span class="sxs-lookup"><span data-stu-id="4c947-105">The service provider translates this request to a type-20 packet, which IPX routers recognize and forward.</span></span> <span data-ttu-id="4c947-106">O pacote visita todas as sub-redes e pode ser duplicado várias vezes.</span><span class="sxs-lookup"><span data-stu-id="4c947-106">The packet visits all subnets and may be duplicated several times.</span></span> <span data-ttu-id="4c947-107">Os receptores devem lidar com várias cópias duplicadas do datagrama.</span><span class="sxs-lookup"><span data-stu-id="4c947-107">Receivers must handle several duplicate copies of the datagram.</span></span>

<span data-ttu-id="4c947-108">O uso desse tipo de difusão não é popular entre os administradores de rede, portanto, seu uso deve ser extremamente limitado.</span><span class="sxs-lookup"><span data-stu-id="4c947-108">Use of this broadcast type is unpopular among network administrators, so its use should be extremely limited.</span></span> <span data-ttu-id="4c947-109">Muitos roteadores desativam esse tipo de difusão, deixando partes da sub-rede invisíveis para o pacote.</span><span class="sxs-lookup"><span data-stu-id="4c947-109">Many routers disable this type of broadcast, leaving parts of the subnet invisible to the packet.</span></span>

 

 



