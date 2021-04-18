---
title: Função D2DSampleInputAtOffset (D2d1effecthelpers. h)
description: Exemplos de entrada N em um deslocamento de deslocamento da coordenada de entrada. Disponível somente para entradas complexas.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- Direct2D da função D2DSampleInputAtOffset
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755807"
---
# <a name="d2dsampleinputatoffset-function"></a>Função D2DSampleInputAtOffset

Exemplos de entrada N em um deslocamento de deslocamento da coordenada de entrada. Disponível somente para entradas complexas.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*N* \[ em\]
</dt> <dd>

O número de entrada.

</dd> <dt>

*deslocamento* \[ no\]
</dt> <dd>

O deslocamento UV.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um **FLOAT4**, no formato TEXCOORDN.

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra a função que está sendo usada como parte de uma máscara de gradiente de realce e sombra.

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
}  
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vinculação de Sombreador de Efeito](effect-shader-linking.md)
</dt> <dt>

[Auxiliares de HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





