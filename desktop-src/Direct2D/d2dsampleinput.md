---
title: Função D2DSampleInput (D2d1effecthelpers. h)
description: Exemplos de entrada N na posição UV. Disponível somente para entradas complexas.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- Função D2DSampleInput Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c887221ade413b63456ecb3c4a91c7a5b480858b04e1f34e89506fdcf071dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075270"
---
# <a name="d2dsampleinput-function"></a>Função D2DSampleInput

Exemplos de entrada N na posição UV. Disponível somente para entradas complexas.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*N* \[ em\]
</dt> <dd>

O número de entrada.

</dd> <dt>

*UV* \[ no\]
</dt> <dd>

A posição UV.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um **FLOAT4**, no formato TEXCOORDN.

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra a função que está sendo usada para calcular os Normals da superfície.

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
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

 

 





