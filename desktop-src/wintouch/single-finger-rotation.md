---
title: Rotação de Single-Finger
description: Esta seção explica como girar um objeto usando um ponto dinâmico.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Touch, rotação
- Windows Touch, manipulações
- Windows Touch, rotação de dedo único
- Windows Touch, rotação de ponto dinâmico
- manipulações, rotação
- rotação, pontos dinâmicos
- rotação, um único dedo
- gestos, rotação de dedo único
- rotação de dedo único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d74263f502749e2aaf942c4bbec5aa0a284e76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822429"
---
# <a name="single-finger-rotation"></a><span data-ttu-id="b2f4b-112">Rotação de Single-Finger</span><span class="sxs-lookup"><span data-stu-id="b2f4b-112">Single-Finger Rotation</span></span>

<span data-ttu-id="b2f4b-113">Esta seção explica como girar um objeto usando um ponto dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-113">This section explains how to rotate an object using a pivot point.</span></span>

<span data-ttu-id="b2f4b-114">A imagem a seguir ilustra a rotação de um único dedo.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-114">The following image illustrates single-finger rotation.</span></span>

![ilustração mostrando dois tipos de rotação de um único dedo: ao lado do centro ou ao lado da borda](images/sfrotation.png)

<span data-ttu-id="b2f4b-116">No exemplo A, o objeto é girado em volta do ponto central do objeto usando o gesto de rotação.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-116">In example A, the object is rotated around the center point of the object by using the rotation gesture.</span></span> <span data-ttu-id="b2f4b-117">No exemplo B, o objeto é girado movendo-se um único dedo ao lado da borda do objeto.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-117">In example B, the object is rotated by moving a single finger around the edge of the object.</span></span> <span data-ttu-id="b2f4b-118">O processador de manipulação habilita essa rotação usando os valores de ponto dinâmico e raio dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-118">The manipulation processor enables this rotation by using pivot point and pivot radius values.</span></span> <span data-ttu-id="b2f4b-119">A imagem a seguir ilustra os componentes da rotação de um único dedo.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-119">The following image illustrates the components of single-finger rotation.</span></span>

![ilustração mostrando os componentes de rotação de um único dedo: pivotpointx, pivotpointy e pivotradius](images/sfrotation-components.png)

<span data-ttu-id="b2f4b-121">Depois de definir os valores [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)e [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) , as mensagens de tradução subsequentes incorporarão a rotação.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-121">After you set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy), and [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) values, subsequent translation messages will incorporate rotation.</span></span> <span data-ttu-id="b2f4b-122">Quanto maior o raio dinâmico, maior a alteração em x e y deve ser para girar o objeto.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-122">The larger the pivot radius, the greater the change in x and y must be to rotate the object.</span></span> <span data-ttu-id="b2f4b-123">O código a seguir mostra como esses valores podem ser definidos no processador de manipulação.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-123">The following code shows how these values could be set in the manipulation processor.</span></span>


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



<span data-ttu-id="b2f4b-124">No exemplo anterior, a distância para a borda do objeto (dimensionada para 40 por cento) é usada como o raio dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-124">In the previous example, the distance to the edge of the object (scaled to 40 percent) is used as the pivot radius.</span></span> <span data-ttu-id="b2f4b-125">Como o tamanho do objeto é levado em consideração, esse cálculo é válido para cada Delta de objeto.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-125">Because the object size is taken into consideration, this calculation is valid for every object delta.</span></span> <span data-ttu-id="b2f4b-126">À medida que o objeto é dimensionado, o raio dinâmico aumenta.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-126">As the object scales, the pivot radius grows.</span></span> <span data-ttu-id="b2f4b-127">Esse valor e os valores x e y centrais do objeto são passados para o processador de manipulação para girar o objeto em volta do ponto dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-127">This value and the object's center x and y values are passed to the manipulation processor to rotate the object around the pivot point.</span></span>

> [!Note]  
> <span data-ttu-id="b2f4b-128">O valor de [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) nunca deve estar entre 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="b2f4b-128">The [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) value should never be between 0.0 and 1.0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b2f4b-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2f4b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f4b-130">Manipulações</span><span class="sxs-lookup"><span data-stu-id="b2f4b-130">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> <dt>

[<span data-ttu-id="b2f4b-131">**PivotRadius**</span><span class="sxs-lookup"><span data-stu-id="b2f4b-131">**PivotRadius**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[<span data-ttu-id="b2f4b-132">**PivotPointX**</span><span class="sxs-lookup"><span data-stu-id="b2f4b-132">**PivotPointX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[<span data-ttu-id="b2f4b-133">**PivotPointY**</span><span class="sxs-lookup"><span data-stu-id="b2f4b-133">**PivotPointY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




