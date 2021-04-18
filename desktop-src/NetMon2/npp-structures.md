---
description: Esta seção descreve as estruturas NPP usadas pelos métodos NPP.
ms.assetid: f0729dc5-6b5f-4f24-85d6-47c45f1bf9be
title: Estruturas NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b514bded37450f6a7c33a016b231bb38f0c1812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761414"
---
# <a name="npp-structures"></a><span data-ttu-id="0939b-103">Estruturas NPP</span><span class="sxs-lookup"><span data-stu-id="0939b-103">NPP Structures</span></span>

<span data-ttu-id="0939b-104">Esta seção descreve as estruturas NPP usadas pelos métodos NPP.</span><span class="sxs-lookup"><span data-stu-id="0939b-104">This section describes the NPP structures used by NPP methods.</span></span> <span data-ttu-id="0939b-105">Essas estruturas são usadas para recuperar estatísticas, fornecer status do sistema e informações estatísticas e indicar quais computadores estão em execução Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="0939b-105">These structures are used to retrieve statistics, provide system status and statistical information, and indicate which computers are running Network Monitor.</span></span> <span data-ttu-id="0939b-106">As tabelas a seguir descrevem essas estruturas.</span><span class="sxs-lookup"><span data-stu-id="0939b-106">The following tables describes these structures.</span></span>



| <span data-ttu-id="0939b-107">Estruturas NPP</span><span class="sxs-lookup"><span data-stu-id="0939b-107">NPP Structures</span></span>                     | <span data-ttu-id="0939b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0939b-108">Description</span></span>                                                                                                                      |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0939b-109">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="0939b-109">SESSIONSTATS</span></span>](sessionstats.md)   | <span data-ttu-id="0939b-110">Fornece informações de sessão quando as estatísticas de conversa são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="0939b-110">Provides session information when conversation statistics are retrieved.</span></span>                                                         |
| [<span data-ttu-id="0939b-111">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="0939b-111">STATIONSTATS</span></span>](stationstats.md)   | <span data-ttu-id="0939b-112">Fornece estatísticas sobre uma [*estação*](s.md)específica.</span><span class="sxs-lookup"><span data-stu-id="0939b-112">Provides statistics about a specific [*station*](s.md).</span></span>                                                     |
| [<span data-ttu-id="0939b-113">ESTATÍSTICA</span><span class="sxs-lookup"><span data-stu-id="0939b-113">STATISTICS</span></span>](statistics.md)       | <span data-ttu-id="0939b-114">Fornece estatísticas de rede quando as estatísticas totais são recuperadas e quando a captura atual foi pausada ou interrompida.</span><span class="sxs-lookup"><span data-stu-id="0939b-114">Provides network statistics when total statistics are retrieved and when the current capture has paused or stopped.</span></span>              |
| [<span data-ttu-id="0939b-115">CONSULTA</span><span class="sxs-lookup"><span data-stu-id="0939b-115">QUERYTABLE</span></span>](querytable.md)       | <span data-ttu-id="0939b-116">Indica quais computadores estão usando Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="0939b-116">Indicates which computers are using Network Monitor.</span></span>                                                                             |
| [<span data-ttu-id="0939b-117">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="0939b-117">STATIONQUERY</span></span>](stationquery.md)   | <span data-ttu-id="0939b-118">Fornece informações sobre um computador que está usando Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="0939b-118">Provides information about a computer that is using Network Monitor.</span></span> <span data-ttu-id="0939b-119">Essa estrutura é usada pela estrutura do NPP **QUERYTABLE** .</span><span class="sxs-lookup"><span data-stu-id="0939b-119">This structure is used by the NPP **QUERYTABLE** structure.</span></span> |
| [<span data-ttu-id="0939b-120">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="0939b-120">NETWORKSTATUS</span></span>](networkstatus.md) | <span data-ttu-id="0939b-121">Fornece o status da rede atual em termos de estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="0939b-121">Provides current network status in terms of system state.</span></span>                                                                        |



 

 

 



