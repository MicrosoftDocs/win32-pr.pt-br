---
title: SV_GroupIndex
description: O \ 0034;nivelado \ 0034; índice de um thread de sombreador de computação dentro de um grupo de threads, que transforma o GroupThreadID de SV \_ multidimensional em um valor 1D. O SV \_ GroupIndex varia de 0 a (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211; 1.
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd8c10212a2dd91e4ecbe7fd48a427e4019b2cd79b3d56457635ab9ef9d9262a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508246"
---
# <a name="sv_groupindex"></a>SV \_ GroupIndex

O índice "nivelado" de um thread de sombreador de computação dentro de um grupo de threads, que transforma o GroupThreadID de SV multidimensional em \_ um valor 1D. O SV \_ GroupIndex varia de 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.

## <a name="type"></a>Tipo



| Tipo |
|------|
| uint |



 

## <a name="remarks"></a>Comentários


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



em que dimx e dimy são as dimensões especificadas no [atributo numthreads](sm5-attributes-numthreads.md) para o ponto de entrada.

Esse valor do sistema é opcional. No entanto, seu uso garante que um thread só grava em sua região de memória atribuída na variável groupshared.

A ilustração a seguir mostra a relação entre os parâmetros passados para [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), os valores especificados no [atributo numthreads,](sm5-attributes-numthreads.md) numthreads(10,8,3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread (SV \_ GroupIndex,[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)[SV \_ GroupThreadID,](sv-groupthreadid.md)[SV \_ GroupID](sv-groupid.md)).

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

 

 