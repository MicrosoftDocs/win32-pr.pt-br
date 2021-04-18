---
description: A lista a seguir fornece descrições concisas de cada estrutura de ATM do Winsock. Para obter informações adicionais sobre qualquer estrutura, clique no nome da estrutura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Estruturas ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813765"
---
# <a name="winsock-atm-structures"></a><span data-ttu-id="19084-104">Estruturas ATM do Winsock</span><span class="sxs-lookup"><span data-stu-id="19084-104">Winsock ATM Structures</span></span>

<span data-ttu-id="19084-105">A lista a seguir fornece descrições concisas de cada estrutura de ATM do Winsock.</span><span class="sxs-lookup"><span data-stu-id="19084-105">The following list provides concise descriptions of each Winsock ATM structure.</span></span> <span data-ttu-id="19084-106">Para obter informações adicionais sobre qualquer estrutura, clique no nome da estrutura.</span><span class="sxs-lookup"><span data-stu-id="19084-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="19084-107">Estrutura ATM</span><span class="sxs-lookup"><span data-stu-id="19084-107">ATM Structure</span></span>                           | <span data-ttu-id="19084-108">Description</span><span class="sxs-lookup"><span data-stu-id="19084-108">Description</span></span>                                                |
|-----------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="19084-109">**\_endereço ATM**</span><span class="sxs-lookup"><span data-stu-id="19084-109">**ATM\_ADDRESS**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | <span data-ttu-id="19084-110">Armazena dados de endereço ATM para soquetes baseados em ATM.</span><span class="sxs-lookup"><span data-stu-id="19084-110">Stores ATM address data for ATM-based sockets.</span></span>             |
| [<span data-ttu-id="19084-111">**\_BHLI ATM**</span><span class="sxs-lookup"><span data-stu-id="19084-111">**ATM\_BHLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | <span data-ttu-id="19084-112">Identifica informações de B-HLI para um Soquete ATM associado.</span><span class="sxs-lookup"><span data-stu-id="19084-112">Identifies B-HLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="19084-113">**\_BLLI ATM**</span><span class="sxs-lookup"><span data-stu-id="19084-113">**ATM\_BLLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | <span data-ttu-id="19084-114">Identifica informações de B-LLI para um Soquete ATM associado.</span><span class="sxs-lookup"><span data-stu-id="19084-114">Identifies B-LLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="19084-115">**SOCKADDR \_ ATM**</span><span class="sxs-lookup"><span data-stu-id="19084-115">**sockaddr\_atm**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | <span data-ttu-id="19084-116">Armazena informações de endereço de soquete para Soquetes ATM.</span><span class="sxs-lookup"><span data-stu-id="19084-116">Stores socket address information for ATM sockets.</span></span>         |



 

<span data-ttu-id="19084-117">Para serviços ATM nativos, use \_ o ATM AF para a família de endereços e a estrutura de endereço de soquete [**\_ ATM SOCKADDR**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) .</span><span class="sxs-lookup"><span data-stu-id="19084-117">For native ATM services, use AF\_ATM for address family and the [**sockaddr\_atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) socket address structure.</span></span> <span data-ttu-id="19084-118">Para abrir um Soquete ATM nativo, passe AF \_ ATM, Sock \_ RAW e ATMPROTO \_ AAL5 ou ATMPROTO \_ AALUSER para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="19084-118">To open a native ATM socket, pass AF\_ATM, SOCK\_RAW, and ATMPROTO\_AAL5 or ATMPROTO\_AALUSER into the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function, respectively.</span></span>

 

 



