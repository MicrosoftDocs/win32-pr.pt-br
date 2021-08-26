---
description: Envia um raio para uma pesquisa de ocorrências em uma estrutura de aceleração.
ms.assetid: ''
title: Função TraceRay
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TraceRay
api_type:
- NA
ms.openlocfilehash: 4e22a26d7bd2fd91029c106133667bce98c163d90d99f0700dac7f2bdf0796fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027976"
---
# <a name="traceray-function"></a>Função TraceRay

Envia um raio para uma pesquisa de ocorrências em uma estrutura de aceleração.

## <a name="syntax"></a>Syntax
Essa definição de função intrínseca é equivalente ao seguinte modelo de função:

```
Template<payload_t>
void TraceRay(RaytracingAccelerationStructure AccelerationStructure,
              uint RayFlags,
              uint InstanceInclusionMask,
              uint RayContributionToHitGroupIndex,
              uint MultiplierForGeometryContributionToHitGroupIndex,
              uint MissShaderIndex,
              RayDesc Ray,
              inout payload_t Payload);

```



## <a name="parameters"></a>Parâmetros

`AccelerationStructure`

A estrutura de aceleração de nível superior a ser usada. A especificação de uma estrutura de aceleração nula força um erro.

`RayFlags`

Combinação válida de valores de [ray_flag](ray_flag.md) . Somente os sinalizadores de Ray definidos são propagados pelo sistema, ou seja, são visíveis para o sombreador [RayFlags](rayflags.md) intrínseco.

`InstanceInclusionMask`

Um inteiro sem sinal, os 8 bits inferiores que são usados para incluir ou rejeitar instâncias de geometria com base no InstanceMask em cada instância. Por exemplo:
```
if(!((InstanceInclusionMask & InstanceMask) & 0xff)) { //ignore intersection }
```

`RayContributionToHitGroupIndex`

Um inteiro não assinado que especifica o deslocamento a ser adicionado aos cálculos de endereçamento em tabelas de sombreamento para indexação de grupo de acesso.  Somente os 4 últimos bits desse valor são usados.

`MultiplierForGeometryContributionToHitGroupIndex`

Um inteiro não assinado que especifica o stride para multiplicar por *GeometryContributionToHitGroupIndex*, que é apenas o índice baseado em 0 que a geometria foi fornecida pelo aplicativo em sua estrutura de aceleração de nível inferior. Somente os 16 bits inferiores desse valor de multiplicador são usados.

`MissShaderIndex`

Um inteiro sem sinal que especifica o índice do sombreador ausente dentro de uma tabela de sombreador.

`Ray`

Um [**RayDesc**](raydesc.md) que representa o raio a ser rastreado.

`Payload`

Uma carga Ray definida pelo usuário foi acessada tanto para entrada quanto para saída por sombreadores invocados durante raytracing.  Após a conclusão do [**TraceRay**](traceray-function.md) , o chamador também pode acessar a carga.

## <a name="return-value"></a>Valor Retornado

**livre**

## <a name="remarks"></a>Comentários

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de resolução**](miss-shader.md)
* [**Sombreador da geração de raio**](ray-generation-shader.md)



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




