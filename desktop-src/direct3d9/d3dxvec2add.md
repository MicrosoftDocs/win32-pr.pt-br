---
description: Adiciona dois vetores 2D.
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: Função D3DXVec2Add (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9ab63d23a4370c2c64143d2289bd1324a3ebf684d30caf06db3eab2cd4e2915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730889"
---
# <a name="d3dxvec2add-function"></a>Função D3DXVec2Add

Adiciona dois vetores 2D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2Add(
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

Ponteiro para uma [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é a soma dos dois vetores.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec2Add** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Subtract**](d3dxvec2subtract.md)
</dt> <dt>

[**D3DXVec2Scale**](d3dxvec2scale.md)
</dt> </dl>

 

 




