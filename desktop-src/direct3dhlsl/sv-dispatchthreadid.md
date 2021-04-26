---
title: SV_DispatchThreadID
description: Índices para os quais thread e grupo de threads combinados um sombreador de computação está sendo executado.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9653d98ebbfef6dd25bb137af3358a14d177f3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996513"
---
# <a name="sv_dispatchthreadid"></a>\_DISPATCHTHREADID VA

Índices para os quais thread e grupo de threads combinados um sombreador de computação está sendo executado. \_DISPATCHTHREADID VA é a soma de VA \_ GroupId \* numthreads e GroupThreadID. Varia em todo o intervalo especificado em [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numthreads](sm5-attributes-numthreads.md). Por exemplo, se a expedição (2, 2, 2) for chamada em um sombreador de computação com numthreads (3, 3, 3) \_ , DISPATCHTHREADID VA terá um intervalo de 0.. 5 para cada dimensão.

## <a name="type"></a>Digite



|       |
|-------|
| Digite  |
| uint3 |



 

## <a name="remarks"></a>Comentários

Esse valor de sistema é opcional.

A ilustração a seguir mostra a relação entre os parâmetros passados para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md), VA \_ DispatchThreadID,[VA \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupId](sv-groupid.md)).

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

 

 
