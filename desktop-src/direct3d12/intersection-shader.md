---
description: Um sombreador que é usado para implementar primitivos de interseção personalizados para raios interseccionando um volume limitado associado (caixa delimitadora).
ms.assetid: ''
title: Sombreador de interseção
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786308"
---
# <a name="intersection-shader"></a>Sombreador de interseção

Um sombreador que é usado para implementar primitivos de interseção personalizados para raios interseccionando um volume limitado associado (caixa delimitadora). 

O sombreador de interseção não tem acesso à carga Ray, mas define os atributos de interseção para cada um deles através de uma chamada para [**ReportHit**](reporthit-function.md).  O tratamento de **ReportHit** pode parar o sombreador de interseção cedo, se o **sinalizador Ray Flag ray \_ \_ aceitar \_ primeiro \_ HIT_ \AND \_ \END \_ Search** estiver definido ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) for chamado de um sombreador any.  Caso contrário, retornará true se o pressionamento for aceito ou false se o pressionamento for rejeitado.  Isso significa que um sombreador qualquer clique, se presente, deve ser executado antes que o controle retorne condicionalmente para o sombreador de interseção.

## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("intersection")]
```



## <a name="example"></a>Exemplo

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




