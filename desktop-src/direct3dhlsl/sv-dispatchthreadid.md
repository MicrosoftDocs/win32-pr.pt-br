---
title: SV_DispatchThreadID
description: Índices para os quais o thread combinado e o grupo de threads em que um sombreador de computação está sendo executado.
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
ms.openlocfilehash: a5f7dbc7f4aa4b508d801736529628dbb25c29fb6c37f1db04f91874e85ee9a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023386"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Índices para os quais o thread combinado e o grupo de threads em que um sombreador de computação está sendo executado. SV \_ DispatchThreadID é a soma de \_ numthreads de GroupID SV \* e GroupThreadID. Ela varia entre o intervalo especificado em [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) e [numthreads.](sm5-attributes-numthreads.md) Por exemplo, se Dispatch(2,2,2) for chamado em um sombreador de computação com numthreads(3,3,3) SV DispatchThreadID terá um intervalo \_ de 0,.5 para cada dimensão.

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Comentários

Esse valor do sistema é opcional.

A ilustração a seguir mostra a relação entre os parâmetros passados para [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), os valores especificados no [atributo numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e os valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([SV \_ GroupIndex,](sv-groupindex.md)SV \_ DispatchThreadID,[SV \_ GroupThreadID,](sv-groupthreadid.md)[SV \_ GroupID](sv-groupid.md)).

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

 

 
