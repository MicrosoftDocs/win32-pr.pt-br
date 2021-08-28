---
title: Tradução avançada
description: Tradução avançada
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Toque, tradução
- Windows Toque, tradução avançada
- Windows Toque, manipulações
- manipulações, tradução
- manipulações, tradução avançada
- tradução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4712375c12420e076bb93c1240d18dc8e3c1d58006eb24ced7a62a7485e01c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810337"
---
# <a name="advanced-translation"></a>Tradução avançada

A ilustração a seguir mostra duas interpretações de tradução.

![ilustração que mostra primeiro a conversão simples, na qual um objeto é movido sem rotação e, em seguida, mostra a tradução avançada, que envolve a movimentação com rotação](images/translation.png)

No exemplo a, o exemplo de conversão simples, o objeto é movido sem rotação. No exemplo B, o objeto é girado durante a tradução, dependendo de onde está o ponto de contato do objeto. Se você habilitar a rotação de dedo único, conforme descrito em [rotação de dedo único](single-finger-rotation.md), poderá habilitar a tradução complexa. O diagrama a seguir mostra os vários componentes da rotação de um único dedo quando você está executando a tradução.

![ilustração que mostra os componentes de rotação de um único dedo: pivotpointx, pivotpointy e pivotradius](images/translation-complex-components.png)

À medida que o objeto é movido, o raio é recalculado e o ponto dinâmico é movido.

O código a seguir mostra uma maneira de fazer isso em uma implementação de [**ManipulationDelta**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) que habilita a tradução complexa.


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
> As transformações de objeto ocorrem antes que os pontos dinâmicos e o raio sejam calculados. Dessa maneira, o objeto será movido corretamente se o usuário executar a expansão no objeto enquanto ele estiver sendo movido.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações](getting-started-with-manipulations.md)
</dt> </dl>

 

 




