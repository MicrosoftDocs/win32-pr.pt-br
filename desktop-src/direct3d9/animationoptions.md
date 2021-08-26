---
description: Permite definir opções de animação.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346eaa1b94637fa357f09cd701ac9d99d5ddf2076ee12654076e54bce82527fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069426"
---
# <a name="animationoptions"></a>AnimationOptions

Permite definir opções de animação.

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

Em que:

-   openclosed – use 0 para uma animação fechada ou 1 para uma animação aberta. Por padrão, uma animação é fechada.
-   igualdade de posição – de definir a qualidade da posição para todas as chaves de posição especificadas. Use 0 para posições spline ou 1 para posições lineares.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



