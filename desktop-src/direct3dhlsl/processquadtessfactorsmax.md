---
title: Função ProcessQuadTessFactorsMax
description: Gera os fatores de mosaico corrigidos para um patch quádruplo. | Função ProcessQuadTessFactorsMax
ms.assetid: a0c91430-db25-49c9-bcc8-d2be1d0e6f6c
keywords:
- HLSL da função ProcessQuadTessFactorsMax
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62219301e93bebf7825328fd381b5d2fbb607925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968463"
---
# <a name="processquadtessfactorsmax-function"></a>Função ProcessQuadTessFactorsMax

Gera os fatores de mosaico corrigidos para um patch quádruplo.

## <a name="syntax"></a>Sintaxe

``` syntax
void ProcessQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RawEdgeFactors* \[ no\]
</dt> <dd>

Tipo: **FLOAT4**

Os fatores de mosaico de borda, passados para o estágio Tessellator.

</dd> <dt>

*InsideScale* \[ no\]
</dt> <dd>

Tipo: **float**

O fator de escala aplicado aos fatores de mosaico UV calculados pelo estágio de mosaico. O intervalo permitido para InsideScale é de 0,0 a 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ fora\]
</dt> <dd>

Tipo: **FLOAT4**

Os fatores de borda arredondada-mosaico calculados pelo estágio Tessellator.

</dd> <dt>

*RoundedInsideTessFactors* \[ fora\]
</dt> <dd>

Tipo: **float2**

Os fatores de mosaico arredondados calculados pelo estágio Tessellator para bordas internas.

</dd> <dt>

*UnroundedInsideTessFactors* \[ fora\]
</dt> <dd>

Tipo: **float2**

Os fatores de mosaico calculados pelo estágio Tessellator para bordas internas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Gera os fatores de mosaico corrigidos para um patch quádruplo, computando os fatores de mosaico internos como o máximo dos fatores de mosaico de borda. Os fatores de Tess internos serão valores idênticos determinados pelo máximo de todas as quatro bordas dimensionadas pelo InsideScale. O resultado é arredondado com base no modo de particionamento, mas os resultados não arredondados estão disponíveis usando o parâmetro *UnroundedInsideTessFactors* .

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




