---
title: função ddy_fine
description: Computa uma derivada parcial de alta precisão em relação à coordenada x de espaço de tela. | função ddy_fine
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- função ddy_fine HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989262"
---
# <a name="ddy_fine-function"></a>ddy \_ função fina

Computa uma derivada parcial de alta precisão em relação à coordenada x de espaço de tela.

## <a name="syntax"></a>Sintaxe

``` syntax
float ddy_fine(
  in float value
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

O derivativo parcial de alta precisão do *valor*.

## <a name="remarks"></a>Comentários

As seguintes versões sobrecarregadas também estão disponíveis:

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
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

 

 




