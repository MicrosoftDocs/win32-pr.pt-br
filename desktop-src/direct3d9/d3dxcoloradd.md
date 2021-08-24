---
description: Adiciona dois valores de cor juntos para criar um novo valor de cor.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Função D3DXColorAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb96d811f94975d8c7be3225349fd4412a0d1168167066001888084a4ef59136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631606"
---
# <a name="d3dxcoloradd-function"></a>Função D3DXColorAdd

Adiciona dois valores de cor juntos para criar um novo valor de cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.

</dd> <dt>

 \ \[ no\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.

</dd> <dt>

*pC2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é a soma de dois valores de cor.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado em pOut. Dessa forma, a função **D3DXColorAdd** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorSubtract**](d3dxcolorsubtract.md)
</dt> </dl>

 

 




