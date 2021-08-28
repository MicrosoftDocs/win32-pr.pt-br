---
description: Função D3DXVec3Normalize (D3dx9math. h) – retorna a versão normalizada de um vetor 3D.
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: Função D3DXVec3Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 161978529f12518280284c8c62328756e92b313a63caf0210a6da35ec23ffe0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791466"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a>Função D3DXVec3Normalize (D3dx9math. h)

Retorna a versão normalizada de um vetor 3D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que é a versão normalizada do vetor especificado.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXVec3Normalize** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




