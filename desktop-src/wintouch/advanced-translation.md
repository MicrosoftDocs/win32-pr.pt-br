---
title: Tradução avançada
description: Tradução avançada
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Touch, tradução
- Windows Touch, tradução avançada
- Windows Touch, manipulações
- manipulações, tradução
- manipulações, tradução avançada
- tradução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822311"
---
# <a name="advanced-translation"></a><span data-ttu-id="0ca59-109">Tradução avançada</span><span class="sxs-lookup"><span data-stu-id="0ca59-109">Advanced Translation</span></span>

<span data-ttu-id="0ca59-110">A ilustração a seguir mostra duas interpretações de tradução.</span><span class="sxs-lookup"><span data-stu-id="0ca59-110">The following illustration shows two interpretations of translation.</span></span>

![ilustração que mostra primeiro a conversão simples, na qual um objeto é movido sem rotação e, em seguida, mostra a tradução avançada, que envolve a movimentação com rotação](images/translation.png)

<span data-ttu-id="0ca59-112">No exemplo a, o exemplo de conversão simples, o objeto é movido sem rotação.</span><span class="sxs-lookup"><span data-stu-id="0ca59-112">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="0ca59-113">No exemplo B, o objeto é girado durante a tradução, dependendo de onde está o ponto de contato do objeto.</span><span class="sxs-lookup"><span data-stu-id="0ca59-113">In example B, the object is rotated during the translation, depending on where the object contact point is.</span></span> <span data-ttu-id="0ca59-114">Se você habilitar a rotação de dedo único, conforme descrito em [rotação de dedo único](single-finger-rotation.md), poderá habilitar a tradução complexa.</span><span class="sxs-lookup"><span data-stu-id="0ca59-114">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span> <span data-ttu-id="0ca59-115">O diagrama a seguir mostra os vários componentes da rotação de um único dedo quando você está executando a tradução.</span><span class="sxs-lookup"><span data-stu-id="0ca59-115">The following diagram shows the various components of single-finger rotation when you are performing translation.</span></span>

![ilustração que mostra os componentes de rotação de um único dedo: pivotpointx, pivotpointy e pivotradius](images/translation-complex-components.png)

<span data-ttu-id="0ca59-117">À medida que o objeto é movido, o raio é recalculado e o ponto dinâmico é movido.</span><span class="sxs-lookup"><span data-stu-id="0ca59-117">As the object is moved, the radius is recalculated and the pivot point is moved.</span></span>

<span data-ttu-id="0ca59-118">O código a seguir mostra uma maneira de fazer isso em uma implementação de [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) que habilita a tradução complexa.</span><span class="sxs-lookup"><span data-stu-id="0ca59-118">The following code shows one way that you can do this in an implementation of [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) that enables complex translation.</span></span>


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> <span data-ttu-id="0ca59-119">As transformações de objeto ocorrem antes que os pontos dinâmicos e o raio sejam calculados.</span><span class="sxs-lookup"><span data-stu-id="0ca59-119">Object transformations occur before the pivot points and radius are calculated.</span></span> <span data-ttu-id="0ca59-120">Dessa maneira, o objeto será movido corretamente se o usuário executar a expansão no objeto enquanto ele estiver sendo movido.</span><span class="sxs-lookup"><span data-stu-id="0ca59-120">In this manner the object will move correctly if the user performs expansion on the object while it is moving.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0ca59-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ca59-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ca59-122">Manipulações</span><span class="sxs-lookup"><span data-stu-id="0ca59-122">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




