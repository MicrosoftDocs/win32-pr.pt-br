---
title: Obter funções
description: As funções Get de gerenciamento de rede recuperam informações sobre um domínio. Você também pode chamar essas funções para recuperar informações sobre contas de usuário locais, globais, de estação de trabalho e de servidor.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498732"
---
# <a name="get-functions"></a><span data-ttu-id="e7765-104">Obter funções</span><span class="sxs-lookup"><span data-stu-id="e7765-104">Get Functions</span></span>

<span data-ttu-id="e7765-105">As funções Get de gerenciamento de rede recuperam informações sobre um domínio.</span><span class="sxs-lookup"><span data-stu-id="e7765-105">The network management get functions retrieve information about a domain.</span></span> <span data-ttu-id="e7765-106">Você também pode chamar essas funções para recuperar informações sobre contas de usuário locais, globais, de estação de trabalho e de servidor.</span><span class="sxs-lookup"><span data-stu-id="e7765-106">You can also call these functions to retrieve information about local, global, workstation, and server user accounts.</span></span>

<span data-ttu-id="e7765-107">As funções Get de gerenciamento de rede são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7765-107">The network management get functions are listed following.</span></span>



| <span data-ttu-id="e7765-108">Função</span><span class="sxs-lookup"><span data-stu-id="e7765-108">Function</span></span>                                                               | <span data-ttu-id="e7765-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7765-109">Description</span></span>                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7765-110">**NetGetAnyDCName**</span><span class="sxs-lookup"><span data-stu-id="e7765-110">**NetGetAnyDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | <span data-ttu-id="e7765-111">Retorna o nome de qualquer controlador de domínio para um domínio que é diretamente confiável para um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="e7765-111">Returns the name of any domain controller for a domain that is directly trusted by a specified server.</span></span>                                   |
| [<span data-ttu-id="e7765-112">**NetGetDCName**</span><span class="sxs-lookup"><span data-stu-id="e7765-112">**NetGetDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | <span data-ttu-id="e7765-113">Retorna o nome do controlador de domínio primário (PDC) para o domínio especificado.</span><span class="sxs-lookup"><span data-stu-id="e7765-113">Returns the name of the primary domain controller (PDC) for the specified domain.</span></span>                                                        |
| [<span data-ttu-id="e7765-114">**NetGetDisplayInformationIndex**</span><span class="sxs-lookup"><span data-stu-id="e7765-114">**NetGetDisplayInformationIndex**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | <span data-ttu-id="e7765-115">Retorna o índice da primeira entrada de informações de exibição cujo nome começa com uma cadeia de caracteres especificada ou segue em ordem alfabética a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7765-115">Returns the index of the first display information entry whose name begins with a specified string or alphabetically follows the string.</span></span> |
| [<span data-ttu-id="e7765-116">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="e7765-116">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | <span data-ttu-id="e7765-117">Retorna informações de conta de usuário, computador ou grupo global.</span><span class="sxs-lookup"><span data-stu-id="e7765-117">Returns user, computer, or global group account information.</span></span>                                                                             |



 

<span data-ttu-id="e7765-118">As informações retornadas pela função [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) estão disponíveis nos seguintes níveis:</span><span class="sxs-lookup"><span data-stu-id="e7765-118">The information returned by the [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) function is available at the following levels:</span></span>

-   [<span data-ttu-id="e7765-119">**\_grupo de exibição NET \_**</span><span class="sxs-lookup"><span data-stu-id="e7765-119">**NET\_DISPLAY\_GROUP**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [<span data-ttu-id="e7765-120">**\_computador de exibição NET \_**</span><span class="sxs-lookup"><span data-stu-id="e7765-120">**NET\_DISPLAY\_MACHINE**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [<span data-ttu-id="e7765-121">**NET \_ Display \_ usuário**</span><span class="sxs-lookup"><span data-stu-id="e7765-121">**NET\_DISPLAY\_USER**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




