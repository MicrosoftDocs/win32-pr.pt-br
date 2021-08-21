---
title: Função ProcessIsolineTessFactors
description: Gera os fatores de mosaico arredondados para uma isoline.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Função ProcessIsolineTessFactors HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34c6f4d579ee7fbaee9416d7a607e3856a7793021cca7149723d3d6e5a2b4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986286"
---
# <a name="processisolinetessfactors-function"></a>Função ProcessIsolineTessFactors

Gera os fatores de mosaico arredondados para uma isoline.

## <a name="syntax"></a>Sintaxe

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RawDetailFactor* \[ Em\]
</dt> <dd>

Tipo: **float**

O fator de detalhes desejado.

</dd> <dt>

*RawDensityFactor* \[ Em\]
</dt> <dd>

Tipo: **float**

O fator de densidade desejado.

</dd> <dt>

*RoundedDetailFactor* \[ out\]
</dt> <dd>

Tipo: **float**

O fator de detalhes arredondado fixado em um intervalo que pode ser usado pelo mosaico.

</dd> <dt>

*RoundedDensityFactor* \[ out\]
</dt> <dd>

Tipo: **float**

O fator de densidade arredondado fixado em um intervalo que pode ser usado pelo mosaico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

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

 

 




