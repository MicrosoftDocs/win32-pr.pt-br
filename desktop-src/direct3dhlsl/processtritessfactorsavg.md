---
title: Função ProcessTriTessFactorsAvg
description: Gera os fatores de mosaico corrigidos para um patch tri. | Função ProcessTriTessFactorsAvg
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- HLSL da função ProcessTriTessFactorsAvg
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d119ee7011bbd4a03a2a2c8247b9df9e95f983e07ffd3ab3e4603a3a3eaa7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067766"
---
# <a name="processtritessfactorsavg-function"></a>Função ProcessTriTessFactorsAvg

Gera os fatores de mosaico corrigidos para um patch tri.

## <a name="syntax"></a>Sintaxe

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RawEdgeFactors* \[ no\]
</dt> <dd>

Tipo: **float3**

Os fatores de mosaico de borda, passados para o estágio Tessellator.

</dd> <dt>

*InsideScale* \[ no\]
</dt> <dd>

Tipo: **float**

O fator de escala aplicado aos fatores de mosaico UV calculados pelo estágio de mosaico. O intervalo permitido para InsideScale é de 0,0 a 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ fora\]
</dt> <dd>

Tipo: **float3**

Os fatores de borda arredondada-mosaico calculados pelo estágio Tessellator.

</dd> <dt>

*RoundedInsideTessFactor* \[ fora\]
</dt> <dd>

Tipo: **float**

Os fatores de mosaico calculados pelo estágio Tessellator e arredondados.

</dd> <dt>

*UnroundedInsideTessFactor* \[ fora\]
</dt> <dd>

Tipo: **float**

Os fatores de mosaico original, não arredondados e UV calculados pelo estágio de mosaico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Gera os fatores de mosaico corrigidos para o tri patch, computando o fator de mosaico interno como a média dos fatores de mosaico de borda, que é então dimensionada por InsideScale. O resultado é arredondado com base no modo de particionamento, mas os resultados não arredondados estão disponíveis usando o parâmetro UnroundedInsideTessFactor.

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




