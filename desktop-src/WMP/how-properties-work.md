---
title: Como funcionam as propriedades
description: Como funcionam as propriedades
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636256"
---
# <a name="how-properties-work"></a><span data-ttu-id="0eeb5-108">Como funcionam as propriedades</span><span class="sxs-lookup"><span data-stu-id="0eeb5-108">How Properties Work</span></span>

<span data-ttu-id="0eeb5-109">Os valores de propriedade são armazenados em variáveis de membro.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-109">Property values are stored in member variables.</span></span>

<span data-ttu-id="0eeb5-110">As propriedades tornam-se acessíveis por pares de métodos.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-110">Properties are made accessible by method pairs.</span></span> <span data-ttu-id="0eeb5-111">Um método fornece a implementação para especificar o valor da propriedade; seu nome começa com Put \_ .</span><span class="sxs-lookup"><span data-stu-id="0eeb5-111">One method provides the implementation to specify the property value; its name starts with put\_.</span></span> <span data-ttu-id="0eeb5-112">O outro método fornece a implementação para recuperar o valor da propriedade; seu nome começa com get \_ .</span><span class="sxs-lookup"><span data-stu-id="0eeb5-112">The other method provides the implementation to retrieve the property value; its name starts with get\_.</span></span> <span data-ttu-id="0eeb5-113">A definição de interface está em Echo. idl.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-113">The interface definition is in Echo.idl.</span></span> <span data-ttu-id="0eeb5-114">Os protótipos do método de propriedade estão em Echo. h.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-114">The property method prototypes are in Echo.h.</span></span> <span data-ttu-id="0eeb5-115">Eles são implementados em Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-115">They are implemented in Echo.cpp.</span></span>

<span data-ttu-id="0eeb5-116">As próximas três seções mostrarão como modificar os métodos de propriedade existentes para atender às suas necessidades e como adicionar os métodos para uma propriedade adicional.</span><span class="sxs-lookup"><span data-stu-id="0eeb5-116">The next three sections will show you how to modify the existing property methods to suit your needs and how to add the methods for an additional property.</span></span>

-   [<span data-ttu-id="0eeb5-117">Variáveis para armazenar propriedades</span><span class="sxs-lookup"><span data-stu-id="0eeb5-117">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="0eeb5-118">Modificando a propriedade Scale</span><span class="sxs-lookup"><span data-stu-id="0eeb5-118">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="0eeb5-119">Adicionando a propriedade de combinação úmida</span><span class="sxs-lookup"><span data-stu-id="0eeb5-119">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="0eeb5-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0eeb5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eeb5-121">**Propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="0eeb5-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




