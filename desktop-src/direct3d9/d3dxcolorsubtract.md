---
description: Subtrai dois valores de cor para criar um novo valor de cor.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: Função D3DXColorSubtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a1d0d9c884dbbfb8e4ae718985be90d22002bd0f2a4cf25f45d02ded12718d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300136"
---
# <a name="d3dxcolorsubtract-function"></a>Função D3DXColorSubtract

Subtrai dois valores de cor para criar um novo valor de cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorSubtract(
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

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é a diferença entre dois valores de cor.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função **D3DXColorSubtract** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdd**](d3dxcoloradd.md)
</dt> </dl>

 

 




