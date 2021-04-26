---
title: SV_GroupID
description: Índices para os quais o grupo de threads um sombreador de computação está sendo executado.
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
ms.openlocfilehash: cf96e1db7dbb93c88ec741e309413dea3df2b01d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996993"
---
# <a name="sv_groupid"></a>\_GroupId da VA

Índices para os quais o grupo de threads um sombreador de computação está sendo executado. Os índices são para o grupo inteiro e não para um thread individual. Os valores possíveis variam entre o intervalo passado como parâmetros para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch). Por exemplo, chamar dispatch (2, 1, 1) resulta em valores possíveis de 0, 0, 0 e 1, 0, 0.

Define o deslocamento do grupo dentro de uma chamada de [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) , por dimensão da chamada de expedição.

## <a name="type"></a>Digite



|       |
|-------|
| Digite  |
| uint3 |



 

## <a name="remarks"></a>Comentários

Esse valor de sistema é opcional.

A ilustração a seguir mostra a relação entre os parâmetros passados para [**expedição**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md),[VA \_ DispatchThreadID](sv-dispatchthreadid.md),[VA \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupId).

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

 

 
