---
title: Single-Finger rotação
description: Esta seção explica como girar um objeto usando um ponto de pivô.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Toque, rotação
- Windows Toque, manipulações
- Windows Toque, rotação de dedo único
- Windows Toque, rotação de ponto de pivô
- manipulações, rotação
- rotação, pontos de pivô
- rotation,single-finger
- gestos, rotação de dedo único
- rotação de dedo único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36fe7e92f6d68515e1d13b39c32ee4af5b6b03e675479242210fe302b84e6395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110638"
---
# <a name="single-finger-rotation"></a>Single-Finger rotação

Esta seção explica como girar um objeto usando um ponto de pivô.

A imagem a seguir ilustra a rotação de dedo único.

![ilustração mostrando dois tipos de rotação de dedo único: ao redor do centro ou ao redor da borda](images/sfrotation.png)

No exemplo A, o objeto é girado em torno do ponto central do objeto usando o gesto de rotação. No exemplo B, o objeto é girado movendo um único dedo ao redor da borda do objeto. O processador de manipulação habilita essa rotação usando valores de ponto de pivô e raio de pivô. A imagem a seguir ilustra os componentes da rotação de dedo único.

![ilustração mostrando os componentes da rotação de dedo único: pivotpointx, pivotpointy e pivotradius](images/sfrotation-components.png)

Depois de definir os [**valores PivotPointX,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)e [**PivotRadius,**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) as mensagens de tradução subsequentes incorporarão a rotação. Quanto maior o raio de pivô, maior a alteração em x e y deve ser para girar o objeto. O código a seguir mostra como esses valores podem ser definidos no processador de manipulação.


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



No exemplo anterior, a distância até a borda do objeto (dimensionada para 40%) é usada como o raio de pivô. Como o tamanho do objeto é levado em consideração, esse cálculo é válido para cada delta de objeto. À medida que o objeto é dimensionado, o raio de pivô aumenta. Esse valor e os valores x e y do objeto são passados para o processador de manipulação para girar o objeto em torno do ponto pivô.

> [!Note]  
> O [**valor pivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) nunca deve estar entre 0,0 e 1,0.

 

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

 

 




