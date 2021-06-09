---
title: SV_GroupID
description: Índices para os quais um sombreador de computação está sendo executado por um grupo de threads.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827035"
---
# <a name="sv_groupid"></a>GroupID de SV \_

Índices para os quais um sombreador de computação está sendo executado por um grupo de threads. Os índices são para todo o grupo e não para um thread individual. Os valores possíveis variam entre o intervalo passado como parâmetros para [**Dispatch.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) Por exemplo, chamar Dispatch(2,1,1) resulta em valores possíveis de 0,0,0 e 1,0,0.

Define o deslocamento de grupo dentro de uma [**chamada dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) por dimensão da chamada de expedição.

## <a name="type"></a>Tipo



| Tipo      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Comentários

Esse valor do sistema é opcional.

A ilustração a seguir mostra a relação entre os parâmetros passados para [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), os valores especificados no [atributo numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e os valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread [(SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)[SV \_ GroupThreadID,](sv-groupthreadid.md)SV \_ GroupID).

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

 

 
