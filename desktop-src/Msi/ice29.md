---
description: ICE29 valida se os nomes de fluxo truncados permanecem exclusivos. Qualquer tabela que tenha uma coluna binária ou de objeto é validada. Consulte o tipo de dados coluna binária.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921373"
---
# <a name="ice29"></a><span data-ttu-id="096bc-105">ICE29</span><span class="sxs-lookup"><span data-stu-id="096bc-105">ICE29</span></span>

<span data-ttu-id="096bc-106">ICE29 valida se os nomes de fluxo truncados permanecem exclusivos.</span><span class="sxs-lookup"><span data-stu-id="096bc-106">ICE29 validates that truncated stream names remain unique.</span></span> <span data-ttu-id="096bc-107">Qualquer tabela que tenha uma coluna binária ou de objeto é validada.</span><span class="sxs-lookup"><span data-stu-id="096bc-107">Any table having a Binary or Object column is validated.</span></span> <span data-ttu-id="096bc-108">Consulte o tipo de dados coluna [binária](binary.md) .</span><span class="sxs-lookup"><span data-stu-id="096bc-108">See the [Binary](binary.md) column data type.</span></span>

<span data-ttu-id="096bc-109">A manipulação de fluxos pela implementação de armazenamento estruturado OLE do Win32 limita os nomes de fluxo.</span><span class="sxs-lookup"><span data-stu-id="096bc-109">Handling of streams by the Win32 OLE structured storage implementation limits stream names.</span></span> <span data-ttu-id="096bc-110">Consulte [limitações de OLE em fluxos](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="096bc-110">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="096bc-111">O instalador pode compactar nomes de fluxo de até 62 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="096bc-111">The installer can compress stream names up to 62 characters in length.</span></span> <span data-ttu-id="096bc-112">Nomes maiores que isso são truncados.</span><span class="sxs-lookup"><span data-stu-id="096bc-112">Names longer than this are truncated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="096bc-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="096bc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="096bc-114">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="096bc-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



