---
title: Rotação avançada
description: Esta seção explica como girar um objeto com base em onde o usuário está executando a manipulação de rotação.
ms.assetid: 56b339b1-a062-4c0e-91c8-aec08a17bc65
keywords:
- Windows Touch, rotação
- Windows Touch, rotação avançada
- Windows Touch, manipulações
- manipulações, rotação
- manipulações, rotação avançada
- rotação, avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a84679f4189d28941262cda2585887b0932c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915989"
---
# <a name="advanced-rotation"></a><span data-ttu-id="f4d67-109">Rotação avançada</span><span class="sxs-lookup"><span data-stu-id="f4d67-109">Advanced Rotation</span></span>

<span data-ttu-id="f4d67-110">Esta seção explica como girar um objeto com base em onde o usuário está executando a manipulação de rotação.</span><span class="sxs-lookup"><span data-stu-id="f4d67-110">This section explains how to rotate an object based on where the user is performing the rotation manipulation.</span></span>

<span data-ttu-id="f4d67-111">A imagem a seguir ilustra duas maneiras diferentes que um objeto pode ser girado.</span><span class="sxs-lookup"><span data-stu-id="f4d67-111">The following image illustrates two different ways that an object can be rotated.</span></span>

![ilustração mostrando dois tipos de rotação de dedo único: ao lado do centro ou ao lado da borda, com a borda que envolve a rotação e a translação](images/rotation.png)

<span data-ttu-id="f4d67-113">No exemplo A, o objeto é manipulado em volta do ponto central do objeto.</span><span class="sxs-lookup"><span data-stu-id="f4d67-113">In example A, the object is manipulated around the center point of the object.</span></span> <span data-ttu-id="f4d67-114">No exemplo B, o objeto é girado em volta do ponto central da manipulação.</span><span class="sxs-lookup"><span data-stu-id="f4d67-114">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="f4d67-115">Para dar suporte à manipulação em um ponto diferente do ponto central do objeto, você deve executar uma manipulação composta que executa a rotação e a conversão.</span><span class="sxs-lookup"><span data-stu-id="f4d67-115">To support manipulation around a point other than the center point of the object, you must perform a compound manipulation that performs both rotation and translation.</span></span> <span data-ttu-id="f4d67-116">O código a seguir mostra como essa manipulação é executada e calculada.</span><span class="sxs-lookup"><span data-stu-id="f4d67-116">The following code shows how this manipulation is performed and calculated.</span></span>


```C++
RotateVector(FLOAT *vector, FLOAT *tVector, FLOAT fAngle) {
    FLOAT fAngleRads = fAngle / 180.0f * 3.14159f;
    FLOAT fSin = sin(fAngleRads);
    FLOAT fCos = cos(fAngleRads);

    FLOAT fNewX = (vector[0]*fCos) - (vector[1]*fSin);
    FLOAT fNewY = (vector[0]*fSin) + (vector[1]*fCos);

    tVector[0] = fNewX;
    tVector[1] = fNewY;
}
     
```



## <a name="related-topics"></a><span data-ttu-id="f4d67-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4d67-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4d67-118">Manipulações avançadas</span><span class="sxs-lookup"><span data-stu-id="f4d67-118">Advanced Manipulations</span></span>](advanced-manipulations.md)
</dt> <dt>

[<span data-ttu-id="f4d67-119">Manipulações</span><span class="sxs-lookup"><span data-stu-id="f4d67-119">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




