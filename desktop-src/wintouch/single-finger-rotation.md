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
# <a name="single-finger-rotation"></a>Rotação de Single-Finger

Esta seção explica como girar um objeto usando um ponto dinâmico.

A imagem a seguir ilustra a rotação de um único dedo.

![ilustração mostrando dois tipos de rotação de um único dedo: ao lado do centro ou ao lado da borda](images/sfrotation.png)

No exemplo A, o objeto é girado em volta do ponto central do objeto usando o gesto de rotação. No exemplo B, o objeto é girado movendo-se um único dedo ao lado da borda do objeto. O processador de manipulação habilita essa rotação usando os valores de ponto dinâmico e raio dinâmico. A imagem a seguir ilustra os componentes da rotação de um único dedo.

![ilustração mostrando os componentes de rotação de um único dedo: pivotpointx, pivotpointy e pivotradius](images/sfrotation-components.png)

Depois de definir os valores [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)e [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) , as mensagens de tradução subsequentes incorporarão a rotação. Quanto maior o raio dinâmico, maior a alteração em x e y deve ser para girar o objeto. O código a seguir mostra como esses valores podem ser definidos no processador de manipulação.


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



No exemplo anterior, a distância para a borda do objeto (dimensionada para 40 por cento) é usada como o raio dinâmico. Como o tamanho do objeto é levado em consideração, esse cálculo é válido para cada Delta de objeto. À medida que o objeto é dimensionado, o raio dinâmico aumenta. Esse valor e os valores x e y centrais do objeto são passados para o processador de manipulação para girar o objeto em volta do ponto dinâmico.

> [!Note]  
> O valor de [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) nunca deve estar entre 0,0 e 1,0.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações](getting-started-with-manipulations.md)
</dt> <dt>

[**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




