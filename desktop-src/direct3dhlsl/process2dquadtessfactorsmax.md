---
title: Função Process2DQuadTessFactorsMax
description: Gera os fatores de mosaico corrigidos para um patch quad. | Função Process2DQuadTessFactorsMax
ms.assetid: 1de95946-d82d-42ba-93d7-ab8383fd5018
keywords:
- Função Process2DQuadTessFactorsMax HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f3325f08d1457230f52a539eaa9a7694d56266b7f2fd8cfd921c7a70e61ab568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510941"
---
# <a name="process2dquadtessfactorsmax-function"></a>Função Process2DQuadTessFactorsMax

Gera os fatores de mosaico corrigidos para um patch quad.

## <a name="syntax"></a>Sintaxe

``` syntax
void Process2DQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
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

Tipo: **float2**

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

Gera os fatores de mosaico corrigidos para um patch quad, computando os fatores de mosaico interno como o máximo dos fatores de mosaico de borda. Você e V dentro dos fatores de mosaico são computados independentemente usando os máximos de lados opostos do domínio e, em seguida, são dimensionados por InsideScale. O resultado é arredondado com base no modo de particionamento, mas os resultados não encontrados estão disponíveis usando o parâmetro UnroundedInsideTessFactors.

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

 

 




