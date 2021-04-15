---
description: Cada linha tem um ou mais canais. Os provedores de serviço normalmente tratam como os canais são expostos como endereços a um aplicativo, e o usuário final ou o servidor não requer conhecimento específico de canais.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canal (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502050"
---
# <a name="channel-telephony-api"></a><span data-ttu-id="0d0f0-104">Canal (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="0d0f0-104">Channel (Telephony API)</span></span>

<span data-ttu-id="0d0f0-105">Cada linha tem um ou mais canais.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-105">Each line has one or more channels.</span></span> <span data-ttu-id="0d0f0-106">Os provedores de serviço normalmente tratam como os canais são expostos como endereços a um aplicativo, e o usuário final ou o servidor não requer conhecimento específico de canais.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-106">The service providers normally handle how channels are exposed as addresses to an application, and the end user or server does not require specific knowledge of channels.</span></span>

<span data-ttu-id="0d0f0-107">Os canais são idênticos e, portanto, intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-107">Channels are identical and therefore interchangeable.</span></span> <span data-ttu-id="0d0f0-108">Em POTS (serviço de telefone antigo), exatamente um canal existe em uma linha e o canal é usado exclusivamente para voz.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-108">In POTS (Plain Old Telephone Service), exactly one channel exists on a line, and the channel is used exclusively for voice.</span></span> <span data-ttu-id="0d0f0-109">Com o ISDN, pelo menos três (e até 30 ou mais) canais podem existir em uma linha simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-109">With ISDN, at least three (and as many as 30 or more) channels can exist on a line simultaneously.</span></span>

<span data-ttu-id="0d0f0-110">Cada canal pode ter seu próprio endereço, o que significa que uma linha pode ter tantos endereços quantos tenham canais.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-110">Each channel can have its own address, which means a line could have as many addresses as it has channels.</span></span> <span data-ttu-id="0d0f0-111">A relação exata entre canais e endereços expostos a um aplicativo depende da implementação de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-111">The precise relationship between channels and addresses exposed to an application is dependent on a service provider's implementation.</span></span>

<span data-ttu-id="0d0f0-112">Alguns provedores de serviços dão suporte à atribuição de mais de um endereço a um único canal.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-112">Some service providers support the assignment of more than one address to a single channel.</span></span> <span data-ttu-id="0d0f0-113">Em linhas POTS, vários endereços são possibilitados por vários sistemas, como DID (Direct Inward Dialing) ou toque distintivo, que são serviços de tarifa adicional que a empresa telefônica fornece.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-113">On POTS lines, multiple addresses are made possible by various systems, such as direct inward dialing (DID) or distinctive ringing, which are extra-fee services that the telephone company provides.</span></span>

<span data-ttu-id="0d0f0-114">Muitas grandes corporações usam o DID para chamadas de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-114">Many large corporations use DID for incoming calls.</span></span> <span data-ttu-id="0d0f0-115">Antes de uma chamada ser conectada, seu número de extensão de destino é sinalizado para o PBX, o que faz com que a extensão toque em vez do telefone do operador.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-115">Before a call is connected, its destination extension number is signaled to the PBX, which causes the extension to ring instead of the operator's phone.</span></span> <span data-ttu-id="0d0f0-116">Um exemplo de toque distintivo em uma casa privada seria se os pais usavam um endereço, os filhos, outro e um computador de fax um terceiro.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-116">An example of distinctive ringing in a private home would be if the parents used one address, the children another, and a fax machine a third.</span></span> <span data-ttu-id="0d0f0-117">Como apenas uma linha conecta a casa à rede telefônica, todos os telefones tocam quando uma chamada é exibida, mas o padrão de anel é diferente dependendo do número que a parte de chamada tiver discado.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-117">Because only one line connects the house to the telephone network, all phones ring when a call appears, but the ring pattern is different depending on the number that the calling party dialed.</span></span> <span data-ttu-id="0d0f0-118">Com o toque distintivo, as pessoas sabem a quem é a chamada de entrada e a máquina de fax responde suas chamadas reconhecendo seu próprio estilo de toque.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-118">With distinctive ringing, the people know who the incoming call is for, and the fax machine answers its calls by recognizing its own ringing style.</span></span>

<span data-ttu-id="0d0f0-119">No ISDN, os vários canais B podem não ter endereços separados.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-119">In ISDN, the various B channels might not have separate addresses.</span></span> <span data-ttu-id="0d0f0-120">Como esses B canais podem estar no mesmo endereço, é o provedor de serviços (e não o aplicativo ou uma pessoa que tenha discado o número) que atribui chamadas a esses canais.</span><span class="sxs-lookup"><span data-stu-id="0d0f0-120">Because these B channels might be on the same address, it is the service provider (and not the application or a person who has dialed the number) that assigns calls to these channels.</span></span>

 

 



