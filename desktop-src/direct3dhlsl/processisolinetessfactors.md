---
title: Função ProcessIsolineTessFactors
description: Gera os fatores de mosaico arredondados para um Isoline.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- HLSL da função ProcessIsolineTessFactors
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638675"
---
# <a name="processisolinetessfactors-function"></a>Função ProcessIsolineTessFactors

Gera os fatores de mosaico arredondados para um Isoline.

## <a name="syntax"></a>Sintaxe

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RawDetailFactor* \[ no\]
</dt> <dd>

Tipo: **float**

O fator de detalhe desejado.

</dd> <dt>

*RawDensityFactor* \[ no\]
</dt> <dd>

Tipo: **float**

O fator de densidade desejado.

</dd> <dt>

*RoundedDetailFactor* \[ fora\]
</dt> <dd>

Tipo: **float**

O fator de detalhe arredondado clamped a um intervalo que pode ser usado pelo Tessellator.

</dd> <dt>

*RoundedDensityFactor* \[ fora\]
</dt> <dd>

Tipo: **float**

O fator de densidade arredondado clamped a um rangethat pode ser usado pelo Tessellator.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

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

 

 




