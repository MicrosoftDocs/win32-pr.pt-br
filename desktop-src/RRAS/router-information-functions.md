---
title: Funções de informações do roteador
description: Use as funções a seguir para manipular blocos e cabeçalhos de informações do roteador. Um cabeçalho de informações é composto de metadados privados e blocos de informações. Os blocos de informações são matrizes de estruturas de informações de vários tipos.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004787"
---
# <a name="router-information-functions"></a><span data-ttu-id="5467a-105">Funções de informações do roteador</span><span class="sxs-lookup"><span data-stu-id="5467a-105">Router Information Functions</span></span>

<span data-ttu-id="5467a-106">Use as funções a seguir para manipular blocos e cabeçalhos de informações do roteador.</span><span class="sxs-lookup"><span data-stu-id="5467a-106">Use the following functions to manipulate router information headers and blocks.</span></span> <span data-ttu-id="5467a-107">Um cabeçalho de informações é composto de metadados privados e blocos de informações.</span><span class="sxs-lookup"><span data-stu-id="5467a-107">An information header is composed of private meta-data and information blocks.</span></span> <span data-ttu-id="5467a-108">Os blocos de informações são matrizes de [estruturas de informações](router-information-structures.md) de vários [tipos](router-information-enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="5467a-108">Information blocks are arrays of [information structures](router-information-structures.md) of various [types](router-information-enumerations.md).</span></span>

<span data-ttu-id="5467a-109">As seguintes funções manipulam os cabeçalhos de informações:</span><span class="sxs-lookup"><span data-stu-id="5467a-109">The following functions manipulate information headers:</span></span>

-   [<span data-ttu-id="5467a-110">**MprInfoCreate**</span><span class="sxs-lookup"><span data-stu-id="5467a-110">**MprInfoCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [<span data-ttu-id="5467a-111">**MprInfoDelete**</span><span class="sxs-lookup"><span data-stu-id="5467a-111">**MprInfoDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [<span data-ttu-id="5467a-112">**MprInfoDuplicate**</span><span class="sxs-lookup"><span data-stu-id="5467a-112">**MprInfoDuplicate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [<span data-ttu-id="5467a-113">**MprInfoRemoveAll**</span><span class="sxs-lookup"><span data-stu-id="5467a-113">**MprInfoRemoveAll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

<span data-ttu-id="5467a-114">As seguintes funções manipulam blocos de informações dentro de um cabeçalho de informações:</span><span class="sxs-lookup"><span data-stu-id="5467a-114">The following functions manipulate information blocks within an information header:</span></span>

-   [<span data-ttu-id="5467a-115">**MprInfoBlockAdd**</span><span class="sxs-lookup"><span data-stu-id="5467a-115">**MprInfoBlockAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [<span data-ttu-id="5467a-116">**MprInfoBlockFind**</span><span class="sxs-lookup"><span data-stu-id="5467a-116">**MprInfoBlockFind**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [<span data-ttu-id="5467a-117">**MprInfoBlockQuerySize**</span><span class="sxs-lookup"><span data-stu-id="5467a-117">**MprInfoBlockQuerySize**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [<span data-ttu-id="5467a-118">**MprInfoBlockRemove**</span><span class="sxs-lookup"><span data-stu-id="5467a-118">**MprInfoBlockRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [<span data-ttu-id="5467a-119">**MprInfoBlockSet**</span><span class="sxs-lookup"><span data-stu-id="5467a-119">**MprInfoBlockSet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

<span data-ttu-id="5467a-120">Muitas das [funções de administração e configuração do roteador](understanding-mprinfo-functions-and-information-headers.md) usam cabeçalhos de informações.</span><span class="sxs-lookup"><span data-stu-id="5467a-120">Many of the [router administration and configuration functions](understanding-mprinfo-functions-and-information-headers.md) use information headers.</span></span>

 

 




