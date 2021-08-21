---
description: Retorna um vetor 2D que é feito dos menores componentes de dois vetores 2D.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: Função D3DXVec2Minimize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da16c90ee5757ec72ee98932164a7281194553e63b4921ca42c666f660f7f904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044624"
---
# <a name="d3dxvec2minimize-function"></a>Função D3DXVec2Minimize

Retorna um vetor 2D que é feito dos menores componentes de dois vetores 2D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é feita dos menores componentes dos dois vetores.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec2Minimize** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Maximize**](d3dxvec2maximize.md)
</dt> </dl>

 

 




