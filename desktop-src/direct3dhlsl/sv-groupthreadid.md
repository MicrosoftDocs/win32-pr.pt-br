---
title: SV_GroupThreadID
description: Índices para os quais um thread individual em um grupo de threads em que um sombreador de computação está sendo executado.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d36e5639b017dfa94e0f3c9f84d6725f6b6a283
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996983"
---
# <a name="sv_groupthreadid"></a>\_GROUPTHREADID VA

Índices para os quais um thread individual em um grupo de threads em que um sombreador de computação está sendo executado. A \_ GroupThreadID de VA varia entre o intervalo especificado para o sombreador de computação no atributo [numthreads](sm5-attributes-numthreads.md) . Por exemplo, se numthreads (3, 2, 1) tiver sido especificado, os valores possíveis para o \_ valor de entrada GroupThreadID de VA terão esse intervalo de valores (0-2, 0-1, 0).

## <a name="type"></a>Digite



|       |
|-------|
| Digite  |
| uint3 |



 

## <a name="remarks"></a>Comentários

Esse valor do sistema é opcional e está sempre dentro dos limites dos valores passados para o atributo [numthreads](sm5-attributes-numthreads.md) .

A ilustração a seguir mostra a relação entre os parâmetros passados para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md),[VA \_ DispatchThreadID](sv-dispatchthreadid.md), VA \_ GroupThreadID,[SV \_ GroupId](sv-groupid.md)).

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domain | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Semântica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
