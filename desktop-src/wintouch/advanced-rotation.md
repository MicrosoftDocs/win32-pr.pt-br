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
# <a name="advanced-rotation"></a>Rotação avançada

Esta seção explica como girar um objeto com base em onde o usuário está executando a manipulação de rotação.

A imagem a seguir ilustra duas maneiras diferentes que um objeto pode ser girado.

![ilustração mostrando dois tipos de rotação de dedo único: ao lado do centro ou ao lado da borda, com a borda que envolve a rotação e a translação](images/rotation.png)

No exemplo A, o objeto é manipulado em volta do ponto central do objeto. No exemplo B, o objeto é girado em volta do ponto central da manipulação. Para dar suporte à manipulação em um ponto diferente do ponto central do objeto, você deve executar uma manipulação composta que executa a rotação e a conversão. O código a seguir mostra como essa manipulação é executada e calculada.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulações avançadas](advanced-manipulations.md)
</dt> <dt>

[Manipulações](getting-started-with-manipulations.md)
</dt> </dl>

 

 




