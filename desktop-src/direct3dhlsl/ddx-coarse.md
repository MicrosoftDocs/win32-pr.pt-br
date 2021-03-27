---
title: função ddx_coarse
description: Computa uma derivada parcial de baixa precisão em relação à coordenada x de espaço de tela.
ms.assetid: 5719f45d-b2ae-4916-8f31-c2797b661814
keywords:
- função ddx_coarse HLSL
topic_type:
- apiref
api_name:
- ddx_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f9d4805a1d516a5d8980fcd8209fd6733fe86c4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006679"
---
# <a name="ddx_coarse-function"></a>\_função campo DDX grande

Computa uma derivada parcial de baixa precisão em relação à coordenada x de espaço de tela.

## <a name="syntax"></a>Sintaxe

``` syntax
float ddx_coarse(
  in float value
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do no\]
</dt> <dd>

Tipo: **float**

O valor de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **float**

O derivativo parcial de baixa precisão do *valor*.

## <a name="remarks"></a>Comentários

As seguintes versões sobrecarregadas também estão disponíveis:

``` syntax
float2 ddx_coarse(float2 value);
float3 ddx_coarse(float3 value);
float4 ddx_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




