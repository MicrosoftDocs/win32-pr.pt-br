---
title: Propriedades de exemplo de eco
description: Propriedades de exemplo de eco
ms.assetid: 16f6f963-d746-42dc-872f-6f4db296cab9
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ae368a75817320e346dab7e3061fb6b3d7d490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364189"
---
# <a name="echo-sample-properties"></a><span data-ttu-id="53d09-108">Propriedades de exemplo de eco</span><span class="sxs-lookup"><span data-stu-id="53d09-108">Echo Sample Properties</span></span>

<span data-ttu-id="53d09-109">O exemplo Echo expõe duas propriedades: o tempo de atraso e o nível de efeito (mixagem úmida).</span><span class="sxs-lookup"><span data-stu-id="53d09-109">The Echo sample exposes two properties: the delay time and the effect level (wet mix).</span></span> <span data-ttu-id="53d09-110">O valor do nível de sinal seco (mistura seca) sempre é derivado do valor de mistura úmida.</span><span class="sxs-lookup"><span data-stu-id="53d09-110">The value for the dry signal level (dry mix) is always derived from the wet mix value.</span></span> <span data-ttu-id="53d09-111">Você precisa modificar o código existente e adicionar um novo código para tornar essas propriedades acessíveis.</span><span class="sxs-lookup"><span data-stu-id="53d09-111">You need to modify existing code and add some new code to make these properties accessible.</span></span>

<span data-ttu-id="53d09-112">As seções a seguir explicam como modificar o código de propriedades:</span><span class="sxs-lookup"><span data-stu-id="53d09-112">The following sections explain how to modify the properties code:</span></span>

-   [<span data-ttu-id="53d09-113">Como funcionam as propriedades</span><span class="sxs-lookup"><span data-stu-id="53d09-113">How Properties Work</span></span>](how-properties-work.md)
-   [<span data-ttu-id="53d09-114">Variáveis para armazenar propriedades</span><span class="sxs-lookup"><span data-stu-id="53d09-114">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="53d09-115">Modificando a propriedade Scale</span><span class="sxs-lookup"><span data-stu-id="53d09-115">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="53d09-116">Adicionando a propriedade de combinação úmida</span><span class="sxs-lookup"><span data-stu-id="53d09-116">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="53d09-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53d09-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53d09-118">**O exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="53d09-118">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




