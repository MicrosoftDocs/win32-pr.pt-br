---
title: Expansão avançada
description: Expansão avançada
ms.assetid: 29db15a1-fa56-441a-af99-9e858d143804
keywords:
- Windows Touch, expansão
- Windows Touch, expansão avançada
- Windows Touch, manipulações
- manipulações, expansão
- manipulações, expansão avançada
- expansão, avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81a3a395da053b7d0e8f79a115a2489f3e63190
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159379"
---
# <a name="advanced-expansion"></a><span data-ttu-id="d7cb4-109">Expansão avançada</span><span class="sxs-lookup"><span data-stu-id="d7cb4-109">Advanced Expansion</span></span>

<span data-ttu-id="d7cb4-110">A ilustração a seguir mostra duas maneiras que um objeto pode ser expandido.</span><span class="sxs-lookup"><span data-stu-id="d7cb4-110">The following illustration shows two ways that an object can be expanded.</span></span>

![ilustração que mostra a expansão simples em relação ao ponto central de um objeto e a expansão avançada em relação ao ponto central da manipulação](images/expansion.png)

<span data-ttu-id="d7cb4-112">No exemplo a, o exemplo de expansão simples, o objeto é expandido em todo o seu ponto central.</span><span class="sxs-lookup"><span data-stu-id="d7cb4-112">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="d7cb4-113">No exemplo B, o objeto é expandido em volta do ponto central da manipulação.</span><span class="sxs-lookup"><span data-stu-id="d7cb4-113">In example B, the object is expanded around the center point of the manipulation.</span></span> <span data-ttu-id="d7cb4-114">Para habilitar isso, você deve converter o objeto enquanto ele está sendo expandido.</span><span class="sxs-lookup"><span data-stu-id="d7cb4-114">To enable this, you must translate the object while it is being expanded.</span></span> <span data-ttu-id="d7cb4-115">O valor que você converterá o objeto será o mesmo da distância do centro do objeto até o ponto central do gesto.</span><span class="sxs-lookup"><span data-stu-id="d7cb4-115">The amount that you will translate the object is the same as the distance from the center of the object to the center point of the gesture.</span></span> <span data-ttu-id="d7cb4-116">Intuitivamente, é como se você estivesse expandindo o objeto do ponto central do gesto de expansão e, em seguida, movendo-o para que ele ainda esteja no mesmo centro de sua posição inicial.</span><span class="sxs-lookup"><span data-stu-id="d7cb4-116">Intuitively, it is as though you are expanding the object from the center point of your expansion gesture and then moving it so that it is still at the same center as its initial position.</span></span> <span data-ttu-id="d7cb4-117">O código a seguir mostra uma maneira que esse conceito pode ser aplicado para habilitar a expansão em um ponto central.</span><span class="sxs-lookup"><span data-stu-id="d7cb4-117">The following code shows one way that this concept can be applied to enable expansion around a center point.</span></span>


```C++
    if(m_fFactor != 1.0f)
    {
        // We represent our vectors as an array.
        // x: vx[0], y: vx[1]

        FLOAT v1[2];
        v1[0] = this->get_CenterX() - fOffset[0];
        v1[1] = this->get_CenterY() - fOffset[1];

        FLOAT v2[2];
        v2[0] = v1[0] * m_fFactor;
        v2[1] = v1[1] * m_fFactor;
        
        m_fdX += v2[0] - v1[0];
        m_fdY += v2[1] - v1[1];
    }
   
```



## <a name="related-topics"></a><span data-ttu-id="d7cb4-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7cb4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7cb4-119">Manipulações</span><span class="sxs-lookup"><span data-stu-id="d7cb4-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




