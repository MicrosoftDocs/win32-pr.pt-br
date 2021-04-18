---
description: Define um conjunto de dois valores Boolianos usados no modelo MeshFaceWraps para definir a topologia de textura de uma face individual. Use em vez de Boolean2d quando as coordenadas de textura (u, v) abrangem o intervalo de 0 a 2 em vez de 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105815515"
---
# <a name="materialwrap"></a>MaterialWrap

Define um conjunto de dois valores Boolianos usados no modelo [**MeshFaceWraps**](meshfacewraps.md) para definir a topologia de textura de uma face individual. Use em vez de [**Boolean2d**](boolean2d.md) quando as coordenadas de textura (u, v) abrangem o intervalo de 0 a 2 em vez de 0 a 1.

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

Em que:

-   valor u-booliano. Consulte [**booliano**](boolean.md).
-   valor de v-booliano. Consulte [**booliano**](boolean.md).

> [!Note]  
> O modelo [**MeshFaceWraps**](meshfacewraps.md) não é mais usado.

 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



