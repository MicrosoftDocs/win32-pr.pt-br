---
title: Função D2DSampleInputAtPosition (D2d1effecthelpers. h)
description: A entrada de exemplos N é uma posição de cena absoluta, em vez de uma posição relativa à entrada. Disponível somente para entradas complexas.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Direct2D da função D2DSampleInputAtPosition
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759512"
---
# <a name="d2dsampleinputatposition-function"></a>Função D2DSampleInputAtPosition

A entrada de exemplos N é uma posição de cena absoluta, em vez de uma posição relativa à entrada. Disponível somente para entradas complexas.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
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

## <a name="return-value"></a>Retornar valor

A função retorna um **FLOAT4**, no formato TEXCOORDN.

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra a função usada em um encapsulamento circular.

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
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

 

 





