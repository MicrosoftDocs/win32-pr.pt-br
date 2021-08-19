---
description: Define um conjunto de chaves de animação. Uma chave de matriz é útil para conjuntos de dados de animação que precisam ser representados como matrizes de transformação.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bad23a6cc519b0b0525cd0dac1b488184b3bf91e99359e252f44dca435ace529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806401"
---
# <a name="animationkey"></a>AnimationKey

Define um conjunto de chaves de animação. Uma chave de matriz é útil para conjuntos de dados de animação que precisam ser representados como matrizes de transformação.

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

Em que:

-   keyType – especifica se as chaves são chaves de rotação, escala, posição ou matriz (usando os inteiros 0, 1, 2 ou 3, respectivamente).
-   nKeys – número de chaves.
-   keys – uma matriz de chaves. Consulte [**TimedFloatKeys**](timedfloatkeys.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



