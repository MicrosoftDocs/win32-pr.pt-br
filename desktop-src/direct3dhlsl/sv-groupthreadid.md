---
title: SV_GroupThreadID
description: Índices para os quais um thread individual dentro de um grupo de threads em que um sombreador de computação está sendo executado.
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
ms.openlocfilehash: d399008f1a9314ceb1fd4b1499b51340b499600b
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827025"
---
# <a name="sv_groupthreadid"></a>SV \_ GroupThreadID

Índices para os quais um thread individual dentro de um grupo de threads em que um sombreador de computação está sendo executado. O SV GroupThreadID varia de acordo com o intervalo especificado para o \_ sombreador de computação no [atributo numthreads.](sm5-attributes-numthreads.md) Por exemplo, se numthreads(3,2,1) tiver sido especificado valores possíveis para o valor de entrada GroupThreadID SV têm esse intervalo de valores \_ (0-2,0-1,0).

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Comentários

Esse valor do sistema é opcional e está sempre dentro dos limites dos valores passados para o [atributo numthreads.](sm5-attributes-numthreads.md)

A ilustração a seguir mostra a relação entre os parâmetros passados para [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), os valores especificados no [atributo numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e os valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Semântica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
