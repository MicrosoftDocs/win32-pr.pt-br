---
description: Define um conjunto de chaves de animação. Uma chave de matriz é útil para conjuntos de dados de animação que precisam ser representados como matrizes de transformação.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807849"
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

-   KeyType – especifica se as chaves são rotação, escala, posição ou chaves de matriz (usando os inteiros 0, 1, 2 ou 3, respectivamente).
-   nKeys-número de chaves.
-   chaves-uma matriz de chaves. Consulte [**TimedFloatKeys**](timedfloatkeys.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



