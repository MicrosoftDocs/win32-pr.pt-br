---
title: SV_GroupIndex
description: O \ 0034; achatado \ 0034; índice de um thread de sombreador de computação dentro de um grupo de threads, que transforma a GroupThreadID de VA multidimensional \_ em um valor 1D. \_GROUPINDEX VA varia de 0 a (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211; uma.
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
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641319"
---
# <a name="sv_groupindex"></a>\_GROUPINDEX VA

O índice "achatado" de um thread de sombreador de computação em um grupo de threads, que transforma a GroupThreadID de VA multidimensional \_ em um valor 1D. \_A GroupIndex de VA varia de 0 a (numthreadsX \* numthreadsY \* numThreadsZ) – 1.

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



em que Dimx e Dimy são as dimensões especificadas no atributo [numthreads](sm5-attributes-numthreads.md) para o ponto de entrada.

Esse valor de sistema é opcional. No entanto, seu uso garante que um thread só grave em sua região atribuída de memória na variável groupshared.

A ilustração a seguir mostra a relação entre os parâmetros passados [**para ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no [atributo numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread (VA \_ GroupIndex,[VA \_ DispatchThreadID](sv-dispatchthreadid.md),[VA \_ GroupThreadID](sv-groupthreadid.md), a [ \_ DefaultGroupID](sv-groupid.md)).

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Semântica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 