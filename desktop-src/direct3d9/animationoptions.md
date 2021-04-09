---
description: Permite definir opções de animação.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: Animaçãooptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089361"
---
# <a name="animationoptions"></a>Animaçãooptions

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

-   openclosed-Use 0 para uma animação fechada ou 1 para uma animação aberta. Por padrão, uma animação é fechada.
-   positionquality-defina a qualidade da posição para qualquer chave de posição especificada. Use 0 para posições de spline ou 1 para posições lineares.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



