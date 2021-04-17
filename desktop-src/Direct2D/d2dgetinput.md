---
title: Função D2DGetInput (D2d1effecthelpers. h)
description: Retorna a cor da entrada N na coordenada de entrada. Disponível somente para entradas simples.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Direct2D da função D2DGetInput
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752924"
---
# <a name="d2dgetinput-function"></a>Função D2DGetInput

Retorna a cor da entrada N na coordenada de entrada. Disponível somente para entradas simples.

## <a name="syntax"></a>Sintaxe

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*N* \[ em\]
</dt> <dd>

O número de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um **FLOAT4**, contendo a cor RGBA no formato inputn.

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra a função que está sendo usada como parte de um efeito composto aritmético.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Além disso, consulte os comentários para [a \_ \_ entrada do PS D2D](d2d-ps-entry.md) para outro exemplo de uso dessa função.

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

 

 





