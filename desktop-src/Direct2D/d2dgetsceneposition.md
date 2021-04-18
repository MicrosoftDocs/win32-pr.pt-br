---
title: Função D2DGetScenePosition (D2d1effecthelpers. h)
description: Retorna o valor da posição da cena de entrada \_ . Disponível somente quando D2D \_ requer \_ que \_ a posição da cena seja declarada no arquivo de origem.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Direct2D da função D2DGetScenePosition
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756405"
---
# <a name="d2dgetsceneposition-function"></a>Função D2DGetScenePosition

Retorna o valor da posição da cena de entrada \_ . Disponível somente quando D2D \_ requer \_ que \_ a posição da cena seja declarada no arquivo de origem.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

A função retorna um **FLOAT4** no formato posição da cena \_ .

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra o uso da função na geração de um padrão de dissolução.

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
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

 

 





