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
# <a name="advanced-expansion"></a>Expansão avançada

A ilustração a seguir mostra duas maneiras que um objeto pode ser expandido.

![ilustração que mostra a expansão simples em relação ao ponto central de um objeto e a expansão avançada em relação ao ponto central da manipulação](images/expansion.png)

No exemplo a, o exemplo de expansão simples, o objeto é expandido em todo o seu ponto central. No exemplo B, o objeto é expandido em volta do ponto central da manipulação. Para habilitar isso, você deve converter o objeto enquanto ele está sendo expandido. O valor que você converterá o objeto será o mesmo da distância do centro do objeto até o ponto central do gesto. Intuitivamente, é como se você estivesse expandindo o objeto do ponto central do gesto de expansão e, em seguida, movendo-o para que ele ainda esteja no mesmo centro de sua posição inicial. O código a seguir mostra uma maneira que esse conceito pode ser aplicado para habilitar a expansão em um ponto central.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações](getting-started-with-manipulations.md)
</dt> </dl>

 

 




