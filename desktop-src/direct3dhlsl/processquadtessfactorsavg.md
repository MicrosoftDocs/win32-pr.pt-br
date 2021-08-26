---
title: Função ProcessQuadTessFactorsAvg
description: Gera os fatores de mosaico corrigidos para um patch quad. | Função ProcessQuadTessFactorsAvg
ms.assetid: 3af1dad3-1923-45f3-9908-ca403e7f0cfe
keywords:
- Função ProcessQuadTessFactorsAvg HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 601036c20651da03de15fe4de807ccb6e9d73f5e0b6fc9c1cefc48ccb48b9147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067786"
---
# <a name="processquadtessfactorsavg-function"></a>Função ProcessQuadTessFactorsAvg

Gera os fatores de mosaico corrigidos para um patch quad.

## <a name="syntax"></a>Sintaxe

``` syntax
void ProcessQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RawEdgeFactors* \[ Em\]
</dt> <dd>

Tipo: **float4**

Os fatores de mosaico de borda, passados para o estágio do mosaico.

</dd> <dt>

*InsideScale* \[ Em\]
</dt> <dd>

Tipo: **float**

O fator de escala aplicado aos fatores de mosaico UV calculados pelo estágio de mosaico. O intervalo acessível para InsideScale é de 0,0 a 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Tipo: **float4**

Os fatores arredondados de mosaico de borda calculados pelo estágio do mosaico.

</dd> <dt>

*RoundedInsideTessFactors* \[ out\]
</dt> <dd>

Tipo: **float2**

Os fatores de mosaico arredondados calculados pelo estágio do mosaico para dentro das bordas.

</dd> <dt>

*UnroundedInsideTessFactors* \[ out\]
</dt> <dd>

Tipo: **float2**

Os fatores de mosaico calculados pelo estágio do mosaico para bordas internas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Gera os fatores de mosaico corrigidos para um patch quad, computando os fatores de mosaico interno como a média dos fatores de mosaico de borda. Os fatores dentro do Tess serão valores idênticos determinados pela média de todas as quatro bordas dimensionadas por InsideScale. O resultado é arredondado com base no modo de particionamento, mas os resultados não encontrados estão disponíveis usando o parâmetro UnroundedInsideTessFactors.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




