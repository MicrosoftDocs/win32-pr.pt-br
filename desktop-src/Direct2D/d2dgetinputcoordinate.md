---
title: Função D2DGetInputCoordinate (D2d1effecthelpers. h)
description: Retorna o valor do TEXCOORDN de entrada. Disponível somente para entradas complexas.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Função D2DGetInputCoordinate Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3fe0d825dea70c8e5211b8c13f1e850fa513670bbc93de98f1f8e2b87ef046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075290"
---
# <a name="d2dgetinputcoordinate-function"></a>Função D2DGetInputCoordinate

Retorna o valor do TEXCOORDN de entrada. Disponível somente para entradas complexas.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*N* \[ em\]
</dt> <dd>

O número de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um **FLOAT4**, no formato TEXCOORDN.

## <a name="remarks"></a>Comentários

A coordenada retornada por essa função está no espaço Texel. Um sombreador não deve assumir nenhuma dependência de como esse valor é calculado. Ele deve usá-lo apenas para exemplificar a entrada do sombreador de pixel. Para obter mais informações, consulte [adicionando um sombreador de pixel a uma transformação personalizada](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).

O exemplo a seguir mostra a função usada para um efeito de mapa de deslocamento.

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
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

 

