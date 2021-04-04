---
title: Localizando um driver específico
description: Localizando um driver específico
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Gerenciador de compactação de áudio (ACM), localizando drivers
- ACM (Gerenciador de compactação de áudio), localizando drivers
- Exemplos do ACM, localizando drivers
- Localizando drivers
- função acmDriverEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822937"
---
# <a name="finding-a-specific-driver"></a><span data-ttu-id="437b5-108">Localizando um driver específico</span><span class="sxs-lookup"><span data-stu-id="437b5-108">Finding a Specific Driver</span></span>

<span data-ttu-id="437b5-109">Talvez você queira que seu aplicativo envie uma mensagem diretamente para um driver específico ou para identificar determinados drivers da lista.</span><span class="sxs-lookup"><span data-stu-id="437b5-109">You might want your application to send a message directly to a specific driver or to identify certain drivers from the list.</span></span> <span data-ttu-id="437b5-110">Por exemplo, talvez você queira que seu aplicativo identifique os drivers que dão suporte a filtros e, em seguida, consulte cada driver para determinar quais marcas de filtro ele suporta.</span><span class="sxs-lookup"><span data-stu-id="437b5-110">For example, you might want your application to identify those drivers that support filters and then query each driver to determine which filter tags it supports.</span></span> <span data-ttu-id="437b5-111">Você pode usar a função [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) para obter um identificador para o driver ou os drivers desejados; Esse identificador pode ser usado para se comunicar com esse driver.</span><span class="sxs-lookup"><span data-stu-id="437b5-111">You can use the [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) function to obtain a handle to the desired driver or drivers; this handle can then be used to communicate with that driver.</span></span>

<span data-ttu-id="437b5-112">Observe que, quando um aplicativo instala um driver local para seu próprio uso, a função [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) retorna um identificador de driver, que pode ser usado para se comunicar com o driver.</span><span class="sxs-lookup"><span data-stu-id="437b5-112">Note that when an application installs a local driver for its own use, the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function returns a driver handle, which can be used to communicate with the driver.</span></span> <span data-ttu-id="437b5-113">Não é necessário usar **acmDriverEnum** nesse caso.</span><span class="sxs-lookup"><span data-stu-id="437b5-113">It is not necessary to use **acmDriverEnum** in this case.</span></span>

 

 




