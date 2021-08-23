---
description: Um sombreador usado para implementar primitivos de interseção personalizados para raios intersecção de um volume delimitador associado (caixa delimitador).
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
ms.openlocfilehash: d7f9f81fdedae0fc6f6aa0448e6771c331af9c0d8924ab0f091d281565e4cfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850876"
---
# <a name="intersection-shader"></a>Sombreador de interseção

Um sombreador usado para implementar primitivos de interseção personalizados para raios intersecção de um volume delimitador associado (caixa delimitador). 

O sombreador de interseção não tem acesso à carga de raio, mas define os atributos de interseção para cada ocorrência por meio de uma chamada para [**ReportHit**](reporthit-function.md).  A manipulação do **ReportHit** poderá interromper o sombreador de interseção no início, se o sinalizador de raio **RAY FLAG ACCEPT FIRST \_ \_ \_ \_ HIT_\AND \_ \END \_ SEARCH** estiver definido ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) for chamado de qualquer sombreador de ocorrência.  Caso contrário, ele retornará true se o hit tiver sido aceito ou false se o hit tiver sido rejeitado.  Isso significa que qualquer sombreador de acerto, se presente, deve ser executado antes que o controle retorne condicionalmente ao sombreador de interseção.

## <a name="shader-type-attribute"></a>Atributo Tipo de Sombreador


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

 

 




