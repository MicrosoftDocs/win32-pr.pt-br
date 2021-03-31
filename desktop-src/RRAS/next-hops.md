---
title: Próximos saltos
description: As rotas têm um ou mais próximos saltos associados a elas.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004997"
---
# <a name="next-hops"></a><span data-ttu-id="ceb72-103">Próximos saltos</span><span class="sxs-lookup"><span data-stu-id="ceb72-103">Next Hops</span></span>

<span data-ttu-id="ceb72-104">As rotas têm um ou mais próximos saltos associados a elas.</span><span class="sxs-lookup"><span data-stu-id="ceb72-104">Routes have one or more next hops associated with them.</span></span> <span data-ttu-id="ceb72-105">Se o destino não estiver em uma rede conectada diretamente, o próximo salto será o endereço do próximo roteador (ou rede) na rede de saída que pode melhor rotear os dados para o destino.</span><span class="sxs-lookup"><span data-stu-id="ceb72-105">If the destination is not on a directly connected network, the next hop is the address of the next router (or network) on the outgoing network that can best route data to the destination.</span></span> <span data-ttu-id="ceb72-106">A melhor rota é a rota que tem o menor custo, com base na política de roteamento em uso.</span><span class="sxs-lookup"><span data-stu-id="ceb72-106">The best route is the route that has the least cost, based on the routing policy in use.</span></span> <span data-ttu-id="ceb72-107">Cada próximo salto pode ser usado para encaminhar dados no caminho para o destino.</span><span class="sxs-lookup"><span data-stu-id="ceb72-107">Each next hop can be used to forward data on the path to the destination.</span></span> <span data-ttu-id="ceb72-108">Todas as rotas de propriedade de um cliente compartilham um conjunto comum de entradas de próximo salto que foram adicionadas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="ceb72-108">All routes owned by a client share a common set of next-hop entries that were added by the client.</span></span>

<span data-ttu-id="ceb72-109">Cada próximo salto é identificado exclusivamente pelo endereço do próximo salto e o índice de interface usado para alcançar o próximo salto.</span><span class="sxs-lookup"><span data-stu-id="ceb72-109">Each next hop is uniquely identified by the address of the next hop and the interface index used to reach the next hop.</span></span>

<span data-ttu-id="ceb72-110">Se o próximo salto em si não estiver diretamente conectado, ele será marcado como um próximo salto "remoto".</span><span class="sxs-lookup"><span data-stu-id="ceb72-110">If the next hop itself is not directly connected, it is marked as a "remote" next hop.</span></span> <span data-ttu-id="ceb72-111">Nesse caso, o encaminhador deve executar outra pesquisa usando o endereço de rede do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="ceb72-111">In this case, the forwarder must perform another lookup using the next hop's network address.</span></span> <span data-ttu-id="ceb72-112">Essa pesquisa é necessária para localizar o próximo salto "local" usado para alcançar o próximo salto e o destino remotos.</span><span class="sxs-lookup"><span data-stu-id="ceb72-112">This lookup is necessary to find the "local" next hop used to reach the remote next hop and the destination.</span></span>

<span data-ttu-id="ceb72-113">Uma entrada de próximo salto na tabela de roteamento inclui:</span><span class="sxs-lookup"><span data-stu-id="ceb72-113">A next-hop entry in the routing table includes:</span></span>

-   <span data-ttu-id="ceb72-114">O endereço de rede do próximo salto</span><span class="sxs-lookup"><span data-stu-id="ceb72-114">The network address of the next hop</span></span>
-   <span data-ttu-id="ceb72-115">O proprietário do próximo salto</span><span class="sxs-lookup"><span data-stu-id="ceb72-115">The owner of the next hop</span></span>
-   <span data-ttu-id="ceb72-116">O identificador da interface de saída</span><span class="sxs-lookup"><span data-stu-id="ceb72-116">The identifier of the outgoing interface</span></span>
-   <span data-ttu-id="ceb72-117">O estado do próximo salto</span><span class="sxs-lookup"><span data-stu-id="ceb72-117">The state of the next hop</span></span>
-   <span data-ttu-id="ceb72-118">Sinalizadores associados ao próximo salto</span><span class="sxs-lookup"><span data-stu-id="ceb72-118">Flags associated with the next hop</span></span>
-   <span data-ttu-id="ceb72-119">Informações que são privadas para o proprietário do próximo salto</span><span class="sxs-lookup"><span data-stu-id="ceb72-119">Information that is private to the owner of the next hop</span></span>
-   <span data-ttu-id="ceb72-120">Um identificador para o destino correspondente ao próximo salto remoto</span><span class="sxs-lookup"><span data-stu-id="ceb72-120">A handle to the destination corresponding to the remote next hop</span></span>

 

 




