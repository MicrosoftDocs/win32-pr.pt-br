---
description: As nuvens são usadas pelas infraestruturas de agrupamento e Grafação de pares.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Nuvens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091644"
---
# <a name="clouds"></a><span data-ttu-id="b8566-103">Nuvens</span><span class="sxs-lookup"><span data-stu-id="b8566-103">Clouds</span></span>

<span data-ttu-id="b8566-104">As nuvens são usadas pelas infraestruturas de [agrupamento](grouping-api.md) e [grafação](graphing-api.md) de pares.</span><span class="sxs-lookup"><span data-stu-id="b8566-104">Clouds are used by the Peer [Grouping](grouping-api.md) and [Graphing](graphing-api.md) Infrastructures.</span></span> <span data-ttu-id="b8566-105">O [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) identifica uma nuvem como um conjunto de pares que podem se comunicar dentro do mesmo escopo do IPv6.</span><span class="sxs-lookup"><span data-stu-id="b8566-105">The [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifies a cloud as a set of peers that can communicate within the same IPv6 scope.</span></span> <span data-ttu-id="b8566-106">As nuvens estão fortemente relacionadas aos escopos de IPv6.</span><span class="sxs-lookup"><span data-stu-id="b8566-106">Clouds are closely related to the IPv6 scopes.</span></span> <span data-ttu-id="b8566-107">A lista a seguir identifica alguns dos recursos de nuvem exclusivos:</span><span class="sxs-lookup"><span data-stu-id="b8566-107">The following list identifies some of the unique cloud features:</span></span>

-   <span data-ttu-id="b8566-108">Uma nuvem é identificada por um nome e as nuvens disponíveis podem ser enumeradas usando [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="b8566-108">A cloud is identified by a name, and available clouds can be enumerated by using [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span></span>
-   <span data-ttu-id="b8566-109">Se um computador estiver conectado à Internet, ele faz parte de uma nuvem global, que é identificada pela cadeia de caracteres "global \_ ".</span><span class="sxs-lookup"><span data-stu-id="b8566-109">If a computer is connected to the Internet, it is part of a global cloud, which is identified by the string "Global\_".</span></span>
-   <span data-ttu-id="b8566-110">Se um computador estiver conectado a uma ou mais redes locais (LAN), nuvens individuais estarão disponíveis para cada link.</span><span class="sxs-lookup"><span data-stu-id="b8566-110">If a computer is connected to one or more local area networks (LAN), individual clouds are available for each link.</span></span>
-   <span data-ttu-id="b8566-111">Um computador pode ser conectado a várias redes por meio de vários adaptadores de rede ou usando uma VPN (rede virtual privada), o que significa que um computador com uma interface pode ser visível em muitas nuvens.</span><span class="sxs-lookup"><span data-stu-id="b8566-111">One computer can be connected to many networks by having multiple network adapters or by using a virtual private network (VPN), which means that a computer with one interface can be visible in many clouds.</span></span>
-   <span data-ttu-id="b8566-112">Você pode usar o PNRP para registrar e resolver nomes de pares em uma nuvem específica.</span><span class="sxs-lookup"><span data-stu-id="b8566-112">You can use PNRP to register and resolve peer names in a specific cloud.</span></span>

 

 



